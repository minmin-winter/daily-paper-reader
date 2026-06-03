---
title: "Sounding that Object: Interactive Object-Aware Image to Audio Generation"
title_zh: 为对象发声：交互式对象感知图像到音频生成
authors: "Tingle Li, Baihe Huang, Xiaobin Zhuang, Dongya Jia, Jiawei Chen, Yuping Wang, Zhuo Chen, Gopala Anumanchipalli, Yuxuan Wang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=6KeALGcu2j"
tags: ["query:native-multi"]
score: 4.0
evidence: 通过多模态注意力从图像生成音频，涉及图像和音频模态
tldr: 该论文提出一个交互式对象感知音频生成模型，能够根据用户选择的图像对象生成对应声音。模型将对象中心学习与条件潜在扩散模型结合，通过多模态注意力学习图像区域与声音的关联。理论上验证了注意力机制能够近似测试时分割掩码，确保生成音频与用户选择对齐。该方法为图像到音频生成提供了对象级控制能力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1774, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1775, \"height\": 751, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1776, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 862, \"height\": 212, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 370, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 865, \"height\": 207, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 706, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 869, \"height\": 322, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 724, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6kealgcu2j/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1766, \"height\": 920, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1782, \"height\": 535, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 868, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 871, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 838, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 852, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 867, \"height\": 148, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 866, \"height\": 146, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 794, \"height\": 149, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 580, \"height\": 414, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1087, \"height\": 417, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6kealgcu2j/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 699, \"height\": 257, \"label\": \"Table\"}]"
motivation: 复杂视听场景中多对象声音生成困难，缺乏对象级控制。
method: 集成对象中心学习与条件潜在扩散模型，利用多模态注意力关联图像区域与声音。
result: 模型能根据用户选择的图像对象生成对应声音，理论证明注意力机制近似分割掩码。
conclusion: 实现了对象级可控的音频生成，拓展了多模态生成能力。
---

## Abstract
Generating accurate sounds for complex audio-visual scenes is challenging, especially in the presence of multiple objects and sound sources. In this paper, we propose an interactive object-aware audio generation model that grounds sound generation in user-selected visual objects within images. Our method integrates object-centric learning into a conditional latent diffusion model, which learns to associate image regions with their corresponding sounds through multi-modal attention. At test time, our model employs image segmentation to allow users to interactively generate sounds at the object level. We theoretically validate that our attention mechanism functionally approximates test-time segmentation masks, ensuring the generated audio aligns with selected objects. Quantitative and qualitative evaluations show that our model outperforms baselines, achieving better alignment between objects and their associated sounds.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：在包含多个对象和声源的复杂视听场景中，生成与特定视觉对象准确对齐的声音十分困难。现有方法（如基于文本的音频生成）在处理多事件描述时容易遗漏或混淆声音；基于图像的生成方法则倾向于生成整体音景，无法忠实复现特定物体的声音。
- **研究动机**：借鉴人类听觉场景分析原理，人类能将复杂声景解析为不同对象的声音（如街道中的喇叭声、脚步声）。因此，论文旨在开发一个交互式、对象感知的音频生成模型，让用户通过选择图像中的物体来生成对应的声音。

## 2. 方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：将对象中心学习（object-centric learning）与条件潜在扩散模型结合，通过多模态注意力机制学习图像区域与对应声音的关联。训练时使用文本-图像注意力，推理时用分割掩码替代注意力权重，实现用户可控的对象级声音生成。
- **关键技术细节**：
  - **条件潜伏扩散模型**：基于AudioLDM，在潜在空间进行扩散生成。输入为文本提示和噪声，经过N步去噪得到音频潜在表示。训练目标为噪声预测损失：\(L_\theta = E[\|\epsilon - \epsilon_\theta(z_n, n, t_q)\|^2]\)。
  - **文本-视觉对象定位模型**：使用CLIP文本编码器和CLIP图像编码器提取嵌入，通过缩放点积注意力融合：\(Q = E_t(t_q)W^Q,\ K = E_v(i_q)W^K,\ V = E_v(i_q)W^V\)，然后计算注意力权重 \( \text{Attention}(Q,K,V) = \text{softmax}(QK^T/\sqrt{d_k}) V \)。注意力输出经过MLP精炼后输入扩散模型。
  - **测试时替换**：训练结束后，将注意力权重替换为SAM生成的分割掩码（经归一化），实现用户交互式对象选择。
  - **理论分析**：证明InfoNCE损失与softmax注意力权重的MLE等价性，从而保证注意力机制在测试时可被分割掩码替代，并给出测试误差上界（Theorem 3.1）。

## 3. 实验设计
- **数据集**：
  - 主数据集：AudioSet（原始4616小时，经滤波后748小时）。测试集：AudioCaps（AudioSet子集）和VGG-Sound Sync、ImageHear等跨数据集评估。
- **基准方法**：对比了14种方法：Retrieve & Separate、AudioLDM 1/2、Captioning、Make-an-Audio、Im2Wav、SpecVQGAN、Diff-Foley、CoDi、Seeing & Hearing、FoleyCrafter、SSV2A等。所有方法均进行微调或适配以确保公平。
- **评估指标**：
  - 客观指标：ACC（事件准确率）、FAD（弗雷歇音频距离）、KL散度、IS（初始分数）、AVC（音视频对应性）。
  - 主观指标：OVL（总体质量）、RET（文本相关性）、REI（图像相关性）、REO（对象相关性）——由50名参与者对100个样本评分。

## 4. 资源与算力
- 论文**未明确说明**使用的GPU型号、数量及训练时长。仅提及训练配置：AdamW优化器，batch size 64，学习率1e-4，300个epoch。根据实验规模推断可能需要多块GPU（如4-8块A100或V100），但未提供具体算力信息。

## 5. 实验数量与充分性
- **实验数量**：主要包括：
  - 主对比实验（表1）：14种方法在AudioCaps上的客观和主观指标。
  - 交互满意度实验（表2）：5名参与者比较4种方法的交互效率。
  - 消融实验（表3）：8种变体（冻结扩散权重、多头注意力、加性注意力、不同注意力模态、掩码训练等）。
  - 跨数据集实验：VGG-Sound Sync（表10）、ImageHear（表11）。
  - 附加实验：不同CFG尺度、不同匹配阈值、位置编码、分割模块（SAM vs SAM2）等。
  - 可视化：注意力图与分割掩码对比、交互式生成示例。
- **充分性与公平性**：
  - 充分：覆盖了主流基线、多种消融、跨数据集泛化、主观评价。
  - 客观：所有基线均进行微调或重新训练，尽量保证相同数据条件。但部分基线（如Retrieve & Separate）是两级模型，可能未完全优化。
  - 主观：采用亚马逊MTurk，50人评分，有噪声控制、时间约束、Cohen’s kappa（0.78）和显著性检验（p<0.01），设计较严谨。

## 6. 主要结论与发现
- **性能优势**：在ACC、FAD、KL、IS、AVC等客观指标上大幅超越所有基线，主观评分（尤其REO）显著领先。
- **交互可控性**：用户通过分割掩码可精确生成单对象或多对象声音，交互满意度高（时间、尝试次数、满意度均为最佳）。
- **理论验证**：证明注意力机制与分割掩码功能等价，测试误差有界，且实验显示注意力图与分割掩码高度相似。
- **泛化能力**：在VGG-Sound、ImageHear等跨数据集上仍保持领先。

## 7. 优点
- **创新性**：首次提出交互式对象感知音频生成，将对象中心学习与扩散模型结合，测试时用分割掩码替换注意力，设计巧妙。
- **理论支撑**：提供定理证明测试误差上界，增强方法可信度。
- **实验完整性**：涵盖大量基线、消融、跨数据集、主观评价，且控制严格。
- **应用潜力**：可应用于电影制作、游戏、虚拟现实等，用户能直观选择对象生成声音。

## 8. 不足与局限
- **实验覆盖**：主要基于静态图像，对动态事件（如撞击声）同步性不足；未测试视频输入或长时间音频生成。
- **偏差风险**：AudioSet类别分布不均（车辆、动物占比大），可能影响少数类物体声音生成质量。
- **应用限制**：可能被滥用于生成误导性视频（如虚假音效）。
- **算力资源未说明**：缺少GPU型号、数量、训练时间等复现所需信息。
- **对比公平性**：部分基线（如Im2Wav）原始输出长度不同，虽经重训练但可能未完全适配。
- **交互模式**：依赖SAM分割，对于细小或重叠对象可能不准确；用户需手动点击，自动化程度有限。

（完）
