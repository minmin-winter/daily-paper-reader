---
title: "MODA: MOdular Duplex Attention for Multimodal Perception, Cognition, and Emotion Understanding"
title_zh: MODA：面向多模态感知、认知和情感理解的模组化双工注意力机制
authors: "Zhicheng Zhang, Wuyou Xia, Chenxi Zhao, Zhou Yan, Xiaoqiang Liu, Yongjie Zhu, Wenyu Qin, Pengfei Wan, Di ZHANG, Jufeng Yang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=9hd5WA6QCn"
tags: ["query:balanced-mml"]
score: 10.0
evidence: 提出模块化双工注意力机制，动态平衡跨模态注意力不一致问题
tldr: 多模态大模型在高级认知和情感理解任务中面临跨模态注意力不一致和逐层衰减的注意力缺陷问题。本文提出模组化双工注意力机制（MODA），同时进行模态内精炼和跨模态交互，有效改善了注意力不平衡问题。实验表明MODA在多个多模态任务上取得了显著提升。该工作为多模态学习中动态平衡模态贡献提供了新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 859, \"height\": 588, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1766, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1779, \"height\": 622, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 863, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 286, \"height\": 264, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 286, \"height\": 177, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1771, \"height\": 252, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9hd5wa6qcn/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 850, \"height\": 204, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-9hd5wa6qcn/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1773, \"height\": 285, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9hd5wa6qcn/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1764, \"height\": 774, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9hd5wa6qcn/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 872, \"height\": 757, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9hd5wa6qcn/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 856, \"height\": 710, \"label\": \"Table\"}]"
motivation: 现有MLLM在高级任务中因跨模态注意力不一致和逐层衰减导致注意力缺陷，需平衡模态交互。
method: 提出模组化双工注意力（MODA），同时进行模态内精炼和跨模态交互，动态调整注意力权重。
result: 在多个多模态任务上超越基线，验证了MODA对注意力不平衡问题的有效性。
conclusion: MODA为多模态学习提供了一种有效的动态平衡机制，提升了模型在高级任务上的表现。
---

## Abstract
Multimodal large language models (MLLMs) recently showed strong capacity in integrating data among multiple modalities, empowered by generalizable attention architecture. Advanced methods predominantly focus on language-centric tuning while less exploring multimodal tokens mixed through attention, posing challenges in high-level tasks that require fine-grained cognition and emotion understanding. In this work, we identify the attention deficit disorder problem in multimodal learning, caused by inconsistent cross-modal attention and layer-by-layer decayed attention activation. To address this, we propose a novel attention mechanism, termed MOdular Duplex Attention (MODA), simultaneously conducting the inner-modal refinement and inter-modal interaction. MODA employs a correct-after-align strategy to effectively decouple modality alignment from cross-layer token mixing. In the alignment phase, tokens are mapped to duplex modality spaces based on the basis vectors, enabling the interaction between visual and language modality. Further, the correctness of attention scores is ensured through adaptive masked attention, which enhances the model's flexibility by allowing customizable masking patterns for different modalities. Extensive experiments on 21 benchmark datasets verify the effectiveness of MODA in perception, cognition, and emotion tasks.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：多模态大语言模型（MLLMs）在高级感知、认知和情感理解任务中存在“注意力缺陷障碍”（Attention Deficit Disorder, DDA）问题，表现为跨模态注意力不一致（偏向文本模态）以及逐层衰减的注意力激活，导致模型无法捕捉细粒度多模态细节，在需要精细认知和情感理解的任务中性能低下（如讽刺检测准确率仅约50%）。
- **研究动机**：现有MLLM主要聚焦语言中心的微调，忽视了多模态token通过注意力混合时的平衡问题。作者通过可视化发现SOTA模型（如LLaVA-NeXT）的注意力分数在层间差异可达10倍以上，且视觉模态的注意力远弱于文本模态。因此需要设计更平衡的多模态注意力机制。
- **整体含义**：本文旨在通过模块化双工注意力（MODA）同时进行模态内精炼和跨模态交互，解决注意力不平衡问题，从而提升MLLM在感知、认知和情感理解上的能力。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 2.1 核心思想
- **“校正后对齐”（correct-after-align）策略**：将模态对齐与跨层token混合解耦。先通过双工对齐器将token映射到双模态共享空间，再通过模块化掩码注意力修正注意力分数，实现模态内和跨模态交互的分离调控。

### 2.2 关键技术细节

#### （1）Duplex Attention Alignment（双工注意力对齐）
- **动机**：减少模态间不一致性，将token映射到其他模态的空间。
- **实现**：
  - 基于Gram矩阵提取每个模态的空间基向量：  
    \( \mathbf{G}^m_{ij} = \sum_{k=1}^{N_m} K^m_{ik} K^m_{kj} = (\mathbf{K}^m)^\top \mathbf{K}^m \)
  - 利用归一化Gram矩阵作为核映射函数，将另一模态的键（Key）映射到当前模态空间：  
    \( \mathbf{K}^{\bar{m} \to m} = \mathbf{K}^{\bar{m}} \|\mathbf{G}^m\| \)
  - 对齐后的token与原始token融合，通过LoRA调优的融合器实现，计算复杂度保持线性。

#### （2）Modular Attention Mask（模块化注意力掩码）
- **动机**：缓解注意力矩阵坍塌，防止token过度平滑，并引入模态位置先验。
- **实现**：
  - 为每个模态分别设计自模态掩码 \( \mathbf{M}^m \) 和跨模态掩码 \( \mathbf{M}^{\bar{m}} \)。
  - 采用固定长度伪注意力分数机制（类似StableMask），对超出可关注长度的部分加入衰减分数 \( p_{ij} = p_{\text{base}} - (j-1)\beta \)。
  - 利用归一化Gram矩阵作为指示器，决定哪些部分应施加模态位置偏置，从而分别计算自模态注意力和跨模态注意力：
    \[
    \mathbf{O}_{\text{self}} = \text{Softmax}\left(\frac{\mathbf{Q}^m (\mathbf{K}^m)^\top}{\tau} + \mathbf{M}^m\right) \mathbf{V}^m
    \]
    \[
    \mathbf{O}_{\text{cross}} = \text{Softmax}\left(\frac{\mathbf{Q}^m (\mathbf{K}^{\bar{m}})^\top}{\tau} + \mathbf{M}^{\bar{m}}\right) \mathbf{V}^{\bar{m}}
    \]

#### （3）总体流程
- MODA替换标准Transformer中的注意力层，输入包含图像和上下文提示（背景、对话历史）。每个注意力块的流程：先通过双工对齐器（V-Aligner和T-Aligner）对齐，再通过模块化掩码注意力分别计算自模态和跨模态输出，最后与残差连接和FFN组合。

## 3. 实验设计

### 3.1 数据集与benchmark
- **感知任务**：16个benchmark，分为4类：
  - 通用QA：MME, MMBench, SEED, GQA
  - 知识QA：ScienceQA, MMMU, MathVista, AI2D
  - OCR与图表QA：ChartQA, OCRBench, TextVQA, DocVQA
  - 视觉中心QA：MMVP, RealworldQA, CV-Bench (2D & 3D)
- **认知任务**：MMRole（8个方面：指令遵循、流畅性、连贯性、图文相关性、回答准确性、个性一致性、知识一致性、语气一致性）
- **情感任务**：MVSA-S, MVSA-M, TumEmo, HFM（共4个多模态情感/情绪数据集）

### 3.2 对比方法
- **开源MLLMs**：Mini-Gemini-HD、LLaVA-NeXT、Cambrian-1（8B和34B两种规模）
- **闭源模型**：GPT-4V, Gemini-1.0/1.5 Pro, Grok-1.5, Claude 3 Opus, QWen-VL-Max
- **认知专用模型**：MMRole-9B
- **情感专用模型**：M2CL, MULSER, CMGCN, SPFVTE

### 3.3 评价指标
- 感知：多数benchmark采用准确率或GPT-4评分
- 认知：每个方面分数（0-1或1-2范围），平均分
- 情感：准确率和F1分数

## 4. 资源与算力

- **训练配置**：
  - 基于LLaMA-3-Instruct-8B或Hermes2-Yi-34B
  - 训练1 epoch，batch size 2048
  - 优化器：AdamW，cosine学习率调度
  - 学习率：LLM 2e-5，视觉编码器 2e-6
  - warmup比率：0.03
- **未明确说明**：论文未提及GPU型号、数量、训练时长（仅提到“使用700K训练样本训练1 epoch”），也未说明计算集群细节。但可在开源代码仓库（https://zzcheng.top/MODA）中进一步查找。

## 5. 实验数量与充分性

- **实验数量**：共21个benchmark（感知16个 + 认知1个（含8方面）+ 情感4个），加上消融实验（模块、对齐方式、融合方式、掩码方式各一套），以及注意力分布分析、可视化案例。总实验组数约30+。
- **充分性评价**：
  - **充分**：覆盖三大类任务（感知、认知、情感），且每类包含多个子benchmark；对比了多种开源/闭源SOTA以及任务专用模型；消融实验系统地分析了各组件贡献。
  - **客观公平**：所有对比采用统一设置（相同基座模型、训练数据量700K）；感知任务中使用Cambrian-1的官方评估协议；认知和情感任务引用先前工作的官方数据。
  - **可复现**：提供了开源代码和demo，训练配置公开。

## 6. 论文的主要结论与发现

- MODA有效缓解了多模态注意力缺陷问题：注意力分布更均衡（文本自模态与跨模态差距从56.97%降至50.31%，视觉从62.44%降至41.01%）。
- 在感知任务上，MODA-8B平均优于同规模Cambrian-1、LLaVA-NeXT等，尤其在视觉中心（66.0）和OCR&Chart（74.7）任务中领先；MODA-34B进一步超越Cambrian-1（平均76.7 vs 76.8? 实际表格显示MODA-34B平均76.7略低于Cambrian-1的76.8？但MODA在OCR&Chart和Vision-centric上更高，总体接近）。
- 在认知任务上，MODA-8B平均0.996，超过所有开源MLLM，接近Claude 3 Opus；在情感任务上，MODA-8B平均0.657，超过所有开源MLLM，且通过任务专用微调后达到0.841，与最佳专用模型SPFVTE（0.738）相当（但注意SPFVTE只覆盖部分数据集，MODA覆盖全部）。
- 可视化案例（《教父》场景）展示了MODA在细粒度感知、认知对话分析和情感理解上的优越性。

## 7. 优点

- **方法新颖**：首次系统性地分析多模态注意力缺陷问题，并提出双工对齐+模块化掩码的分离式注意力设计，理论清晰。
- **轻量高效**：线性复杂度的对齐操作（仅首轮计算Gram矩阵），适合工程部署。
- **即插即用**：MODA可替换现有MLLM的注意力模块，无需大幅修改架构。
- **实验全面**：覆盖感知、认知、情感三大领域，21个benchmark，对比充分，消融实验严谨。
- **可解释性**：注意力分布可视化直接证明MODA平衡了模态贡献。
- **开源友好**：提供完整代码、demo，便于复现和扩展。

## 8. 不足与局限

- **算力资源未明确**：未报告GPU型号、数量、训练时间，影响复现效率评估。
- **训练数据规模较小**：仅使用700K样本训练1 epoch，可能未充分挖掘MLLM潜力。在大规模预训练数据上的效果未知。
- **情感任务上的弱势**：虽然MODA领先开源MLLM，但对比情感专用模型（如SPFVTE），在部分情感数据集上仍有一定差距（例如MVSA-S的F1：MODA 0.705 vs SPFVTE 0.801）。说明在纯情感分类上，专用模型仍有优势。
- **认知任务评估**：仅使用MMRole一个benchmark，且评分可能依赖自动评估（GPT评分），存在一定偏差风险。
- **应用限制**：MODA的输出质量受微调数据和基座模型影响，可能产生低质量或幻觉内容，需谨慎使用。商业用途被明确禁止。
- **仅考虑视觉和语言模态**：论文未处理音频、视频等多模态场景，扩展性需进一步验证。
- **消融实验仅基于8B模型**：未在34B规模上做消融，结论的泛化性存疑。

（完）
