---
title: "R2-T2: Re-Routing in Test-Time for Multimodal Mixture-of-Experts"
title_zh: "R2-T2: 多模态混合专家模型中的测试时重路由"
authors: "Zhongyang Li, Ziyue Li, Tianyi Zhou"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=oqPcOMafOF"
tags: ["query:balanced-mml"]
score: 8.0
evidence: 通过多模态MoE的测试时重路由解决视觉—语言不平衡
tldr: 多模态MoE中视觉表示常弱于语言，端到端训练的路由器对测试样本未必最优。本文提出R2-T2测试时重路由，动态调整专家权重以补偿视觉感知不足。实验表明该方法显著提升了下游任务性能，有效缓解了模态不平衡。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 859, \"height\": 779, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1551, \"height\": 693, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1764, \"height\": 665, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1771, \"height\": 906, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 482, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1768, \"height\": 784, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1765, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1775, \"height\": 777, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1583, \"height\": 802, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1768, \"height\": 790, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1766, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1770, \"height\": 416, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1763, \"height\": 413, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oqpcomafof/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1760, \"height\": 385, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 904, \"height\": 444, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1615, \"height\": 581, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1782, \"height\": 1086, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 757, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 565, \"height\": 266, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 763, \"height\": 167, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 547, \"height\": 238, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 712, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 707, \"height\": 182, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 720, \"height\": 470, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 883, \"height\": 214, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 800, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 715, \"height\": 161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 794, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1588, \"height\": 251, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1603, \"height\": 395, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1587, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1585, \"height\": 231, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oqpcomafof/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1413, \"height\": 267, \"label\": \"Table\"}]"
motivation: 多模态MoE中视觉感知弱于语言，端到端路由器测试时非最优。
method: 提出测试时重路由机制，动态调整专家权重以补偿视觉不足。
result: R2-T2在多个视觉语言任务上提升性能，缓解模态不平衡。
conclusion: 测试时重路由有效改善多模态MoE的模态不平衡问题。
---

## Abstract
In large multimodal models (LMMs), the perception of non-language modalities (e.g., visual representations) is usually not on par with the large language models (LLMs)' powerful reasoning capabilities, deterring LMMs' performance on challenging downstream tasks. 
This weakness has been recently mitigated by replacing the vision encoder with a mixture-of-experts (MoE), which provides rich, multi-granularity, and diverse representations required by different downstream tasks. The performance of multimodal MoE largely depends on its router, which reweights and mixes the representations of different experts for each input. However, we find that the end-to-end trained router does not always produce the optimal routing weights for every test sample. To bridge the gap, we propose a novel and efficient method ''**R**e-**R**outing in **T**est-**T**ime (R2-T2)'' that locally optimizes the vector of routing weights in test-time by moving it toward those vectors of the correctly predicted samples in a neighborhood of the test sample. We propose three R2-T2 strategies with different optimization objectives and neighbor-search spaces. R2-T2 consistently and significantly improves state-of-the-art LMMs' performance on challenging multimodal benchmarks of diverse tasks, without training any parameters in the base model. Our code can be accessed here.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：在大规模多模态模型（LMM）中，非语言模态（如图像）的感知能力通常显著弱于大语言模型（LLM）的强大推理能力，导致模态不平衡。
- **现有缓解方案**：将单视觉编码器替换为**混合专家模型（MoE）**，通过多个专家提供丰富、多粒度的表示，并依赖路由器为每个输入分配专家权重。
- **关键发现**：端到端训练出的路由器在测试样本上**并非总是最优**，表2显示Oracle路由（使用真实标签优化）比基模型提升≥10%准确率，说明存在巨大的优化空间。
- **研究目标**：提出**测试时重路由（R2-T2）**，在不训练任何模型参数的前提下，动态优化测试样本的路由权重，从而提升多模态MoE性能。

## 2. 论文提出的方法论
### 核心思想
- 假设：成功任务（参考集中正确预测的样本）的路由权重蕴含可迁移的知识和技能。
- 方法：对每个测试样本，在其**参考集（正确预测样本）** 的邻域中，通过优化或加权聚合来调整路由权重向量，使其更接近邻域中的最佳配置。

### 三种具体策略
1. **邻域梯度下降（NGD）**：
   - 使用邻域样本的损失函数的加权平均作为代理目标函数 \(L(r) = \frac{\sum_{i\in N(x)} K(x_i,x) \cdot \ell[f(x_i,r),y_i]}{\sum K(x_i,x)}\)。
   - 对 \(r\) 进行多步梯度下降更新（余弦退火学习率）。
   - 不需要测试样本的真实标签，仅依赖邻域样本的标签。

2. **核回归（Kernel Regression）**：
   - 直接预测 \(\hat{r}\) 为邻域路由权重的核加权平均。
   - 通过二分搜索在初始 \(r\) 和 \(\hat{r}\) 之间寻找最优插值系数 \(\alpha\)：\(r \leftarrow \alpha r + (1-\alpha)\hat{r}\)。

3. **模式寻找（Mode Finding / Meanshift）**：
   - 在路由权重空间内进行迭代，将 \(r\) 移向局部密度最高的区域（邻域平均 \(\bar{r}\)），更新：\(r \leftarrow \alpha r + (1-\alpha)\bar{r}\)。

### 关键技术细节
- **邻域定义**：在**任务嵌入空间**（通过NV-Embed-V2等模型提取描述嵌入）中采用**kNN**（k=5）或**ϵ-ball**。
- **相似性度量**：使用高斯核函数（最有效）。
- **嵌入模型**：默认NV-Embed-V2，具更好语义区分能力。
- **流程**：离线构建参考集（每个任务使用≤5000个正确预测样本），在线对每个测试样本检索邻域，执行优化。

## 3. 实验设计
### 数据集与场景
- **基模型**：两个多模态MoE模型：**MoAI-7B**（6个专家）和**MoVA-7B**（7个专家）。
- **参考集**：来自8个公开数据集（VQA-V2, Visual7W, CLEVR, COCO-QA, A-OKVQA, TQA, MathVista, ST-VQA, DocVQA），每个采样≤5000样本，覆盖通用视觉理解、知识推理、OCR三大任务类型。
- **评估基准**：8个挑战性测试集：MMBench, MME-P, SQA-IMG, AI2D, TextVQA, GQA, CVBench 2D/3D。
- **额外验证**：MMMU, ChartQA（附录D.1）。

### 对比方法
- **内部对比**：三种R2-T2策略（NGD、核回归、模式寻找）及Oracle（使用真实标签的梯度下降，上界）。
- **外部SOTA**：包括7B/8B/13B/34B的多种VLM（InstructBLIP, Qwen-VL, mPLUG-Owl, ShareGPT4V, LLaVA-NeXT, Cambrian1, Mini-Gemini等）。
- **消融实验**：邻域选择（kNN vs ϵ-ball, k值）、核函数、嵌入模型、NGD步数、学习率调度。
- **其他基线**：集成方法（多重采样、噪声路由）、RAG与In-Context Learning（附录D.2）。

## 4. 资源与算力
- **方法性质**：**完全训练-free**，仅需推理时计算。
- **计算量**（表4，以MMBench+MoAI-7B为例）：
  - 基模型：9.9T FLOPs/样本。
  - NGD：67.5T FLOPs/样本（约6.8倍），但准确率提升5.9%。
  - 模式寻找：10.7T FLOPs（性价比中等）。
- **延迟**（表16，RTX A6000）：
  - 基模型：7.8s/样本。
  - R2-T2：25.6s/样本（约3.3倍）。
- **GPU内存**（表15）：基模型18GB，R2-T2+NV-Embed-V2约27GB；可选轻量嵌入模型（如all_mini_v6）仅20GB。
- **未明确提及**：训练所需的GPU数量/时长（因无需训练），但参考集构建需离线推理一次。

## 5. 实验数量与充分性
- **主实验**：2种模型 × 8个基准 = 16个完整得分表（表2），以及与SOTA对比（表3，含14个外部模型）。
- **消融实验**：至少5个维度（邻域、核、嵌入、步数、学习率），每个均给出详细数值（表5-8, 18-22）。
- **附加验证**：MMMU/ChartQA（+5.6%/4.2%）、集成/噪声路由基线、RAG/ICL对比（附录D.2）。
- **鲁棒性分析**：有限任务覆盖（3DSRBench，+4.5%）、参考集规模（1/10仍+2.9%）、不匹配参考集（OCR子集用作知识推理参考仅+0.3%，验证需要任务相关参考）。
- **数据污染检查**：通过两阶段相似度筛查（嵌入+CLIP），确认无重叠。
- **公平性**：超参数通过独立于测试集的Qbench选定，未对单个基准调优，统一使用相同配置。
- **结论**：实验非常充分、设计严谨，覆盖多种任务类型和外推场景，结果客观可信。

## 6. 论文的主要结论与发现
1. **R2-T2显著提升多模态MoE性能**：NGD在MoAI上平均提升约6%绝对准确率，MoVA提升约5%，接近Oracle上界的70-80%。
2. **无需训练即可超越更大模型**：R2-T2(MoAI-7B)在8个基准上超越多数7/8/13/34B模型（表3）。
3. **NGD是最优策略**：远优于模式寻找和核回归，证明使用邻域损失的梯度下降最为有效。
4. **路由优化纠正了原始路由器的偏差**：原始路由器过度依赖ILANG专家（对齐语言），R2-T2将其转向更合适的专家（如IAUX用于空间推理，LAUX用于对象识别），专家分布更平衡（图4）。
5. **专家转移模式与任务相关**：错误→正确的转移模式主要为ILANG→LIMG（精细视觉）、ILANG→IAUX（物体检测）、ILANG→LAUX（知识整合）；正确→错误转移很少（仅2.31%），净增益显著。
6. **参考集质量和相似性度量至关重要**：高斯核>其他核；NV-Embed-V2>其他嵌入；k=5最优；任务相关参考集才能带来增益。

## 7. 优点
- **创新性强**：首次提出测试时重路由问题，巧妙地利用参考集中正确样本的权重作为先验，无需模型参数微调。
- **高效实用**：完全免训练，仅增加推理计算，部署友好；且可通过轻量嵌入模型降低资源消耗。
- **通用性好**：在两个不同MoE架构（MoAI、MoVA）、多个任务类型（通用视觉、知识推理、OCR）上均取得一致收益；对参考集规模不敏感（1/10规模仍有效）。
- **分析深入**：不仅报告平均性能，还详细分析专家转移模式、预测转换过程（图5），提供直观案例（图2/6-10），解释性强。
- **实验严谨**：固定超参数、独立调参、数据污染筛查、鲁棒性分析，确保结论可靠。

## 8. 不足与局限
- **计算开销**：NGD需要每样本多次前向传播（需计算邻域损失），FLOPs增加6-7倍，延迟增加3.3倍；对于实时性要求高的场景可能受限（作者建议参考集剪枝+高效kNN搜索可缓解）。
- **依赖参考集质量**：参考集需预先构建且任务相关（附录D.3.3显示不匹配参考集增益极小）；对于全新领域或无可用正确预测样本的场景，R2-T2失效。
- **偶尔引入错误**：虽然净收益显著，但优化过程中有约2.31%正确样本变为错误（图5）；在安全关键应用中可能需额外校准。
- **仅适用于MoE架构**：方法专门针对动态路由机制，无法直接用于其他非MoE模型（但这是其设计初衷）。
- **未探索在线学习**：参考集是静态的，没有考虑测试样本本身可加入参考集进行迭代优化（虽然可以扩展）。
- **超参数敏感度**：虽然统一固定，但k、步数、学习率等仍需调优（通过独立基准）；不同领域可能需重新调整。

（完）
