---
title: Aggregation of Dependent Expert Distributions in Multimodal Variational Autoencoders
title_zh: 多模态变分自编码器中依赖专家分布的聚合
authors: "Rogelio A. Mancisidor, Robert Jenssen, Shujian Yu, Michael Kampffmeyer"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=jYmGi1175R"
tags: ["query:unified-mm"]
score: 8.0
evidence: 提出多模态分布聚合新方法
tldr: 现有多模态VAE假设模态独立，聚合过于简单。本文提出基于依赖专家共识（CoDE）的聚合方法，通过学习各模态子集的贡献近似联合似然。CoDE-VAE在多个多模态基准上性能更优，为模态融合提供了更现实的依赖建模方式。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 823, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 609, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 607, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 644, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1729, \"height\": 333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 640, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1586, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1749, \"height\": 401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 586, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 866, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1612, \"height\": 922, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 836, \"height\": 633, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1656, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1659, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1468, \"height\": 868, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 527, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 527, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 528, \"height\": 521, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 527, \"height\": 520, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 827, \"height\": 1085, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 724, \"height\": 239, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 824, \"height\": 912, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1638, \"height\": 784, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1555, \"height\": 850, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1526, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 653, \"height\": 495, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1638, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 856, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1550, \"height\": 594, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1048, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1412, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1411, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1401, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1390, \"height\": 163, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1415, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1457, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1457, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 909, \"height\": 318, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 560, \"height\": 159, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1433, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1608, \"height\": 500, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1302, \"height\": 378, \"label\": \"Table\"}]"
motivation: 现有多模态VAE假设模态独立，聚合过于简化。
method: 提出CoDE方法，通过依赖专家共识学习各模态贡献进行聚合。
result: CoDE-VAE在多个基准上优于现有方法，更好建模模态依赖。
conclusion: 依赖专家共识能有效改进多模态分布聚合。
---

## Abstract
Multimodal learning with variational autoencoders (VAEs) requires estimating joint distributions to evaluate the evidence lower bound (ELBO). Current methods, the product and mixture of experts, aggregate single-modality distributions assuming independence for simplicity, which is an overoptimistic assumption. This research introduces a novel methodology for aggregating single-modality distributions by exploiting the principle of *consensus of dependent experts* (CoDE), which circumvents the aforementioned assumption. Utilizing the CoDE method, we propose a novel ELBO that approximates the joint likelihood of the multimodal data by learning the contribution of each subset of modalities. The resulting CoDE-VAE model demonstrates better performance in terms of balancing the trade-off between generative coherence and generative quality, as well as generating more precise log-likelihood estimations. CoDE-VAE further minimizes the generative quality gap as the number of modalities increases. In certain cases, it reaches a generative quality similar to that of unimodal VAEs, which is a desirable property that is lacking in most current methods. Finally, the classification accuracy achieved by CoDE-VAE is comparable to that of state-of-the-art multimodal VAE models.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：现有多模态变分自编码器（VAE）在估计联合变分后验分布时，广泛使用“专家乘积”（PoE）和“专家混合”（MoE）方法。这两种方法均假设各模态对应的专家分布相互独立，而实际中多模态数据是同一对象的不同信息源，存在显著依赖性，该假设过于乐观。此外，PoE易产生低密度后验，MoE在高维空间效率低且引入子采样策略会损害生成质量与似然估计。
- **整体含义**：本文旨在提出一种能有效建模专家分布间随机依赖性的新聚合方法，并基于此构建新的多模态VAE框架，以突破现有方法在生成一致性、生成质量及似然估计精度上的性能瓶颈。

## 2. 论文提出的方法论

### 核心思想：共识依赖专家（Consensus of Dependent Experts, CoDE）

- 将单模态分布视为“专家分布”，联合后验分布视为“共识分布”。
- 通过专家分布的估计误差建模依赖性：假设第 \( k \) 个共识分布的误差向量 \( \mathbf{e}_k \) 服从多元高斯分布 \( \mathcal{N}(\mathbf{0}, \Sigma_k) \)，其中协方差矩阵 \( \Sigma_k \) 的对角块 \( \Sigma_d \) 包含各专家在维度 \( d \) 上的方差（不确定性）和协方差（依赖性）。
- 利用贝叶斯原理，在平坦先验下推导出共识分布的后验高斯形式（Lemma 2）：
  \[
  q(\mathbf{z}|\mathbf{X}_k) \sim \mathcal{N}(\mathbf{A}_k^{-1}\mathbf{B}_k,\ \mathbf{A}_k^{-1})
  \]
  其中 \( \mathbf{A}_k = \mathbf{u}^T \Sigma_k^{-1} \mathbf{u},\ \mathbf{B}_k = \mathbf{u}^T \Sigma_k^{-1} \boldsymbol{\mu}_k \)，\( \boldsymbol{\mu}_k \) 为所有相关专家给出的点估计向量。当协方差为对角矩阵时，CoDE退化为PoE。

### 关键技术细节

- **依赖性参数**：协方差矩阵 \( \Sigma_d \) 中非对角线元素设为 \( \rho \sigma_i \sigma_j \)，相关性参数 \( \rho \) 通过交叉验证在 \( \{0, 0.2, 0.4, 0.6, 0.8\} \) 中选取。
- **新型ELBO**：引入指示变量 \( \xi \) 服从分类分布 \( \text{Cat}(\pi) \)，其中 \( \pi_k \) 为第 \( k \) 个子集的权重。通过最大化熵学习 \( \pi_k \)，使得更确定（协方差迹更小）的子集贡献更大。总体ELBO为：
  \[
  \mathcal{L}(\mathbf{X}) = \sum_{\mathbf{X}_k} \big[ \pi_k \big( \mathbb{E}_{q_\phi}[\log p_\theta] - \beta \cdot \text{KL} \big) + H(q_\phi(\xi|\mathbf{X}_k)) \big] + C
  \]
- **算法流程**：使用重参数化技巧和Adam优化器，按Algorithm 1迭代更新网络参数 \( \theta, \phi \) 及权重 \( \pi \)。

## 3. 实验设计

### 数据集

- **MNIST-SVHN-Text**：三模态（手写数字、街景数字、文本描述），含大量模态特有信息。
- **PolyMNIST**：5 模态（同数字不同背景与手写风格的MNIST图像），适合分析质量差距随模态度变化。
- **Caltech Birds (CUB)**：双模态（鸟图像与描述），真实复杂数据。
- 额外补充实验：**CelebA**（双模态图像+文本属性）。

### Benchmark与对比方法

- 对比方法：**MVAE** (PoE), **MMVAE** (MoE), **mmJSD**, **MoPoE-VAE**, **MVTCAE**, **MMVAE+**（含模态特有变量）。
- 评估指标：**生成一致性**（条件/无条件分类准确率）、**生成质量**（FID）、**对数似然估计**（ELBO紧度）、**分类准确率**（线性分类器）。

## 4. 资源与算力

- 论文附录 D.1 说明：模型在**单个 A100 GPU** 上训练，处理器为 AMD EPYC Milan（24核）。
- 训练时间：以 MNIST-SVHN-Text 为例，CoDE 每批 46 ms，PoE 为 36 ms；PolyMNIST（z∈R^512）上 CoDE 每批 1050 ms，PoE 为 790 ms。
- 未给出具体训练总时长或 epoch 数，但指出 “feasible even for 5-modality datasets on a single GPU”。

## 5. 实验数量与充分性

- **实验数量**：在 3 个主要数据集（MNIST-SVHN-Text, PolyMNIST, CUB）上进行全面评估，另在 CelebA 上补充对比。PolyMNIST 上训练了 2/3/4/5 模态共4种设置，每种设置需交叉验证 β、ρ、π，总计约 480 个实验，每个运行 3 次。
- **消融实验**：针对权重 π 和学习参数 ρ 进行消融（图6），验证了学习 π 和依赖建模的有效性。
- **公平性**：所有模型采用相同的 β 值范围交叉验证，报告最优结果；MMVAE+ 也包含模态特有变量以体现其优势。但未包含 CMVAE 在主实验内，仅在附录补充。
- **充分性**：实验覆盖了不同复杂度数据集、多模态数、多种指标，且分析了生成质量间隙随模态度增大的趋势，结论较充分。

## 6. 论文的主要结论与发现

1. **CoDE-VAE 在生成一致性与生成质量间取得更优平衡**：在 MNIST-SVHN-Text 上条件一致性达 0.82，高于所有对比方法；FID 虽非最优，但兼顾了高一致性。
2. **生成质量间隙最小化**：随着模态度增加，CoDE-VAE 的 FID 呈线性或下降趋势，在 PolyMNIST 上 4/5 模态时无条件生成质量接近单模态 VAE（图3）。
3. **对数似然估计更精确**：CoDE-VAE 的 ELBO 紧度与 PoE 类方法相当，但显著优于 MoE 类方法。
4. **分类准确率与 SOTA 相当**：在多个数据集上分类准确率与 MVTCAE 等相当。
5. **学习权重 π 和依赖参数 ρ 均有益**：消融实验证明二者共同提升生成质量与似然估计。

## 7. 优点

- **方法创新性**：首次将专家分布间的随机依赖性引入多模态 VAE，并通过贝叶斯原理推导出解析后验，理论完备。
- **计算可扩展性**：仅需对每个 Σ_d 求逆，复杂度与模态度线性相关，未引入过度计算开销。
- **应用普适性**：CoDE 可代替 PoE 用于任何基于 PoE 的多模态 VAE 框架。
- **实验全面性**：涵盖简单合成数据到真实复杂数据，多模态数可至 5，且详细分析了质量间隙这一重要问题。

## 8. 不足与局限

- **依赖参数需交叉验证**：相关性 ρ 通过离散网格搜索获得，在大规模或高维数据上可能效率低；论文未讨论 ρ 自适应学习方法。
- **计算复杂度 O(2^M - 1)**：随着模态数 M 增加，需维护指数级数量的 ELBO 项，虽然文中指出在 M≤5 时可行，但对更大 M（如10+）可能难以扩展。
- **先验与似然选择受限**：论文假设平坦先验和高斯似然，其他先验或非高斯似然下的适用性未探讨。
- **未在极大多模态数据上验证**：实验最大模态数为 5，实际应用中可能存在数十种模态的场景。
- **潜在偏差风险**：对比方法中 MMVAE+ 使用了模态特有变量，而 CoDE-VAE 未显式建模模态特有信息，虽在部分指标上仍具竞争力，但可进一步结合改进。

（完）
