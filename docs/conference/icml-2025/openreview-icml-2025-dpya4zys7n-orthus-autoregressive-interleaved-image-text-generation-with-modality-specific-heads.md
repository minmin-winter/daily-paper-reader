---
title: "Orthus: Autoregressive Interleaved Image-Text Generation with Modality-Specific Heads"
title_zh: Orthus：基于模态特定头的自回归交错图像-文本生成
authors: "Siqi Kou, Jiachun Jin, Zhihong Liu, Chang Liu, Ye Ma, Jian Jia, Quan Chen, Peng Jiang, Zhijie Deng"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=dPyA4ZYs7n"
tags: ["query:unified-mm"]
score: 8.0
evidence: 统一的模态特定头的交错图像-文本生成多模态模型
tldr: Orthus是一种统一的多模态模型，采用自回归框架与模态特定头：语言模型头预测离散文本令牌，扩散头生成连续图像特征。其连续视觉信号处理减少信息损失，全自回归公式简化模态间相关性建模。通过替换向量量化操作实现高效构建。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1779, \"height\": 300, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1561, \"height\": 581, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1648, \"height\": 1059, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1638, \"height\": 771, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 821, \"height\": 288, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 364, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 364, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 352, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 363, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 363, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 365, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 364, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 363, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 364, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 366, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 365, \"height\": 367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 363, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 366, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 365, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 369, \"height\": 370, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 365, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1594, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dpya4zys7n/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1679, \"height\": 1444, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-dpya4zys7n/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 866, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dpya4zys7n/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1743, \"height\": 687, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dpya4zys7n/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 883, \"height\": 643, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dpya4zys7n/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 905, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dpya4zys7n/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 850, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dpya4zys7n/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1079, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dpya4zys7n/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1051, \"height\": 280, \"label\": \"Table\"}]"
motivation: 现有方法在处理交错图像-文本生成时信息损失大，模态间相关性建模复杂。
method: 采用自回归框架，对文本用语言模型头，对图像用扩散头，连续处理视觉信号。
result: 在交错生成任务中表现优异，信息损失少，模型构建高效。
conclusion: Orthus为统一多模态生成提供了一种有效且高效的架构。
---

## Abstract
We introduce Orthus, a unified multimodal model that excels in generating interleaved images and text from mixed-modality inputs by simultaneously handling discrete text tokens and continuous image features under the \textbf{AR} modeling principle. The continuous treatment of visual signals minimizes the information loss while the fully AR formulation renders the characterization of the correlation between modalities straightforward. Orthus leverages these advantages through its modality-specific heads---one regular language modeling (LM) head predicts discrete text tokens and one diffusion head generates continuous image features. We devise an efficient strategy for building Orthus---by substituting the Vector Quantization (VQ) operation in the existing unified AR model with a soft alternative, introducing a diffusion head, and tuning the added modules to reconstruct images, we can create an Orthus-base model effortlessly (e.g., within 72 A100 GPU hours). Orthus-base can further embrace post-training to craft lengthy interleaved image-text, reflecting the potential for handling intricate real-world tasks. For visual understanding and generation, Orthus achieves a GenEval score of 0.58 and an MME-P score of 1265.8 using 7B parameters, outperforming competing baselines including Show-o and Chameleon.

---

## 论文详细总结（自动生成）

好的，作为您的资深学术论文分析助手，我将根据您提供的论文内容，按照您的要求生成一份详细、客观的中文总结。

---

### 论文概述与深入分析

#### 1. 核心问题与整体含义（研究动机和背景）

*   **核心问题**：现有统一多模态模型（统一处理图像理解和生成）存在两大缺陷。一是**信息损失**问题：如Chameleon等全自回归模型，使用矢量量化（VQ）将图像转换为离散token，导致高频细节丢失。二是**噪声干扰**问题：如Transfusion等混合模型，在图像上应用扩散过程，需要向模型输入噪声图像，这破坏了模型对清晰图像的理解，给图文交错生成带来困难。
*   **整体含义**：该论文旨在设计一种新型的统一多模态模型，能够同时进行交错图像-文本的生成，仅通过一个紧凑模型实现，避免上述两种方法的缺陷，从而提升性能并简化模型设计。

#### 2. 论文提出的方法论

*   **核心思想**：提出Orthus模型，在**全自回归（AR）框架**下统一处理离散文本和连续图像。模型通过**模态特定头（Modality-Specific Heads）** 进行输出：一个标准的语言模型（LM）头用于预测下一个离散文本token；一个**扩散头（Diffusion Head）** 用于生成连续的图像特征。这种设计避免了VQ的信息损失和混合模型中噪声对图像理解的干扰。
*   **关键技术细节**：
    1.  **连续视觉信号处理**：使用预训练的变分自编码器（VAE）编码器将图像转换为连续的块级特征，而非VQ的离散token。
    2.  **可微分的视觉嵌入模块**：为了从已有的全AR模型（如Chameleon）高效构建Orthus，作者将原有的硬argmin VQ操作替换为一个**软替代（soft alternative）**，即基于温度的softmax加权求和。这使得原本离散的嵌入过程变得可微，允许模型通过梯度更新码本，更好地适应多模态学习任务。
    3.  **扩散头**：一个浅层的MLP，包含自适应层归一化（AdaLN），用于根据条件向量（Transformer backbone输出）和时间步进行噪声预测，从而生成图像特征。
    4.  **训练与推理流程**：
        *   **训练**：输入序列为连续图像特征和离散文本token的混合。Transformer backbone使用因果注意力处理。输出向量路由到对应模态的头：文本部分计算自回归损失（交叉熵），图像部分计算扩散损失（L2损失）。
        *   **推理**：模型以自回归方式依次预测下一个元素。当预测到`[BOI]`（Begin of Image）特殊token时，切换到“下一patch预测”模式，使用扩散头生成一个固定数量的图像patch。生成完毕后，插入`[EOI]`（End of Image）token，并切换回文本token预测模式。

#### 3. 实验设计

*   **数据集与场景**：
    *   **基础模型构建**：使用LAION-COCO-Aesthetic数据集中的10k张高质量图像。
    *   **交错图文下游任务**：
        *   **图像编辑**：使用Instruct-Pix2Pix数据集。
        *   **故事书生成**：使用StoryStream数据集。
    *   **视觉理解与生成**：使用LLaVA-v1.5-665K、JourneyDB、LAION-COCO-Aesthetic（由ShareGPT-4v重新生成描述）等数据的混合集。
*   **Benchmark**：
    *   **视觉理解**：POPE（物体幻觉）、MME-P（多模态评估）、VQAv2、GQA（场景图问答）、MMMU（多模态理解）。
    *   **图像生成**：GenEval（文本-图像对齐）、HPSv2（人类偏好评分）。
    *   **图像编辑**：CLIP相似度（-T: 文本指令对齐，-I: 图像保真度，-D: 图像整体结构一致性）。
*   **对比方法**：
    *   **统一模型**：Chameleon（7B，完全自回归）、Show-o（1.3B）、LWM（7B）、Transfusion、Emu3-Chat/Gen等。
    *   **专用模型**：LLaVA-v1.5、InstructBLIP（视觉理解）、SDXL、DALL-E 2（图像生成）、Instruct-Pix2Pix（图像编辑）。

#### 4. 资源与算力

*   **论文明确提及**：
    *   使用**8块 NVIDIA A100 80GB GPU**。
    *   **构建Orthus基础模型（Orthus-base）**：仅需**72 GPU小时（9小时训练）**。
    *   **指令微调**：默认设置下进行35,000步训练（具体GPU时长未明确，但可推测在8卡A100上耗时数天）。
*   **总结**：算力需求公开透明，且构建成本非常低，是本文的一大亮点。

#### 5. 实验数量与充分性

*   **实验数量**：较为充分。包括：
    1.  **主实验**：在视觉理解（5个benchmark）和图像生成（2个benchmark）上与多种SOTA方法进行了定量对比。
    2.  **消融实验**：
        *   单独训练（理解/生成）vs 统一训练。
        *   不同视觉嵌入模块（softmax, argmin, linear layer）的影响。
        *   扩散损失 vs MSE损失的对比（见附录）。
    3.  **下游任务评估**：图像编辑（定量+定性）、故事书生成（定性）。
    4.  **定性展示**：展示了大量图像生成、编辑、理解和故事生成的案例。
*   **公平性**：论文比较了多个基线的公开结果。特别地，为公平对比，论文将自己的模型与同一数据集后训练的Chameleon（标记为†）做了比较。消融实验中对不同组件的控制也较为严谨。因此，实验设计总体是客观、公平的。

#### 6. 论文的主要结论与发现

*   **方法有效性**：Orthus作为一种统一模型，在多项视觉理解和生成基准上优于或媲美了Chameleon、Show-o等竞品，以及部分专用模型（如SDXL）。这证明其“连续特征+全AR+扩散头”的设计是高效且有效的。
*   **交错生成能力**：在图像编辑和故事书生成等复杂交错任务中，Orthus不仅表现出色，还展现了零样本泛化和上下文学习能力。
*   **统一训练优于分离训练**：消融实验表明，同时进行理解和生成任务的统一训练，比单独训练各项任务效果更好，证明了跨模态学习的协同增益。
*   **高效构建策略的成功**：通过“软替代VQ”和仅微调新模块的方法，能够以极低的成本（72 A100 GPU小时）从Chameleon构建出强大的Orthus-base，验证了其构建策略的实用性和高效性。

#### 7. 优点

1.  **方法设计的创新性**：巧妙地结合了全自回归和扩散模型的优点，避免了VQ的信息损失和混合模型中噪声干扰的缺点，实现了两者的“取其精华，去其糟粕”。
2.  **极高的构建效率**：提出了一种从现有模型高效迁移的策略，极大地降低了从头训练巨大多模态模型的门槛和成本（72 GPU小时），展示了极强的实用性。
3.  **强大的交错生成能力**：模型在需要长期依赖和模态间一致性的复杂任务（如图像编辑和长故事生成）上表现出色，验证了其作为基础多模态模型的潜力。
4.  **全面的实验验证**：不仅在标准理解/生成任务上做了定量评估，还在复杂的交错生成任务上做了定性展示，实验覆盖全面，说服力强。

#### 8. 不足与局限

1.  **推理延迟**：论文明确指出，由于生成图像需要多次通过扩散头（DDIM 100步），带来了较高的推理延迟。这是该方法的固有代价。
2.  **模型规模受限**：受限于计算资源，实验仅局限于7B参数规模的模型。论文指出，未来可以通过扩大参数和数据规模来进一步提升性能，暗示了当前结果的提升空间。
3.  **图像分辨率有限**：所有图像生成均在512x512分辨率下进行，与一些高分辨率图像生成模型（如SDXL的1024x1024）相比尚有差距。
4.  **对VQ模型的依赖**：构建策略依赖于Chameleon等已有模型的预训练权重。尽管构建成本低，但初始模型的选择和其预训练数据的质量会直接影响Orthus-base的性能。如果初始模型性能不佳，其上界也可能受限。

（完）
