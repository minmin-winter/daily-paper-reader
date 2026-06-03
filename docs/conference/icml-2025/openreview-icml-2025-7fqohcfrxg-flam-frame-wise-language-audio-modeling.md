---
title: "FLAM: Frame-Wise Language-Audio Modeling"
title_zh: FLAM：帧级语言-音频建模
authors: "Yusong Wu, Christos Tsirigotis, Ke Chen, Cheng-Zhi Anna Huang, Aaron Courville, Oriol Nieto, Prem Seetharaman, Justin Salamon"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=7fQohcFrxG"
tags: ["query:mm-reasoning"]
score: 6.0
evidence: 帧级音频与语言对齐，采用logit调整
tldr: 本文针对音频语言模型在帧级事件定位上的不足，提出了FLAM模型，将对比学习扩展到帧级别并引入logit调整以抑制虚假相关性。该方法在开放词汇场景下实现了精确的音频事件时间定位，突破了传统模型仅能识别预定义类别的限制。实验表明，FLAM在帧级理解任务上显著优于现有基准。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1715, \"height\": 647, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1761, \"height\": 568, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1769, \"height\": 1066, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1773, \"height\": 1202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1772, \"height\": 1065, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1776, \"height\": 1295, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1781, \"height\": 1139, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7fqohcfrxg/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1779, \"height\": 1295, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 324, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 483, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 736, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1773, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 733, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1765, \"height\": 417, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1765, \"height\": 544, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7fqohcfrxg/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 838, \"height\": 418, \"label\": \"Table\"}]"
motivation: 现有多模态音频语言模型在帧级音频理解上表现不足，且难以泛化到未见事件类别。
method: 提出FLAM，一种基于对比学习的开词汇音频语言模型，采用帧级目标函数和logit调整来处理虚假相关性。
result: FLAM实现了精确的事件定位和帧级理解，优于现有方法。
conclusion: FLAM通过帧级对比学习有效解决了开放词汇音频事件定位问题。
---

## Abstract
Recent multi-modal audio-language models (ALMs) excel at text-audio retrieval but struggle with frame-wise audio understanding. Prior works use temporal-aware labels or unsupervised training to improve frame-wise capabilities, but they still lack fine-grained labeling capability to pinpoint when an event occurs. While traditional sound event detection models can precisely localize events, they are limited to pre-defined categories, making them ineffective for real-world scenarios with out-of-distribution events. In this work, we introduce FLAM, an open-vocabulary contrastive audio-language model capable of localizing specific sound events. FLAM employs a memory-efficient and calibrated frame-wise objective with logit adjustment to address spurious correlations, such as event dependencies and label imbalances during training. To enable frame-wise supervision, we leverage a large-scale dataset with diverse audio events, LLM-generated captions and simulation. Experimental results and case studies demonstrate that FLAM significantly improves the open-vocabulary localization capability while maintaining strong performance in global retrieval and downstream tasks.

---

## 论文详细总结（自动生成）

# 论文总结：FLAM: Frame-Wise Language-Audio Modeling

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：现有对比式音频-语言模型（ALM，如CLAP）擅长文本-音频全局检索，但无法实现帧级（frame-wise）的时间定位——即无法回答“某个声音事件在音频中的确切何时发生”。传统声音事件检测（SED）模型虽然能精确定位，但只能识别预定义类别，无法处理开放词汇（open-vocabulary）的未见事件。
- **整体含义**：本文提出FLAM，将ALM扩展为既能输出全局嵌入又能输出帧级嵌入，并通过帧级对比学习实现开放词汇的声音事件时空定位，弥合了全局检索与细粒度检测之间的鸿沟。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：在传统ALM的实例级对比损失基础上，增加一个帧级二元分类对比损失，使音频编码器输出的每个时间帧与文本描述对齐，从而检测事件是否在该帧出现。
- **关键技术细节**：
  - **帧级对比目标**：对于批数据中每个音频片段 \(X_i\) 的帧 \(l\) 和文本事件描述 \(Y_k\)，定义一个二元标签 \(z_{i,k,l} \in \{-1,1\}\)，优化二元交叉熵损失：
    \[
    L_{\text{SED}} = -\frac{1}{BKL} \sum_{i,k,l} \log \sigma(z_{i,k,l} \, h(X_i, l, Y_k))
    \]
    其中 logit 函数 \(h(x, l, y) = \alpha_{t(y)} (e^{\text{loc}}_l \cdot e^t) + \beta_{t(y)}\)，\(\alpha_{t(y)}\) 和 \(\beta_{t(y)}\) 是依赖于文本的事件级缩放和偏置。
  - **Logit 调整**：为克服标签不平衡（大部分帧-文本对为负）和事件依赖的虚假相关（如“雷声”出现少而短，“雨声”出现多而长），引入文本相关的偏置 \(\beta_{t(y)}\)（通过一个轻量MLP从文本特征预测），并单独训练偏置损失 \(L_p\)。推理时采用无偏分类器 \(s(x,l,y) = \sigma(\log(p(y|x,l)/p(y)))\)，统一阈值为0.5。
  - **内存高效训练**：采用类SigLIP的分块策略，在多个GPU之间轮转文本嵌入，避免全对数配对的显存爆炸。
  - **数据增广流水线**：从大规模音频-文本语料库中筛选小于10秒的“事件”和≥10秒的“背景”，随机混合1~10个事件（最多3个重叠），进行分割/重复、随机响度、边界修正（基于A加权RMS），生成100万条10秒合成SED样本，并附带精确的帧级标签。

## 3. 实验设计

- **使用的数据集/场景**：
  - **开放词汇SED**：合成保留集（Held-out，保留5k背景和10k事件）、ASFX-SED（使用Adobe Audition SFX库中未见事件）。
  - **传统封闭集SED**：DESED、MAESTRO、AudioSet-Strong、UrbanSED。
  - **检索**：Clotho、AudioCaps、ASFX。
  - **零样本分类**：ESC-50、US8K、VGGSound。
- **Benchmark**：采用各数据集标准指标（PSDS、MPAUC、AUROC），以及帧级AUROC、召回率、分类准确率。
- **对比方法**：
  - FLAM-Global（仅全局对比损失，类似CLAP）
  - MGA-CLAP（自监督多粒度对齐，原论文数据或重新训练在同一数据）
  - LAION-CLAP、CompA、MGA-CLAP（原报告值）

## 4. 资源与算力

- **文中未明确说明**所用的GPU型号、数量及总训练时长。仅提及：
  - FLAM-Global：batch size 768，学习率1e-4，训练50,000步（附录C.5）。
  - FLAM：batch size 512，学习率1e-4，训练120,000步（附录C.6）。
  - 使用Adam优化器，cosine warmup 3200步后线性衰减。
  - 模型架构：HTSAT（音频）+ RoBERTa（文本），参数量中等。
- 由于缺少硬件细节，无法准确评估算力开销。

## 5. 实验数量与充分性

- **实验数量**：
  - 主实验表1（SED on 6个数据集）、表2（检索 on 3个数据集）、表3（零样本 on 3个数据集）。
  - 消融实验：图3（F1曲线，不同阈值下对比是否含事件级偏置/缩放）、表4（SED消融：全局初始化、全局损失、封闭集数据影响）、表5（Spearman相关性对齐指标）、附录C.12（全局损失消融、帧数L=128消融）。
  - 定性结果：图2、附录A/B展示检测输出案例。
- **充分性与公平性**：
  - 公平性较好：重新训练MGA-CLAP在同一数据上比较（标注*），控制训练数据一致。
  - 多维度评估（SED+检索+分类+对齐质量），涵盖开放词汇和封闭集。
  - 消融实验验证了关键组件（logit偏置/缩放、封闭集数据、全局损失）的有效性。
  - **不足**：未在真实长音频、自适应阈值场景下测试；合成SED数据可能与真实分布有差距；少量数据集（如DESED仅692个样本）结果方差可能较大。

## 6. 主要结论与发现

- FLAM在开放词汇SED任务上显著优于FLAM-Global和MGA-CLAP（表1），AUROC提升10~20个百分点，PSDS提升数倍。
- 同时保持或略有牺牲全局检索性能（表2），零样本分类甚至提升（表3），说明帧级对齐增强了全局表征的判别力。
- 事件级logit调整（偏置+缩放）有效缓解标签不平衡，产生更校准的概率输出（图3）。
- 合成数据+封闭集数据的联合训练对性能至关重要（消融表4中移除封闭集数据导致大幅下降）。

## 7. 优点

- **方法创新**：首次将帧级对比学习与logit调整结合用于开放词汇SED，理论推导了无偏分类器。
- **数据策略**：大规模合成数据（1M样本）提供了精确帧级标签，弥补了真实标注稀缺问题，且开源ASFX-SED有助于基准。
- **效率设计**：内存高效训练策略使大batch训练可行。
- **实验全面**：覆盖SED、检索、分类、对齐质量、消融和定性案例，结果具有说服力。

## 8. 不足与局限

- **数据规模仍有限**：相比图像领域数十亿对数据，音频文本数据仍较小，可能限制泛化。
- **固定时间窗口与粗帧率**：输入固定10秒，帧分辨率0.3125秒（HTSAT的L=32），难以处理更长音频或更细微的时间边界（附录C.12尝试L=128有所改进但牺牲检索）。
- **依赖合成数据**：合成混合与现实环境（多源竞争、房间混响等）仍有差距，真实场景鲁棒性需进一步验证。
- **未评估真实世界长音频**：实验中多为10秒片段，实际应用需处理分钟级音频和事件重叠。
- **算力信息不透明**：无法复现计算成本。
- **未探讨生成式或弱监督方法**：未来可结合LLM生成更丰富描述或利用弱监督。

（完）
