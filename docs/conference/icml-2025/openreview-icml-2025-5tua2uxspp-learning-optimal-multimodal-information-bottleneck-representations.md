---
title: Learning Optimal Multimodal Information Bottleneck Representations
title_zh: 学习最优多模态信息瓶颈表示
authors: "Qilong Wu, Yiyang Shao, Jun Wang, Xiaobo Sun"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=5TUa2UXSpp"
tags: ["query:balanced-mml"]
score: 8.0
evidence: 通过最优信息瓶颈解决模态不平衡
tldr: 现有基于多模态信息瓶颈的方法忽略了模态间任务相关信息的不平衡，导致无法获得最优瓶颈。本文提出最优多模态信息瓶颈（OMIB）框架，通过优化目标确保实现最优MIB，理论保证其有效性。实验表明OMIB在多个数据集上优于现有方法，为模态不平衡提供了理论驱动的解决方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-5tua2uxspp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 789, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5tua2uxspp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 791, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5tua2uxspp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1579, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5tua2uxspp/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 825, \"height\": 272, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5tua2uxspp/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 886, \"height\": 1031, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-5tua2uxspp/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 892, \"height\": 548, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-5tua2uxspp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 894, \"height\": 372, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5tua2uxspp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 863, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5tua2uxspp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1174, \"height\": 134, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5tua2uxspp/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 862, \"height\": 470, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5tua2uxspp/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1771, \"height\": 489, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5tua2uxspp/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 857, \"height\": 116, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-5tua2uxspp/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 945, \"height\": 963, \"label\": \"Table\"}]"
motivation: 现有MIB方法忽视模态间信息不平衡，限制了最优瓶颈的达成。
method: 提出OMIB框架，通过优化目标保证实现最优多模态信息瓶颈。
result: OMIB在多个数据集上优于现有方法，有效平衡模态贡献。
conclusion: OMIB为模态不平衡问题提供了理论驱动的解决方案。
---

## Abstract
Leveraging high-quality joint representations from multimodal data can greatly enhance model performance in various machine-learning based applications. Recent multimodal learning methods, based on the multimodal information bottleneck (MIB) principle, aim to generate optimal MIB with maximal task-relevant information and minimal superfluous information via regularization. However, these methods often set regularization weights in an *ad hoc* manner and overlook imbalanced task-relevant information across modalities, limiting their ability to achieve optimal MIB. To address this gap, we propose a novel multimodal learning framework, Optimal Multimodal Information Bottleneck (OMIB), whose optimization objective guarantees the achievability of optimal MIB by setting the regularization weight within a theoretically derived bound. OMIB further addresses imbalanced task-relevant information by dynamically adjusting regularization weights per modality, ensuring the inclusion of all task-relevant information. Moreover, we establish a solid information-theoretical foundation for OMIB's optimization and implement it under the variational approximation framework for computational efficiency. Finally, we empirically validate the OMIB’s theoretical properties on synthetic data and demonstrate its superiority over the state-of-the-art benchmark methods in various downstream tasks.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 核心问题与研究动机
多模态信息瓶颈（MIB）方法通过正则化平衡任务相关信息的最大化与冗余信息的压缩，旨在学习最优多模态表示。然而，现有方法存在三个关键局限：
- 正则化权重（β）的设置缺乏理论指导，采用临时（*ad hoc*）赋值，无法保证获得最优 MIB；
- 未考虑各模态间任务相关信息的不平衡，当某个模态包含少量但关键的任务信息时，过大的正则化可能将其排除；
- 理论框架不完整，未能同时涵盖一致性、特异性、互补性、充分性和简洁性五个因素，也未区分共享与模态特定的任务相关信息。

为此，论文提出**最优多模态信息瓶颈（OMIB）**框架，通过理论推导的权重界限和动态调整策略，实现真正最优的 MIB。

### 2. 方法论
OMIB 包含两个阶段：
- **Warm-up 训练**：为每个模态训练一个任务相关分支（TRB），编码器 `Enc_i` 提取充分表示 `z_i`（满足 `I(z_i; y)=I(v_i; y)`），通过拼接高斯噪声并最小化预测损失（交叉熵/SVDD距离等）确保 `z_i` 包含最大任务相关信息。
- **主训练**：保留 TRB，新增**最优多模态融合（OMF）块**。OMF 包含：
  - 变分自编码器（VAE）：将 `z_i` 映射为高斯分布的均值 `μ_i` 和方差 `Σ_i`，通过重参数化采样得到 `ζ_i`；
  - 交叉注意力网络（CAN）：融合各模态的 `ζ_i` 生成融合表示 `ξ`；
  - 任务预测头 `dDec`：输出最终预测 `ŷ`；
  - 动态正则化权重 `r`：根据各模态剩余任务相关信息比例（由 KL 散度估计）实时调整，公式为 `r = 1 - tanh(ln(KL ratio))`，保证弱模态不被过度正则化；
  - β 的上界 `M_u = 1/(3*(H(v1)+H(v2)-I(v1;v2)))`（从数据中预先计算），理论证明当 `β ≤ M_u` 时优化可收敛到最优 MIB（包含全部任务信息、排除冗余信息）。

整体损失函数为：`L_OMF = -I(ξ; y) + β (I(ξ; z1) + r I(ξ; z2))`，通过变分近似实现可计算的上界。

### 3. 实验设计
- **数据集**：
  - 合成数据集 SIM-{I,II,III}：模拟任务相关信息不平衡/平衡情况，用于验证理论界限。
  - CREMA-D：音视频情感识别，6 种情绪，约 7400 样本。
  - CMU-MOSI：多模态情感分析（视觉、音频、文本），2199 个话语，评分区间 [-3,3]。
  - 10x-hBC-{A-D}：人类乳腺癌异常组织检测，包含组织学图像与基因表达双模态，训练于健康组织，测试于癌变组织。
- **基准方法**：
  - 非 MIB：Concat、BiGated、MISA
  - MIB：deep IB、MMIB-Cui、MMIB-Zhang、DMIB、E-MIB、L-MIB、C-MIB
- **评价指标**：分类准确率、F1、AUC、MAE、Pearson 相关系数等。

### 4. 资源与算力
论文未明确说明使用的 GPU 型号、数量及具体训练时长，仅提到所有实验使用 PyTorch 实现。因此无法量化算力消耗。

### 5. 实验数量与充分性
- **实验组数**：共 4 大类任务（合成数据验证 + 3 个真实数据集），每个任务中对比了 10 种以上的基线方法；
- **消融实验**：在 CREMA-D 数据集上进行了 4 项消融（去 warm-up、去 cross-attn、去整个 OMF、去动态 r），显示了各组件贡献；
- **复杂度分析**：给出了理论复杂度 O(N)，并实证展示了 warm-up 和主训练阶段随样本规模线性扩展；
- **充分性评价**：实验覆盖了分类、回归、异常检测等多种场景，并针对模态不平衡设计了合成验证。但消融实验仅在一个数据集上进行，缺乏跨数据集的鲁棒性验证；也未报告多次运行的标准差或置信区间，可能削弱结论的统计可靠性。

### 6. 主要结论
- 理论证明：当 β ≤ M_u 时，OMIB 优化可达到最优 MIB 状态（包含全部任务相关信息且排斥冗余信息）；
- 动态权重 r 能有效缓解模态间任务相关信息不平衡，使弱模态贡献不被忽略；
- 在 CREMA-D、CMU-MOSI、10x-hBC 数据集上，OMIB 在所有指标上均优于现有 MIB 和非 MIB 方法，提升显著（如 CREMA-D 准确率提升 3.6% vs 最佳 MIB，异常检测 AUC 平均提升 11.4% vs 最佳基线）。

### 7. 优点
- **理论严格性**：首次证明最优 MIB 的**可达条件**，给出了 β 的明确上界，并为多信息因素（一致性、特异性、互补性、充分性、简洁性）提供了统一的优化视角；
- **动态平衡机制**：根据模态剩余任务信息动态调整正则化权重，避免固定权重带来的信息丢失；
- **通用框架**：可自然扩展到三个以上模态（附录提供理论推导与方法）；
- **实践验证充分**：在合成数据和三个真实多模态任务上均有显著优势，消融实验验证了各模块必要性。

### 8. 不足与局限
- **理论假设较强**：依赖“各信息成分互不相交”的简化假设（Assumption 5.3），实际数据中信息可能高度纠缠，可能影响理论适用性；
- **计算资源未披露**：无法评估方法的训练代价，尤其在处理高维图像/基因数据时；
- **消融实验范围有限**：仅在 CREMA-D 上进行，未在其他数据集验证各组件（尤其是动态 r）的泛化性；
- **统计报告不足**：未报告多次运行的平均值和方差，无法判断方法稳定性；
- **应用边界**：主要验证了分类/回归/异常检测，未涉及多模态生成、检索等任务；扩展至大规模多模态（>3 模态）时仅提供理论，未做实验验证；
- **对比方法范围**：未与最新非 MIB 的最优方法（如基于 Transformer 的跨模态融合）进行全面比较，可能高估相对优势。

（完）
