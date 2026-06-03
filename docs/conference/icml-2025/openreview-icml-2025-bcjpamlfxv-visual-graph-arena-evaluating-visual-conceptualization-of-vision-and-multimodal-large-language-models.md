---
title: "Visual Graph Arena: Evaluating Visual Conceptualization of Vision and Multimodal Large Language Models"
title_zh: 视觉图竞技场：评估视觉和多模态大语言模型的视觉概念化能力
authors: "Zahra Babaiee, Peyman Kiasari, Daniela Rus, Radu Grosu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=BCJPAmlfxv"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 使用基于图形的任务评估概念化与视觉推理
tldr: 针对多模态大模型在视觉概念化能力上的缺失，本文提出Visual Graph Arena（VGA）数据集，包含六种基于图形布局的任务，用于评估模型对同一概念在不同视觉形式下的抽象推理能力。实验发现，当前最先进的视觉模型和多模态LLM在此类任务上远低于人类水平（人类近完美），揭示了AI在视觉抽象上的根本短板。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1718, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1673, \"height\": 481, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1646, \"height\": 951, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 565, \"height\": 252, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 334, \"height\": 297, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 386, \"height\": 246, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 843, \"height\": 482, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1418, \"height\": 2031, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1690, \"height\": 878, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1694, \"height\": 877, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1691, \"height\": 876, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1690, \"height\": 875, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1688, \"height\": 874, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1689, \"height\": 877, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1715, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1715, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1716, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1714, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1718, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1091, \"height\": 1097, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1093, \"height\": 1098, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1095, \"height\": 1097, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1095, \"height\": 1098, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1097, \"height\": 1099, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bcjpamlfxv/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1097, \"height\": 1101, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-bcjpamlfxv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1504, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bcjpamlfxv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1588, \"height\": 704, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bcjpamlfxv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 826, \"height\": 317, \"label\": \"Table\"}]"
motivation: 多模态大模型缺乏识别并推理同一概念不同视觉形式的能力。
method: 设计VGA数据集，包含六种图形任务，使用不同布局测试视觉抽象推理。
result: 人类接近完美，而AI模型在VGA上表现显著较差，凸显概念化能力的缺陷。
conclusion: VGA揭示了多模态LLM在视觉概念化上的不足，为未来研究提供了评估工具。
---

## Abstract
Recent advancements in multimodal large language models have driven breakthroughs in visual question answering. Yet, a critical gap persists, `conceptualization'—the ability to recognize and reason about the same concept despite variations in visual form, a basic ability of human reasoning. To address this challenge, we introduce the Visual Graph Arena (VGA), a dataset featuring six graph-based tasks designed to evaluate and improve AI systems’ capacity for visual abstraction. VGA uses diverse graph layouts (e.g., Kamada-Kawai vs. planar) to test reasoning independent of visual form. Experiments with state-of-the-art vision models and multimodal LLMs reveal a striking divide: humans achieved near-perfect accuracy across tasks, while models totally failed on isomorphism detection and showed limited success in path/cycle tasks. We further identify behavioral anomalies suggesting pseudo-intelligent pattern matching rather than genuine understanding. These findings underscore fundamental limitations in current AI models for visual understanding. By isolating the challenge of representation-invariant reasoning, the VGA provides a framework to drive progress toward human-like conceptualization in AI visual models. The Visual Graph Arena is available at: \href{https://vga.csail.mit.edu/}{vga.csail.mit.edu}.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：当前多模态大语言模型在视觉问题回答上取得进展，但缺乏**视觉概念化**能力——即识别并推理同一概念在不同视觉表现形式下（如不同布局）的能力。这是人类推理的基本能力，而AI模型存在显著差距。
- **背景**：尽管存在多个视觉推理数据集，但它们未能系统性地隔离“概念化”这一挑战。现有图数据集多为GNN设计，而非视觉形式；而视觉推理数据集（如CLEVR）也未针对表示不变性进行测试。
- **整体含义**：本文通过构建一个以**图结构**为载体的基准（Visual Graph Arena），专门评估和推动AI模型对**不变概念属性**的理解，而非表层模式匹配。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用**图布局多样性**（如Kamada-Kawai布局 vs. 平面布局）在训练集和测试集之间制造视觉差异，迫使模型仅凭图的结构属性（而非视觉样式）进行推理，从而测试其概念化能力。
- **关键技术细节**：
  - 数据集包含**6个任务**，分为三大类：
    - **图同构检测**：判断两图是否同构（易：随机选择非同构配对；难：仅选取度序列相同的非同构配对）。
    - **路径寻找**：哈密顿路径检测（二分类）、最短路径长度（四分类：1/2/3/4）。
    - **环检测**：哈密顿环检测（二分类）、最大无弦环长度（四分类：3/4/5/6）。
  - 训练集使用一种布局（同构任务：训练用Kamada-Kawai和平面同时？实际细节：同构训练用两种布局？从表1和图3说明看：同构任务训练和测试都包含两种布局？需要澄清。论文中描述：同构任务中训练集和测试集均采用Kamada-Kawai和平面布局对，但测试集均为未见过的图。路径任务：训练用随机/Kawai，测试用不同布局。环任务：训练用Kawai，测试用平面。具体见原文Table 1说明。
  - 每个图包含**8-9个节点**，保证视觉可分辨。
  - 数据集规模：训练样本27,500–155,718，测试样本2,480–15,718。
- **无特定公式或算法**：该工作为数据集和评估框架，不提出新模型或训练算法。

### 3. 实验设计：数据集、基准、对比方法

- **数据集**：Visual Graph Arena自有6个任务数据集。
- **基准**：**人类表现**——15名受试者（工程院学生/员工，24道题，每任务4题），作为近完美对照。
- **对比方法**：
  - **视觉模型**（微调10个epoch）：ViT Base, Swin-T Base, ConvNeXt Base（均ImageNet预训练）；SigLIP Base（视觉-语言预训练）；DINOv2 Base（自监督预训练）。
  - **多模态大语言模型**（零样本评估，100样本/任务）：GPT-4o, GPT-o1, Claude 3.5 Sonnet, Google Gemini等。
- **评价指标**：准确率（分类任务）。

### 4. 资源与算力

- 论文明确提及：使用**2块NVIDIA TITAN RTX GPU**，训练**10个epochs**，优化器Adam，学习率1e-4，batch size 32。
- **未说明**：具体训练总时长、能耗；也未提及MLLMs评估所用的硬件（推测为API调用）。

### 5. 实验数量与充分性

- **实验数量**：视觉模型在6个任务上各训练一次，报告最佳验证准确率；MLLMs在每任务上评100样本。人类仅24问。共约 **6（任务）× 5（视觉模型）+ 4（MLLM模型）× 6任务 + 1人类基线**，约30+组实验。
- **充分性与客观性**：
  - 实验设计**合理**：特意分离训练/测试布局，测试概念泛化；平衡正负样本。
  - **局限性**：缺少**消融实验**（如不同预训练策略、不同模型规模）；未对每个模型进行多次运行取平均以评估方差；MLLMs评估样本量小（100个），可能受随机性影响；人类评估样本小（15人），统计效力有限。
  - 整体上**较充分**，但未进行严格的统计显著性检验。

### 6. 论文的主要结论与发现

- **人类近完美**：所有任务准确率88.2%–100%。
- **视觉模型在同构任务上完全失败**（除SigLIP在Easy上54.4%略高），其他任务上也远低于人类。
- **ConvNeXt优于Transformer模型**（ViT, Swin-T），在部分任务上差距可达17个百分点。
- **MLLMs几乎全部随机水平**，仅GPT-o1在最短路径（55%）和哈密顿环（66.7%）上略好；但其成功主要依赖识别叶节点（简单启发式），而非真正理解。
- **异常行为识别**：GPT-o1存在“中等分数异常”和“简单更差异常”（如最短路径长度1准确率29%，长度2反倒70%），表明其依赖伪智能模式匹配，而非概念化。

### 7. 优点：方法或实验设计上的亮点

- **系统隔离概念化挑战**：通过变换布局，排除基于视觉样式作弊的可能，直接测试结构推理。
- **任务难度梯度设计合理**：同构任务从易到难（随机配对→度序列等价配对），路径/环任务覆盖不同复杂程度。
- **人类基线验证**：证明任务对人类可解，排除任务本身不可能。
- **异常行为分析**：提出“中等分数异常”和“简单更差异常”作为诊断伪智能的有力框架。
- **数据集开源且具规模**：提供足够样本供训练深度学习模型。

### 8. 不足与局限

- **图规模有限**：仅8-9节点，不足以评估复杂图的推理能力；布局种类仅两种（Kamada-Kawai, 平面/随机），泛化性受限。
- **评估方法局限**：MLLMs评估每任务仅100样本，可能因偶然性导致不确定性；未报告多次运行结果。
- **缺乏对模型内部行为的深入分析**：仅基于输出准确率推断伪智能，未结合注意力可视化或梯度分析。
- **视觉模型训练策略单一**：仅10个epoch，未探索更长训练或数据增强；也未对比其他视觉架构（如纯MLP或GNN）。
- **人类评估样本小**：15人、24问，且未控制受试者先验知识差异（部分概念被提前解释）。
- **未探索领域迁移**：论文提及可扩展到化学结构、逻辑电路，但未实际验证。
- **潜在偏差风险**：数据集合成方式可能引入特定布局下的可区分模式（如平面图与非平面图的结构差异），模型可能利用这些线索而非真正概念化。
- **缺失计算资源细节**：MLLMs的API调用成本、并发等未描述。

（完）
