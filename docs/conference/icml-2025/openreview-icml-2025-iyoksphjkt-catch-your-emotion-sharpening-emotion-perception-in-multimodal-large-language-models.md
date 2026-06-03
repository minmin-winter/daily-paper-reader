---
title: "Catch Your Emotion: Sharpening Emotion Perception in Multimodal Large Language Models"
title_zh: 捕捉你的情绪：增强多模态大模型的情感感知
authors: "Yiyang Fang, Jian Liang, Wenke Huang, He Li, Kehua Su, Mang Ye"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=IYOksPHJKT"
tags: ["query:mm-reasoning"]
score: 4.0
evidence: 多模态大模型中的情感推理
tldr: 本文针对多模态大模型在情感推理中语义相似情绪区分困难和冗余视觉信息干扰的问题，提出了一种无需训练的渐进式注意力重校准方法SPARC，通过增强关键视觉令牌的贡献来提升情感感知能力。实验表明该方法有效提高了情绪分类准确率，为情感理解提供了一种轻量级解决方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-iyoksphjkt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 822, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyoksphjkt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1589, \"height\": 648, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyoksphjkt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 828, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyoksphjkt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1758, \"height\": 1117, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyoksphjkt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 733, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyoksphjkt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1767, \"height\": 640, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-iyoksphjkt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1652, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyoksphjkt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 847, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyoksphjkt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 843, \"height\": 254, \"label\": \"Table\"}]"
motivation: 多模态大模型在情感推理中难以区分相似情绪且易受冗余视觉信息干扰。
method: 提出SPARC方法，在解码阶段选择性渐进式重校准视觉注意力，增强核心视觉令牌贡献。
result: 实验验证该方法显著提升了情绪分类准确率，无需额外训练。
conclusion: SPARC为多模态大模型的情感理解提供了一种轻量且有效的推理增强方法。
---

## Abstract
Multimodal large language models (MLLMs) have achieved impressive progress in tasks such as visual question answering and visual understanding, but they still face significant challenges in emotional reasoning. Current methods to enhance emotional understanding typically rely on fine-tuning or manual annotations, which are resource-intensive and limit scalability. In this work, we focus on improving the ability of MLLMs to capture emotions during the inference phase. Specifically, MLLMs encounter two main issues: they struggle to distinguish between semantically similar emotions, leading to misclassification, and they are overwhelmed by redundant or irrelevant visual information, which distracts from key emotional cues. To address these, we propose Sharpening Emotion Perception in MLLMs (SEPM), which incorporates a Confidence-Guided Coarse-to-Fine Inference framework to refine emotion classification by guiding the model through simpler tasks. Additionally, SEPM employs Focus-on-Emotion Visual Augmentation to reduce visual redundancy by directing the attention of models to relevant emotional cues in images. Experimental results demonstrate that SEPM significantly improves MLLM performance on emotion-related tasks, providing a resource-efficient and scalable solution for emotion recognition.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

多模态大模型（MLLMs）在视觉问答、视觉理解等传统任务上取得了显著进展，但在情感推理方面仍面临重大挑战。当前增强情感理解的方法主要依赖微调或人工标注，资源消耗大且可扩展性差。论文指出MLLMs在推理阶段存在两个关键问题：① 难以区分语义相似的情感类别（如“乐趣”与“兴奋”），导致分类混淆；② 图像中冗余或无关的视觉信息干扰模型提取关键情感线索。为此，作者提出一种无需额外训练的方法SEPM（Sharpening Emotion Perception in MLLMs），旨在推理阶段提升情感感知能力，实现资源高效且可扩展的情感识别解决方案。

## 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：通过两阶段粗到细推理和视觉注意力增强，在不训练、无标注的前提下，引导MLLMs聚焦情感关键信息，提升情感分类准确性。

**关键技术细节**：

- **Confidence-Guided Coarse-to-Fine Inference (CCI)**  
  - 第一阶段（粗粒度）：将所有情感类别分为正面和负面两组，构造粗粒度查询，让模型判断图像情感极性（Positive/Negative）。  
  - 置信度评估：基于模型Softmax输出的概率方差计算置信度C。若C低于阈值α（默认0.1），认为粗粒度结果不可靠，后续将保留所有类别并添加模糊描述提示；否则根据粗粒度结果仅保留对应极性类别进行细粒度推理。  
  - 第二阶段（细粒度）：根据粗粒度结果构造细粒度查询，指定正/负面情感类别列表，简化任务，减少语义相似性干扰。

- **Focus-on-Emotion Visual Augmentation (FoE)**  
  - 在查询前添加“Please focus on emotion”提示，引导模型关注情感。  
  - 利用第一阶段LLM最后一层注意力图，计算FoE提示词token与视觉token之间的平均注意力得分，作为视觉token的重要性指标。  
  - 丢弃得分最低的k个token（k = ⌊βN_v⌋，β为丢弃比例，默认0.2），保留与情感最相关的视觉token，降低视觉冗余。

- **算法流程**（文字说明）：  
  1. 输入样本D和粗粒度查询Qc，MLLM进行粗粒度推理得到极性标签Ê及注意力图A。  
  2. 计算置信度C，根据阈值确定细粒度查询Qf（可靠时仅含对应极性类别，不可靠时保留全部类别并加模糊描述）。  
  3. 基于注意力图计算FoE提示词与视觉token的平均得分，生成丢弃映射R。  
  4. 丢弃冗余视觉token后，与细粒度查询组成新样本D'，输入MLLM进行细粒度推理，得到最终情感类别E。

## 3. 实验设计：数据集、benchmark、对比方法

**数据集**：四个情感数据集，涵盖不同场景和类别数：  
- Emotion6（6类）  
- EmoSet（8类）  
- WebEmo（两种粒度：7类、25类）  
- Abstract（8类）

**基准模型**：  
- LLaVA-7b、VILA-8b

**对比方法**：  
- Zero-shot（基础零样本推理）  
- Zero-shot-CoT（添加“Let's think step by step”提示）  
- SparseVLM（一种通过丢弃任务无关视觉令牌提升推理效率的训练无关方法）  
- 随机丢弃、查询相关丢弃（与FoE相关丢弃对比）  
- 消融实验：分别评估CCI、FP（FoE Prompt）、VTA（视觉令牌增强）各组件。

## 4. 资源与算力

论文明确说明：“All experiments are conducted on 8 NVIDIA 4090 GPUs, each with 24GB of memory.” 由于SEPM是完全无需训练的方法，不涉及训练时长，仅需推理计算。文中未报告具体推理耗时。

## 5. 实验数量与充分性

- **主实验**：在4个数据集上，对比LoRA、VILA两种架构下的5种方法（Zero-shot、Zero-shot-CoT、SparseVLM、SEPM β=0.1、SEPM β=0.2），共产生10组对比结果。
- **丢弃策略对比**：在Emotion6和EmoSet上测试随机丢弃、查询相关丢弃和FoE相关丢弃，共6组。
- **消融实验**：分离CCI、FP、VTA组件，在Emotion6和EmoSet上进行5组（基线、单独CCI、单独FP、CCI+FP、三者全量）。
- **敏感性分析**：在Emotion6和EmoSet上分别变化超参数α（0.05~0.4）和β（0.1~0.4），共约16组。
- **可视化分析**：包括丢弃标记可视化、置信度估计评估、细粒度类别准确率雷达图。

**充分性评价**：实验覆盖了多个数据集、两种主流模型架构、多种对比方法、充分消融和超参数敏感性分析，并辅以可视化分析，整体设计较为系统、客观。但未在更大规模模型（如13B、34B）上验证，且未与最新微调方法（如EmoVIT、Emotion-LLaMA）直接对比（因为它们需训练，无法直接纳入零样本比较）。

## 6. 论文的主要结论与发现

- SEPM在不需额外训练或标注的情况下，显著提升MLLMs在情感任务上的分类准确率。在LLaVA-7b上，WebEmo 7类提升17.19%，整体平均提升约6%。
- 粗到细两阶段推理有效缓解了语义相似情感类别的混淆；置信度评估能识别不可靠推理并加以矫正。
- FoE注意力引导丢弃策略优于随机丢弃或查询相关丢弃，表明情感关键信息集中于特定视觉区域。
- 实验表明MLLMs在情感任务中存在较多冗余视觉信息，丢弃冗余令牌有助于突出关键情感线索。
- 不同情感类别准确率波动较大，模型对文本提示有偏好，整体性能提升的同时可能牺牲个别类别的精度。

## 7. 优点

- **无需训练**：完全在推理阶段操作，避免了昂贵的微调成本和人工标注，具有良好的可扩展性和实用性。
- **方法简洁有效**：粗到细推理与注意力引导丢弃逻辑清晰，易于复现和集成到现有MLLMs。
- **全面实验验证**：在多个数据集、多种架构、多种对比方法下验证了有效性，并通过消融和敏感性分析验证了各组件贡献。
- **可视化分析深入**：对丢弃标记、置信度与准确率关系、细粒度类别表现进行了可视化，提供了直观理解。

## 8. 不足与局限

- **依赖注意力图质量**：FoE丢弃策略基于第一阶段注意力图，若第一阶段推理偏差较大，丢弃可能误删关键信息。置信度机制虽尝试缓解，但高阈值下可能保留过多冗余。
- **类别偏好问题**：模型对不同情感类别有内在偏好，SEPM虽提升整体准确率，但可能加剧类别不平衡（如某些类别准确率下降）。
- **实验覆盖有限**：仅测试了7B/8B级别的LLaVA和VILA，未在更大模型（如13B、34B）或更复杂的多模态模型（如GPT-4V）上验证。此外，未与需要训练的先进方法（如EmoVIT、Emotion-LLaMA）进行性能对比（因场景不同）。
- **仅限情感分类**：方法专门针对情感分类任务设计，对更广义的情感理解（如情感推理、生成）的适用性未探讨。
- **超参数敏感性**：β和α需人为设定，最优值可能因数据集和模型而异，缺乏自适应调整机制。

（完）
