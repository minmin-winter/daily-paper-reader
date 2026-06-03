---
title: "FG-CLIP: Fine-Grained Visual and Textual Alignment"
title_zh: FG-CLIP：细粒度视觉与文本对齐
authors: "Chunyu Xie, Bin Wang, Fanjing Kong, Jincheng Li, Dawei Liang, Gengshen Zhang, Dawei Leng, Yuhui Yin"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=eih5Gy3Pjt"
tags: ["query:native-multi"]
score: 7.0
evidence: 使用长描述和区域标注实现细粒度视觉-文本对齐
tldr: FG-CLIP通过三方面改进增强细粒度理解：生成16亿长描述-图像对捕获全局语义；构建1200万图像和4000万区域标注的高质量数据集；引入1000万硬负样本。显著提升了CLIP的细粒度对齐能力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1763, \"height\": 921, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 401, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 396, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 397, \"height\": 269, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 583, \"height\": 2024, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1617, \"height\": 1073, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1586, \"height\": 971, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-eih5gy3pjt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1592, \"height\": 1136, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 853, \"height\": 508, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 855, \"height\": 576, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 678, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1646, \"height\": 512, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 863, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1770, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1525, \"height\": 1895, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1495, \"height\": 185, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-eih5gy3pjt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1382, \"height\": 252, \"label\": \"Table\"}]"
motivation: CLIP由于聚焦于粗粒度短描述，在细粒度理解上表现不足。
method: 利用大模型生成长描述对，构建区域级标注数据，并加入硬负样本训练。
result: 在细粒度检索和分类任务上显著超越原始CLIP。
conclusion: 细粒度数据增强有效提升多模态模型的细粒度对齐能力。
---

## Abstract
Contrastive Language-Image Pre-training (CLIP) excels in multimodal tasks such as image-text retrieval and zero-shot classification but struggles with fine-grained understanding due to its focus on coarse-grained short captions. To address this, we propose Fine-Grained CLIP (FG-CLIP), which enhances fine-grained understanding through three key innovations. First, we leverage large multimodal models to generate 1.6 billion long caption-image pairs for capturing global-level semantic details. Second, a high-quality dataset is constructed with 12 million images and 40 million region-specific bounding boxes aligned with detailed captions to ensure precise, context-rich representations. Third, 10 million hard fine-grained negative samples are incorporated to improve the model's ability to distinguish subtle semantic differences. We construct a comprehensive dataset, termed FineHARD, by integrating high-quality region-specific annotations with challenging fine-grained negative samples. Corresponding training methods are meticulously designed for these data. Extensive experiments demonstrate that FG-CLIP outperforms the original CLIP and other state-of-the-art methods across various downstream tasks, including fine-grained understanding, open-vocabulary object detection, image-text retrieval, and general multimodal benchmarks. These results highlight FG-CLIP's effectiveness in capturing fine-grained image details and improving overall model performance. The data, code, and models are available at https://github.com/360CVGroup/FG-CLIP.

---

## 论文详细总结（自动生成）

好的，以下是对该论文的详细中文总结。

### FG-CLIP: 细粒度视觉与文本对齐

#### 1. 核心问题与整体含义

*   **核心问题**：现有视觉-语言预训练模型（如CLIP）在图像-文本检索、零样本分类等任务中表现出色，但其文本编码器仅支持77个token，且训练数据多为粗粒度短描述，导致模型在处理**细粒度**的视觉内容（如物体的属性、颜色、材质、空间关系）时表现不佳。模型难以区分同一类别但属性有细微差别的物体。
*   **研究动机**：为了解决CLIP在细粒度理解上的局限性，作者旨在通过数据驱动和训练策略的创新，显著提升模型在全局和局部区域级别的细节感知与对齐能力。
*   **整体含义**：本文提出了FG-CLIP，通过三个关键创新构建了一个更强大的细粒度对比学习框架，显著提升了模型在多种细粒度下游任务上的性能，为多模态理解领域提供了新基准。

#### 2. 方法论

*   **核心思想**：通过大规模、高质量、多粒度的数据和针对性的训练策略，增强CLIP从全局到局部、从粗到细的对齐学习能力。具体分为三个关键部分：
    1.  **大规模长描述数据**：使用大语言模型为图像生成细致的描述，增强全局语义的对齐精度。
    2.  **高质量区域级数据**：构建包含精确区域边界框和对应详细描述的数据集，提升局部区域的对齐能力。
    3.  **硬负样本**：引入大量的、属性细微不同的负样本，迫使模型学习更具区分性的特征。
*   **关键技术细节**：
    *   **两阶段训练**：
        *   **第一阶段（全局对齐）**：仅使用全局对比学习，在**16亿**图像-长描述对上训练，增强模型对全局语义细节的感知能力。文本编码器的位置嵌入被扩展至支持至多248个token。
        *   **第二阶段（精细化对齐）**：在第一阶段模型基础上，加入区域对比学习和硬负样本学习。结合全局、区域和硬负样本损失函数进行联合优化。
    *   **区域对比学习**：使用RoIAlign从图像特征中提取区域特征，将整个图像的描述按区域分割成对应文本，然后进行区域-文本的对比学习。
    *   **硬负样本学习**：通过直接修改正样本描述（例如改变颜色、材质等属性）来生成语义相似但不同的负样本，并设计特定的损失函数来强制模型区分这些细微差别。
*   **核心公式**：整体损失函数为 `L = L_global + α * L_regional + β * L_hard`。其中`L_global`是标准的InfoNCE损失（用于图像-全局描述），`L_regional`是区域级的InfoNCE损失（用于区域-区域描述），`L_hard`是专为硬负样本设计的特定损失函数（强制将区域特征与正样本对齐，与多个负样本远离）。

#### 3. 实验设计

*   **数据集**：
    *   **预训练数据**：第一阶段的**16亿**图像-长描述对（基于LAION-2B，使用CogVLM2-19B重新生成描述）和第二阶段的**1200万**图像-区域标注对（名为**FineHARD**，包含4000万个边界框和1000万硬负样本）。
    *   **下游任务数据集**：涵盖细粒度、检测、检索和分类等多种任务。包括：
        *   **细粒度理解**：FG-OVD基准（包含hard, medium, easy, trivial四个难度级别）。
        *   **区域分类**：COCO-val2017, LVIS, Open Images。
        *   **开放词汇目标检测**：OV-COCO。
        *   **图像-文本检索**：ShareGPT4V, DCI (长描述), MSCOCO 5K, Flickr30K (短描述)。
        *   **零样本图像分类**：ImageNet-1K, ImageNet-v2。
        *   **通用多模态基准**：GQA, POPE, RefCOCO。
*   **对比方法**：对比了大量主流方法，包括CLIP、EVA-CLIP、LongCLIP、FineCLIP，以及开放词汇检测领域的OV-RCNN、RegionCLIP、Detic、VLDet等。
*   **核心基准**：论文的主要基准是**FG-OVD**，它专门评估模型对局部区域及其细微属性变化的区分能力。

#### 4. 资源与算力

*   **明确提及**：在数据处理（生成1.6B数据和FineHARD）阶段，使用了一个由**160个节点**组成的集群，每个节点配备**910B NPU**。
*   **训练耗时**：
    *   生成1.6B长描述：耗时30天。
    *   构建FineHARD数据集：耗时7天。
    *   训练模型（未明确提及具体GPU/TPU型号和数量）：在第二阶段，采用了DeepSpeed、CUDA TF32、Bfloat16等技术加速训练，每个NPU的batch size为512。

#### 5. 实验数量与充分性

*   **数量**：论文进行了大量实验，涵盖了6大类不同的基准任务（细粒度、区域分类、开放词汇检测、长/短描述检索、零样本分类、通用多模态），并在每个任务中与多个SOTA方法进行了对比。此外，还进行了详细的消融实验（表6）。
*   **充分性与公平性**：
    *   实验设计非常充分，覆盖了从粗到细、从识别到检索的全方位能力评估，这证明了方法在不同场景下的有效性。
    *   对比方法设置合理，包含了CLIP系列的最强变体。在开放词汇检测任务中，采用了统一的F-ViT框架，使得对比具备公平性。
    *   消融实验系统地分析了各个组件（全局对比、区域对比、硬负样本）的贡献，验证了每个设计的必要性。

#### 6. 主要结论与发现

*   **性能显著提升**：FG-CLIP在所有评估的细粒度任务（如FG-OVD）上，相比CLIP、EVA-CLIP、LongCLIP和FineCLIP等基线模型，都取得了显著的性能提升。尤其在FG-OVD的hard和medium子集上提升巨大。
*   **多任务均衡强化**：在专注于细粒度能力的同时，FG-CLIP并未牺牲其在全局任务上的表现，相反，在长/短描述图像-文本检索、零样本分类等任务上也取得了领先或可比的结果。
*   **通用性验证**：作为视觉骨干网络用于LLaVA时，FG-CLIP在GQA、POPE、RefCOCO等通用多模态基准上相比原始CLIP也展现了优势，证明了其作为基础视觉编码器的有效性。

#### 7. 优点

*   **数据规模空前**：构建了规模极其庞大的长描述（16亿）和区域标注（4000万边界框）数据集，这为模型学习海量细粒度知识提供了充分的数据保障。
*   **硬负样本设计创新**：系统性地生成并利用了1000万硬负样本，这是现有工作所欠缺的，也是模型在区分细微属性差异上取得突破的关键。
*   **两阶段训练策略**：先进行全局对齐再精细化微调，这种渐进式学习策略既保证了模型对宏观语义的把控，又有效提升了对细节的感知。
*   **实验全面且社区贡献大**：公开了模型、代码和数据集，为后续研究提供了宝贵资源，实验设计涵盖了广泛的基准，全面展示了方法的优劣。

#### 8. 不足与局限

*   **计算成本高昂**：无论是训练16亿数据还是处理1200万区域数据，都需要巨大的计算资源（160节点 x 910B NPU），这显著提高了研究的门槛，不利于其他研究者在类似规模上进行复现或改进。
*   **数据生成依赖LMM和LLM**：长描述和硬负样本的生成分别依赖于CogVLM2-19B和Llama-3.1-70B。这些模型的性能直接决定了数据质量，引入了一定偏差（如伪造事实、描述不准确）的风险。
*   **潜在的区域标注噪声**：通过Yolo-World自动生成的边界框和匹配的文本描述，尽管经过非极大值抑制过滤（保留置信度>0.4的框），但仍可能存在定位不准确或语义匹配错误的情况，这会影响区域对比学习的效果。
*   **负样本质量验证**：虽然对3000个负样本进行了人工抽检显示98.9%合格，但该样本量相对整个数据集（1000万）来说非常小，其全局代表性有待商榷，可能存在未被发现的噪声。
*   **语言限制**：所有数据和实验都基于英文，模型在其他语言上的泛化能力未知。

（完）
