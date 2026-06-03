---
title: "Textural or Textual: How Vision-Language Models Read Text in Images"
title_zh: 纹理还是文字：视觉语言模型如何读取图像中的文字
authors: "Hanzhang Wang, Qingyuan Ma"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=fUvuEfZSEE"
tags: ["query:mm-reasoning"]
score: 4.0
evidence: 分析视觉语言模型如何读取图像中的文字，区分字形与语义
tldr: 视觉语言模型常被诟病将文本语义融入视觉表征，但其内部机制不明。本文构建ToT数据集，通过同义词和形近词控制实验，结合内在维度逐层分析，发现早期层存在字形与语义的竞争，后期层语义编码占优。该发现揭示了多模态融合中视觉与文本特征的交互本质，为理解典型攻击提供了理论视角。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1737, \"height\": 351, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 790, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1723, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 855, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 843, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1207, \"height\": 829, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 823, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1310, \"height\": 794, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1737, \"height\": 2233, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fuvuefzsee/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 926, \"height\": 563, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-fuvuefzsee/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1539, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fuvuefzsee/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1398, \"height\": 439, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fuvuefzsee/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 810, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fuvuefzsee/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1039, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fuvuefzsee/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1304, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fuvuefzsee/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1372, \"height\": 303, \"label\": \"Table\"}]"
motivation: 多模态模型中的典型攻击现象常归因于文本语义与视觉特征的融合，但具体机制尚不清晰。
method: 构建ToT数据集，利用同义词/形近词对解耦字形与语义，通过逐层内在维度分析探究表征演变。
result: 发现早期层字形与语义竞争，后期层语义编码逐渐占据主导。
conclusion: 该研究揭示了视觉语言模型中文本语义融入视觉表征的动态过程。
---

## Abstract
Typographic attacks are often attributed to the ability of multimodal pre-trained models to fuse textual semantics into visual representations, yet the mechanisms and locus of such interference remain unclear. We examine whether such models genuinely encode textual semantics or primarily rely on texture-based visual features. To disentangle orthographic form from meaning, we introduce the ToT dataset, which includes controlled word pairs that either share semantics with distinct appearances (synonyms) or share appearance with differing semantics (paronyms). A layer-wise analysis of Intrinsic Dimension (ID) reveals that early layers exhibit competing dynamics between orthographic and semantic representations. In later layers, semantic accuracy increases as ID decreases, but this improvement largely stems from orthographic disambiguation. Notably, clear semantic differentiation emerges only in the final block, challenging the common assumption that semantic understanding is progressively constructed across depth. These findings reveal how current vision-language models construct text representations through texture-dependent processes, prompting a reconsideration of the gap between visual perception and semantic understanding. The code is available at: https://github.com/Ovsia/Textural-or-Textual

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

视觉语言模型（如CLIP）在读取图像中的文字时，究竟是真正理解语义，还是仅将其当作另一种视觉纹理？典型攻击（typographic attacks）暴露了模型脆弱性——例如在狗的图像上覆盖“laptop”文本会导致错误分类为电子设备。然而，这种干扰的机制和发生位置尚不明确。论文旨在解耦字形（orthographic form）与语义（meaning），探究模型逐层构建文本表征的过程，并回答：“视觉语言模型是‘读取’文字内容，还是‘感知’文字纹理？”

## 2. 论文提出的方法论

- **核心思想**：通过设计可控的字形-语义解耦实验（形近词对 vs. 同义词对），利用内在维度（Intrinsic Dimension, ID）逐层量化表征复杂度，并结合线性探针（Linear Probe）分析每层的判别能力，从而揭示语义涌现的时点与机制。
- **关键技术细节**：
  - **ToT数据集**：
    - 子集1（语义混淆）：基于ImageNet-1k，对图像覆盖语义一致（Consistent）、无关（Irrelevant）或无意义（Nonsense）的文字，字体大小为80pt（另有20-120pt变化实验）。
    - 子集2（形近词/同义词对）：10组单词对，例如goose（基础词）– moose（形近词）– gander（同义词），用于分离字形相似性与语义相似性。
  - **内在维度（ID）估计**：使用TwoNN算法，逐层计算每对样本到最近邻和次近邻的距离比值，基于Pareto分布的最大似然估计得到该层的ID值。
  - **线性探针**：在ViT-B/16的12个Residual Attention Block的输出上，训练逻辑回归分类器，分别区分形近词对（考察字形判别能力）和同义词对（考察语义判别能力）。
- **算法流程**（文字说明）：
  1. 随机采样n张图像；2. 对每个层λ，提取表示Z[λ]；3. 对每个样本，计算到第一、第二近邻的距离d1、d2，得到比率R=d1/d2；4. 从R的分布通过最大似然估计该层的ID。

## 3. 实验设计

- **数据集与场景**：
  - 主数据集：ToT（基于ImageNet-1k，100类别，每类500张，共50,000张）。
  - 验证泛化性：Caltech101（用同样文字覆盖方法）。
  - 防御跨数据集评估：Disentangle、PAINT、Prefix三个公开的手写体典型攻击数据集。
- **Benchmark**：
  - 比较模型：CLIP ViT-B/16（多模态）、MetaCLIP（多模态）、ViT-B/16（纯视觉）、DINOv2（纯视觉）。
  - 方法对比：Disentangle、PAINT、Prefix等SOTA防御方法。
- **防御任务难度分级**：
  - Easy：忽略文字，正确分类图像内容。
  - Medium：检测文字是否存在（不关心语义）。
  - Hard：同时理解图像和文字语义（如判断文字是否符合图像内容）。
- **对比方法**：CLIP原始、Disentangle（Materzyńska et al.）、PAINT（Ilharco et al.）、Prefix（Azuma & Matsui）。
- **评估指标**：分类准确率（%），内在维度（ID），相关性（Spearman ρ）。

## 4. 资源与算力

论文明确提到：**所有实验在一张GeForce RTX 3090 GPU上完成**，batch size=512，学习率1×10⁻⁴，weight decay=0.2，优化器为Adam。但**未提供具体训练时长**（如微调所需epoch数或总时间）。

## 5. 实验数量与充分性

- **实验组数**：
  - ID分析：跨越12个Transformer block，每个block分析3个子层（Attn、c_fc、c_proj），对比4种文字条件（Orig, Cons, Irr, Nons），覆盖6种不同架构（图4、9）。
  - 线性探针：10组形近词/同义词对，逐层训练逻辑回归，共约12×20次训练（图5）。
  - 字体大小恒常性：9种字体大小×3种语义条件×4种模型（表1）。
  - 防御实验：Easy/Medium/Hard三级，对比3种SOTA方法，交叉评估3个外部数据集（表2-4）。
  - 消融实验：微调不同块（Swell/Shrink/Shrink-Last/Last）对比（表2）。
  - 相关性分析：Spearman相关系数（表6）。
- **充分性与公平性**：
  - 实验设计较全面：涵盖不同架构（ViT-B/16, ViT-B/32, ViT-L/16, ViT-H/14, ResNet-50x4, DINOv2, MetaCLIP, SigLip2, ShareGPT-4v），不同数据集（ToT, Caltech101, 外部手写体数据集）。
  - 公平性：防御实验与SOTA方法在相同测试集上比较，且进行了跨数据集评估（表3），避免过拟合特定数据集。
  - 局限：未在更多真实场景（如复杂背景、任意字体、自然场景文字）下验证。

## 6. 论文的主要结论与发现

1. **语义涌现的非渐进性**：早期层（纹理主导阶段）字形和语义表征竞争，准确率上升主要来自字形识别；真正语义区分（基于意义而不是形状）仅在最后一层（Last block）才明确出现。
2. **ID模式符合信息瓶颈**：先膨胀（增加复杂度）后收缩（压缩），但不同语义的ID只在最后块出现显著分化。
3. **多模态模型对语义敏感，纯视觉模型仅视文字为纹理**：CLIP在Consistent文字下准确率增至98.4%，Irrelevant下降至42.9%；而ViT和DINOv2在不同语义条件下性能几乎不变。
4. **防御策略有效性**：仅微调最后块即可在保持原始任务性能的同时，有效抵御典型攻击，优于微调其他块或全量微调。

## 7. 优点

- **方法创新性**：首次利用形近词/同义词对+ID逐层分析，系统解耦字形与语义的表征动态，揭示语义涌现的非渐进性。
- **实验设计严谨**：提出三级难度防御任务，覆盖从简单忽略到复杂语义理解，并与多个SOTA方法在相同基准和跨数据集上比较，泛化性强。
- **实用价值**：提出的“仅微调最后块”防御策略简单、高效，易于部署，且不依赖额外数据或模型修改。
- **开源代码**：提供完整代码和数据，可复现。

## 8. 不足与局限

- **模型覆盖面**：主要聚焦CLIP ViT-B/16，虽扩展了其他架构，但未深入探讨不同预训练范式（如对比学习、生成式）下的差异；CNN模型（如ResNet）的ID模式与ViT不同，但分析较浅。
- **实验场景局限**：文字覆盖仅在固定字体、颜色、位置下进行，未模拟真实场景中文字变形、遮挡、噪声等复杂情况；手写体数据集仅用于防御交叉验证，未在自然场景文本图像上评估。
- **任务单一**：仅评估分类任务，未扩展到VQA、图像描述等需要更深层语义理解的任务。
- **缺乏理论证明**：ID与语义涌现的因果关系未严格证明，仅通过相关性推断。
- **训练细节缺失**：未说明微调所需epoch数、收敛条件，可复现性略打折扣。

（完）
