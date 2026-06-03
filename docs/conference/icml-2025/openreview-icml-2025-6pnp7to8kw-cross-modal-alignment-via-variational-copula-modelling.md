---
title: Cross-Modal Alignment via Variational Copula Modelling
title_zh: 基于变分Copula建模的跨模态对齐方法
authors: "Feng Wu, Tsai Hor Chan, Fuying Wang, Guosheng Yin, Lequan Yu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=6pNp7to8kW"
tags: ["query:native-multi"]
score: 8.0
evidence: 基于Copula的跨模态对齐与融合
tldr: 现有跨模态对齐与融合方法通常使用拼接或克罗内克积，忽略了模态间高阶交互。本文引入Copula理论，变分地建模模态表征的联合分布，捕捉复杂交互结构。在医疗等多模态数据集上，该方法在分类和回归任务中显著优于传统融合方法，为处理复杂多模态交互提供了统计上严谨的建模框架。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-6pnp7to8kw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1604, \"height\": 786, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6pnp7to8kw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1700, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6pnp7to8kw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 775, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6pnp7to8kw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1703, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6pnp7to8kw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1636, \"height\": 548, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 849, \"height\": 368, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1767, \"height\": 664, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 661, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 854, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 858, \"height\": 335, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 859, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1594, \"height\": 392, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1235, \"height\": 622, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1595, \"height\": 486, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1766, \"height\": 1481, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6pnp7to8kw/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1239, \"height\": 347, \"label\": \"Table\"}]"
motivation: 现有融合方法简化了模态间交互结构，未能建模高阶交互关系。
method: 利用Copula作为统计工具，变分地建模多模态表征的联合分布以捕捉高阶交互。
result: 在医疗等多模态数据集上，该方法在分类和回归任务中超越基线。
conclusion: Copula为多模态融合提供了强有力的高阶交互建模能力。
---

## Abstract
Various data modalities are common in real-world applications. (e.g., EHR, medical images and clinical notes in healthcare). Thus, it is essential to develop multimodal learning methods to aggregate information from multiple modalities. The main challenge is appropriately aligning and fusing the representations of different modalities into a joint distribution. Existing methods mainly rely on concatenation or the Kronecker product, oversimplifying interactions structure between modalities and indicating a need to model more complex interactions. Additionally, the joint distribution of latent representations with higher-order interactions is underexplored. Copula is a powerful statistical structure in modelling the interactions between variables, as it bridges the joint distribution and marginal distributions of multiple variables. In this paper, we propose a novel copula modelling-driven multimodal learning framework, which focuses on learning the joint distribution of various modalities to capture the complex interaction among them. The key idea is interpreting the copula model as a tool to align the marginal distributions of the modalities efficiently. By assuming a Gaussian mixture distribution for each modality and a copula model on the joint distribution, our model can also generate accurate representations for missing modalities. Extensive experiments on public MIMIC datasets demonstrate the superior performance of our model over other competitors. The code is anonymously available at https://github.com/HKU-MedAI/CMCM.

---

## 论文详细总结（自动生成）

# 论文结构化总结：Cross-Modal Alignment via Variational Copula Modelling

## 1. 核心问题与研究动机
多模态学习在现实应用中（如医疗中的电子健康记录、医学影像、临床笔记）至关重要，但现有对齐与融合方法（如拼接、克罗内克积）过度简化了模态间的交互结构，无法捕捉高阶交互关系。此外，现有方法大多假设所有模态完整可用，但在实际中常存在模态缺失问题，简单丢弃或均值填充会引入偏差。本文的核心问题是：**如何从概率视角建模多模态表征的联合分布，以准确捕捉复杂交互，并鲁棒地处理缺失模态？**

## 2. 方法论：核心思想与技术细节

### 2.1 核心思想
利用统计学中的 **Copula 模型** 作为桥梁，将多模态的边际分布与联合分布解耦，从而高效对齐各模态分布。通过变分推断优化 Copula 参数，并利用高斯混合模型（GMM）灵活建模各模态的边际分布。

### 2.2 关键技术与流程
- **模态编码**：每个模态通过专用编码器（ResNet34、LSTM、TinyBERT）提取特征嵌入 \(z_m\)。
- **边际分布建模**：假设每个模态的特征嵌入服从 \(K\) 分量高斯混合模型（GMM）：  
  \(f_m(z_m) = \sum_{k=1}^K \pi_{mk} \mathcal{N}(\mu_{mk}, \Sigma_{mk})\)，其中权重、均值、协方差均可训练。
- **联合分布建模**：通过 Copula 函数 \(C\) 连接各边际累积分布函数（CDF）得到联合分布：  
  \(F_{z_1,\dots,z_M}(z) = C(F_1(z_1), \dots, F_M(z_M))\)。
- **变分推断优化**：引入证据下界（ELBO）作为目标函数，结合 Copula 密度对数似然和任务损失（如交叉熵）：  
  \(\text{ELBO} = -\lambda_{\text{cop}} \sum_i [\log c(Q_1(z_1^{(i)}), \dots, Q_M(z_M^{(i)})) - \sum_m \log f_m(z_m^{(i)})] + \mathcal{L}_{\text{task}}\)。
- **缺失模态处理**：从已学习的 GMM 中采样生成缺失模态的伪特征嵌入，再送入融合模块与分类器。
- **理论保证**：基于 Sklar 定理，连续边际分布保证 Copula 唯一，从而增强模型可识别性。

## 3. 实验设计

### 3.1 数据集与场景
- **MIMIC-III**、**MIMIC-IV**（电子健康记录时间序列）、**MIMIC-CXR**（胸部X光图像及放射学报告）、**MIMIC-III NOTE**（临床笔记）。
- 分为**完全匹配**（所有模态均存在）和**部分匹配**（某些模态缺失）两大场景。
- 任务：**院内死亡率预测（IHM）** 和 **30天内再入院预测（READM）**。

### 3.2 Benchmark 与对比方法
- 对比5种已有方法：**MMTM**、**DAFT**、**Unified**、**MedFuse**、**DrFuse**，以及额外基线 **LSMT**、**Interleaved**。
- 评估指标：AUROC 和 AUPR（带95%置信区间，1000次Bootstrap）。

## 4. 资源与算力
- 论文明确说明：所有实验在 **单张 RTX-3090 GPU** 上完成。
- 训练100个epoch，采用早停（15个epoch无改进则停止），批大小随数据集调整（MIMIC-IV: 32, MIMIC-III: 16, DrFuse: 8）。
- 未提及总训练时长/能耗。

## 5. 实验数量与充分性

### 5.1 实验组数
- **主实验**：2个数据集（MIMIC-III, MIMIC-IV）× 2个任务（IHM, READM）× 2种设置（完全匹配、部分匹配）= 8组表格结果（表2、3）。
- **三模态扩展**：MIMIC-IV上加入放射学报告的实验（表7）。
- **消融实验**（表4、5、6）：包括对齐损失对比（Cosine/KL/Copula）、模块移除（无Copula、无梯度保留采样、无融合模块）、不同Copula族对比（Gumbel/Frank/Gaussian）、混合分量数K的影响（图5）。
- **额外基线**（表9、10）：对比LSMT、Interleaved，并测试不同骨干网络（LSTM vs Transformer, ResNet vs ViT）。
- **统计检验**（表11）：计算与基线的显著性p值。

### 5.2 充分性与公平性
- 覆盖完全匹配与部分匹配两种实际场景。
- 使用多种主流基线，且所有对比方法均采用官方代码或作者提供实现，超参数通过网格搜索调优。
- 消融实验系统拆解了各组件贡献，验证了 Copula 对齐的有效性。
- 统计检验表明多数改进显著（p<0.05）。
- 不足：仅在医疗领域MIMIC数据集上验证，未涉及其他领域多模态数据（如视觉-语言）；三模态实验仅一个数据集。

## 6. 主要结论与发现
1. **Copula 对齐优于传统对齐方法**：在完全匹配和部分匹配设置下，CM² 在所有指标上全面超越5种基线，最高提升3.2% AUPR。
2. **生成式缺失模态处理有效**：通过从学习到的 GMM 采样生成缺失模态特征，性能优于零填充或全局表示学习。
3. **Copula 族选择影响性能**：Frank Copula 在平衡正负依赖性上表现更灵活，但整体方法对 Copula 族选择具有一定鲁棒性。
4. **三模态扩展稳健**：在 EHR + CXR + 报告的场景中仍优于基线，表明方法可扩展至更多模态。
5. **理论保证**：Sklar 定理确保唯一性，增强模型可识别性。

## 7. 优点
- **统计严谨性**：首次将 Copula 引入多模态学习，提供了联合分布的可分解建模框架，有理论支撑。
- **鲁棒缺失模态处理**：利用 GMM 采样生成伪特征，避免了传统插补偏差。
- **变分推断可扩展**：采用 ELBO 优化，适应大规模深度学习场景，无需 MCMC 采样。
- **全面实验**：涵盖单模态缺失、多模态匹配、不同Copula族、不同骨干网络，消融分析充分。

## 8. 不足与局限
- **应用领域局限**：仅在医疗数据集（MIMIC）上验证，未在多模态视觉-语言、音频-视频等通用领域评估。
- **Copula 参数优化风险**：联合对数似然可能非凸，作者承认使用神经网络学习可能不够，需考虑部分似然等替代更新算法。
- **假设限制**：假设缺失模态为随机缺失（MAR），在非随机缺失（MNAR）场景下可能失效。
- **实验细节缺失**：未报告训练时间具体数值，且仅使用单GPU，大规模应用时调试可能受限。
- **混合分量数 K 的敏感性**：实验显示性能对 K 较鲁棒，但理论上存在过指定风险，文中未深入讨论选择策略。

（完）
