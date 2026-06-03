---
title: "MindCustomer: Multi-Context Image Generation Blended with Brain Signal"
title_zh: "MindCustomer: 融合脑信号的多上下文图像生成"
authors: "Muzhou Yu, Shuyun Lin, Lei Ma, Bo Lei, Kaisheng Ma"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=06UlFIly8J"
tags: ["query:unified-mm"]
score: 7.0
evidence: 脑信号与图像的跨模态融合管道
tldr: 该论文提出MindCustomer，探索脑信号与图像的多上下文生成。设计图像-脑信号翻译器实现稳定跨主体嵌入，并提出无掩码的跨模态信息融合管道，有效结合图像和脑信号语义。实验表明该方法在图像定制任务中表现优异，开辟了脑信号驱动生成的新方向。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1756, \"height\": 1053, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1712, \"height\": 849, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 829, \"height\": 790, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 816, \"height\": 764, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1686, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1753, \"height\": 715, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1747, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 834, \"height\": 966, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1718, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 800, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1682, \"height\": 1857, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1676, \"height\": 1549, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1695, \"height\": 1142, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1713, \"height\": 809, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1690, \"height\": 1455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1708, \"height\": 921, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1700, \"height\": 2112, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1497, \"height\": 634, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1417, \"height\": 1271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1715, \"height\": 1454, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 629, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 513, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 491, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 843, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1622, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1418, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1417, \"height\": 264, \"label\": \"Table\"}]"
motivation: 现有生成模型主要依赖文本和图像，忽略了脑信号作为直接用户意图表示的可能性，且面临脑信号解释和跨模态融合的挑战。
method: 提出共享神经数据增强和图像-脑信号翻译器，以及无掩码的跨模态语义融合管道。
result: 在多个图像生成定制任务上验证了方法的有效性，实现了高质量的脑信号引导生成。
conclusion: MindCustomer成功将脑信号纳入多上下文图像生成，为交互式图像定制提供了新范式。
---

## Abstract
Advancements in generative models have promoted text- and image-based multi-context image generation. Brain signals, offering a direct representation of user intent, present new opportunities for image customization. However, it faces challenges in brain interpretation, cross-modal context fusion and retention. In this paper, we present MindCustomer to explore the blending of visual brain signals in multi-context image generation. We first design shared neural data augmentation for stable cross-subject brain embedding by introducing the Image-Brain Translator (IBT) to generate brain responses from visual images. Then, we propose an effective cross-modal information fusion pipeline that mask-freely adapts distinct semantics from image and brain contexts within a diffusion model. It resolves semantic conflicts for context preservation and enables harmonious context integration. During the fusion pipeline, we further utilize the IBT to transfer image context to the brain representation to mitigate the cross-modal disparity. MindCustomer enables cross-subject generation, delivering unified, high-quality, and natural image outputs. Moreover, it exhibits strong generalization for new subjects via few-shot learning, indicating the potential for practical application. As the first work for multi-context blending with brain signal, MindCustomer lays a foundational exploration and inspiration for future brain-controlled generative technologies.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：当前生成模型（如扩散模型）在文本和图像驱动的多上下文图像生成方面取得了显著进展，但尚未探索利用脑信号作为用户意图的直接表示。脑信号能够直接反映用户个性化想法，比文本或图像更高效地表达用户意图。然而，脑信号存在解释困难、跨模态上下文融合与保留的挑战。
- **整体含义**：本文首次提出将视觉脑信号融入多上下文图像生成任务，构建了**MindCustomer**框架。该工作为脑控生成技术奠定基础，拓展了脑机接口与生成式AI结合的新方向，具有艺术创作、用户定制、人机交互等应用潜力。

## 2. 方法论：核心思想、关键技术细节与算法流程

- **核心思想**：通过跨主体脑信号增强与无掩码跨模态融合管道，将图像、文本、脑信号三种上下文统一融入扩散模型，实现自然、高质量的生成。
- **关键技术细节**：
  - **Image-Brain Translator (IBT)**：一个轻量级MLP网络（3层），以图像CLIP嵌入为输入，生成伪脑信号体素（8192维），用于数据增强。在脑表示预训练阶段，同时输入真实fMRI和IBT生成的伪fMRI，结合共享深层编码器和按主体浅层编码器，使用SoftCLIP损失和MSE损失训练，将体素映射到CLIP潜在空间。
  - **语义提取器（Semantic Extractor）**：基于ClipCap的映射器，进一步提取脑嵌入中的文本语义，增强语义表示。
  - **扩散模型微调**：使用IBT将图像上下文转换为脑体素表示，提取嵌入后微调Versatile Diffusion (VD)模型，使模型学会从脑信号形式中重建图像。
  - **脑嵌入优化**：冻结微调后的VD，仅优化脑上下文嵌入，使其逼近图像上下文的语义，缓解模态冲突。
  - **嵌入融合**：对于双上下文（图像+脑），直接拼接嵌入；对于三上下文（图像+脑+文本），采用线性插值（超参数α控制比例），并送入VD的图像流和文本流生成最终图像。
- **算法流程**（文字说明）：
  1. **脑表示预训练**：训练主体专用的IBT；然后联合多主体真实与生成的fMRI，训练共享编码器和语义提取器。
  2. **扩散模型微调**：用IBT转移图像上下文到脑空间，微调VD。
  3. **脑嵌入优化**：轻量优化脑上下文嵌入，对齐图像上下文。
  4. **多模态集成生成**：融合嵌入（线性插值或拼接），利用VD生成结果。
- **公式要点**：使用CLIP嵌入、MSE损失、SoftCLIP对比损失，以及扩散模型的噪声预测损失。

## 3. 实验设计

- **数据集**：Natural Scenes Dataset (NSD)，包含8名受试者的7T fMRI扫描，使用其中4名（Subj1,2,5,7）的8859张训练图像，982张测试图像（所有受试者共享视觉刺激）。
- **Benchmark与对比方法**：
  - **Baseline-1**：用脑信号的视觉刺激图像替代脑上下文，直接使用VD进行多上下文生成。
  - **Baseline-2**：用SOTA fMRI到图像模型（MindEye）重建脑上下文为图像，再与另一图像上下文合并输入VD。
  - **与SOTA脑解码方法**（MindBridge, UMBRAE）在脑重建任务上比较。
- **评估指标**：
  - 上下文保留：CLIP-I, DINOv2
  - 生成质量：CLIP-IQA
  - 脑解码：PixCorr, SSIM, AlexNet(2)/(5), Inception, CLIP
  - 用户研究：对生成图像的质量和一致性打分（1-3分）。

## 4. 资源与算力

文中提及：单张图像生成约需 **6分钟** 在 **单张Tesla A100 GPU** 上。未明确说明训练总时长或使用的GPU数量（推测可能为1-4张A100）。其他训练参数（IBT 200轮，脑嵌入600轮，VD微调200轮，脑优化100轮）已给出。

## 5. 实验数量与充分性

- **主要实验**：
  - 跨主体多上下文生成定性结果（多图展示）。
  - 与两个基线的定性和定量对比（CLIP-I, DINOv2, CLIP-IQA）。
  - 用户研究（220份答案，110对图像，22名参与者）。
  - 对新主体的少样本生成实验（10%, 20%, 40%数据）。
  - 消融实验：去除IBT/微调/优化/ClipCap等组件，分别定性与定量分析。
  - 脑解码对比（与MindBridge, UMBRAE）。
  - 不同融合策略（插值 vs 拼接）比较。
  - 不同随机种子生成示例。
- **充分性**：实验覆盖了主要方法对比、消融、少样本泛化、用户研究等多个维度，设计较为全面。结果客观，指标多样且包含人类评估。但缺少与其他脑-图像生成方法（如MindPainter）的直接对比，可能因为任务定义最新。

## 6. 主要结论与发现

- MindCustomer成功实现了脑信号驱动的多上下文图像生成，生成图像在语义保留和自然融合方面优于基线方法。
- IBT数据增强有效提升了跨主体脑嵌入稳定性，脑重建性能与SOTA方法持平或更优。
- 提出的无掩码跨模态融合管道解决了语义冲突，实现了高质量融合。
- 少样本学习（<20%数据）即可迁移到新主体，展示了实际应用潜力。
- 用户研究一致偏好MindCustomer生成结果。

## 7. 优点

- **创新性**：首次将脑信号引入多上下文图像生成任务，开创了脑控生成新范式。
- **技术亮点**：
  - IBT伪数据增强缓解了神经数据稀缺问题。
  - 跨模态融合管道无需掩码，可从单张图像实时生成。
  - 采用扩散微调+脑嵌入优化策略，有效对齐模态并保留语义。
  - 支持可调节的α参数，实现图像与脑上下文的平滑过渡。
- **实验充分**：包含定量、定性、用户研究、消融、少样本、跨主体等多种评估，验证了鲁棒性。
- **可迁移性**：对新主体的少样本泛化能力强，实用价值高。

## 8. 不足与局限

- **数据局限**：仍受限于脑信号采集成本高、样本量小（NSD仅8人）且信号噪声大，影响精细语义控制。
- **对比不够充分**：缺少与同时期相关工作（如MindPainter）的直接比较（尽管任务略有不同）。
- **细节限制**：当前脑信号更适合全局上下文融合，难以处理细节特征或具体指令（如面部细节编辑）。在附录中也承认简单插值可能损失部分保真度。
- **算力报告不完整**：未给出完整训练的总时间和GPU数量，可复现性略显不足。
- **实验室环境限制**：fMRI数据采集条件理想，真实应用场景中可能面临信号质量下降。
- **用户研究规模**：220份答案、22名参与者，样本量尚可但可扩大。

（完）
