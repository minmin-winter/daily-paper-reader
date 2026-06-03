---
title: Improving LLM Video Understanding with 16 Frames Per Second
title_zh: 通过每秒16帧提升LLM视频理解
authors: "Yixuan Li, Changli Tang, Jimin Zhuang, Yudong Yang, Guangzhi Sun, Wei Li, Zejun MA, Chao Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=3H7qAT9Qow"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 高帧率视频理解的多模态LLM
tldr: 现有视频理解多模态LLM通常使用低帧率采样，丢失关键动态信息。本文提出F-16，首款支持16 FPS高帧率视频理解的多模态LLM，通过每秒片段内压缩视觉令牌高效捕获动态特征。实验表明高帧率显著提升视频理解性能，为视频模型提供了新方向。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-3h7qat9qow/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1735, \"height\": 931, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3h7qat9qow/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 647, \"height\": 684, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3h7qat9qow/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 871, \"height\": 530, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3h7qat9qow/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 870, \"height\": 525, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3h7qat9qow/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1371, \"height\": 274, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3h7qat9qow/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1369, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-3h7qat9qow/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1369, \"height\": 2283, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1765, \"height\": 617, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 855, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1764, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 739, \"height\": 340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 772, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1677, \"height\": 1141, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1241, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1272, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1243, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-3h7qat9qow/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1642, \"height\": 1116, \"label\": \"Table\"}]"
motivation: 低帧率采样导致视频理解中动态视觉信息丢失，限制了LLM对视频的理解能力。
method: 设计16 FPS帧率输入，并在每秒片段内压缩视觉令牌以保持语义信息。
result: 在多个视频理解基准上超越低帧率方法，验证了高帧率的有效性。
conclusion: F-16证明了高帧率对视频理解的重要性，为多模态LLM视频处理开辟了新途径。
---

## Abstract
Human vision is dynamic and continuous. However, in video understanding with multimodal large language models (LLMs), existing methods primarily rely on static features extracted from images sampled at a fixed low frame rate of frame-per-second (FPS) $\leqslant$2, leading to critical visual information loss. In this paper, we introduce F-16, the first multimodal LLM designed for high-frame-rate video understanding. By increasing the frame rate to 16 FPS and compressing visual tokens within each 1-second clip, F-16 efficiently captures dynamic visual features while preserving key semantic information.
Experimental results demonstrate that higher frame rates considerably enhance video understanding across multiple benchmarks, providing a new approach to improving video LLMs beyond scaling model size or training data. F-16 achieves state-of-the-art performance among 7-billion-parameter video LLMs on both general and fine-grained video understanding benchmarks, such as Video-MME and TemporalBench. Furthermore, F-16 excels in complex spatiotemporal tasks, including high-speed sports analysis (*e.g.*, basketball, football, gymnastics, and diving), outperforming SOTA proprietary visual models like GPT-4o and Gemini-1.5-pro.
Additionally, we introduce a novel decoding method for F-16 that enables highly efficient low-frame-rate inference without requiring model retraining. We will release the source code, model checkpoints, and data at [https://github.com/bytedance/F-16](https://github.com/bytedance/F-16).

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **背景**：现有视频理解多模态大语言模型（LLM）通常以每秒帧数（FPS）≤2 的低帧率采样，或仅选取固定数量的帧（如8帧、16帧），将视频视为少量静态图像的集合。这种做法虽然能捕捉视频的整体主题和场景，但会丢失快速变化的视觉细节（如身体动作、微表情等动态信息）。
- **核心问题**：低帧率采样导致关键的动态视觉信息丢失，制约了模型对动态场景的理解能力，尤其在需要精细时间理解的任务（如高速运动、动作识别）中表现不足。
- **整体含义**：本文首次提出高帧率（16 FPS）视频 LLM，通过增加帧率并压缩每秒内的视觉令牌，高效捕获动态特征，为提升视频理解提供了新方向，超越了仅通过扩大模型或数据规模的路径。

## 2. 方法论
### 核心思想
- 以16 FPS 密集采样视频帧（最多1760帧/110秒），并在每个1秒的窗口内压缩视觉令牌，保留语义信息的同时提取帧间动态特征。
- 将预训练的图像 LLM（LLaVA-OneVision）扩展到视频领域，通过块矩阵分解初始化高帧率对齐器，实现知识迁移。
- 提出训练无关的变帧率解码方法，在不重训练的情况下适配低帧率推理。

### 关键技术细节
- **模型架构**：采用图像编码器（SigLIP）+ 高帧率对齐器（3层MLP）+ 骨干LLM（Qwen2-7B）。高帧率对齐器将连续w帧（w=16）的图像特征沿特征维度拼接，然后通过两层线性变换（中间带GELU激活）映射到LLM输入空间，再经过2×2最大池化压缩令牌数量（约4倍减少）。
- **初始化**：从预训练图像LLM的单帧对齐器参数（权重矩阵WA, WB）通过块矩阵分解构建高帧率对齐器的参数WP（块对角矩阵，每块为WA）和WQ（垂直拼接WB并除以w），实现初始状态为各帧表示的平均。
- **变帧率解码**：测试时若需降低帧率k倍，则将每个实际帧的特征重复k次，使其输入维度匹配训练时的窗口大小。此法无需额外训练即可在低帧率下推理。
- **训练策略**：第一阶段全模型训练（除图像编码器冻结），学习率2×10⁻⁵，1 epoch；第二阶段对体育任务使用LoRA微调（rank=128, scaling=2.0），学习率相同，5 epochs。

## 3. 实验设计
### 使用数据集/场景
- **通用视频理解**：LLaVA-Video-178K, LLaVA-Hound, NExT-QA, ActivityNet-QA, PerceptionTest。
- **高速体育视频**：FineGym（体操）, Diving48（跳水）, SoccerNet（足球）中的“Ball Action”子集，以及自收集的NBA视频（276场比赛）。任务包括动作分类、传球计数、投篮是否命中、详细字幕生成。

### Benchmark
- **通用基准**：Video-MME（短/中/长）, NeXT-QA, TemporalBench, MotionBench, VideoVista, MLVU, LongVideoBench。
- **体育基准**：体操准确率、跳水分阶段动作预测准确率、NBA（F1分数）、足球（准确率）。

### 对比方法
- **开源模型**：Qwen2-VL-7B, VideoLLaMA2-7B, VideoChat2-HD-7B, LLaVA-OV-7B, MiniCPM-V2.6-8B, LLaVA-Video-7B, NVILA-7B。
- **商业模型**：GPT-4o, Gemini-1.5-Pro。

## 4. 资源与算力
- **第一阶段（通用视频训练）**：使用128块H100 GPU，训练1 epoch，学习率2×10⁻⁵。未说明训练总时间。
- **第二阶段（体育数据LoRA微调）**：使用64块H100 GPU，训练5 epochs，学习率2×10⁻⁵。未说明总时间。
- **推理分析**：论文提供了不同帧率下各模块（编码器、对齐器、LLM）的时间消耗数据，但未给出整体训练时长。

## 5. 实验数量与充分性
### 实验组数
- 通用视频理解：在7个基准上对比，包括3个子维度（如Video-MME短/中/长），共10余个指标。
- 体育任务：4个场景（体操、跳水、NBA、足球），每个场景有多个指标（如体操准确率、跳水四阶段准确率）。
- 消融实验：帧率对比（1 vs 16 FPS）、池化位置（pre vs post）、变帧率解码方法（重复 vs 裁剪）、不同对齐器结构（Linear vs CNN vs Attention vs Dual Linear）。
- 变帧率分析：推理时间与性能权衡，训练帧率与测试帧率匹配性。

### 充分性与公平性
- **充分性**：覆盖通用与细粒度视频理解、高速运动场景，消融实验深入分析关键设计选择（对齐器初始化、池化策略、变帧率解码）。实验设计较为全面。
- **公平性**：与同尺寸（7B）模型对比时保持参数规模一致；体育任务中与商业模型对比时输入帧数设为120帧（公平设置）。但部分基准（如MLVU, LongVideoBench）F-16未达到最优，论文如实报告并给出合理解释（帧间变化大使压缩更具挑战性）。

## 6. 主要结论与发现
1. **高帧率显著提升视频理解**：16 FPS 相比1 FPS在通用基准（Video-MME +2.1%）和细粒度基准（TemporalBench +13.5%）上均有提升。
2. **高速体育任务中超越商业模型**：F-16在体操（+15.6%）、跳水（+10.5%）、NBA（+12.3% F1）、足球（+14.6%）上均显著优于GPT-4o和Gemini-1.5-Pro。
3. **变帧率解码有效**：以16 FPS训练的模型在8 FPS测试时，使用“重复帧”方法几乎保持性能（64.0→63.9），而“裁剪”方法性能下降较多，说明对齐器学习到了帧间运动信息而不只是局部参数调整。
4. **高帧率对齐器优于简单平均**：初始化时的平均操作在训练后演变出更复杂的帧间特征提取能力。
5. **池化后置于对齐器之后更优**：后池化（post-pooling）比前池化（pre-pooling）对高帧率模型更关键（+4.2% vs +0.6%），因为前池化过早丢失细节。

## 7. 优点
- **方法创新性**：首次将视频LLM的帧率提升至16 FPS，并提出相应的高帧率对齐器和块矩阵初始化策略，解决了高帧率带来的冗余和初始化难题。
- **高效性与灵活性**：变帧率解码方法无需额外训练即可适应低帧率场景，平衡了计算开销与性能。
- **实验结果扎实**：在多个基准上取得SOTA（7B级别），消融实验充分，对比公平，并提供了推理时间分析。
- **实际应用价值**：在高速体育场景中显著超越商业模型，展示了高帧率在需要精细时间理解任务中的巨大潜力。

## 8. 不足与局限
- **长视频理解略有劣势**：在Video-MME Long、MLVU、LongVideoBench等长视频基准上，F-16性能略低于LLaVA-Video-7B，因为长视频内窗口帧间变化大，压缩损失更多信息。论文将其归因于模型设计在长视频上的挑战。
- **计算成本高**：16 FPS编码导致推理速度慢（图像编码器耗时占据主导），变帧率解码虽可缓解但牺牲部分性能。
- **数据集局限**：体育数据集规模较小（NBA仅1万条注释），且任务定义较窄（传球计数、投篮命中），缺乏更多样化的高帧率应用场景。
- **对齐器结构探索有限**：仅尝试了线性、CNN、注意力等变体，未探索更复杂的时序建模模块（如Transformer、3D卷积），可能限制了高帧率特征的进一步提取。
- **初始化依赖预训练图像LLM**：若源图像LLM结构不同，块矩阵初始化方法可能不直接适用，泛化性受限。
- **未测试更极端的帧率**：仅尝试16 FPS，未探索32 FPS或更高帧率下的性能与效率权衡。

（完）
