---
title: Improving Multimodal Learning Balance and Sufficiency through Data Remixing
title_zh: 通过数据重混合改善多模态学习的平衡性与充分性
authors: "Xiaoyu Ma, Hao Chen, Yongjian Deng"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=hDH3KfZSsF"
tags: ["query:balanced-mml"]
score: 10.0
evidence: 通过数据重混合缓解模态不平衡，实现平衡多模态学习
tldr: 多模态联合训练中不同模态的优化轨迹存在显著差异，导致模态懒惰和模态冲突，造成不平衡不充分学习。现有方法只关注强化弱模态，未能同时保证单模态充分性和多模态平衡。本文首次提出多模态数据重混合方法：解耦多模态数据并为每个模态筛选困难样本，从而缓解模态不平衡。实验证明该方法在多个多模态基准上实现了更平衡且更充分的学习。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-hdh3kfzssf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 888, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hdh3kfzssf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1718, \"height\": 992, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hdh3kfzssf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1704, \"height\": 389, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-hdh3kfzssf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 806, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hdh3kfzssf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 872, \"height\": 529, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hdh3kfzssf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 864, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hdh3kfzssf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 802, \"height\": 355, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hdh3kfzssf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 842, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hdh3kfzssf/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 846, \"height\": 369, \"label\": \"Table\"}]"
motivation: 现有方法无法同时实现单模态充分性和多模态平衡。
method: 提出多模态数据重混合，包括解耦数据和为每个模态筛选困难样本。
result: 在多个多模态任务上实现了更均衡且充分的学习，显著提升性能。
conclusion: 数据重混合是一种简单有效的方法，可同时解决模态不平衡和单模态学习不足问题。
---

## Abstract
Different modalities hold considerable gaps in optimization trajectories, including speeds and paths, which lead to *modality laziness* and *modality clash* when jointly training multimodal models, resulting in insufficient and imbalanced multimodal learning.
Existing methods focus on enforcing the weak modality by adding modality-specific optimization objectives, aligning their optimization speeds, or decomposing multimodal learning to enhance unimodal learning. These methods fail to achieve both unimodal sufficiency and multimodal balance.
In this paper, we, for the first time, address both concerns by proposing multimodal Data Remixing, including decoupling multimodal data and filtering hard samples for each modality to mitigate modality imbalance; and then batch-level reassembling to align the gradient directions and avoid cross-modal interference, thus enhancing unimodal learning sufficiency. 
Experimental results demonstrate that our method can be seamlessly integrated with existing approaches, improving accuracy by approximately **6.50\%$\uparrow$** on CREMAD and **3.41\%$\uparrow$** on Kinetic-Sounds, without training set expansion or additional computational overhead during inference. The source code is available at Data Remixing.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）
- 多模态学习中，不同模态的优化轨迹（速度与路径）存在显著差异，导致两个关键问题：
  - **模态懒惰（Modality Laziness）**：模型倾向于依赖强势模态，弱势模态训练不足。
  - **模态冲突（Modality Clash）**：即使模态间平衡，梯度更新方向不一致仍会造成交叉干扰，使得各模态学习不充分。
- 现有方法（如梯度调整、知识蒸馏、原型学习等）多聚焦于加速弱模态或对齐优化速度，但未能同时保证**单模态学习充分性**与**多模态整体平衡性**，且部分方法受限于特定模型架构或降低训练效率。

## 2. 方法论：数据重混合（Data Remixing）
- **核心思想**：通过样本级解耦与批次级重组，同时缓解模态懒惰与模态冲突，无需扩增数据集或引入推理额外计算。
- **关键技术细节**：
  1. **热身训练（Warm-up）**：先用完整多模态数据训练少量epoch，使模型具备基本表征能力。
  2. **样本级解耦（Decouple Multimodal Data）**：
     - 对每个样本，计算各单模态预测概率与均匀分布之间的KL散度，度量该模态的分离能力。
     - 保留KL散度最小（分离能力最差）的弱模态输入，将其余模态输入掩码为零，构造新的单模态数据集。
     - 效果：弱模态获得更多训练样本，强势模态样本数减少，自然平衡。
  3. **批次级重组（Reassemble Unimodal Data）**：
     - 将解耦后的样本按所保留模态分组，每个batch仅包含同一模态的数据。
     - 数学分析表明，当batch内只含单一模态时，梯度更新方向仅受该模态影响，从而消除跨模态梯度干扰。
  4. **交替训练**：在热身阶段后，每个epoch交替执行解耦分配和按批次重组训练，直至收敛。
- **算法流程**（伪代码，文字描述）：详见Algorithm 1，整体步骤如上述。

## 3. 实验设计
- **数据集**：
  - **CREMA-D**：视听情感识别，7442个视频片段，6类情绪，划分约9:1训练/测试。
  - **Kinetic-Sounds**：来自Kinetics的31类动作，约19k视频，15k训练、1.9k验证、1.9k测试。
- **Benchmark与对比方法**：
  - 传统融合：Concat（基线）、Sum、Decision Fusion、FiLM、Bi-Gated。
  - 不平衡学习方法：G-Blend、OGM-GE、Greedy、PMR、MLA、Resample。
  - 复杂跨模态架构：MMTM、CentralNet。
- **实验组别**：
  - 表1：五种传统融合 + 本方法改进。
  - 表2：六种不平衡方法对比，以及本方法对其改进（+Remix）。
  - 表3：训练时间比较。
  - 表4：与复杂架构结合。
  - 表5：消融实验（分别移除解耦/重组）。
  - 表6：不同单模态预测方法（Dropout vs 分类头）。
  - 图3：样本分配统计、不平衡比变化、梯度方向差异。

## 4. 资源与算力
- 文中明确说明：
  - GPU型号：2块NVIDIA RTX 3090。
  - Batch size：64。
  - 训练时长见Table 3：CREMA-D上Baseline 1536s，Remix 2537s；Kinetic-Sounds上Baseline 3849s，Remix 4946s。

## 5. 实验数量与充分性
- 共进行了**6组主要表格实验**和**3组图示分析**，覆盖：
  - 传统融合、先进不平衡方法、复杂架构、消融、训练效率、单模态预测方法。
  - 所有报告结果为三次随机种子平均，实验设计较为严谨。
- 充分性评价：
  - **优点**：对比方法全面，消融实验清晰证明了每个组件的贡献；效率对比客观。
  - **不足**：仅使用两个视听数据集（均属于音视频领域），未在文本-图像、图文-语音等更多模态组合上验证，泛化性有待确认。

## 6. 主要结论与发现
- 数据重混合方法能同时缓解模态懒惰和模态冲突，显著提升多模态学习性能。
- 在CREMA-D上提升约**6.50%**，在Kinetic-Sounds上提升约**3.41%**，且不扩增训练集、不增加推理开销。
- 可无缝集成到现有方法（如Resample、MLA）中，进一步提升效果。
- 首次从batch层面分析并解决模态冲突，理论分析与实验一致。

## 7. 优点
- **创新性**：首次指出模态冲突的根源在batch层面，并提出批次级重组这一简洁解决方案。
- **实用性**：无需修改模型架构，不增加训练集大小或推理计算，兼容多种融合方法与复杂架构。
- **实验全面**：在多个维度进行消融、与SOTA对比、效率评估，证明方法有效且高效。
- **代码开源**：可复现性强。

## 8. 不足与局限
- **应用限制**：当某一模态仅作为辅助、含信息量极少时，基于KL散度的分配策略可能不够精细（原文也提及需进一步优化）。
- **实验覆盖**：仅在视听两个数据集上验证，缺乏更多模态组合（如文本+图像、视频+深度）的测试，泛化性有风险。
- **偏差风险**：实验中所有模型使用ResNet-18作为特征提取器，可能缺乏对更大规模预训练模型（如Transformer架构）的评估。
- **训练效率**：虽然未扩增数据集，但解耦和重组增加了每次epoch的分配计算，训练耗时相比基线有所增加（约1.6倍），但优于Resample和MLA。

（完）
