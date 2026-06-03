---
title: Understanding the Emergence of Multimodal Representation Alignment
title_zh: 理解多模态表示对齐的涌现
authors: "Megan Tjandrasuwita, Chanakya Ekbote, Liu Ziyin, Paul Pu Liang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=4NJCI4Q3Za"
tags: ["query:native-multi"]
score: 6.0
evidence: 多模态表示隐式对齐的涌现研究
tldr: 多模态表示学习通常需要显式对齐，但近期发现大规模独立训练的单模态模型会隐式对齐。本文系统探究了这一涌现现象：何时发生？原因是什么？以及对齐是否可靠指示性能？通过大量实证，揭示了数据规模、模型容量等因素的影响，为多模态对齐提供了新视角。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 780, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 680, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 844, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1763, \"height\": 345, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 647, \"height\": 530, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1764, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1708, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1767, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1764, \"height\": 268, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1769, \"height\": 710, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1757, \"height\": 1753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1757, \"height\": 1753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1758, \"height\": 1763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1771, \"height\": 1760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1773, \"height\": 1766, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1773, \"height\": 1766, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1711, \"height\": 2058, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1710, \"height\": 2058, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1711, \"height\": 2057, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1758, \"height\": 1295, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1712, \"height\": 1510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1758, \"height\": 1756, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1709, \"height\": 2067, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1713, \"height\": 1268, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1699, \"height\": 1274, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1704, \"height\": 1265, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1618, \"height\": 2084, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1769, \"height\": 2196, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4njci4q3za/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1771, \"height\": 444, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-4njci4q3za/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1417, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4njci4q3za/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 402, \"height\": 419, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4njci4q3za/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 406, \"height\": 418, \"label\": \"Table\"}]"
motivation: 独立训练的单模态模型为何能隐式对齐尚不清楚。
method: 通过大规模实证分析，研究隐式对齐的涌现条件及性能关联。
result: 发现数据规模和模型容量是隐式对齐的关键因素，且对齐度与性能非单调相关。
conclusion: 隐式对齐现象挑战了显式对齐的必要性，为设计更高效的多模态学习方法提供了指导。
---

## Abstract
Multimodal representation learning is fundamentally about transforming incomparable modalities into comparable representations. While prior research has primarily focused on *explicitly* aligning these representations through targeted learning objectives and model architectures, a recent line of work has found that independently trained unimodal models of increasing scale and performance can become *implicitly* aligned with each other. These findings raise fundamental questions regarding the emergence of aligned representations in multimodal learning. Specifically: (1) when and why does alignment emerge implicitly? and (2) is alignment a reliable indicator of performance? Through a comprehensive empirical investigation, we demonstrate that both the emergence of alignment and its relationship with task performance depend on several critical data characteristics. These include, but are not necessarily limited to, the degree of similarity between the modalities and the balance between redundant and unique information they provide for the task. Our findings suggest that alignment may not be universally beneficial; rather, its impact on performance varies depending on the dataset and task. These insights can help practitioners determine whether increasing alignment between modalities is advantageous or, in some cases, detrimental to achieving optimal performance.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：多模态表示学习的关键在于将不可比较的不同模态（如文本与图像）转换为可比较的表示。传统方法依赖显式对齐（如对比学习、特定架构），但近期“柏拉图表示假设”（Platonic Representation Hypothesis）发现，独立训练的大规模单模态模型（如视觉模型和语言模型）之间会隐式涌现出对齐，且模型越大、性能越好，对齐越强。这一发现质疑了显式对齐的必要性，引发了基本问题。
- **核心问题**：① 对齐何时以及为何会隐式涌现？② 对齐是否是下游任务性能的可靠指标？
- **整体含义**：对齐并非普遍有益，其对性能的影响取决于数据特性（模态异质性和交互性）。需要重新审视对齐在多模态学习中的作用。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式与算法流程

- **核心思想**：利用两个维度—— **异质性**（Heterogeneity）和 **交互性**（Interactions）——来分类多模态数据。异质性度量模态间的固有相似性（如文本vs视频 vs 两种语言）；交互性度量任务相关的冗余/独特信息比例。通过系统性地改变这两个维度，观察对齐涌现和对齐性能关系的变化。
- **关键技术细节**：
  - **合成数据生成**：构建两种模态 \(X_1=[x_r, x_{u1}]\)，\(X_2=[x_r, x_{u2}]\)，其中 \(x_r\) 是冗余信息，\(x_{u1}, x_{u2}\) 是独特信息。标签 \(Y\) 由部分特征的非线性函数生成。通过控制用于生成标签的冗余特征数量 \(R\) 和独特特征数量 \(U\) 来调控交互性。异质性通过将 \(X_2\) 输入一个 \(D_\phi\) 层的MLP（ \(\phi\) ）变换实现。
  - **对齐度量**：主要使用 **Centered Kernel Alignment (CKA)**，公式为：
    \[
    \text{CKA}(Z_1, Z_2) = \frac{\text{HSIC}(Z_1Z_1^T, Z_2Z_2^T)}{\sqrt{\text{HSIC}(Z_1Z_1^T, Z_1Z_1^T) \cdot \text{HSIC}(Z_2Z_2^T, Z_2Z_2^T)}}
    \]
    对于大规模模型，使用计算效率更高的 **mutual k-nearest neighbors (mutual KNN)** 变体。
  - **算法流程**：① 生成具有不同 \(U\) 和 \(D_\phi\) 的合成数据集；② 对每个模态独立训练编码器（单层或深层MLP，深度可变）；③ 计算编码器表示之间的对齐；④ 训练下游分类器（线性或MLP）评估性能；⑤ 分析对齐与性能、深度之间的相关性。
- **真实数据变体**：在Wikipedia真实图文数据中，使用GPT-4生成不同独特程度的文本描述（替代原caption），以控制独特性。

## 3. 实验设计：数据集/场景、基准、对比方法

- **合成数据集**：二维输入（如二进制向量），标签由非线性函数（如OR）生成。固定总任务相关特征数 \(n_Y=8\)，改变 \(U\in\{0,\dots,8\}\)，变换深度 \(D_\phi\in\{1,3,5,7,9\}\)。对比不同编码器深度 \(D_{\text{Enc}}\in\{1,\dots,10\}\) 和不同随机种子（5 seeds）。
- **真实数据集**：
  - **Wikipedia Caption数据集**：原始图文对，用GPT-4生成独特化文本（10%～100%独特程度）。度量使用的视觉模型：DINOv2、ImageNet21k、CLIP、MAE等；语言模型：BLOOM、OpenLLaMA、LLaMA等（不同规模）。
  - **MultiBench**：情感分析（MOSEI, MOSI）、幽默检测（URFUNNY）、嘲讽检测（MUStARD）、数字分类（AVMNIST，冗余高）。使用Transformer编码器，深度1～10。
  - **MM-IMDb**：电影流派分类（23个二分类任务），使用电影海报和剧情文本。对齐性能线性拟合成斜率，用于指导显式对齐的权重选择。
- **对比方法**：主要对比不同模型容量（深度/参数规模）、不同独特性水平、不同异质性下对齐和性能的变化。没有与特定对比方法进行比较，而是系统性地探索关系。

## 4. 资源与算力

- **说明**：文中仅在致谢部分提到“We acknowledge NVIDIA’s GPU support”，未明确说明GPU型号、数量、训练时长等具体算力信息。因此，无法进行详细资源评估。

## 5. 实验数量与充分性

- **实验数量**：非常丰富。
  - 合成数据：覆盖 \(U=0\) 至 \(8\)，每个深度组合5个随机种子，总计超过 \(9 \times 5 \times 10 \times 5\)（变换深度×种子×编码深度×异质性）组实验。
  - 视觉-语言模型：使用5种视觉模型族、多种语言模型（13个模型）、5个独特等级（10%,30%,50%,70%,90%），每组有不同规模点。
  - MultiBench：5个数据集 × 3种模态对（视-音、视-文本、音-文本）× 10个编码深度 × 3种子 = 约450组对齐性能数据点。
  - MM-IMDb：23个类别 × 多种视觉模型族 × 10个CLIP权重。
- **消融实验**：
  - 不同对齐度量（CKA线性核/RBF、SVCCA、mutual KNN），不同批大小（256/512/1024）。
  - 不同E1深度（1/2/3）。
  - 随机初始化神经网络的对比。
- **充分性与客观性**：实验设计系统，覆盖了理论与实践的关键维度，统计方法（Spearman相关系数、线性拟合）恰当，结果一致性高。公平性较好，因为使用了公开数据集和预训练模型。唯一不足是真实数据独特性控制（GPT-4生成）可能引入偏差，但附录验证了语义相似性单调下降。

## 6. 论文的主要结论与发现

1. **对齐涌现受数据特性限制**：最大可实现对齐随独特性的增加而显著下降，随异质性的增加而下降。模型容量增加仅在冗余高时有效提升对齐；在独特信息高时，增加容量无法提升对齐。
2. **对齐与性能并非总是正相关**：在冗余高的数据上，对齐与性能强正相关；但在独特信息高的数据上，相关性能变弱甚至变为负。模型深度与性能始终正相关，而与对齐的相关性在独特高时消失。
3. **对齐-性能关系是数据集的内在属性**：在真实多模态数据集（如情感分析）中，对齐-性能相关性较弱或为负，而在冗余高的AVMNIST上强正。这一关系可用于指导显式对齐的权重选择（MM-IMDb实验验证）。
4. **对柏拉图表示假设的修正**：在完全冗余时支持该假设，但随着独特性和异质性增加，该假设不成立。

## 7. 优点

- **系统性维度框架**：提出异质性和交互性两个清晰维度，使研究结构化、可解释。
- **合成与真实数据互补**：合成数据提供因果控制，真实数据验证泛化性，两者结合增强结论可信度。
- **实际应用指导**：通过MM-IMDb实验展示了量化对齐-性能关系可直接用于优化训练（选择显式对齐权重），具有实用价值。
- **全面的消融和鲁棒性验证**：使用多种对齐度量、多种批大小、多种编码器深度，确保结论不依赖单一设定。
- **开源代码**：提供代码和实验细节，便于复现与扩展。

## 8. 不足与局限

- **实验覆盖**：主要考虑二维模态（图像-文本、视频-音频-文本），未涵盖更多模态（如3D、传感器数据）或更复杂的多模态交互（如多模态融合架构中隐式对齐）。
- **独特性控制偏差**：真实数据中独特性通过GPT-4修改文本实现，可能引入与原始图文无关的语义偏移或质量不均，影响对齐度量的可靠性。
- **模型简单性**：合成数据使用浅层MLP，真实数据使用Transformer但仅改变深度，未探索更现代的大规模模型（如VLM本身）的隐式对齐行为。
- **缺乏理论证明**：结论基于大量实证，但缺乏严格的数学解释（如信息论上界），限制了通用性。
- **潜在应用限制**：对齐-性能关系虽可用于算法设计，但计算成本较高（需训练多种模型并计算对齐），不利于快速部署。

（完）
