---
title: "Generalizing from SIMPLE to HARD Visual Reasoning: Can We Mitigate Modality Imbalance in VLMs?"
title_zh: 从简单到困难视觉推理的泛化：能否缓解VLM中的模态不平衡？
authors: "Simon Park, Abhishek Panigrahi, Yun Cheng, Dingli Yu, Anirudh Goyal, Sanjeev Arora"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=reuPtSzCU9"
tags: ["query:balanced-mml"]
score: 9.0
evidence: 直接研究缓解视觉语言模型中的模态不平衡
tldr: 视觉语言模型在复杂视觉推理中表现弱，源于模态不平衡。本文构建合成推理基准明确分析该问题，并提出从简单任务训练泛化到困难任务的策略。实验证明该策略能有效缓解模态不平衡，提升VLM的推理能力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1740, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1707, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 830, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 834, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1606, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 833, \"height\": 466, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 855, \"height\": 369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1605, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 616, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 661, \"height\": 554, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1250, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1065, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1776, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1744, \"height\": 530, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1156, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1772, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1249, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1771, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1757, \"height\": 497, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1727, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 697, \"height\": 479, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1068, \"height\": 794, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1773, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1775, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1249, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1750, \"height\": 1119, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1742, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1616, \"height\": 665, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1604, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 1291, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 416, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 361, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1355, \"height\": 1074, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-reuptszcu9/fig-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 480, \"height\": 524, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 462, \"height\": 443, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1138, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1449, \"height\": 437, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1339, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1425, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1667, \"height\": 486, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1660, \"height\": 488, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1232, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1753, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1405, \"height\": 669, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1449, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 863, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1480, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1332, \"height\": 525, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1517, \"height\": 1034, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 898, \"height\": 491, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 821, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 909, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 821, \"height\": 361, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1260, \"height\": 920, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 552, \"height\": 458, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-reuptszcu9/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 470, \"height\": 131, \"label\": \"Table\"}]"
motivation: VLM在多步视觉推理中存在模态不平衡导致性能差。
method: 构建合成推理基准，提出从简单任务训练泛化到困难任务的策略。
result: 训练策略有效缓解模态不平衡，提升VLM在困难任务上的性能。
conclusion: 通过简单任务训练能有效改善VLM的模态不平衡问题。
---

## Abstract
Vision Language Models (VLMs) are impressive at visual question answering and image captioning. But they underperform on multi-step visual reasoning---even compared to LLMs on the same tasks presented in text form---giving rise to perceptions of *modality imbalance* or *brittleness*. Towards a systematic study of such issues, we introduce a synthetic framework for assessing the ability of VLMs to perform algorithmic visual reasoning, comprising three tasks: Table Readout, Grid Navigation, and Visual Analogy. Each has two levels of difficulty, SIMPLE and HARD, and even the SIMPLE versions are difficult for frontier VLMs. We propose strategies for training on the SIMPLE version of tasks that improve performance on the corresponding HARD task, i.e., simple-to-hard (S2H) generalization. This controlled setup, where each task also has an equivalent text-only version, allows a quantification of the modality imbalance and how it is impacted by training strategy. We show that 1) explicit image-to-text conversion is important in promoting S2H generalization on images, by transferring reasoning from text; 2) conversion can be internalized at test time. We also report results of mechanistic study of this phenomenon. We identify measures of gradient alignment that can identify training strategies that promote better S2H generalization. Ablations highlight the importance of chain-of-thought.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：Vision Language Models (VLMs) 在多步视觉推理任务中表现明显差于其在文本模态下的能力（例如，用图像输入比用文本输入的准确率低很多），这种 **模态不平衡 (modality imbalance)** 导致 VLM 的推理显得脆弱 (brittle)。  
- **研究动机**：量化并缓解这种模态不平衡，探索能否通过 **简单到困难 (SIMPLE-to-HARD, S2H) 泛化** 的训练策略，将文本模态已具备的强泛化能力迁移到图像模态，从而提升 VLM 在困难推理任务上的表现。  
- **整体含义**：该工作为系统性研究 VLM 的模态不平衡提供了可控制、可量化的合成框架，揭示了训练策略（特别是显式的图像到文本转换）对跨模态泛化的关键作用，并为未来构建更鲁棒的 VLM 提供了指导。

---

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想

- **合成任务框架**：设计了三个需要多步推理的算法性视觉任务（Table Readout、Grid Navigation、Visual Analogy），每个任务均有 **SIMPLE（简单）** 和 **HARD（困难）** 两个难度等级，且每个任务都有对等的 **图像输入** 和 **文本输入**（如 LaTeX 代码或文本描述），以便直接对比不同模态下的性能。
- **S2H 泛化**：模型在 SIMPLE 示例上训练，然后评测在 HARD 示例上的表现，以此衡量泛化能力。
- **训练策略**：核心是利用文本模态已有的 S2H 泛化能力，通过混合多种监督形式来“教”模型在图像模态下也能实现类似的泛化。

### 关键技术细节

1. **监督类型 (supervision types)**：
   - **Text**: 输入为文本（如 LaTeX 代码），输出包含 CoT 链和答案。
   - **Image**: 输入为图像，输出包含 CoT 和答案。
   - **Image-via-Text**: 输入为图像，但输出先包含转换提示 (P_convert) 和转换后的文本，再跟 CoT 和答案（强制显式转换）。
   - **Text+Image**: 等比例混合 Text 和 Image 监督。
   - **Mix**: 等比例混合 Text、Image、Image-via-Text 三种监督。
   - **Mix+**: 在 Mix 基础上额外加入 **HARD Text** 示例。
   - **Align-Mix+**: 先进行一个**对齐阶段**（用少量 SIMPLE 的 Text 和 Image-via-Text 训练），再进行 Mix+ 训练。

2. **链式思维 (CoT)**：所有训练输出都包含完整的逐步推理 CoT，对模型学习推理至关重要。实验表明完全移除 CoT 会导致 S2H 泛化失败。

3. **梯度对齐分析**：提出**梯度对齐分数 (Gradient Alignment Score)** 来量化 SIMPLE 梯度与 HARD 梯度的关系，分数越高表示 SIMPLE 训练对 HARD 损失下降越有效。该分数用于解释不同策略为何有效。

4. **损失分析**：分别测量 HARD 图像上的三类损失：
   - \(l^{(H)}_{(I\#;T)}\): 图像->文本转换损失
   - \(l^{(H)}_{(I,\#T;S)}\): 给定图像和转换文本后的推理损失
   - \(l^{(H)}_{(I;S)}\): 图像直接推理损失
   这种分解帮助理解模型在哪个环节卡住了。

---

## 3. 实验设计：数据集/场景、基准、对比方法

### 数据集/场景

- **三个合成任务**，每个都有 SIMPLE 和 HARD 版本：
  - **Consecutive Table Readout**: 表格中按行优先顺序读取单元格数值，SIMPLE 长度 5-10，HARD 长度 25-30。
  - **Table Readout**: 表格中沿高亮路径（螺旋/正弦图案）读取数值，SIMPLE 平均长度 12，HARD 平均长度 35。
  - **Grid Navigation**: 在网格中从起点到终点收集指定物体、避开障碍物，SIMPLE 含 1-2 个物体和 1 种障碍，HARD 含 2-5 个物体和 3-5 种障碍。
  - **Visual Analogy**: 基于抽象图形的类比推理，SIMPLE 中示例与查询共享同一属性域和关系，HARD 中属性域不同且关系组合为训练中未见的。
- **文本等价版本**：每个任务都能用文本（LaTeX、文本描述）表示，以便直接对比模态差异。

### Benchmark

- 主要评测指标：**Exact Match 准确率**（所有数值/路径/选项完全正确）。
- 额外分析指标：生成长度、损失曲线、梯度对齐分数。

### 对比方法

- **基线**：分别在 SIMPLE 上使用 Text、Image、Text+Image 监督训练。
- **所提策略**：Image-via-Text、Mix、Mix+、Align-Mix+。
- **闭源模型对比**：GPT-4o、Claude-3.5 Sonnet 在相同任务上的零样本表现（附录 I.1）。
- **跨模型验证**：部分实验也在 Qwen2.5-VL-3B/7B 上复现（附录 F）。

---

## 4. 资源与算力

- **模型**：Eagle-X2-Llama3-8B（基于 Llama3-8B-Instruct，视觉编码器为 CLIP-448 + ConvNeXt），使用 Deepspeed ZeRO Stage 2 进行分布式训练。
- **GPU 数量**：8 块 GPU（HPC 集群）。
- **训练时长**：文中未明确给出每个实验的具体耗时，但提供了训练步数（如图 7 显示约 200-400 步）和总数据量（如 12×10^4 示例）。附录 D 提到使用 AdamW 优化器、线性预热、余弦衰减。**训练时长未明确说明，但可推断每轮在 8 卡上耗时数小时量级**。
- **算力规模较小**：仅使用 8B 参数模型，未涉及更大模型或更长训练。

---

## 5. 实验数量与充分性

- **主要实验组数**：
  - 在 Consecutive Table Readout 上对比了 5 种监督类型，改变训练数据量（2k~16k），并报告 MEDIUM 和 HARD 两个难度等级（图 3、4）。
  - 在其他三个非 S2H 任务（Table Readout, Grid Navigation, Visual Analogy）上，对比了 Text、Image、Mix、Mix+、Align-Mix+ 等策略，在多个数据量下（0.5k~24k）报告准确率（图 5、6）。
  - 梯度分析实验：损失动态跟踪（图 8）、梯度对齐散点图（图 7、9）。
- **消融实验丰富**：
  - 对比不同监督比例（附录 I.2）
  - 对齐阶段的数据量及组成（附录 I.3）
  - 文本预热阶段的数据量（附录 I.4）
  - 显式 vs 隐式文本转换（附录 I.6）
  - CoT 完全移除 vs 逐步内化（附录 I.7）
  - 多任务联合训练（附录 I.8）
  - HARD 示例重复次数（附录 I.9）
  - 损失性 vs 无损文本表示（附录 I.5）
- **公平性**：所有策略在相同总训练数据量下比较（附录 C.1 控制独特样本数、训练轮数）；对比时固定批大小、学习率等超参数。  
- **结论**：实验设计系统、充分，覆盖了主要假设和备选解释。但**局限在合成任务**，真实场景泛化性未直接验证（见第 7 节讨论）。

---

## 6. 论文的主要结论与发现

1. **模态不平衡显著**：在 Consecutive Table Readout 上，Text 监督在 HARD 文本上可达 80% 准确率，而 Image 监督在 HARD 图像上仅 20%——差距达 60 个百分点。
2. **Mix 策略有效缓解不平衡**：对于 S2H 泛化良好的任务（Consecutive Table Readout），Mix 监督（混合 Text、Image、Image-via-Text）将图像泛化准确率从 20% 大幅提升（接近文本水平），同时保持较低的推理开销（因为不需要显式转换）。
3. **非 S2H 任务需引入 HARD 文本**：在其他三个任务上，单独使用 SIMPLE 数据无法泛化到 HARD。**Mix+**（加入 HARD Text）成功将文本推理能力迁移到图像：Table Readout 64%、Grid Navigation 92%、Visual Analogy 35%（12×10^4 数据时）。
4. **两阶段对齐 (Align-Mix+)** 进一步提升：增加一个对齐阶段（用 SIMPLE 的 Text + Image-via-Text 预训练）后，图像泛化准确率进一步提升至 76%、96%、56%。
5. **文本转换可内化**：Mix+ 训练后的模型在测试时若被提示“Convert”，能自动执行图像到文本转换，且转换后性能更优，但即使不提示直接推理也有不错性能——说明转换能力已被内化。
6. **梯度对齐可解释效果**：Mix+ 和 Align-Mix+ 的梯度对齐分数更高，尤其在梯度范数大时，这解释了它们为何能更有效地降低 HARD 图像的损失。
7. **CoT 至关重要**：移除或逐渐内化 CoT 会导致图像 S2H 泛化完全失败，表明显式推理步骤是跨模态迁移的必要条件。

---

## 7. 优点：方法或实验设计上的亮点

- **可控的合成框架**：每个任务都有明确定义的 SIMPLE/HARD 界限、等价的文本版本，使模态不平衡的量化成为可能，且排除了真实数据中的混杂因素。
- **多监督对比**：系统对比了 Text、Image、Image-via-Text、Mix 等一系列策略，清晰揭示了各成分的作用，特别是 Image-via-Text 的关键性。
- **梯度机制分析**：不仅报告最终性能，还通过损失分解和梯度对齐分数深入理解训练动态，为策略有效性提供了理论基础。
- **推理效率考量**：Mix 策略在保持高性能的同时避免了显式转换带来的过长输出，兼顾了实用性与泛化性。
- **跨模型验证**：在 Qwen2.5-VL 系列上复现了核心结果（附录 F），说明结论具有一定泛化性。

---

## 8. 不足与局限

- **任务合成性**：所有任务均为合成，视觉分布单一，与现实场景（如自然图像、图表、文档）差异大。虽然附录 G.6 展示了在真实基准（MMMU、ChartQA）上的正向迁移，但**结论是否能直接推广到更复杂的真实推理任务仍需验证**。
- **模型规模有限**：仅使用 8B 参数的 VLM，未测试更大模型（如 70B）或更强基础模型（如 GPT-4V）。作者在讨论中指出未来更强 LLM 可能进一步缩小差距。
- **CoT 依赖**：完全移除 CoT 会导致泛化失败，说明当前方法尚未实现真正的“内化”推理；逐步内化尝试也未成功，表明对 CoT 模板的脆弱性。
- **计算开销**：Image-via-Text 和 Mix+ 等策略需要生成或训练包含长文本转换的序列，训练和推理成本较高（如生成长度增加 3 倍）。Align-Mix+ 需要两个阶段训练，增加了复杂度。
- **文本表示要求**：方法依赖任务存在合适的文本等价表示（如 LaTeX、结构描述）。对于难以用语言精确描述的视觉场景（如纹理、光照），该方法可能失效。但附录 I.5 表明即使使用有损文本表示也能工作，缓解了部分担忧。
- **消融范围有限**：未探索课程学习、动态数据混合等更先进的策略；未测试在其他 VLM 架构（如 LLaVA-NeXT）上的可迁移性。
- **性能天花板**：在 Visual Analogy 等复杂任务上，即使 Align-Mix+ 也仅达到 56% 准确率，与文本的 95%+ 仍有差距，模态不平衡未完全消除。

（完）
