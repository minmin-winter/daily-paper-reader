---
title: "Graph4MM: Weaving Multimodal Learning with Structural Information"
title_zh: Graph4MM：利用结构信息编织多模态学习
authors: "Xuying Ning, Dongqi Fu, Tianxin Wei, Wujiang Xu, Jingrui He"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=FB2e8PV6qg"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 基于图建模模态内和模态间关系
tldr: 针对现有多模态学习未能充分利用结构化信息、将图视为独立模态导致整体理解碎片化的问题，本文提出Graph4MM框架。该框架通过图结构建模模态内和模态间多跳邻居关系，并将结构化信息注入基础模型。在多个多模态任务上，Graph4MM有效提升了融合表示的质量和下游性能，证明了利用图结构增强多模态学习的有效性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-fb2e8pv6qg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 797, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fb2e8pv6qg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 713, \"height\": 305, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fb2e8pv6qg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1729, \"height\": 599, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fb2e8pv6qg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1267, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fb2e8pv6qg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1169, \"height\": 600, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fb2e8pv6qg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1117, \"height\": 543, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fb2e8pv6qg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1193, \"height\": 454, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1769, \"height\": 969, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 868, \"height\": 324, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 853, \"height\": 391, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 871, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 991, \"height\": 769, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1096, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 814, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1133, \"height\": 188, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1184, \"height\": 189, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fb2e8pv6qg/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1340, \"height\": 304, \"label\": \"Table\"}]"
motivation: 现有方法忽略多跳邻居结构信息并孤立处理图模态，导致多模态理解碎片化。
method: 设计Graph4MM框架，将多跳邻居的结构信息整合入基础模型，并融合模态特定特征。
result: 在多模态基准上，Graph4MM优于不考虑结构信息的方法，提升了融合表示能力。
conclusion: 图结构信息是增强多模态学习的重要资源，Graph4MM有效融合了结构化与非结构化模态。
---

## Abstract
Real-world multimodal data usually exhibit complex structural relationships beyond traditional one-to-one mappings like image-caption pairs. Entities across modalities interact in intricate ways, with images and text forming diverse interconnections through contextual dependencies and co-references. Graphs provide powerful structural information for modeling intra-modal and inter-modal relationships. However, previous works fail to distinguish multi-hop neighbors and treat the graph as a standalone modality, which fragments the overall understanding. This limitation presents two key challenges in multimodal learning: (1) integrating structural information from multi-hop neighbors into foundational models, and (2) fusing modality-specific information in a principled manner. To address these challenges, we revisit the role of graphs in multimodal learning within the era of foundation models and propose Graph4MM, a graph-based multimodal learning framework. To be specific, we introduce Hop-Diffused Attention, which integrates multi-hop structural information into self-attention through causal masking and hop diffusion. Furthermore, we design MM-QFormer, a multi-mapping querying transformer for cross-modal fusion. Through theoretical and empirical analysis, we show that leveraging structures to integrate both intra- and inter-modal interactions improves multimodal understanding beyond treating them as a standalone modality. Experiments on both generative and discriminative tasks show that Graph4MM outperforms larger VLMs, LLMs, and multimodal graph baselines, achieving a 6.93% average improvement.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义  
- **研究动机**：现实世界中的多模态数据（如文档中的图像、文本、标题）不是孤立的一对一关系，而是存在复杂的**多跳结构依赖**（如图1所示的图像与前后节内容、页面描述之间的交织关系）。现有方法（如VLMs、MMGL）要么仅建模单图像-文本对，要么将图结构视为一个独立的模态（如用GCN编码后与文本/视觉嵌入简单相加），导致**多跳邻居信息被忽略、图模态与预训练视觉/语言空间存在语义鸿沟**，最终整体理解碎片化。  
- **核心问题**：如何有效整合多跳邻居的结构信息到基础模型中，并以原则性方式融合模态特定信息，从而提升多模态理解能力。

### 论文提出的方法论  
- **核心思想**：**不将图作为独立模态，而是用图结构（邻接先验）指导模态内和模态间的融合**。  
- **关键技术细节**：  
  1. **多模态图建模**：定义节点含可选文本/图像属性，边分为文本-文本、图像-图像、文本-图像三种类型，并诱导出文本子图 \(G_t\) 和图像子图 \(G_p\)。  
  2. **Hop-Diffused Attention**：  
     - 对文本/视觉嵌入分别进行**自注意力**，计算初始注意力矩阵 \(A'\)。  
     - 使用**因果掩码** \(M_{i,j}\) 限制注意力只作用于有边连接的节点。  
     - 通过**扩散机制**（\(A = \sum_{i=0}^{\infty} \theta_i A^i\)，\(\theta_i = \alpha(1-\alpha)^i\)）聚合多跳结构信息，保留全局拓扑同时避免过平滑。  
     - 理论证明（命题3.1）该机制比堆叠多层GAT能保持更高Dirichlet能量，缓解过平滑。  
  3. **MM-QFormer（多映射查询Transformer）**：  
     - 使用可学习查询令牌 \(Q_v\)，通过**共享自注意力**（文本-查询交互）和**跨注意力**（查询-视觉提取）实现文本条件化的视觉特征提取，生成多模态令牌供下游LLM使用。  
  4. **轻量替代**：Hop-Aware Attention通过添加可学习跳数嵌入（\(h_{hop}^{(h)}\)）降低复杂度，同时保留拓扑信息。  
- **框架流程**（图3）：文本/视觉输入 → Hop-Diffused Attention → MM-QFormer → 预训练LLM（用Prefix-Tuning/LoRA微调）→ 输出。

### 实验设计  
- **数据集**：  
  - **生成任务**：WikiWeb2M（10K页面，13539训练/1768测试样本），任务：根据多模态子图生成缺失的节首句。  
  - **判别任务**：Ele-Fashion（97766节点，11类，零样本分类），任务：利用节点及其邻居的多模态信息预测产品类别。  
- **Benchmark & 对比方法**：  
  - **PLMs**：OPT-125M, LLaMA-1B（仅文本输入）。  
  - **VLMs**：BLIP2-OPT-2.7B, Qwen2-VL-7B-Instruct（单/多图输入）。  
  - **MMGL**：多种变体（Node's Text, Subgraph's Text & Image, +GNN等）。  
  - **Graph4MM**：MM-QFormer、Hop-Aware MM-QFormer、Hop-Diffused MM-QFormer。  
- **评价指标**：生成用BLEU-4, ROUGE-L, CIDEr；判别用ROUGE-L, Accuracy, Recall, Precision。

### 资源与算力  
- **未明确说明总训练时长**，但提供了实验环境：**2× NVIDIA A100 或 2× NVIDIA Ada A6000 GPU**。  
- 训练超参（附录Table 5）：batch size 2，梯度累积16，OPT-125M训练50 epoch，LLaMA-1B训练3 epoch。所有方法使用相同PEFT（Prefix-Tuning/LoRA）确保公平。

### 实验数量与充分性  
- **主要实验组**：  
  - 生成任务：在OPT-125M和LLaMA-1B两个骨干上对比8种baseline，报告3个指标。  
  - 判别任务：同样两个骨干，零样本分类（OPT-125M用5个未见类，LLaMA-1B用9个未见类）。  
  - **消融实验**：分别移除文本/视觉子图的结构先验（Table 2）。  
  - **鲁棒性比较**：混合Hop-Diffused与Hop-Aware Attention在文本/视觉上的组合（Table 3）。  
  - **图作为独立模态 vs 引导融合**（Table 4, Table 6）。  
  - **图密度影响**（Table 7）、随机种子稳定性（Table 9）、不同未见类数量（Figure 5）、链接预测（Table 10）。  
- **充分性评价**：实验覆盖生成与判别两类任务、多种骨干、多种结构建模方式，并做了细致的消融和鲁棒性分析，对比方法全面（包括VLM/PLM/MMGL）。结果一致显示Graph4MM最优，平均提升6.93%。实验设计客观、公平（统一PEFT设置）。

### 主要结论与发现  
1. **图结构应作为引导而非独立模态**：直接编码图拓扑为嵌入（+GNN）反而降低性能（Table 4）。  
2. **Hop-Diffused Attention能有效整合多跳邻居信息**，且比堆叠GAT层更抗过平滑（理论+实证）。  
3. **MM-QFormer通过文本条件化的跨模态查询**，比简单线性投影更有效融合视觉与文本。  
4. Graph4MM在生成和判别任务上**全面超越**更大规模的VLMs、LLMs和MMGL。

### 优点  
- **方法论创新**：重新定义了图在多模态学习中的角色（从独立模态→引导融合），并提出Hop-Diffused Attention和MM-QFormer两个通用模块。  
- **理论支撑充分**：证明扩散注意力保持行归一化、等价于PPR；证明其Dirichlet能量高于GAT层（命题3.1）。  
- **实验扎实**：多任务、多骨干、多baseline，并包含消融/鲁棒性分析，提供了代码（GitHub）。  
- **轻量设计**：Hop-Aware Attention作为高效替代，性能几乎持平。

### 不足与局限  
- **数据集规模有限**：仅使用WikiWeb2M（10K页面）和Ele-Fashion（~98K节点），未在更大规模多模态图（如完整Wikipedia、多模态知识图谱）上验证。  
- **骨干模型较小**：仅测试OPT-125M和LLaMA-1B（1B），未探索更大LLM（如LLaMA-7B/13B）或更强VLM。  
- **零样本分类的类数设置不够全面**：OPT-125M仅6训练5测试，LLaMA-1B为2训练9测试，可能受随机划分影响。  
- **计算开销**：Hop-Diffused Attention涉及矩阵幂运算（虽有截断），复杂度仍高于简单加嵌入；文中未报告完整训练/推理时间。  
- **模态覆盖单一**：仅考虑文本和图像，未扩展到音频、视频、表格等其他模态。  
- **应用场景局限**：仅验证文档摘要和电商分类，对其他多模态结构（如社交媒体、科学论文）的泛化性未知。

（完）
