---
title: "RollingQ: Reviving the Cooperation Dynamics in Multimodal Transformer"
title_zh: "RollingQ: 恢复多模态Transformer中的合作动态"
authors: "HaoTian Ni, Yake Wei, Hang Liu, Gong Chen, Chong Peng, Hao Lin, Di Hu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=R07oAGxwhG"
tags: ["query:balanced-mml"]
score: 9.0
evidence: 恢复多模态Transformer合作动态以对抗模态偏差
tldr: 多模态Transformer中的自注意力机制动态适应性会逐渐衰退，导致模型偏向某一模态并形成自我强化循环。本文观察到该现象并提出RollingQ方法，通过调整注意力关键分布来恢复模态间合作动态。实验证明该方法有效消除了模态偏差，提升了多模态融合性能。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1706, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 856, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 862, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1716, \"height\": 515, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 855, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1697, \"height\": 1403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1433, \"height\": 602, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1704, \"height\": 1146, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r07oagxwhg/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1704, \"height\": 963, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 872, \"height\": 1207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1754, \"height\": 806, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 885, \"height\": 199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 845, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 880, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 824, \"height\": 191, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 865, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 516, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1071, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1673, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1028, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r07oagxwhg/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 837, \"height\": 194, \"label\": \"Table\"}]"
motivation: 发现自注意力模型在多模态融合中动态适应性下降，产生模态偏向并损害融合效果。
method: 提出RollingQ机制，重新平衡注意力关键分布以恢复模态间合作。
result: 在多个多模态任务上消除了偏差，显著提升了融合准确率。
conclusion: RollingQ揭示了多模态Transformer中的自强化偏差并提供了有效修正方案。
---

## Abstract
Multimodal learning faces challenges in effectively fusing information from diverse modalities, especially when modality quality varies across samples. Dynamic fusion strategies, such as attention mechanism in Transformers, aim to address such challenge by adaptively emphasizing modalities based on the characteristics of input data. However, through amounts of carefully designed experiments, we surprisingly observed that the dynamic adaptability of widely-used self-attention models diminishes. Model tends to prefer one modality regardless of data characteristics. This bias triggers a self-reinforcing cycle that progressively overemphasizes the favored modality, widening the distribution gap in attention keys across modalities and deactivating attention mechanism's dynamic properties. To revive adaptability, we propose a simple yet effective method Rolling Query (RollingQ), which balances attention allocation by rotating the query to break the self-reinforcing cycle and mitigate the key distribution gap. Extensive experiments on various multimodal scenarios validate the effectiveness of RollingQ and the restoration of cooperation dynamics is pivotal for enhancing the broader capabilities of widely deployed multimodal Transformers. The source code is available at https://github.com/GeWu-Lab/RollingQ_ICML2025.

---

## 论文详细总结（自动生成）

# 论文《RollingQ: Reviving the Cooperation Dynamics in Multimodal Transformer》详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：多模态Transformer中广泛使用的自注意力机制在动态融合时，其“动态适应能力”会逐渐丧失——模型倾向于过度关注某一模态（即使该模态被替换为噪声），导致多模态合作动态失效。这种模态偏向会触发一个**自我强化循环**：前馈阶段偏向模态获得更高注意力权重，反向传播中该模态获得更多梯度更新，进一步扩大模态间注意力键的分布差距，最终使注意力机制丧失根据数据质量动态调整权重的功能。
- **研究动机**：现有动态融合方法理论上应优于静态融合，但实验发现简单静态融合（如拼接）反而表现更好，说明注意力机制并未按预期工作。论文通过理论和实验揭示这一现象的内在原因，并试图恢复其合作动态。
- **整体含义**：该工作揭示了多模态Transformer中一个被忽视的关键问题——注意力机制的动态属性会因训练过程中的自我强化循环而失活，并提出了简单有效的补救方案，对提升多模态融合效果具有重要启示。

## 2. 论文提出的方法论

### 2.1 核心思想
通过**旋转查询向量（Query）** 来打破自我强化循环，重新平衡注意力在不同模态上的分配，缩小模态间注意力键的分布差距，从而恢复注意力机制的动态适应能力。

### 2.2 关键技术细节

#### （1）问题诊断——注意力平衡率指标（AIR）
- 定义：`AIR = E[cosθ_a - cosθ_v] ∈ [-2, 2]`，其中 `cosθ_m` 是查询与模态m平均键的余弦相似度。
- 当 `|AIR| ≥ β`（β为阈值）时，认为模态间分布差距显著，需要干预。

#### （2）计算平衡锚点（Rebalance Anchor）
- 公式：`qb = (α * E[K̂_a]/||E[K̂_a]||₂ + (1-α) * E[K̂_v]/||E[K̂_v]||₂) * ||E[Q]||₂`
- 权重α由AIR通过双曲正切函数得到：`α = 0.5 * [1 + Tanh(-ρ * AIR)]`，ρ>0为超参数。当AIR>0（模态a偏向）时，α<0.5，使得锚点偏向弱势模态。

#### （3）旋转矩阵计算
- 通过奇异值分解（SVD）计算旋转矩阵 `Rb`，满足 `qb = E[Q] * Rb`。
- 旋转后的查询：`qr = q * Rb`，`q` 是当前查询，`E[Q]` 是当前批次查询均值。

#### （4）算法流程（Algorithm 1）
- 训练过程中，每个epoch结束时计算当前batch的AIR。
- 若 `|AIR| ≥ β`，则冻结模型参数，计算锚点和旋转矩阵，更新累积的旋转矩阵 `R = R * Rb.detach()`，然后解冻模型继续训练。
- 引入旋转次数上限以保证训练稳定性（小数据集1次，大数据集3次）。

### 2.3 扩展性
- 对多层Transformer，采用逐层渐进训练策略：先训练第一层注意力层（将其视为最后层），应用RollingQ；再训练第二层，对第二层应用RollingQ。

## 3. 实验设计

### 3.1 数据集
- **CREMA-D**：音视频情感识别（6类基本情绪），7442个短视频片段。
- **Kinetic-Sound**：音频+视频动作识别（31类），来自Kinetics数据集。
- **CMU-MOSEI**：多模态情感分析（视觉+文本），包含超过23500个视频片段，7类情感标注。

### 3.2 基准方法对比
- **静态融合**：朴素拼接（Concat）、OGM（梯度调制）、PMR（原型模态重平衡）。
- **动态融合**：Vanilla MT（单层/双层注意力）、MulT、MBT、JMT、MMML。
- **消融基线**：单模态（音频、视觉、文本单独训练）。

### 3.3 实验条件
- 主骨干网络：4层ViT-B/16（ImageNet-21k预训练），对MOSEI使用4层Transformer。
- 优化器：SGD，余弦学习率调度；批次大小64；学习率1e-3；训练30个epoch。
- 超参数：AIR阈值β和缩放参数ρ根据数据集调整。

## 4. 资源与算力

- **文中明确提及信息**：未详细说明使用的GPU型号、数量、训练时长。仅提到在CREMA-D上统计了GFLOPs和参数量（见表4）：Vanilla MT有59.87M参数、1489.13 GFLOPs；添加RollingQ后参数增至60.46M（增加约1%），GFLOPs增至1489.20（增加约0.1%）。
- **备注**：算力细节缺失，无法评估整体训练成本，但方法本身轻量。

## 5. 实验数量与充分性

### 实验数量
- **主性能对比**：在3个数据集（CREMA-D、Kinetic-Sound、MOSEI）上对比了约10种基线方法（静态、动态融合），每个数据集报告了多个指标。
- **消融实验**：
  - 批次大小消融（16/64/256）
  - 编码器层数消融（2/4/6层ViT）
  - 不同骨干网络（ResNet18）
  - 注意力掩码/QUAG注意力测试
  - 不同融合层位置（2nd/3rd/4th层）
  - 噪声干扰测试（4个噪声水平）
- **分布分析实验**：可视化注意力键分布、注意力分数变化、梯度演化、噪声输入测试（表2、图4、图5）等。
- **迁移测试**：多模态OOD检测（HMDB51作为ID，HMDB/UCF作为OOD）。
- **扩展至多种Transformer结构**：MulT、MMML等叠加RollingQ。
- **总计**：约15个以上不同实验设置，涵盖准确性、鲁棒性、可视化、相关性分析等多个维度。

### 实验充分性与公平性
- **充分性**：实验覆盖了主流多模态任务（情感识别、动作识别、情感分析）、不同模态组合（A+V、V+T、A+T）、不同骨干（ViT、ResNet）、不同融合范式（早期/晚期融合）、扰动鲁棒性和OOD场景，较为全面。
- **公平性**：对比方法均采用相同的骨干设置（针对不同数据集统一预处理），超参数在相同条件下调优。但注意：部分基线方法（如MBT、JMT）使用了更多参数和复杂模块，比较时并非严格参数等量，但论文已报告参数量和计算量对比（表4），相对透明。
- **风险**：所有实验基于3个特定数据集，领域代表性有限（主要为情感和动作识别）。未在更大规模或更通用多模态任务（如视觉问答、多模态翻译）上验证。

## 6. 论文的主要结论与发现

1. **主要发现**：多模态Transformer中自注意力机制的动态适应能力会在训练中因“自我强化循环”而失活，导致过度偏向某一模态，注意力分数与数据质量无关。
2. **提出的解决方法**：RollingQ通过旋转查询向量，将查询引向一个能平衡模态注意力的锚点，从而打破循环，缩小键分布差距。
3. **有效性验证**：
   - RollingQ在所有数据集上一致提升了原有动态融合方法的准确率（例如在CREMA-D上提升3.1%，Kinetic-Sound上提升2.3%）。
   - 可视化表明，RollingQ后注意力分数对噪声输入更加敏感（相关性系数从0.44/0.52提升至0.78/0.76）。
   - 在噪声扰动下，RollingQ性能下降幅度更小，并且能更好利用弱势模态。
   - 参数量仅增加约1%，计算量增加约0.1%，效率高。
4. **泛化性**：可应用于多种Transformer结构（MulT、MMML、不同层数、不同骨干），均观察到提升。

## 7. 优点

- **问题发现新颖且有洞察力**：指出了动态融合中注意力机制退化的具体机制（自我强化循环），并给出了理论分析和可视化证据。
- **方法简洁高效**：仅通过旋转查询向量即可恢复动态适应性，无需增加复杂模块或额外训练阶段，参数量和计算量极低。
- **实验设计全面**：涵盖了从标准性能对比到分布可视化、消融实验、稳健性测试、OOD检测等多角度验证，结论可信度高。
- **通用性与可迁移性**：方法可集成到现有多种Transformer融合框架中（如MulT、MMML），不限制具体架构，实用性较强。

## 8. 不足与局限

- **理论分析集中于单层注意力**：论文的理论推导主要基于单层注意力层，对于多层Transformer中的表现只给出初步扩展实验，未进行同等深度的理论分析。多层注意力中可能发生更复杂的相互作用。
- **数据集覆盖有限**：实验仅在三个数据集（情感识别和动作识别）上进行，未在视觉问答、多模态翻译、医学图像等更广泛的多模态任务中验证，通用性有待进一步确认。
- **未解决特征质量差异的根源**：RollingQ仅通过调整注意力分配来间接影响特征学习，并未直接提升弱势模态的特征质量。论文也承认这一点，并指出可与特征质量均衡方法（如OGM、PMR）结合。
- **超参数依赖**：AIR阈值β和缩放参数ρ需要根据数据集调优，缺乏自动确定策略。
- **旋转次数上限的设置**：为避免训练不稳定，引入了旋转次数上限（如1次或3次），这一设计可能不适应某些复杂场景。
- **公平性细节**：与某些对比方法（如MBT、JMT）的参数量和计算量差异较大，虽然论文报告了数值，但未进行严格等参数比较，可能影响领先程度的归因。

（完）
