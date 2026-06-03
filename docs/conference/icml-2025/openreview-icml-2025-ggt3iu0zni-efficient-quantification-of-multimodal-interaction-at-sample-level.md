---
title: Efficient Quantification of Multimodal Interaction at Sample Level
title_zh: 多模态交互的样本级高效量化
authors: "Zequn Yang, Hongfa Wang, Di Hu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Ggt3iu0Zni"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 样本级量化冗余、独特性和协同
tldr: 多模态交互（冗余、独特性和协同）的样本级量化存在理论计算挑战。本文提出轻量级样本级多模态交互估计器，基于点式信息论构建冗余估计框架，再推广到一般交互度量。该方法高效且具有理论保证，为理解多模态信息动态提供了新工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 852, \"height\": 603, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1512, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 836, \"height\": 376, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 850, \"height\": 919, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 840, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 841, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1658, \"height\": 479, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggt3iu0zni/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1635, \"height\": 551, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1744, \"height\": 361, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1792, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1702, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 793, \"height\": 658, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1616, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 879, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 768, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 864, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1538, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1016, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggt3iu0zni/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 944, \"height\": 324, \"label\": \"Table\"}]"
motivation: 准确量化多模态交互的样本级信息对于分析多模态系统至关重要，但现有方法存在理论和计算障碍。
method: 利用点式信息论构建冗余估计框架，并基于熵估计提出通用交互度量方法。
result: 在合成和真实数据上验证了量化的准确性和效率，支持下游多模态分析。
conclusion: LSMI为多模态交互的样本级分析提供了轻量级且理论严谨的解决方案。
---

## Abstract
Interactions between modalities—redundancy, uniqueness, and synergy—collectively determine the composition of multimodal information. Understanding these interactions is crucial for analyzing information dynamics in multimodal systems, yet their accurate sample-level quantification presents significant theoretical and computational challenges. To address this, we introduce the Lightweight Sample-wise Multimodal Interaction (LSMI) estimator, rigorously grounded in pointwise information theory. We first develop a redundancy estimation framework, employing an appropriate pointwise information measure to quantify this most decomposable and measurable interaction.
Building upon this, we propose a general interaction estimation method that employs efficient entropy estimation, specifically tailored for sample-wise estimation in continuous distributions. Extensive experiments on synthetic and real-world datasets validate LSMI's precision and efficiency. Crucially, our sample-wise approach reveals fine-grained sample- and category-level dynamics within multimodal data, enabling practical applications such as redundancy-informed sample partitioning, targeted knowledge distillation, and interaction-aware model ensembling. The code is available at https://github.com/GeWu-Lab/LSMI_Estimator.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：多模态数据中的交互类型（冗余、独特性、协同）共同决定了多模态信息的构成。理解这些交互对于分析多模态系统中的信息动态至关重要，但现有方法多数停留在**分布级量化**，无法提供**样本级**的细粒度分析。
- **核心挑战**：样本级量化面临理论和计算双重障碍——点式互信息可能为负，导致传统格点分解框架的单调性失效；且现有分布优化方法（如PID-CVX、PID-Batch）在连续分布上计算开销大、难以扩展到样本级。
- **整体含义**：该工作旨在填补样本级多模态交互量化的空白，提供一种高效、精确且可解释的工具，以揭示数据内部的交互动态，并赋能下游多模态学习应用。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：基于**点式信息论**构建冗余估计框架，将多模态交互分解为冗余（r）、独特性（u1、u2）和协同（s），并利用轻量级熵估计实现样本级计算。
- **关键技术细节**：
  - **冗余定义**：将点式互信息拆分为正分量（i⁺ = -log p(x)）和负分量（i⁻ = -log p(x|y)），两者均满足单调性。冗余定义为两个分量的最小值之差：`r = min(i⁺(x1;y), i⁺(x2;y)) - min(i⁻(x1;y), i⁻(x2;y))`。
  - **交互分解公式**：利用方程 `i(x1;y)=r+u1, i(x2;y)=r+u2, i(x1,x2;y)=r+u1+u2+s` 解出唯一性和协同。
  - **熵估计**：采用KNIFE工具（Pichler et al., 2022）对连续分布进行高效差分熵估计，通过最小化KL散度得到熵的上界，进而计算点式互信息。
- **算法流程**（参见Algorithm 1）：
  1. 输入双模态数据x1、x2、目标y以及预训练的分类模型p(y|x1,x2)、p(y|x1)、p(y|x2)。
  2. 训练熵估计器h_θ1、h_θ2（分别对x1、x2）。
  3. 计算样本级熵h(x1)、h(x2)；通过条件概率计算h(x1|y)、h(x2|y)。
  4. 计算冗余r；再计算点式互信息i(x1;y)、i(x2;y)、i(x1,x2;y)（利用分类模型输出）。
  5. 通过方程反解得到u1、u2、s。

## 3. 实验设计
- **数据集**：
  - **合成数据**：电路逻辑（XOR、OR、XOR+NOT）、混合高斯（调整相关系数ρ控制协同）、预设交互（固定比例混合冗余/独特/协同样本）。
  - **真实数据**：Food-101（图像+文本）、CREMA-D（音频+视觉）、Kinetic-Sounds (KS)（音频+视觉）、UCF-101（RGB+光流）、CMU-MOSEI（视频+文本）、UR-Funny（视频+文本）。
- **基准方法**：
  - 分布级方法：PID-CVX（适用于离散分布）、PID-Batch（适用于连续分布）。
  - 人类判断：对部分数据集标注主观交互分数（0-5）。
- **对比维度**：
  - 精度：合成数据上的GT对比。
  - 效率：时间成本对比。
  - 应用：数据划分、知识蒸馏、模型集成。

## 4. 资源与算力
- **论文未明确说明使用的GPU型号、数量或训练时长**。
- 但在效率对比中给出了LSMI与PID-Batch的时间成本（Table 5），例如在KS数据集上LSMI耗时501.5秒，PID-Batch耗时21928秒，表明LSMI显著更高效。未提及具体硬件配置。

## 5. 实验数量与充分性
- **实验数量**：涵盖3种合成数据 + 6个真实数据集；对比了3种分布级方法（PID-CVX、PID-Batch、人类）；做了多个应用实验（数据划分、蒸馏、集成）；额外进行了模态对分析、分布偏移分析、融合阶段影响分析（见附录）。
- **充分性**：实验设计较全面，验证了精度、效率、可解释性和实用性。消融实验（如不同融合方法、不同模态组合）增强了结论的可靠性。但缺少与更多样本级方法的对比（因为现有方法极少），主要通过合成数据和人类判断间接验证。
- **客观公平性**：合成数据提供精确GT，真实数据采用训练良好的模型近似真实分布，并与人类主观评分相关（Pearson > 0.9），对比基线使用公开实现，设置合理。

## 6. 论文的主要结论与发现
- LSMI能够**精确、高效**地估计样本级多模态交互，在合成数据上接近GT，在真实数据上与PID-Batch和人类判断趋势一致。
- 揭示了**类别和样本级的交互动态**：例如乐器类冗余高，视觉特征明显的类别视觉独特性高，复杂任务（如挠痒）更依赖协同。
- 不同多模态学习方法在交互建模上有差异：特征级融合能学习多种交互，决策级融合擅长冗余，对齐方法增强冗余，重构方法增强独特性。
- **实际应用**：基于冗余的数据划分可提升对齐模型性能；交互引导的蒸馏比直接蒸馏更有效；交互感知的模型集成优于加权集成。

## 7. 优点
- **首次实现连续分布下的样本级多模态交互量化**，突破了现有方法局限于分布级的限制。
- **理论严谨**：基于点式信息论，通过正负分量分解解决非单调性问题，满足格点分解的单调性要求。
- **轻量高效**：仅需熵估计器和分类模型，避免昂贵的分布优化，时间成本远低于PID-Batch，且不随类别数线性增长。
- **可解释性强**：提供样本级和类别级的交互分析，能揭示数据内在信息构成。
- **广泛应用潜力**：展示了在数据划分、蒸馏、集成等方面的实用价值，为多模态学习提供指导。

## 8. 不足与局限
- **理论范围限制**：当前框架仅处理双模态交互。扩展到三模态以上需采用成对分析策略，缺乏统一的PID理论支撑。
- **依赖模型近似**：交互计算需依赖训练良好的分类模型，若模型偏差较大（如存在域偏移），估计结果可能失真（论文附录A.3.2已展示标签噪声和OOD场景下的影响）。
- **负互信息处理**：虽然通过正负分量分解解决了单调性，但对于负互信息的具体解释（如误导信息）未作深入探讨。
- **实验覆盖**：未与更多样本级方法（如基于点式PID的离散方法）在连续数据上直接对比（因现有方法难以适用）。真实数据上的GT缺乏，主要依赖人类主观评分和相关分析。
- **应用验证规模**：应用实验（蒸馏、集成）仅在少数数据集上验证，泛化性有待进一步测试。

（完）
