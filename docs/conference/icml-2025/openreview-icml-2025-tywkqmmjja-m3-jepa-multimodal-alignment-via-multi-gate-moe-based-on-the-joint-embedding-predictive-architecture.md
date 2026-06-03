---
title: "M3-JEPA: Multimodal Alignment via Multi-gate MoE based on the Joint-Embedding Predictive Architecture"
title_zh: M3-JEPA：基于多门控混合专家和联合嵌入预测架构的多模态对齐
authors: "Hongyang Lei, Xiaolong Cheng, Qi Qin, Dan Wang, Huazhen Huang, Qingqing Gu, Yetao Wu, Luo Ji"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=tYwKQMMjJA"
tags: ["query:balanced-mml"]
score: 9.0
evidence: 使用多门控MoE解决多模态学习中的模态坍缩问题，平衡模态贡献
tldr: 该论文针对多模态学习中常见的模态坍缩问题，提出M3-JEPA框架。它利用联合嵌入预测架构将输入映射到潜在空间进行跨模态对齐，并用多门控混合专家实现模态特定与共享信息的解耦。门控函数从信息论角度达到最优平衡。实验表明该方法有效避免了模态坍缩，实现了更均衡的多模态表示。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-tywkqmmjja/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 820, \"height\": 795, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tywkqmmjja/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1774, \"height\": 848, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tywkqmmjja/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 835, \"height\": 738, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tywkqmmjja/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 763, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tywkqmmjja/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 693, \"height\": 467, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1692, \"height\": 827, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1591, \"height\": 345, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 869, \"height\": 176, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 877, \"height\": 499, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 808, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 810, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 795, \"height\": 383, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 477, \"height\": 131, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 856, \"height\": 230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tywkqmmjja/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1053, \"height\": 525, \"label\": \"Table\"}]"
motivation: 现有多模态学习在原始token空间优化易导致模态坍缩，模态贡献不平衡。
method: 采用JEPA进行潜在空间对齐，并用多门控MoE解耦模态特定与共享信息。
result: 有效避免模态坍缩，实现更均衡的多模态表示，信息论最优性得到验证。
conclusion: 为多模态对齐中的平衡贡献提供了有效框架。
---

## Abstract
Current multimodal learning strategies primarily optimize in the original token space. Such a framework is easy to incorporate with the backbone of pretrained language model, but might result in modality collapse. To alleviate such issues, we leverage the Joint-Embedding Predictive Architecture (JEPA) on the multimodal tasks, which converts the input embedding into the output embedding space by a predictor and then conducts the cross-modal alignment on the latent space. We implement this predictor by a Multi-Gate Mixture of Experts (MMoE) and name the framework as M3-JEPA, accordingly. The gating function disentangles the modality-specific and shared information and derives information-theoretic optimality. The framework is implemented with both contrastive and regularization loss, and solved by alternative gradient descent (AGD) between different multimodal tasks. By thoroughly designed experiments, we show that M3-JEPA can obtain state-of-the-art performance on different modalities and tasks, generalize to unseen datasets and domains, and is computationally efficient in both training and inference. Our observation suggests that M3-JEPA might become a new basis to self-supervised learning in the open world.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有多模态学习策略主要在原始 token 空间优化，虽然易于结合预训练语言模型，但容易导致**模态坍缩（modality collapse）**——即不同模态的梯度冲突、缺失模态、数据分布不匹配等使得跨模态对齐难以收敛，且无法有效处理信息的不确定性和冗余。
- **研究动机**：受人类多感官融合启发，作者希望构建一个**轻量、可扩展、通用**的多模态对齐框架，能够处理任意输入-输出模态组合（any-to-any），同时避免模态坍缩，并在潜在空间而非 token/pixel 层面进行对齐。
- **整体含义**：提出 M3-JEPA，将联合嵌入预测架构（JEPA）应用于多模态任务，通过多门控混合专家（MMoE）实现跨模态预测，从而在潜在空间对齐不同模态，达到信息论最优，并成为开放世界自监督学习的新基础。

## 2. 论文提出的方法论

- **核心思想**：
  - 采用 JEPA 范式，将输入编码通过**预测器（predictor）** 投影到输出嵌入空间，然后在潜在空间进行对齐，而非在原始像素/token 空间。
  - 使用**多门控混合专家（MMoE）** 作为预测器，其门控函数能自动解耦模态特定（modality-specific）和共享（shared）信息。
  - 结合**对比损失（contrastive loss）** 和**正则化损失（regularization loss）** 作为能量函数，总损失为两者的线性组合：\( L = \alpha L_{reg} + (1-\alpha)L_{cl} \)。
  - 采用**交替梯度下降（AGD）** 优化，不同多模态任务之间交替更新参数，缓解梯度冲突。

- **关键技术细节**：
  - **编码器**：使用预训练的单模态编码器（LLama3-8B 用于文本，Dinov2-Large 用于图像，LanguageBind 用于音频），仅对 3 层用 LoRA 微调，其余冻结。
  - **MoE 预测器**：N=12 个专家，Top-K=4，双门控（对应两个损失项）。门控函数输入包括输入嵌入和学习到的模态特定嵌入 \( e_m \)，以及共享投影矩阵 \( g \)。
  - **信息论分析**：损失等价于最大化互信息 \( I(x;y) \) 并最小化条件熵 \( H(y|x)+H(x|y) \)，最优权重 \( \alpha=0.5 \) 从理论和实验得到验证。
  - **AGD**：在多个任务间按固定周期交替更新，保证收敛（假设子任务凸且独立解）。

## 3. 实验设计

- **使用的数据集与场景**：
  - **视觉-语言检索**：Flickr30K、COCO（图像→文本、文本→图像）。
  - **音频-语言检索**：Clotho、AudioCaps（零样本评估），训练集使用 WavText5K、Freesound、AudioCaps/Clotho 混合。
  - **图像分类**：ImageNet-1K（1000 类）。
  - **视觉问答（VQA）**：VQAv2、NLVR-2（多模态输入：图像+问题→答案）。

- **对比的方法**：
  - 视觉语言检索：TinyCLIP, MobileCLIP, CLIP, ALIGN, FILIP, Florence, BEIT-3, UNITER, OSCAR, VinVL, ALBEF, BLIP, BLIP-2（含不同 backbone）。
  - 音频语言检索：AVFIC, ImageBind, VALOR, LanguageBind。
  - 图像分类：CLIP-ViT, DinoV2。
  - VQA：ALBEF, BLIP, X-VLM, SimVLM, OFA, Flamingo, CoCa, BLIP-2, BEiT-3。

## 4. 资源与算力

- 论文**未明确说明使用的 GPU 型号、数量、训练时长**。仅提及训练批大小 128，学习率调度为 cosine，warmup 0.1，weight decay 0.005，优化器 Adam。可训练参数量为 140M（主模型总参数量约 8.5B），远小于 BLIP-2 的 474M 训练参数。

## 5. 实验数量与充分性

- **实验组数**：覆盖 4 大类任务（共 7 个数据集），包含主实验结果、消融实验、敏感度分析、效率分析、失败案例分析。
- **消融实验**：
  - MoE vs. MLP 预测器（Table 5）。
  - AGD vs. 非交替优化（Table 5）。
  - 编码器微调方式（冻结/3层LoRA/全层 LoRA）（Table 6）。
  - 损失权重 α 敏感度（0~1 步长 0.25，Figure 4）。
  - MoE 结构参数（专家数 n、Top-K 值）（Appendix B.2）。
- **充分性评价**：实验较充分，覆盖主要多模态任务，并进行了消融和敏感性分析，对比基线均为当时先进方法，公平性较好（如使用统一评估协议、复现部分基线结果）。但缺少大规模预训练数据对比（如 BEiT-3 使用了 COCO+Visual Genome 等更大语料），且音频任务为零样本设置，存在数据集偏差影响。

## 6. 论文的主要结论与发现

- M3-JEPA 在**视觉-语言检索**（Flickr30K、COCO）上取得 SOTA，尤其在 R@1 上大幅超过 BLIP-2（如 COCO 文本→图像 R@1 达 89.7% vs. 68.3%）。
- 在**音频-语言检索**零样本场景下性能优于 LanguageBind 等基线。
- 在**图像分类**上（ImageNet-1K）优于 CLIP-ViT 和 DinoV2，说明可将标签作为另一模态进行自监督学习。
- 在 **VQA** 任务上取得第二好成绩（仅次于 BEiT-3），表明能处理多模态输入，但在复杂多物体场景下仍有失败案例。
- **AGD 和 MoE** 均为关键组件：去除任一会导致性能明显下降。
- **最优损失权重 α=0.5** 理论与实验一致，平衡对比与正则化。
- **计算效率高**：训练参数少，推理时支持模态预计算和在线缓存，检索时间仅 0.02s（比 CLIP 0.16s 和 BLIP-2 0.05s 更快）。

## 7. 优点

- **方法论创新**：首次将 JEPA 推广到任意多模态对齐，并用 MMoE 实现预测器，实现模态特定与共享信息解耦，理论信息最优。
- **轻量高效**：仅微调少量层，可训练参数 140M，远低于同类方法。
- **通用性强**：支持任意输入-输出模态组合，在视觉、语言、音频、标签等多种模态上均有效。
- **零样本泛化**：音频检索任务在未见数据集上表现良好。
- **理论支撑**：提供信息论分析和收敛性讨论，并实验验证最优超参数。

## 8. 不足与局限

- **生成能力缺失**：JEPA 本质为非生成式框架，无法进行文本/图像生成，限制了应用范围。
- **模态扩展非全自动**：引入新模态需手动选编码器、添加对应专家并重新训练，未达到真正模态无关。
- **VQA 性能低于 BEiT-3**：简单拼接多模态输入导致在细粒度、多物体场景下失败（如楼梯数量识别），需要更智能的融合机制（如交叉注意力）。
- **音频实验依赖零样本评估**：训练集与测试集存在偏差（如采样长度、比例），可能影响结论普适性。
- **计算资源未报告**：缺乏 GPU 型号、显存、总训练时长等细节，不利于复现和成本评估。
- **AGD 优化细节未充分探索**：仅与联合优化简单对比，未深入分析不同任务调度、步长等对收敛的影响。

（完）
