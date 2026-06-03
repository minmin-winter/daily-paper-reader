---
title: "GMAIL: Generative Modality Alignment for generated Image Learning"
title_zh: GMAIL：面向生成图像学习的生成式模态对齐
authors: "Shentong Mo, Sukmin Yun"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=u6xeKVHS6K"
tags: ["query:native-multi"]
score: 8.0
evidence: 将生成图像视为独立模态，通过多模态对齐与真实图像在潜空间融合
tldr: 生成图像与真实图像存在模态差异，直接使用会导致模式坍塌。本文提出GMAIL框架，将生成图像视为独立模态，通过多模态对齐在共享潜空间中桥接两者。实验证明该方法能有效利用生成图像提升模型性能，同时避免模态偏差。该工作为多模态表示对齐提供了新视角。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1664, \"height\": 602, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 815, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1634, \"height\": 791, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1738, \"height\": 1163, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1738, \"height\": 1164, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1745, \"height\": 1171, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1743, \"height\": 1168, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1742, \"height\": 1166, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-u6xekvhs6k/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1742, \"height\": 1166, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1559, \"height\": 408, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1430, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1426, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1765, \"height\": 251, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 845, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1299, \"height\": 171, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1145, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 704, \"height\": 174, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1201, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 646, \"height\": 253, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 788, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1392, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1234, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 570, \"height\": 187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 633, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 788, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-u6xekvhs6k/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 963, \"height\": 181, \"label\": \"Table\"}]"
motivation: 生成图像与真实图像存在模态差异，直接混合训练会导致模式坍塌。
method: 将生成图像视为独立模态，通过多模态对齐在共享潜空间桥接真实与合成域。
result: 在多个分类任务上验证了方法的有效性，提升了模型对生成图像的利用效率。
conclusion: GMAIL提供了一种处理生成数据模态差异的有效对齐方法，可改善多模态学习。
---

## Abstract
Generative models have made it possible to synthesize highly realistic images, potentially providing an abundant data source for training machine learning models. Despite the advantages of these synthesizable data sources, the indiscriminate use of generated images as real images for training can even cause mode collapse due to modality discrepancies between real and synthetic domains. In this paper, we propose a novel framework for discriminative use of generated images, coined \textit{GMAIL}, that explicitly treats generated images as a separate modality from real images. Instead of indiscriminately replacing real images with generated ones in the pixel space, our approach bridges the two distinct modalities in the same latent space through a multi-modal learning approach. To be specific, we first fine-tune a model exclusively on generated images using a cross-modality alignment loss and then employ this aligned model to further train various vision-language models with generated images. By aligning the two modalities, our approach effectively leverages the benefits of recent advances in generative models, thereby boosting the effectiveness of generated image learning across a range of vision-language tasks. Our framework can be easily incorporated with various vision-language models, and we demonstrate its efficacy throughout extensive experiments. For example, our framework significantly improves performance on image captioning, zero-shot image retrieval, zero-shot image classification, and long caption retrieval tasks. It also shows positive generated data scaling trends and notable enhancements in the captioning performance of the large multimodal model, LLaVA.

---

## 论文详细总结（自动生成）

# 论文详细中文总结：GMAIL: Generative Modality Alignment for generated Image Learning

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：生成模型（如扩散模型）能合成高质量图像，但直接将其与真实图像混合训练会导致**模态差异**（modality discrepancy）问题，进而引发**模式坍塌**（mode collapse），模型过度拟合合成数据的偏差，降低在真实场景中的泛化能力。
- **整体含义**：本文提出 **GMAIL**（Generative Modality Alignment for generated Image Learning），**明确将生成图像视为与真实图像不同的独立模态**，通过多模态对齐方法在共享潜空间中桥接两者，从而实现生成图像的有效利用，提升下游视觉-语言任务的性能，同时避免模态偏差带来的负面影响。

## 2. 论文提出的方法论

### 核心思想
- 分别维护两个图像编码器：一个针对真实图像（\(f_r\)，冻结），另一个针对生成图像（\(f_g\)，可微调）。通过**交叉模态对齐损失**，使得具有相同文本描述的生成图像与真实图像在特征空间中接近，同时保留各自的模态特性。
- 推理时，真实图像仍使用 \(f_r\) 编码，生成图像使用 \(f_g\) 编码，从而避免推理阶段的模态错配。

### 关键技术细节
- **Gen-CLIP Flow（训练阶段）**：使用生成图像及其对应文本，以对比学习方式微调 \(f_g\)，同时保持 \(f_r\) 不变。
- **CLIP Flow（推理阶段）**：对真实图像使用 \(f_r\) 提取特征，避免模态塌陷。
- **对齐损失**（公式1）：
  \[
  \mathcal{L}_{\text{align}} = -\frac{1}{|B|}\sum_{(x_g, x_r)\in B}\log\frac{\exp(\text{sim}(f_g(x_g), f_r(x_r))/\tau)}{\sum_{x'_r\in B}\exp(\text{sim}(f_g(x_g), f_r(x'_r))/\tau)}
  \]
  该对比损失鼓励生成图像与真实图像的嵌入靠近。
- **高效微调**：采用 **LoRA**（低秩适应）更新 \(f_g\)，减少参数量，防止灾难性遗忘，默认秩为4。
- **双投影头**：为生成模态和真实模态分别设置投影层，进一步分离特征空间。

### 算法流程（文字说明）
1. 加载预训练的 CLIP 模型（\(f_r\) 冻结，\(f_g\) 初始化为 \(f_r\) 副本）。
2. 对每个 mini-batch，提取生成图像特征 \(f_g(x_g)\) 和真实图像特征 \(f_r(x_r)\)。
3. 计算交叉模态对齐损失 \(\mathcal{L}_{\text{align}}\)。
4. 通过 LoRA 更新 \(f_g\) 参数，最小化损失。
5. 将对齐后的生成图像特征与真实图像特征一起用于下游视觉-语言模型（如 LLaVA、LLaMA-3）的微调。

## 3. 实验设计

### 数据集与场景
- **图像描述（Captioning）**：COCO
- **零样本图像检索**：COCO、Flickr30k
- **零样本图像分类**：8个数据集（DTD、Stanford Cars、SUN397、Food101、Aircraft、Oxford Pets、Caltech101、ImageNet1K）
- **长描述检索**：ShareGPT4V
- **多模态推理**：ScienceQA、MMMU
- **数据扩展趋势**：COCO、CC3M、CC12M（生成图像规模递增）

### 基准方法
- 图像描述：ClipCap、IFCap、LLaVA、LLaMA-3（及其+GMAIL版本）
- 零样本检索：CLIP、Long-CLIP
- 零样本分类：CLIP、SynCLR
- 额外对比：SigLIP、Task2Sim

### 评估指标
- 图像描述：BLEU@4、METEOR、CIDEr、SPICE、ROUGE-L、WMD
- 检索：Recall@1、5、10（图像→文本、文本→图像）
- 分类：Top-1 准确率

## 4. 资源与算力

- **生成图像**：使用 **Stable Diffusion v2**，每个caption生成一张图像，50步推理。
- **生成耗时**：
  - COCO（560k图像）：5 GPU days
  - CC3M（3.3M图像）：30 GPU days
  - CC12M（12M图像）：109 GPU days
- **微调硬件**：NVIDIA A100-80GB GPU（未明确数量，估计多卡）
- **微调参数**：LoRA rank=4，学习率1e-4，AdamW，batch size=256，训练50,000步。

## 5. 实验数量与充分性

- **实验组数**：超过10组主要对比实验，涵盖4大类任务，多个数据集。
- **消融研究**：
  - 有无Gen-Real对齐（表6）
  - LoRA秩（2/4/6） vs 全量微调（表11）
  - 不同训练数据规模（表7）
  - 相同训练步数对照（表13）
  - 不同生成模型（FLUX vs SDv2）（表17）
  - 双投影 vs 单投影（表9）
- **可视化与定量分析**：t-SNE、余弦相似度（表14）
- **公平性**：与基线在相同训练步数下比较（表13），控制变量。
- **结论**：实验充分、客观，验证了方法的有效性、可扩展性和兼容性。

## 6. 论文的主要结论与发现

1. **GMAIL 显著提升生成图像的学习效果**：在图像描述、零样本检索、零样本分类、长描述检索等任务上，GMAIL 均优于直接混合训练或单独使用生成图像的方法。
2. **对齐策略是核心**：交叉模态对齐损失有效缩小了生成与真实模态之间的特征差异，余弦相似度从0.52提升至0.89。
3. **数据规模正扩展**：随着生成数据量从COCO到CC12M增加，性能持续提升，表明GMAIL能充分利用大规模合成数据。
4. **兼容性强**：可轻松集成到多种视觉-语言模型（如LLaVA、LLaMA-3、Long-CLIP）中，且效果一致提升。
5. **高效训练**：LoRA微调在仅增加少量参数的情况下达到优于全量微调的性能。

## 7. 优点

- **创新性**：首次将生成图像视为独立模态进行显式对齐，而非直接混合，从根本上解决了模态差异导致的模式坍塌。
- **方法简洁有效**：仅需一个对比损失和LoRA微调，易于复现和扩展。
- **实验全面**：覆盖多个任务、多种模型、大规模数据，消融研究充分，验证了各个设计选择。
- **可扩展性**：支持不同生成模型（SDv2、FLUX）和大规模数据，具有实用价值。
- **计算友好**：LoRA微调降低了参数量和训练时间，便于在实际中应用。

## 8. 不足与局限

- **依赖生成模型质量**：实验主要基于Stable Diffusion v2，不同生成模型可能引入不同的偏差，虽用FLUX验证了部分鲁棒性，但未系统测试更多生成器。
- **对齐损失仅考虑图像层面**：未显式利用文本-文本或更细粒度的跨模态关系（如语义属性对齐），可能留下优化空间。
- **生成数据偏差风险**：生成图像可能放大训练数据中的偏见，论文仅提及需谨慎，未提供具体去偏方案。
- **大规模生成成本**：生成12M图像需109 GPU days，资源消耗较大，可能限制资源有限团队的使用。
- **部分消融不足**：未分析不同对齐损失变体（如使用更复杂的损失函数）的影响；也未见与更多纯合成数据训练方法的对比（如DatasetGAN等）。
- **长描述检索任务仅报告R@1**，未提供R@5、R@10等更完整指标，可能不足以全面评估。

（完）
