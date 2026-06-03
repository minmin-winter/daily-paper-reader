---
title: "$\\mathcal{V}ista\\mathcal{DPO}$: Video Hierarchical Spatial-Temporal Direct Preference Optimization for Large Video Models"
title_zh: VistaDPO：面向大型视频模型的视频层次化时空直接偏好优化
authors: "Haojian Huang, Haodong Chen, Shengqiong Wu, Meng Luo, Jinlan Fu, Xinya Du, Hanwang Zhang, Hao Fei"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=O2jukIZR50"
tags: ["query:native-multi"]
score: 7.0
evidence: 多层次的视频与文本模态对齐
tldr: 本文针对大型视频模型与人类直觉不对齐及视频幻觉问题，提出了VistaDPO框架，在实例、时间和感知三个层次进行层次化时空直接偏好优化。该方法通过细粒度对齐视频内容与文本描述，显著提升了模型的理解准确性和忠实度。实验结果显示，VistaDPO在多个下游任务上优于基线方法，为视频模型的偏好对齐提供了有效途径。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 850, \"height\": 894, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1744, \"height\": 773, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1770, \"height\": 302, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 866, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1778, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 860, \"height\": 318, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 742, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1687, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1769, \"height\": 581, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1318, \"height\": 1051, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1767, \"height\": 868, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1396, \"height\": 173, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1382, \"height\": 171, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1401, \"height\": 172, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o2jukizr50/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1379, \"height\": 168, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-o2jukizr50/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1752, \"height\": 541, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o2jukizr50/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1750, \"height\": 489, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o2jukizr50/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 865, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o2jukizr50/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1751, \"height\": 457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o2jukizr50/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1779, \"height\": 711, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o2jukizr50/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1781, \"height\": 388, \"label\": \"Table\"}]"
motivation: 大型视频模型存在与人类直觉不对齐和视频幻觉问题，现有方法缺乏细粒度对齐。
method: 提出VistaDPO框架，在实例、时间和感知三个层次进行层次化时空直接偏好优化，增强文本-视频对齐。
result: 在视频理解基准上提升了对齐质量，减少了幻觉。
conclusion: VistaDPO通过多级偏好优化有效改善了视频模型与人类偏好的对齐。
---

## Abstract
Large Video Models (LVMs) built upon Large Language Models (LLMs) have shown promise in video understanding but often suffer from misalignment with human intuition and video hallucination issues. 
To address these challenges, we introduce **VistaDPO**, a novel framework for Video Hierarchical Spatial-Temporal Direct Preference Optimization. VistaDPO enhances text-video preference alignment across three hierarchical levels: 
i) **Instance Level**, aligning overall video content with responses; 
ii) **Temporal Level**, aligning video temporal semantics with event descriptions; 
and iii) **Perceptive Level**, aligning spatial objects with language tokens. 
Given the lack of datasets for fine-grained video-language preference alignment, we construct **VistaDPO-7k**, a dataset of 7.2K QA pairs annotated with chosen and rejected responses, along with spatial-temporal grounding information such as timestamps, keyframes, and bounding boxes. Extensive experiments on benchmarks such as Video Hallucination, Video QA, and Captioning performance tasks demonstrate that VistaDPO significantly improves the performance of existing LVMs, effectively mitigating video-language misalignment and hallucination.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：大型视频模型（LVM）在视频理解中表现出色，但普遍存在与人类直觉不一致的问题，以及“视频幻觉”现象——模型输出与视频实际内容不符，例如错误描述不存在的物体、错误的时间顺序或空间关系。
- **根因**：当前LVM架构通常将视频编码器（如ViT）连接到面向文本的大语言模型（LLM）上，视频编码器的能力远弱于LLM，导致LLM基于有偏差甚至错误的视觉感知产生过度自信的输出。监督微调（SFT）虽能部分改善模态对齐，但依赖极大规模数据，成本高昂。
- **现有DPO局限**：已有DPO方法（如Hound-DPO）直接将图像-文本DPO策略应用于视频，忽略了视频的**时空特性**和**细粒度对齐**，仅停留在实例级粗粒度对齐，未能充分建模动态时序和空间语义。

## 2. 方法论：核心思想、关键技术细节

**核心思想**：提出VistaDPO框架，实现视频与文本在三个层次上的细粒度偏好优化：实例层、时间层、感知层。通过构建包含“选择/拒绝”回答及时空标注的数据集，训练LVM偏好正确回答、拒绝错误回答，从而缓解幻觉和不对齐。

### 关键技术细节

- **实例级语义偏好优化**：
  - **回答级对齐**：优化模型对用户提示的整体回答偏好，引入两种非首选回答：相关但错误的（如空间/时间不一致）和完全不相关的（幻觉内容）。公式：使用Bradley-Terry模型，损失函数为`L_DPO_r`。
  - **视频级对齐**：首次引入视频级偏好优化，让模型区分与查询相关的视频（首选）和无关视频（非首选），减少对语言的过度依赖。损失函数`L_DPO_v`。
- **时间语义偏好优化**：
  - **片段级对齐**：将视频中与问题相关的时间段作为首选片段，无关时间段作为非首选片段，对齐视频时序语义与事件描述。损失函数`L_DPO_c`。
- **感知空间-对象偏好优化**：
  - **对象级空间对齐**：选取关键帧中的相关对象区域作为首选实例，对非首选样本掩码关键区域，增强空间布局理解。损失函数`L_DPO_o`。
  - **令牌级对齐**：在细粒度上优化每个token的偏好，解决如“after”/“before”等错误标记问题。使用序列KL散度，损失函数`L_DPO_t`。
- **总损失函数**：
  ```
  L_VistaDPO = L_DPO_v + L_DPO_r + λ·L_DPO_c + μ·L_DPO_o + ρ·L_DPO_t
  ```
  其中λ、μ、ρ为超参数。

## 3. 实验设计

### 数据集

- **训练数据**：自构建数据集 **VistaDPO-7k**（7.2K QA对），源自14个现有视频数据集（MSR-VTT、STAR、VATEX、ActivityNet-QA、NExT-QA、CLEVRER等），涵盖感知（对象、属性、空间关系、OCR等）和时序（动作、动态关系、序列）两大类共10种幻觉类型，标注了选择/拒绝回答及时间戳、关键帧、边界框等时空信息。
- **评估基准**：
  - **视频幻觉**：VideoHallucer、EventHallusion
  - **通用视频问答**：MSVD-QA、MSR-VTT-QA、TGIF-QA、ActivityNet-QA（零样本）
  - **视频字幕**：VideoChatGPT-Bench（5个维度：正确性、细节、上下文、时间理解、一致性）
  - **补充**：MVBench（20项细粒度时序理解任务）

### 对比方法

- 基模型：Video-LLaVA 7B、PLLaVA 7B
- 对比方法：Hound-DPO（当前最先进的视频DPO方法）、原始基模型；此外参考了VideoChatGPT、VideoChat2、LLaMA-VID、LLaMA-Adapter、Video-LLaMA等。

## 4. 资源与算力

论文中明确说明：
- 训练设备：H100 GPU
- 训练参数：学习率5e-7，batch size 8，训练3个epoch
- 未说明使用的GPU数量及总训练时长。

## 5. 实验数量与充分性

### 实验数量

- **主实验**：在2个幻觉基准（VideoHallucer有多个子指标，EventHallusion有多个子指标）、4个QA基准、1个字幕基准（5个维度）、MVBench（20项任务）上进行了全面评估。
- **消融实验**：
  - 对三个层次的损失进行逐一去除（表3）
  - 对比不同视觉非首选样本构造策略（图5：视频级、片段级、对象级各4种策略）
  - 超参数影响分析（图3：损失权重、相关/无关拒绝回答权重）
- **鲁棒性测试**：对抗时间测试（图6）、对抗空间测试（图7、图8b）、对抗令牌测试（图8c）。
- **可视化分析**：T-SNE表示空间分析（图4）、KDE分布分析（图7）。

### 充分性客观性

- **充分**：覆盖了幻觉检测、QA、字幕三大类任务，并进行了多维度消融和鲁棒性分析，实验设计全面。
- **客观公平**：与当前最先进的视频DPO方法（Hound-DPO）在同一基模型上比较，并报告了相对提升百分比。消融实验逐一验证各组件贡献。
- **潜在偏差**：仅使用了7B规模的LVM，未在更大模型（如13B/70B）上验证；数据集仅来自14个现有数据集的验证集，可能未覆盖所有视频场景。

## 6. 主要结论与发现

- VistaDPO显著优于Hound-DPO和原始基模型：在VideoHallucer上“Overall”指标提升最高达**51.7%**（PLLaVA）和**205.1%**（Video-LLaVA），在EventHallusion的“Desc.”指标上提升**100%**以上。
- 层次化时空偏好优化有效：各层级损失均发挥作用，缺失任何一层均导致性能下降。
- 视觉非首选样本的构造策略至关重要：对视频级，“翻转”顺序最优；对片段级，“相关但无关片段”最优；对对象级，“移动关键对象”最优。
- 对抗测试表明VistaDPO具有出色的鲁棒性：时间倒放后性能下降最小；空间掩蔽和令牌替换下依然能正确识别。
- 表示空间分析显示VistaDPO使幻觉与非幻觉表示显著分离，模态对齐更强。

## 7. 优点

- **方法论创新**：首次在视频DPO中引入层次化时空细粒度对齐，超越单纯文本级或粗粒度视觉对齐。
- **数据贡献**：高质量、带时空标注的VistaDPO-7k数据集，可服务后续视频DPO研究。
- **实验全面**：涵盖多种任务、多角度消融、对抗测试和可视化分析，验证充分。
- **结果显著**：在多个基准上取得大幅度提升，且避免了Hound-DPO带来的副作用（如基础指标下降）。
- **鲁棒性强**：在时间、空间、文本三种对抗测试中均表现最佳。

## 8. 不足与局限

- **模型规模局限**：仅实验了7B模型，未验证在更大LVM上的效果。
- **长视频处理**：论文在“Limitation and Future Work”中承认VistaDPO在处理长视频、复杂时序依赖上仍有提升空间。
- **数据偏见风险**：VistaDPO-7k源自14个现有数据集，这些数据集本身可能存在分布偏差；拒绝回答的生成依赖GPT-4等工具，可能引入语言模型自身的偏见。
- **训练资源未量化**：未给出具体GPU数量和时间，可复现性稍弱。
- **应用限制**：当前主要针对视频理解任务，未探索在视频生成、视频编辑等其他视频领域的适用性。

（完）
