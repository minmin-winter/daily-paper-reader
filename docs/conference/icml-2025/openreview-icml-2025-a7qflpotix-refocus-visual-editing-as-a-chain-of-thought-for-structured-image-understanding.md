---
title: "ReFocus: Visual Editing as a Chain of Thought for Structured Image Understanding"
title_zh: ReFocus：将视觉编辑作为思维链用于结构化图像理解
authors: "Xingyu Fu, Minqian Liu, Zhengyuan Yang, John Richard Corring, Yijuan Lu, Jianwei Yang, Dan Roth, Dinei Florencio, Cha Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=a7qFlPOTix"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 以视觉编辑作为思维链，提升多模态LLM的结构化图像理解
tldr: 当前多模态大语言模型缺乏多跳选择性注意力能力，难以理解表格、图表等结构化图像。ReFocus提出一个简单框架，让多模态LLM通过生成Python代码修改输入图像（画框、高亮、掩码等），形成视觉思维链以逐步聚焦关键区域。实验表明该方法在结构化图像理解任务上显著提升了准确率。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1773, \"height\": 657, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1751, \"height\": 670, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1651, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1761, \"height\": 598, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 897, \"height\": 549, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 853, \"height\": 423, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1751, \"height\": 200, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1749, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 798, \"height\": 729, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 809, \"height\": 759, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 521, \"height\": 432, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 529, \"height\": 436, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 530, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-a7qflpotix/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 530, \"height\": 462, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 718, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1764, \"height\": 629, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 185, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 849, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1772, \"height\": 491, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1397, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1395, \"height\": 442, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1019, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-a7qflpotix/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1465, \"height\": 324, \"label\": \"Table\"}]"
motivation: 多模态LLM缺乏多跳注意力，难以理解复杂结构化图像。
method: 让多模态LLM生成Python代码调用工具修改图像，通过视觉编辑形成推理链。
result: 在表格和图表理解任务上大幅超越基线，证明了视觉思维链的有效性。
conclusion: 视觉编辑作为思维链是一种增强多模态LLM结构化理解能力的有效技术。
---

## Abstract
Structured image understanding, such as interpreting tables and charts, requires strategically refocusing across various structures and texts within an image, forming a reasoning sequence to arrive at the final answer. However, current multimodal large language models (LLMs) lack this multihop selective attention capability. In this work, we introduce ReFocus, a simple yet effective framework that equips multimodal LLMs with the ability to generate ``visual thoughts'' by performing visual editing on the input image through code, shifting and refining their visual focuses. Specifically, ReFocus enables multimodal LLMs to generate Python codes to call tools and modify the input image, sequentially drawing boxes, highlighting sections, and masking out areas, thereby enhancing the visual reasoning process. We experiment upon a wide range of structured image understanding tasks involving tables and charts. ReFocus largely improves performance on all tasks over GPT-4o without visual editing, yielding an average gain of 11.0% on table tasks and 6.8% on chart tasks. We present an in-depth analysis of the effects of different visual edits, and reasons why ReFocus can improve the performance without introducing additional information. Further, we collect a 14k training set using ReFocus, and prove that such visual chain-of-thought with intermediate information offers a better supervision than standard VQA data, reaching a 8.0% average gain over the same model trained with QA pairs and 2.6% over CoT.

---

## 论文详细总结（自动生成）

# 中文总结：ReFocus 论文

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：当前多模态大语言模型（MLLMs）在理解表格、图表等结构化图像时，缺乏多跳选择性注意力能力，难以自动聚焦关键信息并忽略无关干扰。现有方法将图像信息先转为文本再依赖文本链式推理（CoT），但过程中“不再回头看图像”，导致视觉推理不足。
- **整体含义**：该论文提出一种新型视觉推理范式——通过图像编辑来生成“视觉思想”，使模型能够以迭代方式修改输入图像（涂色、画框、遮挡等），形成视觉链式思考（Visual Chain-of-Thought），从而显著提升结构化图像的理解能力。

## 2. 论文提出的方法论

- **核心思想**：让多模态LLM生成Python代码，调用预定义的图像编辑工具（画框、高亮、掩盖），对输入图像进行逐步修改；每次编辑后的新图像作为下一轮输入，直到模型得到最终答案。整个流程是可迭代的“思考→编辑→再思考”过程。
- **关键技术细节**：
  - 针对**表格问题**：提供按列/行的高亮、画框、掩盖三类编辑工具（共6种函数）。坐标通过OpenCV的轮廓检测和行/列长度启发式自动获取。
  - 针对**图表问题**：分别支持水平/垂直柱状图的按X/Y值编辑，以及多子图（CharXiv）的子图坐标获取和编辑。坐标来自数据集提供的值坐标或OpenCV检测。
  - **算法流程**（文字描述）：
    1. 多模态LLM接收原始图像和问题。
    2. 模型生成文本“THOUGHT”描述需要关注哪些区域。
    3. 模型输出Python代码调用编辑工具（如`focus_on_columns_with_mask`）。
    4. 代码执行，生成编辑后的新图像。
    5. 新图像反馈给LLM，继续下一轮思考或直接给出答案。
    6. 重复直至输出“ANSWER: …”并结束。
  - **与现有方法区别**：不同于Visual Sketchpad等依赖外部专家知识/额外信息，ReFocus仅通过屏蔽、高亮等操作消除干扰，不引入新信息。

## 3. 实验设计

- **使用数据集**：
  - 表格任务：VWTQ（Wikipedia表格）、VWTQ_syn（合成表格）、VTabFact（表格事实验证）。
  - 图表任务：CharXiv（科学论文多子图）、ChartQA（水平/竖条形图）。其中ChartQA测试集分为水平条（444个样本）和竖条（382个样本），CharXiv随机选取143个多子图问题。
- **Benchmark**：各数据集的标准准确率（Accuracy），使用GPT-4作为裁判判断答案是否正确。
- **对比方法**：
  - 基线多模态LLM：LLaVA-NeXT（7B/13B/34B）、Phi-3-vision、Gemini-Pro 1.5、VisProg（替换为GPT-4o）。
  - 主要对比：GPT-4o（2024-05-13和2024-08-06两个版本）不进行编辑的CoT格式。
  - 此外还对比了将编辑后的图像喂给开源模型（Oracle ReFocus）。
  - 在SFT实验中对比：QA数据、CoT数据、VCoT数据（包含聚焦边界框）。
  - 与Visual CoT方法（Shao et al., 2024）进行间接比较。

## 4. 资源与算力

- 论文明确提到：
  - **推理阶段**（Section 4实验）：使用4块NVIDIA Quadro RTX 8000 GPU，耗时约40 GPU小时，用于运行LLaVA-NeXT和Phi-3-vision等开源模型。
  - **微调阶段**（Section 5）：使用8块NVIDIA RTX A6000 GPU（48GB显存每块），采用全量微调Phi-3.5-vision模型，超参数搜索包括学习率和epoch数。
  - 未明确说明GPT-4o API调用所需算力（依赖OpenAI云服务），实验成本未量化。

## 5. 实验数量与充分性

- **实验数量**：论文进行了多组实验，涵盖6个数据集上的表格和图表任务；对比了多个基线模型；做了消融分析（不同编辑类型效果、编辑频率统计）；做了SFT训练（使用14k数据，对比QA、CoT、VCoT）；还分析了ReFocus增强OCR和视觉定位的原因示例。
- **充分性与客观性**：
  - 控制变量：GPT-4o基线也采用对话格式（CoT）以公平对比。
  - 消融实验：在VWTQ和VWTQ_syn上比较了mask、draw、highlight三种编辑方法，结果显示方法间差异不大，但均优于无编辑。
  - 编辑频率统计：展示了不同数据集上模型选择编辑的占比，避免过度依赖人工干预。
  - SFT实验：超参数搜索报告最佳性能，且对比了相同数据的QA/CoT版本，避免数据量干扰。
  - 局限性：未在更多类型的结构化图像（如流程图、地图）上验证；编辑坐标获取依赖OpenCV启发式，可能存在误差；仅测试了GPT-4o一种主干模型（API调用），未在更多开源MLLM上做完整ReFocus流程（仅测试了编辑后的图像）。
  - 整体充分性较好，但实验覆盖范围可更广。

## 6. 论文的主要结论与发现

- **主要结论**：
  1. **ReFocus显著提升结构化图像理解**：在GPT-4o基础上，表格任务平均提升11.0%（VWTQ +10.4%、VWTQ_syn +3.4%等），图表任务平均提升6.8%（CharXiv +8.3%、水平条+7.2%等）。在更先进版本（2024-08-06）上也保持增益。
  2. **视觉推理优于纯文本推理**：将编辑后的图像喂给开源模型（如LLaVA-NeXT、Phi-3）也能带来部分提升，证明视觉编辑本身改善了模型感知。
  3. **无外部信息增益**：ReFocus不引入新信息，通过排除干扰、增强注意力提升性能（如OCR错误修正、图形定位修正）。
  4. **视觉链式思考数据是更好的监督信号**：用ReFocus生成的14k VCoT数据微调Phi-3.5-vision，比用相同QA数据平均提升8.0%，比用CoT数据提升2.6%，远超Visual CoT方法的训练效果。

## 7. 优点

- **方法简单有效**：仅通过包装好的Python编辑工具让模型自我引导，无需额外训练或外部知识库，即插即用。
- **可解释性强**：每次编辑的“THOUGHT”和代码让推理过程透明，便于分析错误。
- **数据价值高**：收集的VCoT数据为小模型提供比普通VQA/CoT更丰富的监督，有望加速视觉推理蒸馏。
- **广泛适用性**：覆盖表格、多种子图、条形图等多种结构化图像，工具设计可扩展。

## 8. 不足与局限

- **依赖预定义坐标获取**：表格和图表都需要先通过OpenCV或原始数据集获得行列/bar的边界框，通用性受限，对于新类型结构化图像（如散点图、饼图）坐标获取可能失效。
- **仅测试GPT-4o作为编辑主体**：未验证其他MLLM（如Claude、Gemini）是否也能有效生成编辑代码，存在模型依赖性。
- **计算开销**：每次迭代需要调用LLM API并执行图像编辑，成本较高，在小模型上快速推理仍需蒸馏。
- **实验局限**：未在更多元的结构化图像（如信息图、地图）上验证；未进行用户研究评估实际应用价值。
- **潜在偏差**：数据收集时只保留了预测正确的样本（约14k/15k），可能过滤掉困难或噪声样本，导致SFT数据偏向简单。

（完）
