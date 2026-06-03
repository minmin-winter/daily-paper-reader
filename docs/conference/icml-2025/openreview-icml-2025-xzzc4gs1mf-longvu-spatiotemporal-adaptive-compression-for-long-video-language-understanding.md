---
title: "LongVU: Spatiotemporal Adaptive Compression for Long Video-Language Understanding"
title_zh: LongVU：面向长视频语言理解的时空自适应压缩
authors: "Xiaoqian Shen, Yunyang Xiong, Changsheng Zhao, Lemeng Wu, Jun Chen, Chenchen Zhu, Zechun Liu, Fanyi Xiao, Balakrishnan Varadarajan, Florian Bordes, Zhuang Liu, Hu Xu, Hyunwoo J. Kim, Bilge Soran, Raghuraman Krishnamoorthi, Mohamed Elhoseiny, Vikas Chandra"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=XzZC4gs1mf"
tags: ["query:mm-reasoning"]
score: 6.0
evidence: 时空自适应压缩实现长视频-语言理解
tldr: 本文针对多模态大模型在长视频理解中受限于上下文大小的问题，提出LongVU时空自适应压缩机制。利用跨模态查询和帧间依赖，自适应减少时空冗余。在长视频理解任务上取得了高效且保留细节的效果。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-xzzc4gs1mf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 835, \"height\": 447, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xzzc4gs1mf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1730, \"height\": 782, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xzzc4gs1mf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 847, \"height\": 1227, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xzzc4gs1mf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1726, \"height\": 613, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xzzc4gs1mf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1667, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xzzc4gs1mf/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1702, \"height\": 946, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1765, \"height\": 801, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1686, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 855, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1601, \"height\": 231, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1567, \"height\": 309, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1044, \"height\": 403, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1462, \"height\": 566, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1417, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1605, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1300, \"height\": 459, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1700, \"height\": 158, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1685, \"height\": 145, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1080, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1258, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1260, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1259, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1258, \"height\": 314, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1260, \"height\": 324, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xzzc4gs1mf/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1256, \"height\": 208, \"label\": \"Table\"}]"
motivation: MLLM处理长视频时受限于上下文长度。
method: 提出时空自适应压缩，利用跨模态查询和帧间依赖减少视频令牌。
result: 在长视频理解中实现高效且保留细节的压缩。
conclusion: 时空自适应压缩是处理长视频输入的有效方法。
---

## Abstract
Multimodal Large Language Models (MLLMs) have shown promising progress in understanding and analyzing video content. However, processing long videos remains a significant challenge constrained by LLM's context size. To address this limitation, we propose \textbf{LongVU}, a spatiotemporal adaptive compression mechanism that reduces the number of video tokens while preserving visual details of long videos. Our idea is based on leveraging cross-modal query and inter-frame dependencies to adaptively reduce temporal and spatial redundancy in videos. Specifically, we leverage DINOv2 features to remove redundant frames that exhibit high similarity. Then we utilize text-guided cross-modal query for selective frame feature reduction. Further, we perform spatial token reduction across frames based on their temporal dependencies. Our adaptive compression strategy effectively processes a large number of frames with little visual information loss within given context length. Our LongVU consistently surpass existing methods across a variety of video understanding benchmarks, especially on hour-long video understanding tasks such as VideoMME and MLVU. Given a light-weight LLM, our LongVU also scales effectively into a smaller size with state-of-the-art video understanding performance.

---

## 论文详细总结（自动生成）

# LongVU：面向长视频语言理解的时空自适应压缩 —— 论文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：多模态大语言模型（MLLMs）在理解长视频时，受限于 LLM 的上下文长度（通常为 8k tokens）。以 1fps 采样的一小时视频可产生超过 200k tokens，远超模型处理能力。
- **现有方法缺陷**：
  - 均匀采样（uniform sampling）会错过关键帧；
  - 密集采样（dense sampling）会导致令牌超出上下文长度而被截断；
  - 简单池化或 Q-Former 压缩会损失过多视觉细节。
- **整体含义**：本文提出一种**时空自适应压缩机制**，在给定上下文长度内保留尽可能多的视频细节，实现长视频的高效理解。

## 2. 方法论

### 核心思想
利用**跨模态查询**和**帧间依赖**，对视频进行三步自适应压缩，在保持视觉细节的同时显著减少令牌数量。

### 关键技术细节

1. **时间缩减（Temporal Reduction）**  
   - 使用 DINOv2 提取所有帧特征，在非重叠窗口（窗口大小 J=8）内计算每帧与窗口内其他帧的平均余弦相似度。
   - 移除高相似度帧（阈值 0.83），平均保留约 **45.9%** 的帧。
   - 对于保留的 T 帧，分别提取 SigLIP 和 DINOv2 特征，并通过 **Spatial Vision Aggregator (SVA)** 融合。

2. **选择性特征缩减（Selective Feature Reduction via Cross-modal Query）**  
   - 若融合后的令牌数仍超过最大上下文长度，则利用文本查询 Q 与每帧特征的交叉注意力分数，选择 Top-Nh 帧保留完整令牌分辨率（144 tokens），其余帧空间池化为低分辨率（64 tokens）。
   - 保留帧数量公式：  
     \[
     N_h = \max\left(0, \frac{L_{\max} - L_q - T H_l W_l}{H_h W_h - H_l W_l}\right)
     \]
     其中 \(L_{\max}\) 为上下文长度，\(L_q\) 为文本查询长度，\(H_h W_h\) 为高分辨率令牌数，\(H_l W_l\) 为低分辨率令牌数。

3. **空间令牌压缩（Spatial Token Compression, STC）**  
   - 在低分辨率帧上，按滑动窗口（窗口大小 K=8）分组。每组第一帧保留所有令牌，后续帧与第一帧做逐位置余弦相似度比较，相似度高于阈值 θ=0.75 的令牌被剪枝。
   - 平均可减少约 **40.4%** 的令牌。

### 总体流程
输入视频 1fps 采样 → DINOv2 时间缩减 → SigLIP + DINOv2 特征融合 → 交叉模态查询选择性保留 → 空间令牌压缩 → 送入 LLM。

## 3. 实验设计

### 数据集与基准
- **训练数据**：
  - 图像语言预训练：LLaVA-OneVision 的单图像数据（3.2M 样本）。
  - 视频语言微调：VideoChat2-IT 的子集，包括 TextVR、Youcook2、Kinetics-710、NExTQA、CLEVRER、EgoQA、TGIF、WebVidQA、ShareGPT4Video、MovieChat。
- **评估基准**：
  - EgoSchema（~180秒）、MVBench（~16秒）、MLVU（3分钟~2小时）、VideoMME（1分钟~1小时，分为短/中/长）。
- **对比方法**：
  - 闭源：GPT4-V、GPT4-o。
  - 开源：Video-LLaVA、LLaMA-VID、Chat-UniVi、ShareGPT4Video、LLaVA-NeXT-Video、VideoLLaMA2、LongVA、VideoChat2、LLaVA-OneVision 等。
  - 轻量模型：Phi-3.5-vision-instruct、InternVL2。

### 评价指标
准确率（Accuracy），使用贪心解码（num_beams=1）。

## 4. 资源与算力

- **模型训练**：**64 张 NVIDIA H100 GPU**。
- **图像语言预训练**：1 epoch，全局 batch size 128，学习率 1e-5，warmup 0.03。
- **视频语言微调**：1 epoch，全局 batch size 64，学习率 1e-5，warmup 0.03。
- **论文未明确给出总训练时长**（如天数或小时数），但说明使用了大规模 GPU 资源。

## 5. 实验数量与充分性

- **主实验**：7B 和 3B 两个尺度，在 4 个基准上对比了 10+ 种方法（表 1、2）。
- **消融实验**：
  - 令牌数量与上下文长度（表 3）。
  - DINOv2 vs SigLIP 的时间缩减效果（表 3）。
  - 查询引导选择 vs 无选择（表 3、4）。
  - 空间令牌压缩（STC）效果（表 3）。
  - 不同策略（第一帧、中间帧、变化帧）比较（表 5）。
  - DINO 阈值、STC 阈值、滑动窗口大小 K 和 J 的敏感性（表 15-18）。
  - 帧级位置编码（FPE）影响（表 8、9）。
  - 与训练无关的令牌压缩方法对比（表 13）。
  - 上下文长度 6k/8k/12k/16k 的影响（表 14）。
  - Needle-in-a-Video-Haystack 实验（图 6）。
  - 推理时间对比（表 11、12）。
- **充分性评价**：实验覆盖了多种消融和敏感性分析，对比方法全面，但未在更广泛场景（如不同语言、嘈杂视频）测试，且图像到视频 SFT 后图像任务性能下降未充分讨论（仅在附录 G 提及）。

## 6. 主要结论与发现

- LongVU 在多个视频理解基准上**显著超越**现有开源方法，尤其在**长视频**（VideoMME Long 子集）上比 LLaVA-OneVision 提升 **12.8%**。
- 使用**轻量 LLM (Llama3.2-3B)** 仍能取得小规模模型的 SOTA，验证了压缩机制的有效性与可扩展性。
- **自适应压缩**比均匀采样或固定低分辨率池化更优，能够保留关键帧细节同时压缩冗余。
- **DINOv2** 用于时间缩减优于 SigLIP，因其更能捕捉细微帧差异。
- 跨模态查询引导的选择性保留对 **帧检索任务**（计数、针检测）提升明显。

## 7. 优点

- **方法设计巧妙**：三步压缩逐步减少冗余，且利用文本查询指导关键帧保留，符合视频理解的语义需求。
- **训练数据效率高**：仅用 1 epoch 微调，且训练数据为公开子集（相比 LLaVA-OneVision 的未公开 1.6M 数据）。
- **兼容轻量模型**：3B 参数版本仍达 SOTA，适合部署。
- **实验详尽**：消融覆盖核心组件、超参数、上下文长度等，充分验证各模块贡献。
- **推理速度快**：相比 Chat-UniVi、VideoChat2 等方法更快（表 11），且 DINO 缩减步骤可离线预处理。

## 8. 不足与局限

- **图像能力下降**：仅用视频数据微调后，图像理解性能下降（如表 10），需混合图像数据恢复，但论文未给出最终统一模型。
- **缺乏时间定位能力**：由于帧令牌未编码时序位置，模型在时间定位（如事件起止时间）上表现弱，仅尝试了帧级位置编码但效果有限（附录 B）。
- **依赖 DINO 预提取**：DINO 特征提取增加预处理开销，虽可离线但整体流程较复杂。
- **实验覆盖有限**：未在真实场景（如监控、直播）或更长视频（数小时）上验证；只评估了 4 个公开基准，可能存在基准偏差。
- **超参数调优**：DINO 阈值（0.83）、STC 阈值（0.75）、窗口大小（8）等对性能有非单调影响，可能需针对不同视频类型调整，泛化性未充分测试。
- **没有开放全部代码/数据**：仅提供项目网页，可能影响复现性。

（完）
