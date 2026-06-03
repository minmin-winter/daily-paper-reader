---
title: "SK-VQA: Synthetic Knowledge Generation at Scale for Training Context-Augmented Multimodal LLMs"
title_zh: SK-VQA：大规模合成知识生成用于训练上下文增强的多模态大语言模型
authors: "Xin Su, Man Luo, Kris W Pan, Tien Pei Chou, Vasudev Lal, Phillip Howard"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=EVwMw2lVlw"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 为多模态视觉问答生成合成数据集，结合外部知识
tldr: SK-VQA通过大规模合成数据生成，为多模态大语言模型在知识型视觉问答中提供上下文增强训练。该数据集包含超过200万个视觉问答对及其外部知识，旨在提升模型融合文本和图像进行推理的能力，直接服务于多模态推理需求。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 749, \"height\": 756, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1554, \"height\": 673, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 739, \"height\": 688, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1421, \"height\": 629, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 832, \"height\": 571, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1774, \"height\": 628, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1780, \"height\": 735, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 895, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 679, \"height\": 512, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 682, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 446, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 444, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-evwmw2lvlw/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 441, \"height\": 347, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 856, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 859, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 644, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 859, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 858, \"height\": 246, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 855, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1116, \"height\": 917, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 892, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1126, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 696, \"height\": 607, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-evwmw2lvlw/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1649, \"height\": 587, \"label\": \"Table\"}]"
motivation: 现有视觉语言模型不擅长上下文增强生成，合成数据在该领域的应用不足。
method: 构建大规模合成多模态数据集，包含视觉问答对和外部知识源。
result: 数据集可用于训练多模态大语言模型，提升其在知识型视觉问答上的表现。
conclusion: SK-VQA填补了多模态上下文增强生成训练数据的空白。
---

## Abstract
Multimodal retrieval-augmented generation (RAG) plays a crucial role in domains such as knowledge-based visual question answering (KB-VQA), where models should effectively integrate additional knowledge to generate a response. However, existing vision and language models (VLMs) are not inherently designed for context-augmented generation, limiting their effectiveness in such tasks. While synthetic data generation has recently gained attention for training large VLMs, its application for context-augmented generation remains underexplored. To address this gap, we introduce SKVQA, a large-scale synthetic multimodal dataset containing over 2 million visual question-answer pairs, each associated with external knowledge sources to determine the final answer. Compared to previous datasets, SKVQA exhibits 11× more unique questions, greater domain diversity, and a broader spectrum of image sources. Through human evaluations, we confirm the high quality of the generated question-answer pairs and their contextual relevance. Extensive experiments show that SKVQA serves both as a challenging benchmark for knowledge-based VQA and as an effective training resource for adapting generative multimodal models to context-augmented generation. Our results further indicate that models trained on SKVQA demonstrate enhanced generalization in both context-aware VQA and multimodal RAG settings.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：现有的多模态大语言模型（MLLM）在检索增强生成（RAG）场景中并不擅长上下文增强生成，即模型需要同时基于图像、问题和检索到的外部知识文档来生成答案。然而，目前MLLM的训练数据中缺乏这种“多模态查询 + 相关上下文文档”的配对数据，限制了其在知识型视觉问答（KB-VQA）等任务中的应用。
- **整体含义**：为了解决训练数据稀缺的问题，作者提出利用合成数据生成技术，构建大规模、高多样性的多模态RAG训练数据集，从而使MLLM能够更好地适应上下文增强的生成任务。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：使用强大的基础模型（GPT-4）为每张图像自动生成一个相关的上下文文档和多个问答对，从而获得大规模合成数据。
- **关键技术细节**：
  - **数据生成流程**：给定一张图像，向GPT-4提供提示（prompt），要求其生成一段维基百科风格的上下文文档（不直接引用图像），然后生成多个QA对。每个QA对需满足：问题必须引用图像但避免提及图像中的对象名称；答案必须可以从上下文中提取且不能是图像中的对象；答案应简洁（单个词或短语）。
  - **过滤策略**：
    - **IR过滤**：去除上下文文档中直接引用“图像”“照片”等词语的样本。
    - **CAP过滤**（Context Answer Presence）：仅保留答案明确出现在上下文文档中的样本（同时满足IR条件）。最终得到三个版本的数据集：SK-VQA（全集）、SK-VQA_IR、SK-VQA_IR+CAP。
  - **数据来源**：图像来自LAION-400m、Wikipedia（WIT数据集）以及合成图像数据集COCO-Counterfactuals；上下文文档部分由GPT-4生成，部分来自Wikipedia原文（用于对比）。

## 3. 实验设计

- **数据集与场景**：
  - **训练数据集**：SK-VQA（200万QA对），对比数据集InfoSeek（14万子集）、Enc-VQA（22万子集）。
  - **测试数据集**：InfoSeek验证集（11,323样本）、Enc-VQA测试集（5,750）、ViQuAE全部（3,625）、SK-VQA_IR测试集（10,744样本）。
  - **基准（benchmark）**：零样本评估6个MLLM（PaliGemma-3B、LLaVA-v1.5-7B/13B、LLaVA-1.6-7B/13B/34B、Qwen-VL-7B、Idefics2-8B）；微调实验使用LLaVA-7B和PaliGemma-3B。
- **对比方法**：训练模型在SK-VQA、InfoSeek、Enc-VQA上分别微调，对比域内和域外性能；此外还做了RAG检索设置（使用CLIP Score Fusion检索外部知识库）。
- **指标**：精确匹配（Exact Match）和Enc-VQA官方语义评估（BEM）。

## 4. 资源与算力

- **算力使用**：
  - 使用24块Intel Gaudi2 AI加速器进行LLaMA-3-70b的推理（用于LLM评估）。
  - 零样本和微调实验使用内部Linux Slurm集群，配备Nvidia RTX 3090、A6000、A100 GPU，最多并行使用48块GPU。每个并行worker分配14核CPU、124GB RAM、1 GPU。单次任务计算时间6~48小时不等。
- **说明**：论文明确交代了算力配置，但未详细报告训练单个模型的具体GPU小时数。

## 5. 实验数量与充分性

- **实验数量**：涵盖零样本（8个MLLM）、微调（不同模型大小、不同训练数据集）、RAG检索设置、消融实验（图像来源、过滤方法、生成模型（GPT-4 vs LLaVA-34B））、人类评估（100样本）、自动质量评估（语法、偏见、毒性、LLM-as-judge）。
- **充分性与公平性**：
  - 实验设计全面，覆盖了域内和域外泛化、不同数据源、不同过滤策略、不同模型规模。
  - 对比数据集（InfoSeek、Enc-VQA）均通过下采样控制训练量（约200K样本），确保公平比较。
  - 人类评估和自动评估验证了合成数据质量，过滤策略有效。
  - 不足之处：仅测试了GPT-4生成数据，未对其他生成模型做全面对比（LLaVA-34B生成质量差，仅做了小规模验证）；实验未涉及更大参数模型（如LLaVA-34B的微调）、未评估多语言场景。

## 6. 主要结论与发现

1. SK-VQA是目前最大、最多样的KB-VQA数据集（200万QA对，96%为唯一问题，11倍于现有数据集）。
2. 零样本评估表明SK-VQA对现有MLLM构成显著挑战（性能远低于Enc-VQA和ViQuAE），可作为更难的基准。
3. 微调实验显示：在SK-VQA上训练的模型在多个域外数据集上均取得最好或相近的泛化性能，而使用InfoSeek或Enc-VQA训练的模型在域外常出现性能下降。
4. 合成数据（特别是GPT-4生成上下文）可有效替代真实数据，甚至在某些场景下（如COCO-CFs图像+GPT-4上下文）表现更优。
5. 过滤策略（IR和CAP）能进一步提高域外泛化能力，同时减少数据量。
6. RAG模拟实验也验证了SK-VQA训练模型的鲁棒性和泛化性。

## 7. 优点

- **数据规模与多样性**：200万QA对，覆盖LAION、Wikipedia、合成图像，话题广泛（艺术、时尚、体育、建筑等），远超先前数据集。
- **合成数据质量高**：人类评估正确率77%（全集），IR+CAP子集达87%；LLM-as-judge评估显示90.7%答案正确。
- **公开可用**：数据集和生成代码均开源。
- **实验设计系统**：包含零样本、微调、RAG模拟、消融、人类评估等，验证充分。
- **实用价值**：为MLLM在RAG场景下的训练提供了有效资源，且方法可推广至其他领域。

## 8. 不足与局限

- **数据局限**：仅含英文；可能存在GPT-4的幻觉或偏差（尽管过滤和评估缓解部分）；未完全验证所有样本的正确性。
- **生成模型依赖**：仅使用GPT-4（商业模型），开源模型（LLaVA-34B）生成质量差，限制了完全开源复现的可能性。
- **实验覆盖**：未涉及更大的MLLM（如70B+）微调；未评估多语言、多轮对话等场景；RAG实验仅使用单一检索模型（CLIP Score Fusion）。
- **潜在风险**：合成数据可能继承模型偏见，尽管通过自动检测未发现偏见/毒性，但仍需谨慎应用。

（完）
