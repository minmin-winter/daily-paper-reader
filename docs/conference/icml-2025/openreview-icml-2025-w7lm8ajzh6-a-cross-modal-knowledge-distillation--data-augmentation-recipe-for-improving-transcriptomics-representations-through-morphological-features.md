---
title: "A Cross Modal Knowledge Distillation & Data Augmentation Recipe for Improving Transcriptomics Representations through Morphological Features"
title_zh: 跨模态知识蒸馏与数据增强：利用形态学特征改进转录组表征
authors: "Ihab Bendidi, Yassir El Mesbahi, Alisandra Kaye Denton, Karush Suri, Kian Kenyon-Dean, Auguste Genovesio, Emmanuel Noutahi"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=w7lm8AjzH6"
tags: ["query:unified-mm"]
score: 6.0
evidence: 从显微镜图像到转录组的跨模态知识蒸馏
tldr: 为克服弱配对多模态数据稀缺问题并增强转录组表征，本文提出跨模态知识蒸馏与数据增强框架。利用弱配对的显微镜图像与转录组数据，通过跨模态对齐和绑定，将形态学知识注入基因表达表示中。引入数据增强策略缓解样本不足。实验表明，该方法有效提升了转录组表征在下游任务中的性能，弥合了转录组与形态学之间的信息鸿沟。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-w7lm8ajzh6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 855, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-w7lm8ajzh6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1773, \"height\": 872, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-w7lm8ajzh6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-w7lm8ajzh6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 794, \"height\": 841, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-w7lm8ajzh6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1725, \"height\": 1010, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-w7lm8ajzh6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1730, \"height\": 1034, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-w7lm8ajzh6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1774, \"height\": 534, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-w7lm8ajzh6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 868, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-w7lm8ajzh6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1741, \"height\": 292, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-w7lm8ajzh6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1773, \"height\": 1026, \"label\": \"Table\"}]"
motivation: 弱配对的多模态组学数据稀少，且图像模态信息未被有效利用以增强转录组表示。
method: 提出跨模态知识蒸馏框架，通过对齐和绑定弱配对的图像与转录组数据，并引入数据增强。
result: 增强后的转录组表示在下游生物学任务中优于基线，验证了跨模态知识迁移的有效性。
conclusion: 跨模态蒸馏是提升单模态表征的有效途径，尤其适用于数据稀缺的生物医学场景。
---

## Abstract
Understanding cellular responses to stimuli is crucial for biological discovery and drug development. Transcriptomics provides interpretable, gene-level insights, while microscopy imaging offers rich predictive features but is harder to interpret. Weakly paired datasets, where samples share biological states, enable multimodal learning but are scarce, limiting their utility for training and multimodal inference. We propose a framework to enhance transcriptomics by distilling knowledge from microscopy images. Using weakly paired data, our method aligns and binds modalities, enriching gene expression representations with morphological information. To address data scarcity, we introduce (1) *Semi-Clipped*, an adaptation of CLIP for cross-modal distillation using pretrained foundation models, achieving state-of-the-art results, and (2) *PEA* (**P**erturbation **E**mbedding **A**ugmentation), a novel augmentation technique that enhances transcriptomics data while preserving inherent biological information. These strategies improve the predictive power and retain the interpretability of transcriptomics, enabling rich unimodal representations for complex biological tasks.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：理解细胞对刺激的应答是生物发现和药物开发的基础。转录组学（transcriptomics）提供可解释的、基因层面的洞察，而显微镜成像（microscopy imaging）虽富含预测性特征但难以解释。理想的解决方案是结合两种模态，但**完全配对**的数据（同一样本的两种模态）由于实验成本和技术挑战几乎不可行。因此，研究利用**弱配对数据**（weakly paired data：来自不同实验但共享相同细胞系和扰动元数据的转录组和成像样本）进行多模态学习。
- **核心问题**：弱配对多模态数据集本身也非常稀缺，限制了模型训练和推理时的多模态融合。如何利用有限的弱配对数据，将显微镜图像中的形态学知识迁移到转录组表征中，从而在不牺牲转录组可解释性的前提下提升其预测能力？
- **整体含义**：本文提出一个跨模态知识蒸馏与数据增强的框架，旨在通过训练一个转录组适配器，将冻结的显微镜图像编码器产生的特征空间通过对比学习对齐，同时引入一种新颖的生物学启发式数据增强方法（PEA），以缓解数据稀缺问题。最终实现：推理时仅需转录组数据，却包含形态学信息，获得更强的生物学关系检索能力和保持可解释性。

## 2. 方法论

### 核心思想
采用**冻结的预训练单模态编码器**（教师：Phenom-1 显微镜图像编码器；学生：转录组编码器如 scVI、scGPT 或简单的 MLP），训练一个轻量级适配器（adapter）将学生嵌入映射到教师嵌入空间，使用对比学习目标（CLIP loss）进行知识蒸馏。为了避免耦合和退化，教师嵌入完全冻结，仅更新学生适配器。同时，为了应对数据稀缺，设计一种基于批校正（batch correction）的随机增广方法 PEA，在训练时对转录组嵌入施加可控的分布偏移，增强鲁棒性。

### 关键技术细节
- **Semi-Clipped**：一种改进的 CLIP 损失变体。教师模态（图像）使用预训练冻结模型提取嵌入；学生模态（转录组）也使用预训练冻结模型提取嵌入，但经过一个可训练的适配器 MLP（三层，ReLU 激活）。目标是最小化配对样本的对比损失（InfoNCE）。关键点：仅训练学生适配器，教师完全固定，避免相互漂移；采用温度 τ=0.1。
- **PEA（Perturbation Embedding Augmentation）**：将传统批校正技术重新用作训练时数据增广。每个样本随机从一组校正方法（居中、缩放、基于主成分的典型变异归一化 TVN 等）中选取一种，并随机丢弃部分的步骤，随机选取用于校正的对照样本数量，从而引入多样性。在推理时，使用固定批校正对齐到训练分布。
- **训练流程**（Algorithm 1）：对每个批次，提取学生和教师嵌入；从变换集合 A 中采样一个校正函数 A'（随机丢弃部分步骤和随机控制样本数）；应用到学生嵌入得到 zaₛ；通过适配器计算 hₛ = fₛ(zaₛ)；对教师嵌入应用 TVN 校正得到 zbₜ；计算 CLIP 损失并反向传播更新适配器。

### 算法流程（文字说明）
1. 使用冻结图像编码器 Eₜ 和转录组编码器 Eₛ 提取嵌入。
2. 从预定义的批校正变换集合中随机选择一个函数 A（包含居中、缩放、TVN 等步骤），并随机丢弃该函数的部分步骤，随机选取部分对照样本。
3. 应用该随机变换到学生嵌入，得到增广嵌入 zaₛ。
4. 用适配器 fₛ 映射得到 hₛ。
5. 对教师嵌入应用固定的 TVN（B）得到 zbₜ。
6. 计算对比损失（InfoNCE），只更新适配器 fₛ。

## 3. 实验设计

### 数据集
- **训练数据集**：130,000 个阵列式批量转录组样本（HUVEC-CMPD，化学扰动，1,700 种化合物，每种 3 个浓度）和 20,000 张 HUVEC 细胞显微镜图像（Cell Painting）。弱配对：基于细胞系和扰动元数据配对。
- **评估数据集**（三个 OOD 移位场景）：
  - **HUVEC-KO**：120,000 个批量转录组样本，约 300 个 CRISPR 基因敲除，不同实验批次，评估对未见过实验和遗传扰动的泛化。
  - **LINCS**：443,000 个批量转录组样本（L1000 检测方法，不同于训练集测序方法），31 种细胞类型，5,157 个 CRISPR KO。
  - **SC-RPE1**：247,914 个单细胞转录组样本（Retinal Pigmented Epithelium 细胞），2,393 个 CRISPR KO，评估从批量向单细胞的迁移。

### 基准方法
- **比较的蒸馏方法**：KD、SHAKE、C2KD（标签监督方法），以及 CLIP、SigClip、VICReg、DCCA（无标签对齐方法）。所有方法使用相同的预训练编码器和可训练适配器。
- **比较的数据增强方法**：MWO、scVI denoising、MDWGAN-GP、scGFT，以及它们的组合和与 PEA 组合。
- **基线**：随机基线、单模态转录组基线（不进行蒸馏）。

### 评估任务
- **已知生物学关系检索（Known Biological Relationship Recall）**：通过基因嵌入的余弦相似度，检索前 5% 的关系，与 CORUM、HuMAP、StringDB、Reactome、SIGNOR 五个数据库的注释比较，取平均召回率。
- **转录组可解释性保持（Transcriptomic Interpretability Preservation）**：结合结构完整性分数（Structural Integrity）和斯皮尔曼相关性（Spearman correlation），评估重建原始表达谱的能力和控制-扰动关系的保持。

## 4. 资源与算力

- 文中提到：在 **130,000 个弱配对样本** 的版本上，使用 **单个 H100 GPU** 训练适配器约需 **19 小时**。此外，还提到一个 **1.3M 样本** 的扩展版本（但未给出详细训练时间）。所有实验均基于该设置，未明确提及使用的 GPU 数量（推测为单卡或多卡但未具体说明）。

## 5. 实验数量与充分性

- **实验数量**：大量实验覆盖三个 OOD 数据集、多种蒸馏方法、多种数据增强方法、消融研究（超参数、PEA 组件、适配器训练策略等）。主要图表包括：
  - Figure 1：不同训练选择（从头训练 vs 预训练+适配器）的比较。
  - Figure 2(a)：7 种蒸馏方法在 3 个数据集上的 z-score 对比（每个方法5个种子）。
  - Figure 2(b)：数据增广对比（每个设置5个种子）。
  - Figure 3：超参数消融（学习率、温度、batch size、epoch）。
  - Table 1：4 种蒸馏方法 ± PEA 在 15 个种子上的统计比较（Wilcoxon 检验）。
  - Table 2：PEA 组件消融（15个种子）。
  - Figure 4：韦恩图分析不同方法检索的关系重叠。
- **充分性**：实验设计较为全面：多种 OOD 场景、多个种子、统计显著性检验。消融实验覆盖了核心组件。比较的方法多样且公平（使用相同编码器和适配器设置）。还分析了生物学通路富集等定性分析。不足之处：仅测试了 HUVEC 细胞系（训练集）和几种 OOD 细胞类型（LINCS 包含 31 种，但主要来自其他来源），没有覆盖更多组织类型或疾病模型；仅使用一种图像预训练模型（Phenom-1），未比较其他显微镜编码器。

## 6. 主要结论与发现

- **Semi-Clipped 的有效性**：使用冻结的预训练编码器并只训练适配器，显著优于从头训练或微调整个编码器；与其它蒸馏方法相比，Semi-Clipped 在三个 OOD 数据集上均取得最高的已知关系检索召回率，同时保持与单模态基线相当的可解释性。
- **PEA 的卓越性能**：单独使用 PEA 即可大幅提升关系检索（HUVEC-KO +17%，LINCS +55%，SC-RPE1 +20%），且优于所有现有转录组数据增广方法；与其它增广结合时进一步提升（+25%，+69%，+26%）。PEA 在所有蒸馏方法上均有一致显著提升（p<0.05）。
- **无监督对齐优于标签监督**：基于标签的蒸馏方法（KD、SHAKE、C2KD）在大多数 OOD 场景下表现不如无标签对齐方法（如 Semi-Clipped、VICReg），说明弱标签不足以捕获复杂生物学。
- **协同效应**：Semi-Clipped 不仅保留转录组特有的关系，还能整合图像模态独特的信息，并发现单个模态无法发现的通路（如细胞周期检查点、翻译后修饰），产生“1+1>2”的生物学见解。

## 7. 优点

- **方法创新性**：
  - 将预训练大模型和适配器策略应用于跨模态知识蒸馏，适应数据稀缺的生物学场景。
  - 重新定义批校正作为数据增广，引入随机性，增强鲁棒性且保持生物学意义。
- **实用性**：推理时仅需转录组，却从图像中获益，可大规模部署。
- **实验严谨性**：多种子统计检验、多个 OOD 数据集、消融实验详细。
- **跨模态理解**：通过通路富集证明了蒸馏产生的协同效应，超越简单加和。

## 8. 不足与局限

- **配对策略粗糙**：在训练时，随机从同一治疗/浓度组中选择一个图像-转录组对，当组内存在微妙差异时可能稀释表示质量。需要更好的匹配策略。
- **依赖特定预训练模型**：仅用了 Phenom-1 和 scVI/scGPT，未探索其他图像/转录组编码器的通用性。
- **有限的数据规模和细胞类型**：训练集仅一种细胞系（HUVEC），评估仅涉及少量细胞系。虽然 LINCS 包含 31 种，但仍有偏。未能验证在更广泛组织或疾病中的应用。
- **未考虑多模态融合推理**：本文目标是仅使用转录组推理，未探索如果两种模态同时可用时是否可以获得更好性能。
- **计算资源报告不够详细**：仅给出一个训练时间（19小时），未说明多卡并行情况、总 GPU 时数等。
- **增广方法依赖批对照样本**：要求每个批次至少有两个对照样本，这在实际某些实验设计中可能不满足。

（完）
