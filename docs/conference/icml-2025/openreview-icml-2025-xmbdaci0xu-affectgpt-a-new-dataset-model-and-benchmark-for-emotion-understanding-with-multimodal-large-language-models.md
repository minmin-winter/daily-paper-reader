---
title: "AffectGPT: A New Dataset, Model, and Benchmark for Emotion Understanding with Multimodal Large Language Models"
title_zh: AffectGPT：面向多模态大模型情感理解的新数据集、模型和基准
authors: "Zheng Lian, Haoyu Chen, Lan Chen, Haiyang Sun, Licai Sun, Yong Ren, Zebang Cheng, Bin Liu, Rui Liu, Xiaojiang Peng, Jiangyan Yi, Jianhua Tao"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=xmbdACI0xu"
tags: ["query:mm-reasoning"]
score: 5.0
evidence: 多模态情感理解，结合视觉和语言信息
tldr: 本文针对多模态情感理解领域缺乏大规模描述性标注数据集和面向情感理解的多模态框架的问题，构建了MER-Caption数据集和AffectGPT模型。通过模型辅助的众包数据收集策略，实现了从简单判别到复杂情感描述的任务提升。实验表明该框架有效。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1639, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1350, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1758, \"height\": 324, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 812, \"height\": 262, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1733, \"height\": 179, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1750, \"height\": 180, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1694, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 623, \"height\": 471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1460, \"height\": 1071, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xmbdaci0xu/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1308, \"height\": 542, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1598, \"height\": 637, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 799, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 797, \"height\": 546, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 888, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 845, \"height\": 175, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 800, \"height\": 339, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 530, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 687, \"height\": 202, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1610, \"height\": 578, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1207, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1771, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1734, \"height\": 1344, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xmbdaci0xu/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1722, \"height\": 581, \"label\": \"Table\"}]"
motivation: 当前多模态情感理解缺乏大规模描述性标注和面向情感的多模态框架。
method: 构建MER-Caption数据集和AffectGPT模型，利用模型辅助众包收集标注。
result: 实现了从判别到描述的情感理解任务提升。
conclusion: 为多模态情感理解提供了新基准和模型。
---

## Abstract
The emergence of multimodal large language models (MLLMs) advances multimodal emotion recognition (MER) to the next level—from naive discriminative tasks to complex emotion understanding with advanced video understanding abilities and natural language description. However, the current community suffers from a lack of large-scale datasets with intensive, descriptive emotion annotations, as well as a multimodal-centric framework to maximize the potential of MLLMs for emotion understanding. To address this, we establish a new benchmark for MLLM-based emotion understanding with a novel dataset (MER-Caption) and a new model (AffectGPT). Utilizing our model-based crowd-sourcing data collection strategy, we construct the largest descriptive emotion dataset to date (by far), featuring over 2K fine-grained emotion categories across 115K samples. We also introduce the AffectGPT model, designed with pre-fusion operations to enhance multimodal integration. Finally, we present MER-UniBench, a unified benchmark with evaluation metrics tailored for typical MER tasks and the free-form, natural language output style of MLLMs. Extensive experimental results show AffectGPT's robust performance across various MER tasks. We have released both the code and the dataset to advance research and development in emotion understanding: https://github.com/zeroQiaoba/AffectGPT.

---

## 论文详细总结（自动生成）

# AffectGPT 论文详细中文总结

## 1. 核心问题与整体含义

- **研究动机**：传统多模态情感识别（MER）依赖判别式模型，将情感映射到预定义的有限类别（如 Ekman 六类），无法捕捉真实世界中情感表达的**多样性**（如文化差异、隐喻）和**共存性**（同一样本中多种情感并存）。多模态大语言模型（MLLM）通过生成式范式可输出自由形式的自然语言描述，具备描述复杂情感状态的潜力，但目前缺乏大规模、带有丰富描述性标注的情感数据集，也缺乏专门针对情感理解优化的多模态框架。
- **整体含义**：本文旨在从**数据集**、**模型**和**基准**三个维度推动 MLLM 的情感理解能力。通过构建大规模描述性情感数据集 MER-Caption 和专门设计的模型 AffectGPT，并建立统一评估基准 MER-UniBench，将 MER 从封闭集分类推向开放集、描述式理解的新阶段。

## 2. 方法论

### 2.1 数据集构建：MER-Caption（模型主导、人工辅助策略）

- **核心思想**：平衡标注质量与数据集规模。采用**模型主导、人工辅助**的自动标注流程。
- **关键技术细节**：
  - **描述生成**：基于人类先验选择基础模型。通过预实验确定：音频 LLM（ALLM）使用 SALMONN 提取音频线索，视频 LLM（VLLM）使用 Chat-UniVi 提取视觉线索，再用 GPT-3.5 融合音频、视频和文本内容生成最终描述。
  - **样本过滤**：分为两级：
    - **低级过滤**：使用 TalkNet 检测音视频是否匹配（说话者与可见人物是否对应），移除不匹配样本；剔除描述长度异常（过短或过长）的样本。
    - **高级过滤**：训练多个多模态情感和情绪分类器（基于 CLIP ViT-L 和 HUBERT-L，采用注意力融合），通过“模型众包”对未标注数据预测标签，再与从自动描述中提取的标签对比，不一致则移除低质量描述。
  - **最终数据集**：MER-Caption 包含 115,595 个粗标注样本，过滤后得到 MER-Caption+ 包含 31,327 个高质量细标注样本，覆盖超过 2,932 种细粒度情感类别。

### 2.2 模型设计：AffectGPT（预融合操作）

- **核心思想**：传统 MLLM 将全部跨模态交互交给 LLM 处理，不足以应对 MER 任务的多模态特性。本文将跨模态交互**移至 LLM 外部**，引入**预融合操作**。
- **两种预融合方案**：
  - **Q-Former 预融合**：保留时序信息，使用可学习的查询令牌（K 个）通过交叉注意力从拼接的音频和视频特征中提取融合特征。
  - **Attention 预融合**：先对音频和视频特征进行平均池化压缩时序，再计算注意力权重强调重要模态，最终得到融合特征。
- **模型架构**：音频编码器（HUBERT-L）、视频编码器（CLIP ViT-L）、投影层、预融合模块、LLM（Qwen2.5）组成。训练时冻结编码器和 LLM 权重，仅微调 LoRA 模块、投影层和预融合分支。

## 3. 实验设计

### 3.1 使用的数据集与基准（MER-UniBench）

- **细粒度情感识别**：OV-MERD+（扩展版，532 个样本）。
- **基本情感识别**：MER2023（411 样本）、MER2024（1,169 样本）、IEMOCAP（1,241 样本）、MELD（2,610 样本）。
- **情感分析**：CMU-MOSI（686 样本）、CMU-MOSEI（4,659 样本）、CH-SIMS（457 样本）、CH-SIMS v2（1,034 样本）。
- **评估指标**：针对自由文本输出设计，包括击中率（HIT）、集合级精度/召回率/F1（Fs）、加权平均 F 分数（WAF）等。

### 3.2 对比方法

- **仅音频+文本**：OneLLM、SECap、PandaGPT、Qwen-Audio、SALMONN。
- **仅视频+文本**：Otter、Video-LLaVA、PandaGPT、Video-ChatGPT、VideoChat2、LLaMA-VID、VideoChat、Chat-UniVi、mPLUG-Owl。
- **音频+视频+文本**：PandaGPT、Emotion-LLaMA、**AffectGPT（本文）**。
- 所有对比使用官方权重，保持输入模态一致。

## 4. 资源与算力

- 论文明确说明：所有模型在 **80GB NVIDIA Tesla A100 GPU** 上实现训练和推理。
- 训练配置：最大 epoch 数 60，每 epoch 5000 次迭代，batch size 为 3。使用 AdamW 优化器，学习率 1e-5。未明确说明具体 GPU 数量与总训练时长。

## 5. 实验数量与充分性

- **实验组数**：主实验对比了 17 种不同 MLLM（含多种模态组合），在 10 个数据集上报告完整结果（见表 12）。还进行了：
  - **数据集消融**（表 13）：训练数据来自不同来源（通用指令数据集、现有情感描述数据集 vs. MER-Caption/MER-Caption+）。
  - **过滤消融**（表 4）：无过滤、仅低级过滤、仅情绪或情感高级过滤、两者兼用。
  - **预融合消融**（表 5）：无预融合、Q-Former、Attention 三种设置。
  - **输入影响分析**（表 6）：单模态 vs. 多模态，人脸 vs. 帧 vs. 文本。
  - **用户研究**（表 7）：对比 MERR-Coarse 和 MERR-Fine 的描述质量。
  - **LLM、编码器、LoRA 秩的消融**（图 4、表 8）。
  - **采样帧数影响**（图 10）。
- **充分性评价**：实验覆盖了数据集、模型、输入、超参数等多个维度，在 10 个不同场景的数据集上验证，对比了所有主流公开 MLLM，消融实验设计合理。用户研究进一步验证了数据集质量。整体实验足够充分、客观且公平。

## 6. 主要结论与发现

1. **数据集有效性**：MER-Caption/MER-Caption+ 显著优于现有情感描述数据集（如 EmoVIT、MAFW、MERR-Coarse/Fine），在 MER-UniBench 平均得分达 74.77，比最佳现有模型（Emotion-LLaMA）高约 10 个百分点。
2. **模型先进性**：AffectGPT 在所有任务上显著领先于现有 MLLM。以音频+视频+文本模态为例，平均得分 74.77，远超 Emotion-LLaMA（64.17）。
3. **预融合必要性**：预融合操作（Q-Former 或 Attention）带来性能提升，表明将跨模态交互显式建模有利于情感理解。
4. **输入影响**：多模态结果优于单模态；人脸输入略优于帧输入（因为当前数据集主要关注人物面部）。
5. **数据集质量比数量关键**：MER-Caption+（31K）虽样本少于 MER-Caption（115K），但经过过滤后性能更优。
6. **LoRA 有效但秩增加收益有限**：微调 LoRA 提升性能，进一步提高秩（16→32）并未带来显著增益。

## 7. 优点

- **数据集创新**：提出“模型主导、人工辅助”的自动标注策略，在规模（115K/31K）和标注多样性（>2K 情感类别）上均为当前最大描述性情感数据集。
- **模型设计简洁有效**：预融合操作简单但有效，将跨模态交互外置，突出情感任务的多模态特性。
- **基准全面**：MER-UniBench 覆盖三种典型任务（细粒度、基本情感、情感分析），并为 MLLM 的自由文本输出设计了合理的评估指标（击中率、集合指标等）。
- **实验严谨**：进行了丰富消融、用户研究、不同 LLM/编码器/采样帧数的影响分析，结论可靠。
- **开源**：代码和数据集均已开源，便于社区复现和后续研究。

## 8. 不足与局限

- **数据集自动标注误差**：论文承认 MER-Caption+ 可能存在不准确描述（因缺乏人工核查），虽然性能仍优于手工标注数据集，但标注噪声问题未完全解决。
- **评估指标仍不完美**：对于基本情感识别任务，仅使用击中率作为主指标，未评价预测中额外标签的正确性（因为缺乏细粒度参考）。作者已将其列为未来工作。
- **多说话人场景缺失**：当前仅处理单人视频，多人物交互场景（如对话中情感相互影响）未涉及，限制了现实应用。
- **计算资源未详细说明**：GPU 数量、总训练时间等未给出，影响可复现性评估。
- **模型泛化性**：实验仅在英语和中文数据集上进行，未测试跨文化泛化。数据集来源主要是影视剧和自媒体，可能存在偏差。
- **伦理与隐私**：论文声明不涉及新数据采集，原始数据来自 MER2024 未标注部分，但使用时需遵守 CC BY-NC 4.0 许可。未讨论去除人脸后的可能指纹风险。

（完）
