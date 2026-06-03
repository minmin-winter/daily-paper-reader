---
title: "DS-VLM: Diffusion Supervision Vision Language Model"
title_zh: DS-VLM：扩散监督视觉语言模型
authors: "Zhen Sun, Yunhang Shen, Jie Li, Xing Sun, Pingyang Dai, Liujuan Cao, Rongrong Ji"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=NEBa0bs5LR"
tags: ["query:native-multi"]
score: 7.0
evidence: 基于扩散的直接监督用于视觉-语言对齐
tldr: DS-VLM提出一种即插即用的扩散监督框架，通过重建输入图像建立从像素空间到视觉特征的短路径梯度传播，同时保持高层语义对齐。该方法有效缓解了视觉表示学习中的监督退化和文本语义稀疏问题。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-neba0bs5lr/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 770, \"height\": 324, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-neba0bs5lr/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 789, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-neba0bs5lr/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1775, \"height\": 506, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-neba0bs5lr/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1328, \"height\": 841, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-neba0bs5lr/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 858, \"height\": 624, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-neba0bs5lr/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 841, \"height\": 546, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1769, \"height\": 667, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1767, \"height\": 507, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1763, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 803, \"height\": 184, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 801, \"height\": 139, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 802, \"height\": 133, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1764, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-neba0bs5lr/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1222, \"height\": 192, \"label\": \"Table\"}]"
motivation: 视觉语言模型面临梯度传播导致的信息损失和文本监督语义稀疏的问题。
method: 以视觉编码器和连接器的输出为条件重建输入图像，建立像素到特征的短路径梯度通道。
result: 在保持高层语义对齐的同时增强了视觉特征表示，改善了跨模态对齐质量。
conclusion: 扩散直接监督是一种有效的视觉语言对齐增强策略。
---

## Abstract
Vision-Language Models (VLMs) face two critical limitations in visual representation learning: degraded supervision due to information loss during gradient propagation, and the inherent semantic sparsity of textual supervision compared to visual data. We propose the Diffusion Supervision Vision-Language Model (DS-VLM), a plug-and-play framework that introduces diffusion-based direct supervision for vision-language alignment. By reconstructing input images through a diffusion model conditioned on outputs of the visual encoder and the connector, our method establishes a short-path gradient propagation channel from pixel space to visual features. This approach simultaneously preserves high-level semantic alignment through conventional text supervision while enhancing visual feature quality via pixel-level reconstruction constraints. Extensive experiments conducted across various visual encoders and LLMs of different scales demonstrate the effectiveness of our approach.

---

## 论文详细总结（自动生成）

# DS-VLM：扩散监督视觉语言模型（详细中文总结）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有视觉语言模型（VLM）在视觉表示学习中面临两大限制：一是梯度传播路径过长（经过大语言模型导致信息损失），二是文本监督信号固有的语义稀疏性，无法充分捕捉图像中的丰富细节（如空间结构、复杂语义）。
- **研究动机**：希望利用图像本身的像素级信息，通过一条更短的梯度传播路径直接监督视觉编码器和连接器，同时保留高层语义对齐，从而提升视觉特征质量。
- **整体含义**：提出一种即插即用的扩散监督框架（DS-VLM），通过扩散模型以视觉编码器和连接器的输出为条件重建输入图像，建立从像素空间到视觉特征的短路径梯度通道，增强跨模态对齐质量。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

### 核心思想
- 在训练阶段引入一个预训练的扩散模型（基于Stable Diffusion），以视觉编码器的多层级特征（低、中、高层）和连接器的输出特征作为条件，重建原始图像。通过重建损失优化视觉编码器和连接器，使得梯度绕过LLM，直接传播到这两个组件，缩短知识传播链，并利用图像本身的丰富语义。

### 关键技术细节
- **监督特征**：
  - 图像监督特征：从视觉编码器的第8、16、24层提取低、中、高层特征。
  - 文本监督特征：连接器输出的特征（已映射到文本嵌入空间）。
- **多适配器扩散模型（Multi-Adapter Diffusion）**：
  - 基于Stable Diffusion的UNet架构，为每个监督特征设计独立的交叉注意力层（通过MOE交叉注意力机制合并）。
  - MOE交叉注意力：将文本交叉注意力与三个图像交叉注意力（对应低、中、高层）的输出通过可学习的路由权重加权求和，公式如下：
    ```
    P = Softmax(Pooling(Q·Wr))
    Znew = P0 * Z' + Σ Pi * Z''_i   (i=1..3)
    ```
- **训练目标**：
  - 原LLaVA的下一词预测损失（保留高层语义对齐）。
  - 加上扩散模型的重建损失（本文采用感知损失PL，消融实验对比了MAE和SSIM）。
- **整体流程**：
  1. 输入图像通过视觉编码器→连接器→LLM得到文本损失。
  2. 同时，视觉编码器的低、中、高层特征和连接器输出特征分别送入多适配器扩散模型，该模型以这些特征为条件去噪生成图像。
  3. 计算生成图像与原图的感知损失，梯度通过扩散模型反向传播至视觉编码器和连接器（跳过LLM）。
- **推理阶段**：扩散模型可移除，不增加推理参数量和计算开销。

## 3. 实验设计：数据集、基准、对比方法

### 数据集
- **预训练数据**：LLaVA-1.5开源数据集（558K图像描述用于预训练，665K指令微调数据）。
- **额外扩展**：使用Mini-Gemini数据集（1.2M + 1.5M）验证大规模训练效果。
- **评估基准**（10个）：MMBench (MMB)、MMStar (MMS)、MMMU、MathVista (MV)、OCRBench (OCRB)、AI2D、HallusionBench (HB)、LLaVABench (LB)、ScienceQA (SQA)、MME。

### 对比方法
- **基线**：LLaVA-1.5（不同配置：Vicuna-7B/13B，CLIP-L/SigLIP-SO）。
- **SOTA方法**：MiniGPT4、Qwen-VL、VisualGLM、PandaGPT、mPLUG-Owl2、Emu2-chat、Yi-VL、ShareGPT-4V等。

### 实验设置
- **视觉编码器**：CLIP-ViT-L/14-336px 或 SigLIP-SO400m-patch14-384。
- **LLM**：Vicuna-7B/13B，以及Llama3-8B、Qwen2-7B。
- **训练参数**：预训练阶段学习率1e-3，指令微调2e-5；batch size 256/128；LoRA rank=8；扩散模型迭代步数50。

## 4. 资源与算力

- **论文未明确说明**使用的GPU型号、数量及训练时长。仅提及使用PyTorch框架，但未提供具体算力信息。推测采用了常见的8×A100或类似配置进行训练，但无确切依据。

## 5. 实验数量与充分性

### 实验数量
- **主表**（Table 1）：在多种配置（不同LLM、视觉编码器、数据规模）下与基线对比，共10个基准。
- **SOTA对比**（Table 2）：与8种方法对比，覆盖多个基准。
- **消融实验**（4组）：
  1. 监督特征类型（文本监督+多层级图像监督）——5种组合。
  2. 重建损失类型（MAE vs SSIM vs 感知损失）——3种。
  3. 交叉注意力机制（共享 vs 独立MOE）——2种。
  4. 适配器结构（线性适配器 vs Q-Former）——2种。
- **附录补充**：
  - 可训练视觉编码器下的对比（Table 7）。
  - 验证视觉编码器在训练中的关键作用（通过冻结编码器只训练适配器，对比重构损失，Table 8）。
- **定性可视化**：扩散模型去噪过程展示。

### 充分性和公平性
- **充分**：覆盖了主流视觉编码器和多种LLM，验证了方法在不同架构下的泛化性；消融实验系统分析了各组件的贡献；与SOTA方法对比时保持了公平的数据量（均基于LLaVA-1.5设置）。
- **客观**：使用公开数据集和标准评估工具，结果可复现。
- **局限性**：所有实验仅在LLaVA-1.5框架及其衍生配置上进行，未在其他VLM架构（如BLIP-2、MiniGPT-4的原始实现）上测试，泛化性有待进一步验证。

## 6. 论文的主要结论与发现

1. **DS-VLM显著提升基础性能**：在LLaVA-1.5基础上，平均提高1.4%（7B）和1%（13B），尤其在高难度推理（MMMU）、细粒度对齐（MMStar）和幻觉抑制（HallusionBench）上表现突出。
2. **即插即用且无推理开销**：训练时引入扩散模型，推理时可移除，不增加参数量和计算成本。
3. **多层级监督互补**：文本监督与图像低、中、高层特征叠加最佳，单一维度的监督效果有限。
4. **感知损失最优**：相比MAE和SSIM，感知损失能更好地保留语义和结构信息。
5. **独立交叉注意力优于共享**：MOE机制有效减少模态干扰，提升特征融合质量。
6. **线性适配器优于Q-Former**：更简洁的结构反而带来更好效果，说明参数效率与性能可兼得。
7. **与SOTA相当或更优**：即使使用更少数据，DS-VLM在多个基准上达到甚至超越此前最先进模型。

## 7. 优点：方法或实验设计上的亮点

- **创新性**：首次将扩散模型用于直接监督视觉编码器和连接器，通过重建任务提供像素级梯度信号，巧妙解决长路径梯度消失和文本语义稀疏问题。
- **通用性**：验证了方法在多种视觉编码器（CLIP, SigLIP）和LLM（Vicuna, Llama3, Qwen2）下的有效性，适用性强。
- **高效性**：推理阶段无额外开销，训练阶段引入的扩散模型可通过LoRA等方式轻量化。
- **实验设计严谨**：消融实验覆盖关键组件（监督特征、损失函数、注意力机制、适配器结构），并验证了视觉编码器参与训练的必要性（附录B），排除了“适配器主导”的质疑。
- **可视化分析**：定性展示了扩散模型逐步重建图像的效果，直观验证了监督特征携带的语义信息。

## 8. 不足与局限

- **实验覆盖范围有限**：所有实验均在LLaVA-1.5变体上进行，未在其他主流VLM框架（如BLIP-2、InstructBLIP、Flamingo）上验证，泛化性存疑。
- **资源算力不透明**：未提供训练所需GPU型号、数量及时长，难以评估实际部署成本。
- **潜在偏差风险**：依赖预训练的Stable Diffusion模型，其生成质量可能受限于训练数据分布（如照片级图像），对医学、工程等专业领域图像的重建保真度未评估。
- **应用限制**：训练阶段需要额外的扩散模型和前向/反向传播，增加了训练时间和内存消耗（尽管可通过采样步数如50步控制）。对于算力有限的场景可能不友好。
- **仅针对视觉表示学习**：方法未直接优化LLM的语义理解部分，文本侧依然依赖原始LLaVA损失，可能限制跨模态交互的潜力。
- **未讨论扩散模型的潜在生成误差**：如果重构图像与原始图像差异较大（如风格偏移），可能引入噪声监督，论文未对此进行分析。

（完）
