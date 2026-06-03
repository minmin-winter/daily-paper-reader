---
title: "SAE-V: Interpreting Multimodal Models for Enhanced Alignment"
title_zh: SAE-V：面向多模态模型的可解释性增强对齐方法
authors: "Hantao Lou, Changye Li, Jiaming Ji, Yaodong Yang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=S4HPn5Bo6k"
tags: ["query:balanced-mml"]
score: 5.0
evidence: 通过可解释性提升多模态对齐
tldr: 多模态大语言模型因模态融合导致对齐不稳定，易产生幻觉和偏差。本文提出SAE-V，将稀疏自编码器扩展到多模态场景，用于解释跨模态表征。通过解耦模态特定与共享特征，SAE-V提升了模型对齐质量，并揭示低质量数据如何导致模态偏差。实验证明，该方法在减少幻觉和模态不一致方面效果显著。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 767, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 814, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1761, \"height\": 327, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 846, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 845, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 631, \"height\": 551, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 705, \"height\": 392, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1755, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 764, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 702, \"height\": 453, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 762, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 826, \"height\": 552, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-s4hpn5bo6k/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 743, \"height\": 968, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 832, \"height\": 1305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 742, \"height\": 532, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1539, \"height\": 161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 870, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 854, \"height\": 784, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 871, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 858, \"height\": 812, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 865, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 565, \"height\": 408, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 872, \"height\": 696, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 877, \"height\": 700, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 869, \"height\": 987, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 872, \"height\": 1049, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-s4hpn5bo6k/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 868, \"height\": 193, \"label\": \"Table\"}]"
motivation: 多模态大模型的对齐易受低质量数据影响，导致模态不一致和幻觉，亟需可解释性方法。
method: 将稀疏自编码器扩展至多模态，设计跨模态表征解释框架，分离模态特有与共享特征。
result: 在多个多模态基准上，SAE-V有效降低幻觉，提升对齐稳定性。
conclusion: 可解释性技术是改善多模态模型对齐质量的关键工具。
---

## Abstract
With the integration of image modality, the semantic space of multimodal large language models (MLLMs) is more complex than text-only models, making their interpretability more challenging and their alignment less stable, particularly susceptible to low-quality data, which can lead to inconsistencies between modalities, hallucinations, and biased outputs. As a result, developing interpretability methods for MLLMs is crucial for improving alignment quality and efficiency. In text-only LLMs, Sparse Autoencoders (SAEs) have gained attention for their ability to interpret latent representations. However, extending SAEs to multimodal settings presents new challenges due to modality fusion and the difficulty of isolating cross-modal representations. To address these challenges, we introduce SAE-V, a mechanistic interpretability framework that extends the SAE paradigm to MLLMs. By identifying and analyzing interpretable features along with their corresponding data, SAE-V enables fine-grained interpretation of both model behavior and data quality, facilitating a deeper understanding of cross-modal interactions and alignment dynamics. Moreover, by utilizing cross-modal feature weighting, SAE-V provides an intrinsic data filtering mechanism to enhance model alignment without requiring additional models. Specifically, when applied to the alignment process of MLLMs, SAE-V-based data filtering methods could achieve more than 110% performance with less than 50% data. Our results highlight SAE-V’s ability to enhance interpretability and alignment in MLLMs, providing insights into their internal mechanisms.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究动机**：多模态大语言模型（MLLMs）在整合图像模态后，语义空间比纯文本模型更复杂，导致对齐过程不稳定，尤其容易受到低质量数据影响，出现模态不一致、幻觉和偏见输出。现有可解释性方法多用于纯文本 LLM（如稀疏自编码器 SAE），但直接扩展到多模态场景面临模态融合困难、跨模态表征难以解耦的挑战。
- **整体目标**：提出一个名为 **SAE-V** 的机械可解释性框架，将 SAE 范式扩展到 MLLMs，实现对模型行为和数据质量的细粒度解释，并利用该解释性自动过滤低质量数据以提升对齐效率与质量。

## 2. 方法论：核心思想、关键技术细节与算法流程

### 核心思想
- 在 MLLM 的某层隐状态上训练稀疏自编码器（SAE），学习稀疏的可解释特征（features）。通过分析这些特征在不同模态（文本与图像）上的激活模式，衡量特征的跨模态表征能力，并据此对训练数据进行评分与过滤。

### 关键技术细节
- **SAE-V 架构**：采用标准 Top-k SAE 结构（Bricken et al., 2023），包含编码器和特征字典（解码器）。给定输入隐状态 \(H \in \mathbb{R}^{l \times m}\)，编码得到稀疏特征激活 \(Z = \text{ReLU}(H W_{enc} + b_{enc})\)，\(Z \in \mathbb{R}^{l \times n}\)。训练损失为重建损失 \(L_R = \|H - Z (f_1,\dots,f_n)^\top\|_2^2\) 加上 L1 稀疏惩罚。
- **跨模态特征加权**：对于每个 SAE-V 特征 \(f_k\)，收集其在文本 token 和视觉 token 上的 top-K 激活值，计算两组激活的余弦相似度作为该特征的跨模态权重 \(\omega_k\)。
- **数据过滤算法**（Algorithm 1）分三阶段：
  1. **特征激活 Token 收集**：从训练数据中采样一个小子集，前向传播 MLLM 并提取 SAE-V 特征激活，记录每个特征激活的 token（区分文本与视觉）。
  2. **计算跨模态权重**：对每个特征，取其 top-K 文本激活 token 和 top-K 视觉激活 token，计算两组 token 的余弦相似度（公式 7）。
  3. **数据排序**：对每个训练样本，计算其所有激活特征的权重之和作为该样本的“跨模态得分”，按得分排序，保留高分数据用于对齐训练。

## 3. 实验设计

### 数据集与场景
- **SAE-V 模型训练与评估**：文本数据集 Pile（100k 训练，10k 测试），多模态数据集 Obelics（100k 训练，10k 测试）。
- **可解释性应用实验**：
  - ImageNet 分类：通过 SAE-V 特征选择图像 patches，保留不同比例（75%、50%、25%）测试分类精度。
  - VQA 任务：在 A-OKVQA 验证集上分别对文本和图像部分进行 patch 过滤，测量准确率变化。
- **对齐实验**：
  - 主数据集：Align-Anything（40k 多模态偏好子集）。
  - 消融数据集：MMInstruct、RLAIF-V。
  - 训练方法：Direct Preference Optimization (DPO)。
  - 评估基准：LLaVA-Bench。

### 对比方法
- **SAE-V 模型评估**：对比标准 SAE（仅在文本数据上训练）、零基线（Zero）、原始隐状态（Original）。
- **数据过滤方法**：
  - 随机选择（Random）
  - L0 排序、共现 L0 排序（Co-occurrence L0）
  - 余弦相似度排序（Cosine similarity）
  - 额外对比：IFD 指标（需额外训练模型）

### 使用的模型
- 目标 MLLMs：LLaVA-NeXT-Mistral-7B、LLaVA-NeXT-Vicuna-7B、LLaVA-NeXT-Vicuna-13B、Chameleon-7B、Anole-7B。
- 基础 LLM：Mistral-7B（用于 transfer 实验）。

## 4. 资源与算力

- **SAE-V 训练**：所有 SAE 和 SAE-V 训练在 **8×A800 GPUs** 上进行，每个训练大约 **21 小时**（见附录 A.1）。
- **对齐训练**：SFT 和 DPO 训练同样使用 **8×A800 GPUs**，超参数详见附录 B.2（如 batch size 8 per device，gradient accumulation 4，epoch 3，LR 1e-6，cosine scheduler）。

## 5. 实验数量与充分性

- **实验覆盖广泛**：
  - SAE-V 能力评估：在 5 个不同架构的 MLLMs 上训练并比较 L0 和重建损失。
  - 转移性实验：在 Mistral-7B、LLaVA-NeXT-7B 上测试 SAE-V 从 MLLM 到 LLM 的泛化。
  - 图像 patch 过滤：4 种不同指标（L0, L1, Co-occurrence L0, Cosine similarity）× 3 个保留比例（75%, 50%, 25%）+ 随机基线，共 5 组 × 3 = 15 组实验，附加定性案例。
  - 对齐实验：在 LLaVA-NeXT-7B 和 Chameleon-7B 两个模型上，配合三个数据集（Align-Anything、MMInstruct、RLAIF-V），多个过滤比例（0%~100% 步长 10%），对比随机、L0、共现、余弦相似度以及 IFD 等基线，还包括 1/20 子集参数搜索、不同模型规模（13B）等消融。
- **评价**：实验设计比较全面，涵盖了不同架构、不同数据集、不同过滤比例以及多种消融（模型、数据集、数据量、与其他过滤方法对比）。结果客观地展示了 SAE-V 的优势，且进行了统计相关性分析（图 10，r=0.84）。实验充分性较高。

## 6. 主要结论与发现

- **SAE-V 比标准 SAE 更适用 MLLMs**：在多模态模型上，SAE-V 的重建损失显著低于 SAE（低至 SAE 的 38.3%~50.6%），且 L0 更优，表明其能更有效地提取稀疏可解释特征。
- **跨模态特征可转移**：在 MLLM 上训练的 SAE-V 可以较好地迁移到其基础 LLM，甚至超过直接在 LLM 上训练的 SAE。
- **SAE-V 可有效识别图像关键信息**：在 ImageNet 图像 patch 过滤中，即使保留 25% 的 patches，SAE-V 方法仍能保持约 70% 的分类准确率（远高于随机基线）。
- **数据过滤显著提升对齐效率**：
  - 在 LLaVA-NeXT-7B 上，使用 50% 的过滤数据（共现 L0 过滤）达到全数据集性能的 **115%**（分数 108.17），使用 20% 数据达到 **108%**（余弦相似度过滤）。
  - 在 Chameleon-7B 上，余弦相似度过滤在 Align-Anything 上用 70% 数据达到全集的 **120%**；在 MMInstruct 上用 60% 数据达到 **117%**；在 RLAIF-V 上用 10% 数据达到 **125%**。
- **性能与跨模态得分正相关**：模型的平均余弦相似度得分与性能的皮尔逊相关系数达到 **0.84**，证明该指标可作为模型能力的指示器。
- **SAE-V 无需额外模型**：与 IFD 等方法相比，SAE-V 直接利用 MLLM 自身表示进行过滤，效率更高且通用性好。

## 7. 优点

- **新颖性**：首次将稀疏自编码器系统地扩展到多模态可解释性，并用于实际对齐优化，而不是仅停留于分析。
- **内源性数据过滤**：提出的余弦相似度加权机制无需额外模型或人工标注，完全利用 MLLM 内部表示，降低了数据筛选成本。
- **跨模态理解**：通过特征级别的余弦相似度，量化了每个特征对跨模态对齐的贡献，提供了比原始隐状态更细粒度的解释（例如识别“杜宾犬”或“对称性”这样的具体概念）。
- **实验严谨**：在多种架构（CLIP-based 和 early-fusion）、多数据集、多过滤方法、多消融条件下验证，结果一致支持结论。
- **实用价值**：仅使用少量高价值数据即可超越全量数据性能，对降低计算资源和数据收集成本具有实际意义。

## 8. 不足与局限

- **理论基础不充分**：论文承认 SAE-V 跨模态加权与模型性能之间的数学关系未完全揭示，缺乏理论证明（如为何余弦相似度高对应更好的对齐）。
- **模态覆盖有限**：仅验证了文本和视觉模态，未扩展到音频、视频、具身 AI 等场景，通用性待验证。
- **依赖初始数据集质量**：SAE-V 过滤基于模型内部表示，如果初始数据存在系统性偏差（如偏置），过滤后仍可能保留偏差，不能完全消除。
- **可解释性的负面风险**：论文在 Impact Statement 中提及，SAE-V 可能被滥用进行模型操控或逆向工程，需注意伦理使用。
- **实验仅覆盖部分模型**：虽然测试了 LLaVA-NeXT 系列和 Chameleon，但未在 Qwen-VL、Gemini 等流行模型上进行，可能局限于特定架构（不过作者声明未来可推广）。
- **计算成本**：虽然过滤不需要额外模型，但训练 SAE-V 本身仍需 8×A800 约 21 小时，对于超大模型可能成本较高。

（完）
