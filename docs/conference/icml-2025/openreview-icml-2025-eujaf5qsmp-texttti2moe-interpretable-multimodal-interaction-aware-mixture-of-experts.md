---
title: "$\\texttt{I$^2$MoE}$: Interpretable Multimodal Interaction-aware Mixture-of-Experts"
title_zh: I^2MoE：可解释的多模态交互感知专家混合模型
authors: "Jiayi Xin, Sukwon Yun, Jie Peng, Inyoung Choi, Jenna L. Ballard, Tianlong Chen, Qi Long"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=EuJaF5QsMP"
tags: ["query:unified-mm"]
score: 8.0
evidence: 通过专家混合建模多样交互以增强多模态融合
tldr: 现有多模态融合方法仅关注模态对应，忽略异构交互且缺乏可解释性。本文提出I^2MoE，一种端到端专家混合框架，显式建模多种模态交互类型（如互补、冲突），并输出可解释的交互线索。实验表明，I^2MoE在多个多模态任务中取得最优性能，同时提供了对融合过程的可解释洞察。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 859, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1750, \"height\": 836, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 804, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1725, \"height\": 295, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1688, \"height\": 293, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1563, \"height\": 777, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1582, \"height\": 783, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eujaf5qsmp/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1551, \"height\": 766, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 839, \"height\": 917, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1781, \"height\": 499, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 867, \"height\": 374, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 833, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 867, \"height\": 347, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1783, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1612, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1416, \"height\": 627, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1414, \"height\": 624, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1413, \"height\": 515, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1414, \"height\": 625, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eujaf5qsmp/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 800, \"height\": 317, \"label\": \"Table\"}]"
motivation: 现有多模态融合忽略模态间的异构交互，且缺乏可解释性。
method: 提出I^2MoE框架，利用专家混合显式建模多种模态交互模式，并提供可解释的交互权重。
result: 在多个多模态基准上，I^2MoE取得最佳性能，并能解释融合过程中各模态的贡献。
conclusion: 显式建模异构交互和可解释性是多模态融合的重要方向。
---

## Abstract
Modality fusion is a cornerstone of multimodal learning, enabling information integration from diverse data sources. However, existing approaches are limited by $\textbf{(a)}$ their focus on modality correspondences, which neglects heterogeneous interactions between modalities, and $\textbf{(b)}$ the fact that they output a single multimodal prediction without offering interpretable insights into the multimodal interactions present in the data. In this work, we propose $\texttt{I$^2$MoE}$ ($\underline{I}$nterpretable Multimodal $\underline{I}$nteraction-aware $\underline{M}$ixture-$\underline{o}$f-$\underline{E}$xperts), an end-to-end MoE framework designed to enhance modality fusion by explicitly modeling diverse multimodal interactions, as well as providing interpretation on a local and global level. First, $\texttt{I$^2$MoE}$ utilizes different interaction experts with weakly supervised interaction losses to learn multimodal interactions in a data-driven way. Second, $\texttt{I$^2$MoE}$ deploys a reweighting model that assigns importance scores for the output of each interaction expert, which offers sample-level and dataset-level interpretation. Extensive evaluation of medical and general multimodal datasets shows that $\texttt{I$^2$MoE}$ is flexible enough to be combined with different fusion techniques, consistently improves task performance, and provides interpretation across various real-world scenarios. Code is available at https://github.com/Raina-Xin/I2MoE.

---

## 论文详细总结（自动生成）

# I²MoE：可解释的多模态交互感知专家混合模型 —— 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有多模态融合方法存在两个主要局限：① 无法建模模态间异构的交互关系（如互补、冗余、冲突等）；② 缺乏可解释性，不能揭示数据中蕴含的多模态交互模式。
- **背景意义**：多模态学习在医疗、情感分析等领域至关重要，但现有融合方法（如早期融合、后期融合、Transformer 等）通常将所有模态信息平等处理，忽略了信息分解理论（PID）中定义的四种交互类型：模态独有信息、冗余信息、协同信息。这导致模型不能充分利用不同模态间的复杂关系，且决策过程不透明。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
提出 I²MoE（Interpretable Multimodal Interaction-aware Mixture of Experts），一个端到端的专家混合框架，通过**多个交互专家**显式建模不同类型的模态交互，并利用**重加权模型**为每个专家分配重要性分数，提供样本级和数据集级解释。

### 关键技术细节

1. **专家设计**：针对两个模态场景，设置四个交互专家：
   - \(F_{uni1}\)：建模模态1的独有信息
   - \(F_{uni2}\)：建模模态2的独有信息
   - \(F_{syn}\)：建模协同信息（两者结合才能产生的新信息）
   - \(F_{red}\)：建模冗余信息（两者共享的信息）

2. **弱监督交互损失**：通过随机向量替换一个模态生成扰动输入，比较完整输入与扰动输入的输出差异，设计目标函数：
   - 对独有专家：鼓励完整输出与保留本模态、屏蔽另一模态的输出相似，与屏蔽本模态的输出相异
   - 对协同专家：鼓励完整输出与所有屏蔽输出相异
   - 对冗余专家：鼓励所有输出尽可能相似
   - 损失函数可使用 Triplet Margin Loss、余弦相似度、MSE 等，根据任务选择

3. **重加权模型**：一个 MLP，以各模态的隐层嵌入为输入，输出每个交互专家的权重 \(w_i\)，最终预测为加权和：\(\hat{y} = \sum_i w_i \cdot \hat{y}_i\)

4. **扩展到多模态**：增加 n 个独有专家（每模态一个），加上一个协同专家和一个冗余专家，共 n+2 个专家；交互损失相应调整。

5. **训练与推理**：训练时计算任务损失 + 交互损失；推理时只使用完整输入一次前向，获取加权预测及权重。

## 3. 实验设计：数据集、场景、基准与对比方法

- **数据集（5个）**：
  | 数据集 | 类型 | 任务 | 模态 | 样本数 |
  |--------|------|------|------|--------|
  | ADNI | 医疗 | 阿尔茨海默病三分类 | 图像、基因、临床、生物样本（4种） | 2380 |
  | MIMIC-IV | 医疗 | 一年内死亡率二分类 | 检验、笔记、代码（3种） | 9003 |
  | IMDB | 通用 | 多标签电影类型分类（23类） | 图像、语言 | 25959 |
  | MOSI | 通用 | 情感回归与二分类 | 视觉、音频、文本 | 2199 |
  | ENRICO | 通用 | UI设计分类（20类） | 截图、线框图 | 1460 |

- **基准方法**：
  - 传统融合：早期融合（EF）、后期融合（LF）、低秩融合（LRMF）、MulT
  - 高级融合：InterpretCC、SwitchGate、MoE++
  - 对比方式：将 I²MoE 与 MulT 结合形成 I²MoE-MulT，并与上述方法比较；同时将 I²MoE 与其他骨干组合（SwitchGate、InterpretCC、MoE++）验证泛化性

- **评价指标**：Accuracy、AUROC、Micro/Macro F1（因任务而异）

## 4. 资源与算力

论文在附录 D 中给出了详细计算开销：
- 训练平台：单张 NVIDIA A100 GPU
- 对比了 MulT 与 I²MoE-MulT 的训练时间、推理延迟、参数量：
  - 例如 ADNI 数据集：MulT 训练 8.98s/epoch，I²MoE-MulT 16.82s/epoch；参数量从 1.07M 增至 6.70M
  - 增加约 (模态数+2) 倍的计算和参数量，但带来性能与可解释性的显著提升
- 未明确说明总GPU训练时长，但给出了各数据集训练轮数（30~60 epoch）和批次大小（8~128），可估算总计算量。

## 5. 实验数量与充分性

- **实验总数**：涵盖5个数据集，每个数据集至少3次随机种子平均结果。
- **主表（Table 1）**：比较了8种方法（含 I²MoE-MulT），涉及 Accuracy、AUROC、Micro/Macro F1。
- **泛化性表（Table 2）**：将 I²MoE 与 SwitchGate、InterpretCC、MoE++ 结合，在5个数据集上报告改进或下降。
- **消融实验（Table 4）**：5个变体（无交互损失、隐层对比、简化权重、少扰动、缺独有专家），在3个数据集上验证各组件必要性。
- **专家多样性分析（Table 3）**：统计专家一致/分歧比例及模型准确率。
- **个体专家性能对比（Figure 5）**：I²MoE 整体与单个专家比较。
- **人类评估（Appendix H）**：15人评价300个样本的局部解释合理性，70.4%正面反馈。
- **额外定性示例（Appendix I）**：展示多个电影分类的局部解释。
- **扰动策略消融（Appendix B）**：比较随机、均值、零向量三种掩码策略。
- **客观性与公平性**：控制了编码器和预测头一致，采用相同超参数搜索，但部分数据集小、类别不平衡（如 MIMIC 准确率下降但AUROC提升有合理解释）。总体设计较为严谨。

## 6. 论文的主要结论与发现

1. **性能提升显著**：I²MoE-MulT 在 ADNI 上 Accuracy 提升 5.5%，MOSI 上 Accuracy 提升 3%，IMDB 上 Macro F1 提升 1%；与 SwitchGate 结合在 ADNI 上 Accuracy 提升 5.23%。
2. **可解释性强**：提供样本级权重分布，人类评估 70.4% 认为合理；数据集级权重分布揭示不同数据集交互模式差异（如 ADNI 均匀，MIMIC 方差大）。
3. **各组件不可或缺**：消融实验表明移除交互损失、简化权重、减少扰动、去掉独有专家等均导致性能下降，证明设计合理。
4. **泛化性好**：可无缝集成到 MulT、SwitchGate、InterpretCC、MoE++ 等多种骨干，持续提升性能（除少数不平衡场景 Accuracy 下降但 AUROC 上升）。
5. **专家多样性重要**：多数情况下专家存在较高分歧，I²MoE 能有效融合分歧意见，但复杂数据集（如 IMDB、ENRICO）在分歧时准确率仍有待提高。

## 7. 优点：方法或实验设计上的亮点

- **方法创新性**：首次将 PID 理论融入端到端 MoE 框架，显式建模四种交互类型，并通过弱监督损失实现自动学习，无需人工标注。
- **可解释性**：同时提供局部（样本）和全局（数据集）解释，权重可直接解读为各交互模式的贡献度。
- **灵活性**：骨干无关，可与任何融合方法组合；支持任意数量模态（线性扩展）。
- **实验全面**：覆盖医疗和通用任务，多种指标，充分消融和人类评估，验证了各个设计选择。
- **开源**：代码已公开，便于复现和扩展。

## 8. 不足与局限

- **计算开销**：参数和训练时间增加约 (模态数+2) 倍，在模态较多时可能受限。
- **交互损失设计依赖启发式规则**：使用随机向量掩码模拟缺失模态，但未与真实缺失场景严格对齐；对比实验中随机掩码优于均值/零掩码，但理论解释不够深入。
- **分类任务局限性**：主要适用于分类/回归，对序列生成等任务尚未验证。
- **数据集偏倚风险**：MIMIC 存在类别不平衡，导致 Accuracy 下降（但 AUROC 提升），模型可能更关注少数类；IMDB 多标签任务专家分歧时准确率很低（84%错误），说明复杂交互场景下融合策略仍需改进。
- **人类评估规模较小**：仅15人评估300样本，且未控制评估者专业背景，结论推广性有限。
- **缺少更细粒度特征归因**：当前只提供专家整体权重，未深入分析哪些特征影响专家决策。

（完）
