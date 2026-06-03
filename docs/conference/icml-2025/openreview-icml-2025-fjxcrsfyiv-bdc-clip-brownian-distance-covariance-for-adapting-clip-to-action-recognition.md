---
title: "BDC-CLIP: Brownian Distance Covariance for Adapting CLIP to Action Recognition"
title_zh: BDC-CLIP：布朗距离协方差用于适配CLIP进行动作识别
authors: "Fei Long, Xiaoou Li, Jiaming Lv, Haoyuan Yang, Xianjun Cheng, Peihua Li"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=fjXcRSfyIV"
tags: ["query:unified-mm"]
score: 5.0
evidence: 使用布朗距离协方差改进视频-语言对齐用于动作识别
tldr: 现有CLIP视频动作识别方法依赖余弦相似度，难以建模复杂依赖关系且忽略局部时空线索。BDC-CLIP引入布朗距离协方差度量视频与语言表示的相关性，能够捕捉更丰富的依赖关系。在多个动作识别数据集上显著优于余弦相似度方法。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-fjxcrsfyiv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 838, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fjxcrsfyiv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1233, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fjxcrsfyiv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 826, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fjxcrsfyiv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1413, \"height\": 1164, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fjxcrsfyiv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1388, \"height\": 827, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fjxcrsfyiv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 819, \"height\": 826, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fjxcrsfyiv/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1583, \"height\": 1994, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 832, \"height\": 699, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1276, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 960, \"height\": 395, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 765, \"height\": 390, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 688, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 789, \"height\": 1170, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 858, \"height\": 617, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1267, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1242, \"height\": 411, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fjxcrsfyiv/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1768, \"height\": 308, \"label\": \"Table\"}]"
motivation: 基于余弦相似度的视频-语言对齐无法捕捉复杂依赖和局部时空线索。
method: 用布朗距离协方差替代余弦相似度进行视频-语言表示对齐。
result: 在动作识别任务上超越现有方法，验证了布朗距离协方差的有效性。
conclusion: 布朗距离协方差是一种更强大的多模态对齐度量，可应用于视频理解。
---

## Abstract
Bridging contrastive language-image pre-training (CLIP) to video action recognition has attracted growing interest. Human actions are inherently rich in spatial and temporal contexts, involving dynamic interactions among people, objects, and the environment. Accurately recognizing actions requires effectively capturing these fine-grained elements and modeling their relationships with language. However, most existing methods rely on cosine similarity--practically equivalent to the Pearson correlation coefficient--between global tokens for video-language alignment. As a result, they have limited capacity to model complex dependencies and tend to overlook local tokens that encode critical spatio-temporal cues. To overcome these limitations, we propose BDC-CLIP, a novel framework that leverages Brownian Distance Covariance (BDC) to align visual and textual representations. Our method can capture complex relationships--both linear and nonlinear--between all visual and textual tokens, enabling fine-grained modeling in space, time, and language. BDC-CLIP achieves state-of-the-art performance across zero-shot, few-shot, base-to-novel, and fully supervised action recognition settings, demonstrating its effectiveness and broad applicability.

---

## 论文详细总结（自动生成）

# 论文中文总结：BDC-CLIP：布朗距离协方差用于适配CLIP进行动作识别

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：现有将CLIP适配到视频动作识别的方法主要依赖**余弦相似度**（等价于皮尔逊相关系数）对齐视频与语言表示。余弦相似度只能捕捉**线性关系**，且通常仅使用**全局token**（如视频的[CLS] token和文本的[EOS] token），忽略了**局部token**（如patch tokens和word tokens）蕴含的细粒度时空语义线索。这导致模型难以建模视频与语言之间的复杂非线性依赖关系，限制了动作识别的精度。
- **意义**：人类动作涉及人、物体和环境在时空上的动态交互，需要捕捉精细元素并建模跨模态关系。作者提出基于**布朗距离协方差（Brownian Distance Covariance, BDC）** 的对齐框架，突破余弦相似度的局限，实现更丰富的多模态对齐。

## 2. 方法论：核心思想、关键技术细节
### 核心思想
- 用**BDC**替代余弦相似度作为视频与语言表示的匹配度量。BDC能同时捕捉线性和非线性相关性，且天然适用于**集合级**嵌入（即所有视觉token和所有文本token），从而利用局部token中的细粒度信息。
### 关键技术细节
- **视频BDC适配器**：
  1. 对每帧的视觉token（[CLS] + patch tokens）进行**维度降低**（线性层+层归一化）。
  2. **Token加权**：根据每个patch token与[CLS] token的余弦相似度分配权重。
  3. 输出来帧级**BDC矩阵**（通过`Bdc9M`函数计算），并对其进行半向量化得到紧凑向量。
  4. **时间注意力**：将帧级的[CLS] token作为查询（Q）和键（K），帧级BDC向量作为值（V），通过注意力机制聚合帧间关系。
  5. 最终平均池化得到视频级BDC表示。
- **文本BDC适配器**：
  1. 对文本token（[EOS] + word tokens）进行维度降低和token加权。
  2. 直接计算BDC矩阵作为文本表示（无时间注意力）。
- **跨模态对齐**：使用**布朗距离相关性（Brownian Distance Correlation, BDCorr）** 度量视频与文本BDC矩阵的相似度，其值在[0,1]之间，对正交、平移和缩放变换不变。
- **训练目标**：联合优化三个损失：
  - **VL-Ctr adapter**：基于BDCorr的对比损失。
  - **V-Cls adapter**：视觉BDC表示通过全连接层进行分类的交叉熵损失。
  - **VL-Ctr backbone**：保留CLIP原始主干网络的余弦相似度对比损失（用于维持泛化性）。
- **文本增强**：使用LLM（GPT-4o）为每个类别生成描述句子（提示：“Describe the action of {category name} in a video.”）。

## 3. 实验设计：数据集、Benchmark、对比方法
- **数据集**：Kinetics-400 (K400)、Kinetics-600 (K600)、HMDB-51、UCF-101、Something-Something v2 (SSv2)。
- **任务设置**：包括**零样本**、**少样本**（2/4/8/16-shot）、**基类到新类泛化**（base-to-novel generalization）以及**全监督**（closed-set）动作识别。
- **对比方法**：A5, Vita-CLIP, DiST, MoTED, ActionCLIP, X-CLIP, ViFi-CLIP, TC-CLIP, OST, FROSTER, Open-VCLIP, MAXI, ALT等。大部分方法使用ViT-B/16作为视觉编码器。
- **评估指标**：Top-1准确率（主要），部分报告Top-5。零样本任务报告均值±标准差，少样本任务报告多次实验均值。

## 4. 资源与算力
- **GPU型号**：全部实验使用**NVIDIA GeForce RTX 4090** GPU。
- **数量与时长**：文中**未明确说明**实验使用的GPU数量以及具体训练时长。仅提及“All experiments are conducted using GeForce RTX 4090 GPUs with the PyTorch framework.”。不过附录A.3给出了具体超参数（如epoch、batch size、学习率等），可推测训练时间在合理范围内。
- **计算成本分析**：作者比较了参数量、GFLOPS和吞吐量，BDC-CLIP相比ViFi-CLIP参数增加约2%~6%，GFLOPS增加11%，吞吐量降至80%，但优于TC-CLIP等竞争者（如TC-CLIP吞吐量仅33 views/s vs BDC-CLIP的37 views/s）。因此计算开销适度。

## 5. 实验数量与充分性
- **实验数量**：非常丰富。涵盖5个数据集，4类任务（零样本、少样本、基到新、全监督），多组shot数（2/4/8/16）。此外还进行了**多组消融实验**：
  - 组件分析（BDC对齐、BDC视觉分类）
  - 度量与表示对比（BDC vs 余弦相似度 vs Frobenius距离）
  - 维度大小影响（128~384）
  - 文本增强（手工模板 vs LLM生成）
  - token比例、视觉/文本BDC分支、token加权
  - 额外在图像少样本任务上验证（11个数据集）
- **实验充分性**：实验设计**比较全面**。对比了多个近期SOTA方法，消融实验覆盖了核心设计选择。报告了多次运行的均值和标准差，结果具有统计可靠性。但**缺少对更大模型（如ViT-L）或更广泛视频数据集（如EPIC-Kitchens）的验证**，泛化性有待进一步检验。

## 6. 主要结论与发现
- BDC-CLIP在**所有评估任务和数据集上均取得最佳或近乎最佳的性能**，显著超越基于余弦相似度的基线。
- 例如：零样本K600 top-1达78.9%（w/ WSE），比TC-CLIP高0.8%；16-shot HMDB-51达77.3%，比TC-CLIP高4.3%；基到新HMDB-51 HM达69.8%，比TC-CLIP高2.6%；全监督K400 top-1达86.5%（w/ WSE）。
- 消融实验证明：**BDC度量优于余弦相似度**；**利用所有局部token**可带来显著增益；**时间BDC注意力**对动作识别有效；**LLM文本增强**进一步改善性能。
- 因此，BDC是一种比余弦相似度更强大的多模态对齐工具，尤其适用于需要细粒度时空理解的视频动作识别。

## 7. 优点：方法或实验设计亮点
- **方法创新**：首次将BDC引入CLIP的多模态对齐，突破余弦相似度只能捕捉线性关系的局限，且天然支持集合级（所有token）匹配。
- **细粒度建模**：通过利用所有视觉和文本token，以及时间BDC注意力，充分捕捉空间、时间和语言维度的微线索。
- **强泛化能力**：在零样本、少样本、基到新等设置中均表现优异，表明BDC-CLIP学到的表示具有更好的可迁移性。
- **实验设计严谨**：广泛对比多个SOTA基准，消融实验覆盖关键组件（度量、维度、token、文本增强等），并在不同数据集上验证一致性。
- **计算效率可控**：虽有一定计算开销增加，但通过维度降低和半向量化等技巧，整体复杂度仍在可接受范围，且吞吐量优于某些前期方法（如TC-CLIP）。

## 8. 不足与局限
- **计算成本**：相比ViFi-CLIP，GFLOPS增加11%，吞吐量下降20%，在资源受限环境下可能不够友好。
- **模型与数据覆盖**：仅使用ViT-B/16视觉编码器，未探索更大模型（如ViT-L）对性能的进一步提升；仅在5个动作识别数据集上评估，缺乏更复杂场景（如多模态检索、开放世界检测）或更小/更具挑战性数据集的验证。
- **依赖LLM文本增强**：使用GPT-4o生成描述，可能引入LLM的过拟合或偏见，且增加了推理开销。此外，LLM的prompt设计固定，未探索优化。
- **潜在偏差风险**：继承CLIP中存在的性别、种族等偏见，且LLM也可能放大这些偏见。作者在Impact Statement中已指出，但未进行缓解。
- **缺乏消融实验**：未系统研究不同时间注意力变体的影响（如无注意力、简单平均等），未在不同帧采样策略下比较。
- **应用局限性**：当前方法专为视频动作识别设计，迁移到其他视频理解任务（如时序定位、视频-文本检索）需额外适配。

（完）
