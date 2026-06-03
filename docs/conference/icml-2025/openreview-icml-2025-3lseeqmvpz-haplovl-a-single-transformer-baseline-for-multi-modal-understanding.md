---
title: "HaploVL: A Single-Transformer Baseline for Multi-Modal Understanding"
title_zh: HaploVL：用于多模态理解的基础单Transformer模型
authors: "Rui Yang, Lin Song, Yicheng Xiao, Runhui Huang, Yixiao Ge, Ying Shan, Hengshuang Zhao"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=3lsEeqmvpz"
tags: ["query:native-multi"]
score: 9.0
evidence: 原生端到端单Transformer多模态模型，采用早期融合
tldr: 本文针对原生多模态大模型资源消耗大且性能不足的问题，提出了HaploVL，一个基于早期融合的单Transformer模型。该方法在输入阶段将视觉和文本特征融合，然后统一处理，避免了分离编码。实验表明，HaploVL在多项多模态理解任务上达到了与组合方法相当的性能，同时显著降低了计算成本，为构建高效原生多模态模型提供了基线。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 788, \"height\": 735, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1783, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1776, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1742, \"height\": 1195, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1765, \"height\": 561, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 870, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 601, \"height\": 427, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 565, \"height\": 428, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 631, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 358, \"height\": 275, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 403, \"height\": 278, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 358, \"height\": 274, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 641, \"height\": 833, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3lseeqmvpz/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1244, \"height\": 480, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 866, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1773, \"height\": 730, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 838, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 859, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 864, \"height\": 175, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 904, \"height\": 443, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 865, \"height\": 456, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 869, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 873, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1767, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3lseeqmvpz/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1760, \"height\": 1189, \"label\": \"Table\"}]"
motivation: 现有大多数多模态模型分别处理视觉和文本模态，原生单Transformer模型资源消耗大且性能差距明显。
method: 提出一个简单高效的早期融合单Transformer模型，实现原生端到端多模态学习，作为基准模型。
result: 在多个多模态理解基准上取得了与组合方法可竞争的性能，同时更加高效。
conclusion: HaploVL证明早期融合的单Transformer可以高效地实现原生多模态理解。
---

## Abstract
Recent advancements in large language models (LLMs) have significantly propelled the development of large multi-modal models (LMMs), highlighting the potential for general and intelligent assistants. However, most LMMs model visual and textual modalities separately, leading to recent efforts to develop native LMMs using a single transformer. Despite the promise, these native models are resource-intensive and often exhibit performance gaps compared to their compositional counterparts. To alleviate this issue, we propose a simple yet efficient method to construct a baseline for the native and end-to-end large multi-modal model in a single transformer. First, we propose a new early-fusion LMM that can fuse multi-modal inputs in the early stage and respond to visual instructions in an auto-regressive manner. Second, we devise an efficient training recipe for the proposed model, which harnesses the prior knowledge of the pre-trained models, addressing both the performance limitations and the challenge of resource consumption. The proposed model demonstrates superior performance compared to other LMMs using one transformer and significantly narrows the performance gap with compositional LMMs.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

大多数现有的大规模多模态模型（LMM）采用分离的视觉编码器和语言模型，以“编码器‑投影器‑LLM”的组合方式处理视觉和文本模态。尽管性能优异，但由于需要在不同模态的嵌入之间进行转换，模型难以捕捉细粒度的视觉信息。近年来的“原生”单Transformer模型（如Fuyu、Chameleon、EVE）试图统一处理所有模态，但它们要么需要从零训练（资源消耗极大），要么性能与组合模型存在显著差距。本文提出**HaploVL**，一种简单高效的早期融合单Transformer基线模型，通过利用预训练模型的先验知识，以较少的训练数据和计算成本缩小了与组合模型的性能差距，证明了单Transformer架构在多模态理解中的潜力。

## 2. 方法论

### 核心思想
- **早期融合**：图像和文本在输入阶段即被映射到同一潜在空间，然后由单Transformer统一处理，使文本嵌入能够动态地从原始图像嵌入中获取所需视觉线索。
- **两阶段训练**：第一阶段通过知识蒸馏实现模态扩展；第二阶段进行全参数视觉指令微调。

### 关键技术细节
1. **架构组成**（图3）：
   - **多模态嵌入层**：图像使用单线性层（patch embedding）将像素块映射到潜在空间 \( \mathbb{R}^d \)；文本使用预训练LLM的嵌入矩阵加一个线性投影层。
   - **预解码器**（Pre‑decoder）：继承预训练ViT（如CLIP-ViT‑L）的结构和权重，能够同时处理视觉和文本输入，采用因果掩码（文本部分）+双向掩码（图像部分）+跨图像的因果掩码。
   - **后解码器**（Post‑decoder）：继承预训练LLM（Vicuna / Llama‑3）的结构和权重，负责基于融合后的隐藏状态生成语言响应。

2. **训练策略**：
   - **第一阶段（预训练）**：冻结教师模型（CLIP视觉编码器和LLM嵌入层），通过知识蒸馏训练预解码器。损失函数包括：
     - 视觉损失：余弦相似度损失 \( \mathcal{L}_v = 1 - \frac{1}{hw}\sum_{i=1}^{hw} \cos(\hat{H}_{v,i}, T_{v,i}) \)
     - 文本特征损失：L2距离 + 余弦损失 \( \mathcal{L}_{feat} = \frac{1}{S}\sum_{i=1}^{S} \left( \|\hat{H}_{t,i} - T_{t,i}\|_2 - \cos(\hat{H}_{t,i}, T_{t,i}) \right) \)
     - 当前token预测损失（Current Token Prediction Loss）：基于当前token的交叉熵损失 \( \mathcal{L}_{ctp} = -\frac{1}{S}\sum_{i=1}^{S} \sum_{c=1}^{C} y_{i,c} \log \frac{e^{x_{i,c}/\tau}}{\sum_j e^{x_{i,j}/\tau}} \)，其中 \( x_i = \hat{H}_{t,i} \cdot W^T \)
     - 总文本损失：\( \mathcal{L}_t = \mathcal{L}_{feat} + \mathcal{L}_{ctp} \)
   - **第二阶段（全微调）**：丢弃教师模型和头部，对整个HaploVL使用下一个token预测损失进行指令微调。

3. **位置编码**：图像使用可学习位置嵌入，文本使用旋转位置编码（RoPE）。

## 3. 实验设计

### 使用的数据集
- **预训练数据**：665K视觉指令数据（来自LLaVA‑1.5）+ 558K图像标题数据 + 额外纯文本数据（dolphin、Alpaca、ShareGPT），并构造交错的图像‑文本序列。
- **单图像指令数据**：665K（LLaVA‑1.5）或4M（LLaVA‑OneVision过滤后）。
- **多图像指令数据**：来自Li et al. (2024b)的交错数据。

### 评估基准
涵盖11个主流基准：GQA、VQAv2、ScienceQA‑IMG（SQA）、AI2D、MMBench‑EN‑dev（MMB）、MMMU、RealWorldQA（RWQA）、MMStar、POPE、SEED‑Bench‑IMG（SEED）、MMVP（专注于细粒度感知）。

### 对比方法
- **组合LMM**：InstructBLIP、LLaVA‑1.5/1.6、ShareGPT4V、VILA、LLaVA‑OneVision。
- **单Transformer LMM**：Fuyu‑8B、Chameleon‑30B、EVE‑7B、Emu3‑8B。

## 4. 资源与算力

- **GPU**：32块64GB显存的GPU（型号未明确说明，可能是NVIDIA A100或类似）。
- **训练步数**：预训练40K steps（batch size 256），全微调30K steps（batch size 128）。
- **数据量**：主模型使用4M指令数据，耗时约1个epoch。
- 文中未给出精确的GPU小时数，但提及Chameleon‑30B的能耗类比（用GPU小时数估算），而HaploVL的训练资源远小于从头训练的Chameleon。

## 5. 实验数量与充分性

- **主结果**（表2）：对比11个基准上的12种方法（含消融变体），显示HaploVL在所有单Transformer模型中领先，且接近最强的组合模型LLaVA‑OV。
- **消融实验**（表3‑7）：包括不同LLM（Vicuna vs. Llama‑3）、输入分辨率（336 vs. 672）、指令数据量（665K vs. 4M）、预训练阶段有无、数据组成（mix‑v1~v4、MMC4、纯文本）、ImageNet零样本分类性能等。
- **定性分析**（图4‑5）：展示推理样例和注意力可视化，验证早期融合对细粒度感知的提升。
- **更多消融**（附录B）：深入分析预训练阶段数据组成对下游性能的影响。
- **公平性**：在表4中与LLaVA‑1.5‑7B和EVE‑7B在同一LLM（Vicuna‑7B）和同一数据量（665K）对比，控制变量。
- **总体**：实验设计充分，覆盖了多种维度的消融，对比方法全面，结论有说服力。

## 6. 主要结论与发现

1. **性能领先**：HaploVL在所有单Transformer模型上取得最优结果，例如在MMBench上比Emu3高15.1%，比EVE高24.1%；在MMVP（细粒度）上比LLaVA‑1.5‑7B高5.4%。
2. **早期融合优势**：相比使用CLIP高维语义嵌入的组合模型，HaploVL能更好地捕捉细粒度视觉信息（如图4中边缘对象、颜色、数量），从而提升基于细粒度感知的逻辑推理能力。
3. **训练效率**：通过两阶段蒸馏，无需大量数据和计算资源即可达到与组合模型可比的性能；去掉预训练阶段会导致收敛缓慢和性能下降（表5，下降4.3%）。
4. **注意力可视化**（图5）表明文本嵌入能动态关注图像中相关区域，证实早期融合机制有效。

## 7. 优点

- **方法简洁**：仅使用单线性层作为图像嵌入，无需复杂视觉编码器。
- **高效率**：利用预训练模型先验知识，显著减少训练数据和计算成本（仅需1.2M预训练数据 + 4M指令数据）。
- **细粒度感知强**：早期融合避免了CLIP等编码器丢失细节的问题，在MMVP、MMStar等细粒度基准上表现突出。
- **泛化性好**：支持任意输入分辨率（通过调整patch大小实现），且可扩展至多图像和视频输入。
- **公开代码**：开源促进后续研究。

## 8. 不足与局限

- **与顶尖组合模型仍有差距**：HaploVL仍低于LLaVA‑OneVision（如MMBench 75.0 vs. 80.8），作者归因于输入分辨率（HaploVL最大2304 tokens vs. LLaVA‑OV 7290 tokens）和上下文长度限制（6144）。
- **固定分辨率**：尽管支持可变，但实验仅使用了336或672分辨率，未实现动态分辨率裁剪。
- **数据分布影响**：在GQA上扩大指令数据后性能轻微下降，可能与数据分布差异有关。
- **训练资源依然不小**：需32GPU，对于小实验室仍有门槛。
- **未覆盖生成任务**：目前仅做理解任务，未像Emu3扩展到图像/视频生成。
- **未进行人类偏好对齐**：未使用RLHF或DPO等对齐技术。
- **缺乏对幻觉的定量分析**：定性样例中可见轻微幻觉（如表12），但未系统评估。

（完）
