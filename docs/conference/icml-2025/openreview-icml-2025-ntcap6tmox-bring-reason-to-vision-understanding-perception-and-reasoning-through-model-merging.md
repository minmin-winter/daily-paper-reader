---
title: "Bring Reason to Vision: Understanding Perception and Reasoning through Model Merging"
title_zh: 将推理带入视觉：通过模型合并理解感知与推理
authors: "Shiqi Chen, Jinghan Zhang, Tongyao Zhu, Wei Liu, Siyang Gao, Miao Xiong, Manling Li, Junxian He"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=ntCAP6tMoX"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 跨模态模型合并，将LLM推理能力转移到VLM
tldr: 视觉语言模型如何组合感知与推理能力尚不明确。本文提出跨模态模型合并方法，通过连接不同模型的参数，将大语言模型的推理能力转移到视觉语言模型中，无需训练。实验表明模型合并是一种成功路径，显著提升了VLM的推理性能，且保持训练-free。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1752, \"height\": 657, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 850, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 765, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1771, \"height\": 998, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1765, \"height\": 993, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1692, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1076, \"height\": 372, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 625, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 779, \"height\": 790, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ntcap6tmox/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 799, \"height\": 588, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1772, \"height\": 530, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1771, \"height\": 423, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1770, \"height\": 477, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1773, \"height\": 641, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1083, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1777, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1775, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1122, \"height\": 838, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ntcap6tmox/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1610, \"height\": 335, \"label\": \"Table\"}]"
motivation: 现有方法未能有效融合视觉感知与大语言模型的推理能力。
method: 提出跨模态模型合并，直接连接不同模型的参数以转移推理能力。
result: 在多个视觉推理任务上实现了训练-free的推理能力迁移，性能显著提升。
conclusion: 模型合并在跨模态推理能力转移中是一种有效且高效的方法。
---

## Abstract
Vision-Language Models (VLMs) combine visual perception with the general capabilities, such as reasoning, of Large Language Models (LLMs). However, the mechanisms by which these two abilities can be combined and contribute remain poorly understood.
In this work, we explore to compose perception and reasoning through model merging that connects parameters of different models.  
Unlike previous works that often focus on merging models of the same kind, we propose merging models **across modalities**, enabling the incorporation of the reasoning capabilities of LLMs into VLMs. 
Through extensive experiments, we demonstrate that model merging offers a successful pathway to transfer reasoning abilities from LLMs to VLMs in a **training-free** manner.
Moreover, we utilize the merged models to understand the internal mechanism of perception and reasoning and how merging affects it. We find that perception capabilities are predominantly encoded in the early layers of the model, whereas reasoning is largely facilitated by the middle-to-late layers. After merging, we observe that all layers begin to contribute to reasoning, whereas the distribution of perception abilities across layers remains largely unchanged. These observations shed light on the potential of model merging as a tool for multimodal integration and interpretation.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **背景**：视觉语言模型（VLM）综合了视觉感知与大型语言模型（LLM）的通用能力（如推理），但**感知与推理这两种能力如何结合及相互作用**仍不清楚。
- **现状与瓶颈**：现有VLM在复杂多模态推理任务上表现不佳，主要原因之一是**多模态推理训练数据稀缺**；而纯文本LLM在推理方面已取得显著进展。
- **核心问题**：如何将LLM的推理能力**训练-free地**迁移到VLM中？感知和推理在VLM参数空间中的分布是怎样的？
- **整体含义**：本文通过**跨模态模型合并**（model merging）连接VLM的语言组件与推理LLM的参数，实现推理能力转移，并借助合并后的模型揭示感知与推理在VLM内部的层分布机制。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：基于**任务向量（task vector）** 的线性合并。任务向量定义为微调模型与基础模型参数的差值：  
  `τ_vlm = θ_vlm - θ_base`，`τ_reason = θ_reason - θ_base`。
- **合并公式**：  
  `θ'_vlm = θ_base + λ · τ_vlm + (1-λ) · τ_reason`  
  其中λ控制VLM原始能力与推理能力的平衡（本文主要取λ=0.9）。
- **关键细节**：
  - 仅合并VLM的**语言模型部分**，视觉塔（vision tower）和投影器（projector）保持不变。
  - 除线性合并外，还尝试了TIES merging、Dare merging、Layer Swapping等方法，发现线性合并简单且效果相当。
  - 超参数λ通过MathVista验证集调优（搜索范围0.8, 0.85, 0.9），并固定后用于所有实验。
- **算法流程**（文字说明）：
  1. 获取基础LLM（如LLaMA-3-8B）参数θ_base。
  2. 获取VLM的语言组件参数θ_vlm（从预训练VLM中提取）和推理LLM参数θ_reason。
  3. 计算任务向量τ_vlm和τ_reason。
  4. 按权重λ合并，得到新参数θ'_vlm。
  5. 将θ'_vlm替换回原VLM中，保持视觉塔和投影器不变，直接推理。

## 3. 实验设计：数据集、基准与对比方法

- **VLM模型**：LLaVA-NeXT-LLaMA3-8B（主要）、Idefics2-8B、InternVL2-LLaMA3-76B，覆盖不同尺寸和基础模型（LLaMA/Mistral系列）。
- **推理LLM（任务向量来源）**：
  - 数学领域：Dart-Math（两个变体：Dart-Uniform, Dart-Prop2diff）、MAmmoTH-1、MAmmoTH-2、Magpie-v0.3、MetaMath、DeepSeek-R1-Distill。
  - 通用领域：MAmmoTH-2（还覆盖一般推理）。
  - 逻辑推理扩展：LogiCoT（附录D）。
- **基准数据集**：
  - **MathVista**：含通用VQA和数学VQA子集，提供细粒度任务标签。
  - **MathVerse**：分6种难度模式（Text-Dominant, Text-Lite, Vision-Integrated, Vision-Dominant, Vision-Only）。
  - **MathVision**、**DynaMath**、**MMStar**（含Math子集）、**MM-Math**（附录F）。
- **对比方法**：
  - 基线：原始VLM（不合并）。
  - 不同推理任务向量的线性合并（固定λ=0.9）。
  - 不同合并策略（TIES、Dare-TIES、Dare-Linear、Layer Swapping，见附录C）。
  - 额外实验：合并逻辑推理模型（LogiCoT）验证泛化性；合并Qwen2-VL与Qwen2-Math（附录E）。

## 4. 资源与算力

- 论文**未明确说明**使用的GPU型号、数量及训练时长。
- 由于方法为**训练-free**，仅需参数合并和推理（前向传播），算力消耗主要来自推理评估。
- 对于8B模型，单卡（如A100 80GB）可支持推理；对于76B InternVL，可能需要多卡或更大显存，但文中未提及具体配置。
- **注意**：算力细节缺失，无法量化。

## 5. 实验数量与充分性

- **实验数量**：共进行了**数十组实验**，包括：
  - 主要结果表（Table 2）：对LLaVA合并5种推理LLM，覆盖5个基准，每个基准含多个子集（约30个指标）。
  - 其他VLM（Table 3）：Idefics和InternVL各合并多种任务向量，同样覆盖全部基准。
  - 消融与补充：不同合并方法比较（附录C）、逻辑推理泛化（附录D）、Qwen2-VL（附录E）、MM-Math（附录F）、显著性检验（附录G）。
  - 机制分析（Section 5）：通过masking out和1/N替换，逐层分析感知与推理的分布（多组对比）。
- **充分性**：
  - **充分**：覆盖多个VLM类型（不同基础模型、大小）、多个推理LLM（数学专项、通用、逻辑）、多个基准（注重数学推理和通用VQA）、多种合并策略。
  - **客观公平**：统一超参数搜索策略（基于Dart-Prop在MathVista上调优），并应用于所有实验；报告中同时给出正负效果；附录中进行了显著性检验（p<0.05标记）。
  - **潜在不足**：基准主要聚焦数学推理，其他领域（如常识、科学推理）未覆盖；部分合并对视觉密集任务有轻微下降，但分析合理。

## 6. 论文的主要结论与发现

1. **跨模态模型合并有效**：将数学推理LLM合并到VLM（LLaVA）后，在数学推理相关基准上取得**一致提升**（如MathVista数学子集提升3.6个点，MathVerse Text-Dominant提升6个点）；且**无需额外训练**。
2. **推理能力转移与感知能力的影响**：合并主要提升**数学推理与文本主导**的任务；对于依赖强感知的任务（如图表QA），提升有限甚至轻微下降。
3. **推理-时间缩放能力**：合并后，模型在推理密集型任务中输出长度显著增加，性能与长度呈近似线性关系，表明模型具备了**更长的链式推理（CoT）能力**。
4. **感知与推理在参数空间中的层分布**：
   - **感知能力**主要位于**早期层**（前1/3层）。
   - **推理能力**主要位于**中后期层**（后1/3层）。
   - **合并后**：几乎所有层对推理的贡献增加，而感知能力的层分布几乎不变。
5. **可解释性贡献**：模型合并可作为一种**可解释性工具**，帮助分离和理解VLM内部的能力分布。

## 7. 优点：方法与实验设计的亮点

- **方法简洁免训练**：仅需参数算术操作，无需微调或额外数据，易于复现和应用。
- **跨模态合并创新**：此前模型合并多限于同模态（同类型任务），本文首次系统验证了**跨模态（文本→视觉-语言）** 合并的可行性。
- **丰富的可解释分析**：通过knockout、1/N替换等机制实验，揭示了感知与推理在VLM中的层位置，为理解VLM内部机制提供了新视角。
- **实验覆盖面广**：测试了多种VLM（不同基础模型、不同参数量）、多种推理LLM、多个基准，结果一致且具有显著性。
- **公平比较**：统一超参数、对比多种合并方法、报告完整正负结果，并进行了统计显著性检验。

## 8. 不足与局限

- **任务域局限**：仅聚焦数学推理，对其他类型推理（如科学推理、常识推理、视觉常识）的泛化性未验证。
- **感知下降风险**：合并通常导致视觉密集型任务（如图表QA）性能轻微下降，对于需要强感知的应用可能存在权衡。
- **对已训练模型的边际收益**：对已在大量文本数学数据上微调的VLM（如Idefics、Qwen2-VL）提升有限，表明任务向量重叠时效果减弱。
- **超参数敏感性**：λ需要针对特定数据集调优，不同模型/任务的最优λ可能不同，缺乏自适应机制。
- **模型架构限制**：仅适用于**共享同一基础模型**的VLM和LLM合并（都基于LLaMA或Mistral），不能跨架构（如LLaMA与Mistral互不兼容）。
- **算力资源未报告**：缺乏GPU型号、数量和推理时间等细节，影响可复现性。
- **未见更大规模测试**：最大模型为76B，未验证在更大规模（如70B+）上的表现及合并方法的扩展性。

（完）
