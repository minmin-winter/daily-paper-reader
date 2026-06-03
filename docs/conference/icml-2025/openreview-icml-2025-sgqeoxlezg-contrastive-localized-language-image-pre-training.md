---
title: Contrastive Localized Language-Image Pre-Training
title_zh: 对比式局部语言-图像预训练
authors: "Hong-You Chen, Zhengfeng Lai, Haotian Zhang, Xinze Wang, Marcin Eichner, Keen You, Meng Cao, Bowen Zhang, Yinfei Yang, Zhe Gan"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=sGQEOXlezg"
tags: ["query:unified-mm"]
score: 8.0
evidence: 提出区域-文本对比损失与CLIP相结合的多模态预训练目标
tldr: CLIP的图像级对比学习对细粒度区域理解不足。本文提出CLOC方法，在预训练中引入区域-文本对比损失和可提示嵌入模块，显著提升了视觉定位能力。实验表明CLOC作为MLLM的视觉骨干，在下游区域级任务上优于CLIP。该工作为多模态预训练目标的改进提供了有效方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-sgqeoxlezg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1734, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgqeoxlezg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1778, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgqeoxlezg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1514, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgqeoxlezg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1081, \"height\": 2123, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 863, \"height\": 624, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 686, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1764, \"height\": 821, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 850, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1717, \"height\": 547, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 858, \"height\": 388, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 722, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgqeoxlezg/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1456, \"height\": 847, \"label\": \"Table\"}]"
motivation: CLIP的图像级对比学习难以支持细粒度区域理解。
method: 在CLIP基础上增加区域-文本对比损失和可提示嵌入模块，实现区域级视觉-语言对齐。
result: 在区域级理解任务上显著优于CLIP，提升了MLLM的定位能力。
conclusion: CLOC为多模态预训练提供了更细粒度的对齐目标，有助于提升MLLM的表现。
---

## Abstract
CLIP has been a celebrated method for training vision encoders to generate image/text representations facilitating various applications. Recently, it has been widely adopted as the vision backbone of multimodal large language models (MLLMs). The success of CLIP relies on aligning web-crawled noisy text annotations at image levels. However, such criteria may be insufficient for downstream tasks in need of fine-grained vision representations, especially when understanding region-level is demanding for MLLMs. We improve the localization capability of CLIP with several advances. Our proposed pre-training method, Contrastive Localized Language-Image Pre-training (CLOC), complements CLIP with region-text contrastive loss and modules. We formulate a new concept, promptable embeddings, of which the encoder produces image embeddings easy to transform into region representations given spatial hints. To support large-scale pre-training, we design a visually-enriched and spatially-localized captioning framework to effectively generate region-text labels. By scaling up to billions of annotated images, CLOC enables high-quality regional embeddings for recognition and retrieval tasks, and can be a drop-in replacement of CLIP to enhance MLLMs, especially on referring and grounding tasks.

---

## 论文详细总结（自动生成）

# 论文结构化中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

*   **核心问题**：CLIP 依赖图像级别的文本对齐，缺乏对图像区域（region-level）的细粒度理解，限制了多模态大语言模型（MLLM）在指代和定位（referring & grounding）等任务上的表现。
*   **研究动机**：CLIP 作为 MLLM 的视觉骨干，其全局图像-文本对比损失难以捕捉区域语义，亟需一种能同时保持 CLIP 原有能力（如零样本分类）并增强定位能力的方法。
*   **整体含义**：提出 CLOC，通过区域-文本对比学习和可提示嵌入模块，在不牺牲 CLIP 图像级别性能的前提下，显著提升区域级表示能力，可作为 MLLM 的即插即用替代视觉骨干。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

*   **核心思想**：在 CLIP 原有图像-文本对比损失基础上，增加区域-文本对比损失；设计“可提示嵌入”（Promptable Embeddings）概念，使图像编码器能根据空间提示（如边界框）提取区域表示。
*   **关键技术细节**：
    *   **可提示嵌入模块（Prompter）**：一个轻量级单层 Transformer 编码器，接收图像特征和位置编码（框坐标）或文本提示，输出区域嵌入。
    *   **区域-文本对比损失**：对称对比损失（\( \mathcal{L}_{CLOC} \)），对每个区域在batch内进行对比，过滤相似文本以避免冲突。
    *   **接地损失（\( \mathcal{L}_{grounding} \)）**：预测边界框的回归损失，与CLIP损失联合训练。
    *   **整体损失函数**：\( \mathcal{L} = \mathcal{L}_{CLIP} + \lambda(\mathcal{L}_{CLOC} + \mathcal{L}_{grounding}) \)。
*   **VESL 伪标签流程**：给定图像和网页 alt-text，依次进行（1）视觉丰富重标注（VeCap）生成详细描述；（2）命名实体识别（NER）提取区域短语候选；（3）开放词汇检测器（OWLv2）将短语与边界框匹配，生成区域-文本对。

## 3. 实验设计：数据集、Benchmark、对比方法

*   **预训练数据**：
    *   图像-文本对：WiT-300M 和 DFN-5B（经 VeCap 重标注）。
    *   区域-文本对：用 VESL 对 WiT-300M 和 2B 子集进行伪标注，共生成约 2B 图像的区域标签。
*   **评估 Benchmark**（共 31 个任务）：
    *   **图像级任务**：ImageNet 分类（v1, v2）、COCO 图像-文本检索（i2t, t2i）。
    *   **区域级零样本任务**：COCO/LVIS 区域物体分类、GRIT 区域-文本检索（r2t, t2r）。
    *   **MLLM 下游任务**：
        * Ferret-Bench（指代描述、推理、定位对话）。
        * 指代理解（RefCOCO/+/g）、短语定位（Flickr30k Entities）、Referred-LVIS。
        * 通用 VQA（TextVQA、GQA、MMVet、POPE、MME）。
        * 开放词汇检测（COCO minival、ODinW、LVIS minival）。
*   **对比方法**：
    *   CLIP（多个变体：OpenAI-CLIP、自家训练的 CLIP）。
    *   消融版本：去掉 Prompter、替换为 RoI-Align、不使用 VESL、替换检测器为 GLIPv2、去掉文本过滤或接地损失等。
    *   与其他 MLLM 骨干对比（如 Shikra, Ferret 原始版本）。

## 4. 资源与算力

*   **文中明确提及**：
    *   大型模型（ViT L/14）在 **1024 个 v5p TPU** 上训练约 **6 天**。
    *   整体训练看到约 **14B 图像样本**。
    *   VESL 伪标签推理需要数百个 GPU 并行运行数天（未给出确切数字）。
    *   CLOC 额外计算主要来自对比矩阵，Prompter 本身很轻量，总体开销可接受。

## 5. 实验数量与充分性

*   **实验数量**：
    *   零样本图像/区域任务：8 组组合（表 3），含不同骨干（B/16, L/14, H/14）和多种消融（Prompter, VESL, 文本过滤, M=2 等）。
    *   Ferret-Bench：6 组对比（表 4），含不同骨干和采样策略。
    *   指代/定位 13 个数据集：3 组对比（表 5）。
    *   通用 VQA：2 组对比（表 6），含 LLaVA-1.5 和 LLaVA-NeXT。
    *   开放词汇检测：3 组对比（表 7）。
*   **充分性与公平性**：
    *   **充分**：覆盖了图像级、区域级、MLLM 下游、检测任务，消融实验设计全面（架构、数据、损失组件）。训练超参数与 CLIP 基线完全一致，仅增加区域模块。
    *   **公平**：所有下游评估使用官方代码库和统一超参数；与自家 CLIP 基线对比确保数据/计算公平；但与 OpenAI-CLIP 以及其它公开模型（如 GLIP）的数据和训练配置不同，需注意直接数值比较的局限性。

## 6. 论文的主要结论与发现

*   CLOC 在 **区域级零样本任务** 上取得显著提升（如 COCO 区域分类 mAcc 达 70%+，远超之前的方法），同时保持甚至改善图像级性能。
*   **Prompter 是核心组件**：相比 RoI-Align 能更好处理噪声伪标签，更适应 MLLM 的注意力机制。
*   **VESL 数据流程有效**：视觉丰富重标注 + NER 提取短语相比直接用 alt-text 的 n-grams 能生成更多、更准确的区域标签，降低物体幻觉（CHAIR 指标更优）。
*   CLOC 作为 MLLM 骨干（Ferret, LLaVA）一致优于 CLIP，在指代/定位任务上提升 1-6 个百分点；通用 VQA 也有小幅增益。
*   训练规模增大（从 300M 到 2B 区域标签）持续改善下游 MLLM 性能。
*   开放词汇检测性能优于 GLIP。

## 7. 优点：方法或实验设计上的亮点

*   **方法创新**：提出“可提示嵌入”概念，将空间提示与图像特征融合的轻量方案，既保持 CLIP 架构又能高效提取区域特征。
*   **数据工程**：VESL 流程结合视觉丰富重标注和 NER，可扩展至数十亿级别，且对后续模型提升有可验证贡献。
*   **实验设计**：
    *   与自家 CLIP 基线对比，控制变量严格。
    *   消融实验完整（Prompter vs RoI, VESL vs alt-text, 损失组件等）。
    *   覆盖 30+ 任务，从零样本到微调 MLLM，验证通用性。
    *   在 Ferret 中展示 Prompter 可替换原有复杂视觉采样器，体现简洁性。

## 8. 不足与局限

*   **数据成本**：构建 VESL 伪标签需要大量 GPU 资源（数百 GPU 数天），且依赖 OWLv2 等外部模型，可复现性受限（作者承诺开放标签但未提及模型权重）。
*   **实验覆盖的偏差**：
    *   主要与自家 CLIP 基线对比，未与近期专门改进 CLIP 定位的方法（如 Alpha-CLIP, UMG-CLIP）在相同数据预算下比较。
    *   开放词汇检测仅与 GLIP 对比，未与更优的 OV 检测器（如 OWLv2 本身）比较，且检测头简单。
*   **区域级零样本任务局限性**：GRIT 检索采用 recall@10 而非 r@1，说明区域级对比仍存在同义文本冲突；COCO/LVIS 分类使用封闭类名，与开放世界设定有差距。
*   **MLLM 实验温和性**：仅验证了 Ferret 和 LLaVA 系列，未在更多 MLLM 框架（如 Kosmos-2, MiniGPT-4）上验证。
*   **超参调优不足**：作者承认在超参搜索和架构调优上投入较少，可能未达最优性能。
*   **未讨论社会影响**：文末仅声明“无特殊的潜在社会影响”，缺乏对训练数据（网页爬取）偏见、生成性幻象等风险的深入分析。

（完）
