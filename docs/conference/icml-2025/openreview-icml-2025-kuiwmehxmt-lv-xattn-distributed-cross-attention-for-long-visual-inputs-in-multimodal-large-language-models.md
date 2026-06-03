---
title: "LV-XAttn: Distributed Cross-Attention for Long Visual Inputs in Multimodal Large Language Models"
title_zh: LV-XAttn：面向多模态大模型长视觉输入的分布式交叉注意力
authors: "Tzu-Tao Chang, Shivaram Venkataraman"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=kuIwMEHXMT"
tags: ["query:unified-mm"]
score: 7.0
evidence: 分布式精确交叉注意力机制，高效实现视觉-语言融合
tldr: 本文针对多模态大模型在处理长视频输入时交叉注意力层内存消耗大、分布式通信开销高的问题，提出LV-XAttn，一种近似无通信开销的精确分布式交叉注意力机制。通过利用应用特性减少通信，显著提升了长视频理解中的训练和推理效率。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-kuiwmehxmt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 770, \"height\": 704, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kuiwmehxmt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 842, \"height\": 394, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kuiwmehxmt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kuiwmehxmt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 688, \"height\": 554, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kuiwmehxmt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 855, \"height\": 353, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kuiwmehxmt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 833, \"height\": 743, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kuiwmehxmt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 968, \"height\": 785, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-kuiwmehxmt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 872, \"height\": 310, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kuiwmehxmt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 739, \"height\": 373, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kuiwmehxmt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1771, \"height\": 895, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kuiwmehxmt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1649, \"height\": 896, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kuiwmehxmt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 868, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kuiwmehxmt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 850, \"height\": 502, \"label\": \"Table\"}]"
motivation: 长视频输入下交叉注意力层成为分布式训练和推理的瓶颈。
method: 提出LV-XAttn分布式精确交叉注意力，大幅降低通信开销。
result: 实现了高效的分布式训练和推理，适用于长视频理解。
conclusion: LV-XAttn有效缓解了长视觉输入下的跨模态注意力瓶颈。
---

## Abstract
Cross-attention is commonly adopted in multimodal large language models (MLLMs) for integrating visual information into the language backbone. However, in applications with large visual inputs, such as video understanding, processing a large number of visual tokens in cross-attention layers leads to high memory demands and often necessitates distributed computation across multiple GPUs. Existing distributed attention mechanisms face significant communication overheads, making cross-attention layers a critical bottleneck for efficient training and inference of MLLMs. To address this, we propose LV-XAttn, a distributed, exact cross-attention mechanism with minimal communication overhead. We observe that in applications involving large visual inputs, the size of the query block is typically much smaller than that of the key-value blocks.  Thus, in LV-XAttn we keep the large key-value blocks locally on each GPU and exchange smaller query blocks across GPUs. We also introduce an efficient activation recomputation technique to support longer visual context. We theoretically analyze the communication benefits of LV-XAttn and show that it can achieve speedups for a wide range of models. Our evaluations with Llama 3-V, mPLUG-Owl3 and OpenFlamingo models find that LV-XAttn achieves up to 10.62$\times$ end-to-end speedup compared to existing approaches.

---

## 论文详细总结（自动生成）

# LV-XAttn: 分布式交叉注意力加速多模态大模型长视觉输入处理

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：多模态大模型（MLLMs）通过交叉注意力层将视觉信息融入语言骨干网络，在处理长视频等大视觉输入时，交叉注意力层需要大量内存（例如 Llama 3-V 处理 20 分钟视频需 234 GB），远超单 GPU 容量，必须进行分布式计算。
- **现有方法的不足**：现有分布式注意力方法（如 head-parallelism 的 Deepspeed-Ulysses、Megatron-LM，以及 sequence-parallelism 的 Ring Attention）在处理大视觉输入时存在严重通信开销。实验显示，交叉注意力层虽仅占参数的 3%，但在 Ring Attention 下却耗费高达 88% 的迭代时间，成为训练和推理的瓶颈。
- **整体含义**：本文旨在设计一种近似无通信开销的精确分布式交叉注意力机制，以大幅提升 MLLM 在长视频理解等场景中的训练与推理效率。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 2.1 核心观察
在长视频应用中，视觉输入生成的 key-value 序列长度（\( S_{KV} \)）远大于文本 query 序列长度（\( S_Q \)）。例如 Video-MME 基准中，Llama 3-V 处理 1 fps 视频时，\( S_{KV} \approx 15,279,944 \)，而 \( S_Q \approx 5,514 \)。

### 2.2 核心方法：LV-XAttn
- **策略**：将大的 key-value 块（\( K_i, V_i \)）固定存储在每个 GPU 本地，仅在各 worker 之间传输小的 query 块（\( Q_j \)）、注意力输出块（\( O_j \)）和 softmax 统计量（\( L_j \)），以环形拓扑进行交换。
- **算法流程（Forward Pass）**：
  1. 初始化每个 worker i 的局部输出 \( O_i \) 和统计量 \( L_i \)；将 \( Q_i, O_i, L_i \) 作为初始块。
  2. 对于 round = 0 到 n-1：
     - 并行执行：向下一 worker 发送当前块的 \( Q, O, L \)；从上一 worker 接收对应的 \( Q, O, L \)。
     - 使用接收到的 \( Q_j \) 与本地 \( K_i, V_i \) 通过 FlashAttention 计算部分注意力输出 \( \Delta O \) 和 \( \Delta L \)。
     - 更新接收到的 \( O_j, L_j \)（rescaling）。
  3. 经过 n 轮后，最终输出 \( O_i, L_i \) 回到原始 worker i。
- **计算与通信重叠**：由于传输的数据量远小于 Ring Attention，通信可被计算完全隐藏，实际运行时几乎无额外通信开销。

### 2.3 激活重计算技术
- **问题**：存储每个交叉注意力层的大 key-value 块（\( K_i, V_i \)）增加内存压力。
- **观察**：所有交叉注意力层共享相同的视觉输入 y（仅 LM 块中的语言特征 x 会逐层变化）。
- **方法**：仅保留一份视觉特征 y，在反向传播时重新投影计算 \( K_i, V_i \)，避免为每层存储大 KV 张量。只需保存 \( x, O_i, L_i \)。
- **效果**：内存减少使可处理的视觉输入长度提升 1.6 倍，且仅增加不到 8% 的迭代时间开销。

### 2.4 理论分析
- LV-XAttn 计算主要受限于计算（compute-bound），而 Ring Attention 受限于通信（communication-bound）。
- 对于多头部注意力的前向/反向，LV-XAttn 相对于 Ring Attention 的理论加速比与 \( S_Q \)、GPU FLOPS、网络带宽相关。在典型场景下，速度巨大。

## 3. 实验设计

### 3.1 模型与配置
| 模型 | 交叉注意力层数 | LM 块数 |
|------|----------------|----------|
| Llama 3-V-11b | 8 | 40 |
| mPLUG-Owl3-7b/2b/1b | 4 | 28/28/24 |
| OpenFlamingo-9b/3b | 8/24 | 32/24 |
- 使用公开 checkpoint，替换其中的交叉注意力操作为 LV-XAttn 或基线方法。
- 每帧编码的视觉 token 数：Llama 3-V: 6404, mPLUG-Owl3: 729, OpenFlamingo: 64。

### 3.2 集群设置
- **Cluster 1**：16 块 A100 80GB GPU（4 节点，节点内 NVLink，节点间 25 GB/s）。
- **Cluster 2**：8 块 A30 24GB GPU（8 节点，节点间 1.25 GB/s）。
- **Cluster 3**：12 块 A100 40GB GPU（4 节点，节点内 64 GB/s PCIe，节点间 25 GB/s，用于消融实验）。

### 3.3 基线方法
- **主要基线**：Ring Attention（用于交叉注意力层 + LM 块）；两种方法均使用 FlashAttention。
- **对比方法**：Deepspeed-Ulysses（head parallelism + sequence parallelism）。
- 所有方法均应用激活重计算以公平比较。

### 3.4 评价指标
- 单次迭代的 wall-clock time（前向+反向），分别报告交叉注意力（CA）时间和总时间。使用随机生成的输入，进行 5 次测试取平均（含 2 次 warmup）。

## 4. 资源与算力
- **GPU 型号与数量**：使用了 A100 80GB（16 块 / 12 块）和 A30 24GB（8 块）三种配置。具体训练时长未明确说明，仅报告了单次迭代的耗时（秒级）。文中未提及完整训练一个模型的 GPU 小时数。
- **框架**：PyTorch + Triton，使用 torch.distributed 进行通信，自定义 Triton kernel 实现支持 rescaling 的 FlashAttention。

## 5. 实验数量与充分性
- **主要对比实验**：在 6 种模型 × 多种文本/帧数配置下，在两种集群上分别与 Ring Attention 进行对比（Table 3 和 Table 4），共 20+ 组设置。
- **与 Deepspeed-Ulysses 对比**：在 mPLUG-Owl3-2b 和 OpenFlamingo-3b 两种模型上，涵盖不同 GPU 数量和 worker 配置（Table 5 和 Table 6），共 10+ 组。
- **消融实验**：
  - 计算-通信重叠效果（Figure 5）：6 A100 40GB GPUs，不同文本长度下的 CA 时间对比。
  - 激活重计算效果（Figure 6）：mPLUG-Owl3-7b 和 OpenFlamingo-3b 在 3 块 A30 GPU 上，对比保存/不保存 KV 时的帧数上限和耗时。
  - 理论加速比分析（Figure 4）和通用场景讨论（Figure 7）提供了额外理解。
- **充分性评价**：实验覆盖了多种模型尺寸、GPU 型号、跨节点带宽、视觉 token 密度；消融研究验证了核心设计（重叠、重计算）的有效性；对比方法包括最强的分布式注意力基线（Ring Attention 和 Deepspeed-Ulysses），设置公平。但缺少真实视频端到端推理任务（如 Video-MME 上精度对比）——但本文目标为系统加速，精度等价性已通过数值验证说明。总体而言实验充分且客观。

## 6. 论文的主要结论与发现
1. **LV-XAttn 实现显著加速**：在 16 A100 集群上，交叉注意力操作加速高达 45.85×，端到端迭代加速高达 10.62×（Llama 3-V）。在资源受限的 8 A30 集群上，加速比更显著（通信瓶颈更严重）。
2. **通信几乎完全隐藏**：通过计算-通信重叠，LV-XAttn 引入的额外开销低于 0.42%（相较于无通信理想基线）。
3. **激活重计算有效扩展上下文**：内存减少使支持的帧数提升 1.6×，而开销小于 8%。
4. **优于 Deepspeed-Ulysses**：不仅速度更快（1.34-1.55×），而且不受 head 数量限制，能处理更长的序列（训练更长的视频）。
5. **适用范围**：对 MLLM 中的交叉注意力层有效，尤其当 \( S_{KV} \gg S_Q \) 时。对于自注意力（\( S_Q = S_{KV} \)），Ring Attention 仍适用。

## 7. 优点
- **方法创新**：直接利用 MLLM 应用特性（文本短、视觉长）设计分布式注意力，避免了通用的 head-parallelism 和 sequence-parallelism 的通信瓶颈。
- **精确性**：完全等价于标准交叉注意力，无近似误差（与 PyTorch scaled dot-product attention 数值一致）。
- **高效性**：通信开销极低，并能被完全重叠；激活重计算技巧简单但有效。
- **泛化性**：支持多种主流 MLLM 架构（Flamingo、mPLUG-Owl3、Llama 3-V），且可与其他并行策略（数据并行、管道并行等）结合。
- **开源**：代码已公开（https://github.com/uw-mad-dash/LV-XAttn），便于复现和社区使用。

## 8. 不足与局限
- **适用范围限制**：仅适用于交叉注意力层，对自注意力（如 LM 块中的注意力）不适用（文中已说明此时应使用 Ring Attention）。对混合架构（同时包含 concat 和 cross-attention）虽声称可适用，但未实验验证。
- **实验未覆盖真实下游任务**：仅测算了运行时间，未在 Video-MME 等基准上报告模型精度或端到端推理吞吐/延迟，虽然精度理论等价，但分布式实现的数值稳定性在极端长序列下可能引入细微差异。
- **硬件依赖**：实验主要在高性能集群（NVLink、25 GB/s 跨节点网络）上开展。在更低带宽环境（如以太网）的表现未评估，可能通信无法完全隐藏。
- **激活重计算开销**：虽然小于 8%，但在训练高频次迭代或推理时可能累积。文中未讨论推理场景（通常不进行反向传播）是否需要重计算。
- **基准覆盖不全面**：未与更多分布式注意力变体（如 Striped Attention）比较，也未与更近期的系统优化（如 DistFlashAttn）对比。
- **缺乏内存消耗的详细数据**：文中仅给出一个示例（Llama 3-V 需要 234 GB），未提供各模型在 LV-XAttn 下的详细内存使用量对比。

（完）
