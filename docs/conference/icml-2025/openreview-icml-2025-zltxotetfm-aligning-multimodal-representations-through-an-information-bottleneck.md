---
title: Aligning Multimodal Representations through an Information Bottleneck
title_zh: 通过信息瓶颈对齐多模态表征
authors: "Antonio Almudévar, José Miguel Hernández-Lobato, Sameer Khurana, Ricard Marxer, Alfonso Ortega"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=zltxOTEtfm"
tags: ["query:native-multi"]
score: 9.0
evidence: 通过信息瓶颈移除模态特有信息以对齐多模态表征
tldr: 对比损失虽能最大化互信息，但无法移除模态特有信息，导致表征未对齐。本文从信息瓶颈理论出发，提出去除模态特有信息的对齐方法。理论分析和实验表明，该方法能有效消除模态差异，使对齐后的表征在检索和分类任务上显著优于对比损失基线。该工作为多模态表征对齐提供了新的理论视角和实践方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 862, \"height\": 658, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 674, \"height\": 240, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 785, \"height\": 332, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 838, \"height\": 433, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 736, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1751, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 832, \"height\": 428, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 849, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 857, \"height\": 549, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 497, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 505, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 523, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 488, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 502, \"height\": 340, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 492, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 484, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 470, \"height\": 326, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 372, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 373, \"height\": 370, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 362, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 441, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 532, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 499, \"height\": 340, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 429, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 415, \"height\": 314, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 408, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 393, \"height\": 300, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 464, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 241, \"height\": 346, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 397, \"height\": 303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 103, \"height\": 103, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 402, \"height\": 309, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 393, \"height\": 301, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 103, \"height\": 106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-035.webp\", \"caption\": \"\", \"page\": 0, \"index\": 35, \"width\": 261, \"height\": 343, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-036.webp\", \"caption\": \"\", \"page\": 0, \"index\": 36, \"width\": 297, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-037.webp\", \"caption\": \"\", \"page\": 0, \"index\": 37, \"width\": 338, \"height\": 442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-038.webp\", \"caption\": \"\", \"page\": 0, \"index\": 38, \"width\": 386, \"height\": 292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-039.webp\", \"caption\": \"\", \"page\": 0, \"index\": 39, \"width\": 377, \"height\": 288, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-040.webp\", \"caption\": \"\", \"page\": 0, \"index\": 40, \"width\": 445, \"height\": 303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-041.webp\", \"caption\": \"\", \"page\": 0, \"index\": 41, \"width\": 382, \"height\": 293, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-042.webp\", \"caption\": \"\", \"page\": 0, \"index\": 42, \"width\": 420, \"height\": 292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-043.webp\", \"caption\": \"\", \"page\": 0, \"index\": 43, \"width\": 105, \"height\": 103, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-044.webp\", \"caption\": \"\", \"page\": 0, \"index\": 44, \"width\": 384, \"height\": 292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-045.webp\", \"caption\": \"\", \"page\": 0, \"index\": 45, \"width\": 425, \"height\": 290, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-046.webp\", \"caption\": \"\", \"page\": 0, \"index\": 46, \"width\": 102, \"height\": 103, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-047.webp\", \"caption\": \"\", \"page\": 0, \"index\": 47, \"width\": 270, \"height\": 347, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-048.webp\", \"caption\": \"\", \"page\": 0, \"index\": 48, \"width\": 426, \"height\": 293, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zltxotetfm/fig-049.webp\", \"caption\": \"\", \"page\": 0, \"index\": 49, \"width\": 1714, \"height\": 1931, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-zltxotetfm/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 860, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zltxotetfm/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 859, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zltxotetfm/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1437, \"height\": 380, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zltxotetfm/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1532, \"height\": 420, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zltxotetfm/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1150, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zltxotetfm/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 870, \"height\": 586, \"label\": \"Table\"}]"
motivation: 对比损失无法有效移除模态特有信息，导致多模态表征空间未对齐。
method: 基于信息瓶颈原理，提出去除模态特有信息的对齐损失函数。
result: 在多个多模态基准上，对齐后的表征在检索和分类任务中均取得显著提升。
conclusion: 信息瓶颈为多模态表征对齐提供了有效的理论指导。
---

## Abstract
Contrastive losses have been extensively used as a tool for multimodal representation learning. 
However, it has been empirically observed that their use is not effective to learn an aligned representation space.
In this paper, we argue that this phenomenon is caused by the presence of modality-specific information in the representation space. 
Although some of the most widely used contrastive losses maximize the mutual information between representations of both modalities, they are not designed to remove the modality-specific information.
We give a theoretical description of this problem through the lens of the Information Bottleneck Principle. 
We also empirically analyze how different hyperparameters affect the emergence of this phenomenon in a controlled experimental setup.
Finally, we propose a regularization term in the loss function that is derived by means of a variational approximation and aims to increase the representational alignment.
We analyze in a set of controlled experiments and real-world applications the advantages of including this regularization term.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）

- 多模态对比学习（如InfoNCE）广泛应用于表征学习，但经验观察到其学习的表征空间在不同模态间存在严重的**未对齐**（modality gap）现象。
- 现有对比损失虽然能最大化模态间互信息，但**未设计移除模态特有信息**（nuisances），导致表征中保留了大量无关的、仅属于单一模态的噪声，从而造成对齐不良。
- 本文从**信息瓶颈（Information Bottleneck, IB）原理**出发，理论分析并指出：理想的表征应同时满足**充分性**（保留所有模态共有信息）和**最小性**（剔除模态特有信息），而对比损失只保证了充分性，未保证最小性。
- 论文提出一个基于变分近似的正则项，可添加到对比损失中，以显式鼓励表征的最小性，从而提升对齐程度。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：将多模态表征学习建模为信息瓶颈问题：  
  - 对每个模态的输入 \(X_\alpha\)，其表征 \(Z_\alpha\) 应最大化与另一模态输入 \(X_\beta\) 的互信息（充分性），同时最小化与自身输入 \(X_\alpha\) 的互信息（最小性）。  
  - 形式化目标：\(\max I(Z_\alpha; X_\beta) - \beta I(Z_\alpha; X_\alpha)\)。
- **关键技术细节**：
  - 通过 InfoNCE 最大化 \(I(Z_\alpha; Z_\beta)\) 作为 \(I(Z_\alpha; X_\beta)\) 的下界。
  - 对 \(I(Z_\alpha; X_\alpha)\) 极小化一个可计算的**上界**：利用数据对 \((x_\alpha, x_\beta)\)，证明  
    \[
    I(Z_\alpha; X_\alpha) \le \mathbb{E}_{p(x_\alpha, x_\beta)} \left[ D_{\text{KL}}\left(p_\alpha(z|x_\alpha) \parallel p_\beta(z|x_\beta)\right) \right].
    \]
  - 在**球形高斯假设**（\(p_\alpha(z|x_\alpha)=\mathcal{N}(\mu_\alpha, \sigma^2 I)\)，\(p_\beta\) 类似）下，该上界正比于均方误差：  
    \[
    \mathcal{L}_M = \mathbb{E} \left[ \| \mu_\alpha(x_\alpha) - \mu_\beta(x_\beta) \|_2^2 \right].
    \]
  - 最终损失函数：\(\mathcal{L} = \mathcal{L}_{\text{InfoNCE}} + \beta \mathcal{L}_M\)。
- **算法流程**：联合训练两个模态的编码器，在每个batch内计算InfoNCE损失和正则项，反向传播更新参数。正则项仅需正样本对之间的欧氏距离，实现简单、与模态无关。

## 3. 实验设计

- **控制实验（玩具实验）**：
  - 数据集：**DSprites**、**MPI3D**、**Shapes3D**（标准解耦表征学习数据集）。  
  - 将图像和因子（factors）作为两个模态，通过控制因子输入数量来模拟信息不平衡（例如只输入部分因子，缺失的因子即为图像模态的特有信息）。  
  - 测量了：不确定性减少比率（URR）、对齐度（CKA）、互信息估计等。
- **真实世界应用**：
  - 使用 **COCO** 数据集，训练 **Q-Former** 模型（含冻结的LLM）进行图像描述和检索。  
  - 对比方法：基线 ITC+LM（仅对比损失+语言模型损失）；加入 ITM（图像-文本匹配损失）或本文提出的正则项（不同 \(\beta\) 值）。  
  - 评估指标：CIDEr、BLEU@4、检索 R@1。
- **额外的消融实验**：分析温度、编码器深度、架构（ResNet vs ViT）对模态特有信息保留的影响；观察“信息稳态”（Information Homeostasis）现象。
- **benchmark**：无标准公共 benchmark，但使用了广泛接受的解耦数据集和 COCO 图像描述任务，与常见的 Q-Former 变体对比。

## 4. 资源与算力

- 论文**未明确说明**使用的 GPU 型号、数量或训练时长。  
- 仅给出了超参数：如 batch size 128、学习率 0.001（控制实验）或 0.0001（Q-Former）、训练 steps 50000 等。  
- 实验规模属于中等，Q-Former 使用 VIT-g/14 视觉编码器和 BERT-base 文本编码器，训练时间可在单卡上完成，但具体算力未披露。

## 5. 实验数量与充分性

- **控制实验**：
  - 在 3 个解耦数据集上，每个数据集进行了多组场景（如不同数量的缺失因子、不同温度、不同编码器深度、不同架构），总计约 100 个随机场景 × 3 数据集 + 特定参数扫描（如温度、深度）→ 总体实验数量较多。
  - 消融实验：固定温度 vs 可调温度；不同 \(\beta\) 值（0.01~3.0）。
- **真实应用**：
  - 在 COCO 上训练了多个 Q-Former 变体（不同 \(\beta\) 及对比项 ITM），每个训练多次（报告标准差）。
  - 图像描述生成结果展示多幅示例；检索实验中展示了多模态算术示例。
- **充分性**：实验覆盖了理论验证、超参数影响、架构差异、真实应用等多个维度，设计较为全面；多次重复报告均值和标准差，结果可靠。但缺少与其他专门对齐方法（如 CLIP 后处理、多模态蒸馏等）的直接对比，仅与自身基线和 ITM 比较。

## 6. 论文的主要结论与发现

- 对比损失单独无法移除模态特有信息，导致表征未对齐；模态特有信息与 CKA 对齐度呈现**负相关**。  
- 更深的编码器、更高的温度能够隐式移除更多模态特有信息，但效果有限且不可控。  
- 提出的正则项 \(\mathcal{L}_M\) 能有效降低 \(I(Z_\alpha; N_\alpha)\)，提升对齐度，且与训练温度存在交互作用（观察到“信息稳态”现象：当 \(\beta\) 增大时，若温度可训练，编码器会降低温度以抵抗压缩，维持一定熵）。  
- 在图像描述任务中，适度使用正则项（\(\beta=0.1\)）能显著提升 CIDEr 和 BLEU-4，同时检索性能轻微下降；过大 \(\beta\) 会损失过多信息，导致所有指标下降。  
- 多模态算术示例表明，对齐更好的表征可产生更一致的跨模态检索结果。

## 7. 优点

- **理论创新**：首次从信息瓶颈视角严格解释模态差距，并给出充分性与最小性的数学定义，推导了可计算的正则项。  
- **方法简洁有效**：正则项仅基于正样本对之间的 KL 散度上界，易于实现，与模态无关，计算开销低。  
- **实验设计全面**：既有控制变量的解耦数据集验证，又有真实 COCO 任务上的性能评估；分析了温度、深度、架构等多种因素的影响。  
- **发现有趣现象**：如“信息稳态”，为理解对比学习中的自动调节机制提供线索。

## 8. 不足与局限

- **实验覆盖仍有限**：仅使用了 COCO 数据集作为真实应用，未在更大规模的多模态基准（如 CC3M、LAION-5B）或更多任务（如 VQA、文本到图像生成）上进行验证。  
- **基线对比不足**：在真实应用部分，仅与不加正则项和加 ITM 的基线对比，未对比其他专门的对齐方法（如 CLIP 的后处理、互信息最小化变体、多模态蒸馏等）。  
- **模态特定假设**：球形高斯假设在现实中可能不成立，尽管论文指出这仅在 KL 上界推导中用作简化，实际训练中可能偏离。  
- **\(\beta\) 调节敏感**：性能对 \(\beta\) 值的选取敏感，且与温度存在耦合，实际使用时需要仔细调参。  
- **未讨论对检索任务的影响**：正则项在提升对齐的同时降低了检索性能，论文未深入分析其根本原因，也未提出平衡方案。  

（完）
