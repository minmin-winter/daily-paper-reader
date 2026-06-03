---
title: "Modalities Contribute Unequally: Enhancing Medical Multi-modal Learning through Adaptive Modality Token Re-balancing"
title_zh: 模态贡献不均：通过自适应模态标记重平衡增强医学多模态学习
authors: "Jie Peng, Jenna L. Ballard, Mohan Zhang, Sukwon Yun, Jiayi Xin, Qi Long, Yanyong Zhang, Tianlong Chen"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=MzQed6QEmS"
tags: ["query:balanced-mml"]
score: 10.0
evidence: 自适应模态标记重平衡解决模态不平衡问题
tldr: 本文针对医学多模态学习中不同模态和患者间数据质量差异导致的模态不平衡问题，提出自适应模态标记重平衡（AMC）方法。AMC通过自顶向下的动态融合，自适应调整各模态的贡献。在TCGA基准上验证了其有效缓解模态批次效应，提升多模态融合性能。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 856, \"height\": 696, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 842, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 861, \"height\": 305, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 857, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 861, \"height\": 436, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1761, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 861, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzqed6qems/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1724, \"height\": 1703, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1291, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 864, \"height\": 464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 865, \"height\": 464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 867, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 870, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1257, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1764, \"height\": 142, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 898, \"height\": 148, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1073, \"height\": 157, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1074, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzqed6qems/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 553, \"height\": 306, \"label\": \"Table\"}]"
motivation: 医学多模态数据中模态质量差异导致不平衡，需要自适应融合方法。
method: 提出AMC方法，通过自顶向下的动态模态标记重平衡实现自适应融合。
result: 在TCGA基准上有效缓解模态批次效应，提升融合性能。
conclusion: 自适应模态重平衡是提升医学多模态学习的关键。
---

## Abstract
Medical multi-modal learning requires an effective fusion capability of various heterogeneous modalities.
One vital challenge is how to effectively fuse modalities when their data quality varies across different modalities and patients.
For example, in the TCGA benchmark, the performance of the same modality can differ between types of cancer. 
Moreover, data collected at different times, locations, and with varying reagents can introduce inter-modal data quality differences ($i.e.$, $\textbf{Modality Batch Effect}$).
In response, we propose ${\textbf{A}}$daptive ${\textbf{M}}$odality Token Re-Balan${\textbf{C}}$ing ($\texttt{AMC}$), a novel top-down dynamic multi-modal fusion approach.
The core of $\texttt{AMC}$ is to quantify the significance of each modality (Top) and then fuse them according to the modality importance (Down).
Specifically, we access the quality of each input modality and then replace uninformative tokens with inter-modal tokens, accordingly.
The more important a modality is, the more informative tokens are retained from that modality.
The self-attention will further integrate these mixed tokens to fuse multi-modal knowledge.
Comprehensive experiments on both medical and general multi-modal datasets demonstrate the effectiveness and generalizability of $\texttt{AMC}$.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与研究动机

- **核心问题**：医学多模态学习中，不同模态（如病理图像、基因组数据、临床文本）的数据质量存在显著差异，且质量随癌症类型、患者个体、采集批次（**模态批次效应**）动态变化。现有融合方法（如自注意力、门控网络）隐式学习模态贡献，但难以有效处理这种**贡献不均**，且在缺乏显式跨模态映射关系的医学场景中，原始Token融合（Token Fusion）因需要明确映射关系而不可用。
- **研究动机**：开发一种自顶向下的**动态多模态融合方法**，显式量化各模态重要性，并根据重要性自适应地平衡模态贡献，提升医学多模态学习的鲁棒性与可解释性。

## 2. 方法论：自适应模态标记重平衡（AMC）

### 2.1 核心思想
- **自顶向下**：先（Top）计算各模态重要性 → 再（Down）依据重要性进行自定义Token融合。
- **关键假设**：模态贡献不均，应保留重要模态的更多信息性Token，用其他模态的Token替换不重要模态中的无效Token。

### 2.2 关键技术细节

#### 步骤1：模态重要性计算（Modality Importance Calculation）
- 利用**差分注意力模块**（Differential Attention）生成的注意力图 \(A \in \mathbb{R}^{M \times N \times N}\)（M=模态数，N=Token数）。
- 对每模态 \(m\)，计算平均最大注意力值：
  \[
  \sigma[m] = \text{Mean}(\max_k A_{m,n,k})
  \]
- 归一化为模态重要性 \(s_m\)，确定该模态应被替换的Token数 \(K_m = \lfloor s_m \times N \rfloor\)。

#### 步骤2：自定义Token融合（Customized Token Fusion）
- **RQ1（识别无效Token）**：用与重要性计算相同的注意力分数 \(\eta[m,n] = \max_k A_{m,n,k}\) 作为Token分数，选择最低 \(K_m\) 个Token作为无效Token。
- **RQ2（替换来源选择）**：
  - 引入**两级对比学习损失**：
    - 实例级对比学习（\(L_I\)）：同一实例的不同模态特征作为正样本。
    - Token级对比学习（\(L_T\)）：同一位置 \(n\) 的不同模态Token作为正样本。
  - 通过对比学习，使同一位置的不同模态Token对齐，从而将候选替换空间从所有其他Token缩小到同一位置的Token \(\{x_{m'}[n]\}\)。
  - 选择其中**Token分数最高**的模态的Token进行替换。
- **RQ3（融合后预测）**：对每个模态的Token序列进行平均池化，再拼接所有模态的池化向量，输入任务头（线性层）进行预测。

#### 2.3 网络架构关键改进
- **差分注意力**（替代标准自注意力）：将Q、K分为两组，计算两个softmax的加权差，减弱对无关上下文的注意力分配，提升重要性计算的准确性。
- **稀疏混合专家（SMoE）**（替代MLP）：缓解多模态间的梯度冲突，提升参数效率。
- **两级对比学习**（\(L_I + L_T\)）：增强跨模态Token的对齐，无需显式映射关系。

#### 2.4 算法流程（文字描述）
1. 各模态通过特定编码器（如Q-Former）生成等长Token序列（\(N\)个Token）。
2. 沿batch维拼接所有模态Token（batch size = M × 实例数）。
3. 经过多个改进Transformer块（差分注意力+SMoE+Token融合）。
4. 在每个Transformer块后，根据注意力图计算模态重要性 \(s_m\) 和Token分数 \(\eta\)。
5. 对每模态 \(m\)，保留Top-\((N-K_m)\)个Token，并用其他模态中同一位置且分数最高的Token替换Bottom-\(K_m\)个Token。
6. 经过所有层后，分开各模态Token，平均池化并拼接，输入任务头。

## 3. 实验设计

### 3.1 数据集与场景
| 数据集 | 模态 | 任务 | 样本量 |
|--------|------|------|--------|
| **TCGA**（5种癌症：UCEC, LUAD, LGG, BRCA, BLCA） | 全切片图像(WSI)、病理报告、RNA-seq | 生存时间预测（C-index） | 2,585人 |
| **MIMIC-IV** | 实验室测量(Lab)、临床笔记(Note)、账单代码(Code) | 院内一年死亡率预测（二分类） | 9,003人 |
| **ADNI** | 生物流体标志物、临床评估、基因组、神经影像 | 认知状态三分类（CN/MCI/AD） | 2,380人 |
| **ENRICO**（通用基准） | 应用截图(Image)与视图层次(Set) | 20类设计主题分类 | 1,460 |

### 3.2 对比方法
- **多模态融合基线**：FlexMoE、FuseMoE、LiMoE、MAGGate、MulT、TensorFusion（TF）、MUSE
- **单模态基线**（仅ENRICO）：Image Only, Set Only
- **方法变体**：AMC w/ STD, AMC w/ Max, AMC w/o Differential Attention, AMC w/ Original Token Fusion等

### 3.3 实验配置
- 数据拆分：70%训练，15%验证，15%测试
- 每次实验运行5次不同随机种子，取平均值±标准差
- 超参数搜索：学习率[1e-3,1e-4,5e-5,1e-5]，隐藏维度[32,64,128]，batch size[32,64,128]，专家数[4,8,16]，对比损失权重[1.0,0.1]等

## 4. 资源与算力

- 文中提及使用 **RTX 3090 GPUs** 进行实验，**未明确具体数量与训练时长**（仅提到默认每次实验5次重复）。
- 补充：附录表10给出了计算效率对比，AMC的GFLOPs为45.23（低于多数基线），单次迭代平均时间11.5秒（低于部分基线），表明其计算效率良好。

## 5. 实验数量与充分性

- **主要实验**：4个数据集（TCGA含5癌种、ADNI、MIMIC-IV、ENRICO），共8个具体任务。
- **对比基线**：7种主流多模态融合方法，ENRICO额外对比单模态。
- **消融实验**（MIMIC-IV上）：逐一去除Token融合、对比学习、差分注意力、SMoE，共5组。
- **深入分析实验**：
  - 模态重要性计算方法对比（Mean vs STD vs Max）
  - Token得分方法对比（AMC vs 原始Token Fusion vs 无差分注意力）
  - Token交换统计可视化
  - 模态重要性可视化（分布分析）
  - 梯度冲突分析（SMoE vs 密集MLP）
  - 模态缺失场景测试（ADNI）
  - 案例研究（图像质量与模态重要性关联）
- **充分性评价**：实验覆盖了多个医学任务和通用任务，消融充分，统计分析（多次重复）和深入分析（可解释性、梯度、缺失场景）全面。对比方法均为近期主流，公平性较好（采用原论文最优超参或自行搜索）。**总体充分客观**。

## 6. 主要结论与发现

1. **AMC 在多数任务上取得最佳或次佳**：TCGA平均C-index 0.734（最优），ADNI上Accuracy/F1优于基线，MIMIC-IV上Recall/Precision/F1均最优。
2. **自顶向下的显式重要性量化有效**：平均注意力值作为模态重要性指标优于标准差或最大值。
3. **差分注意力提升Token得分质量**：用差分注意力替代标准注意力或原始线性评分网络均能提升性能。
4. **对比学习消除显式映射需求**：两级对比学习实现跨模态对齐，可避免原始Token Fusion需预定义映射的限制。
5. **SMoE缓解模态梯度冲突**：对比分析显示AMC+MoE的模态梯度余弦距离更高（冲突更小）。
6. **可解释性良好**：能够可视化每个实例中模态重要性及Token替换情况，有助于临床信任。

## 7. 优点

1. **方法创新性**：提出首个自顶向下显式量化模态重要性并据此进行Token重平衡的融合框架，解决了医学场景中模态映射缺失的问题。
2. **技术集成合理**：差分注意力、稀疏MoE、两级对比学习的组合相互支撑，共同提升融合质量。
3. **实验全面**：覆盖多种医学任务（生存预测、分类）及通用任务，消融与分析充分。
4. **计算效率**：GFLOPs低于多数基线，实际训练速度较快。
5. **可解释性**：提供模态级别和Token级别的贡献可视化，符合AI4Medical需求。

## 8. 不足与局限

1. **算力消耗未明确**：虽提到使用RTX 3090，但未说明GPU数量和训练总时长，限制了复现和成本评估。
2. **模态缺失仅简单扩展**：将缺失模态的重要性/分数设为0，可能忽略复杂缺失模式（如部分缺失、随机缺失）。
3. **对比学习依赖批量大小**：两级对比学习的效果可能受批次内负样本数量影响，文中未详细分析。
4. **特定场景性能波动**：在TCGA的LGG和BRCA上未达到最佳（分别第三和第二），说明方法对某些癌种适应性有限。
5. **ADNI Precision较低**：虽然Accuracy/F1较高，但Precision低于MUSE和FlexMOE，存在一定假阳性风险。
6. **通用基准覆盖面有限**：仅在ENRICO一个通用数据集上测试，缺少更多样化场景（如视频+音频）的验证。
7. **未讨论长序列效率**：当模态数M增大时，注意力复杂度仍为O(MN²)，未提供进一步优化策略。

（完）
