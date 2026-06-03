---
title: "Cooperation of Experts: Fusing Heterogeneous Information with Large Margin"
title_zh: 专家合作：大间隔异构信息融合方法
authors: "Shuo Wang, Shunyang Huang, Jinghui Yuan, Zhixiang Shen, zhao kang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=lZ18hxItYI"
tags: ["query:unified-mm"]
score: 7.0
evidence: 通过专家融合异构信息的统一框架
tldr: 异构信息融合面临不同语义空间模式差异大的挑战。本文提出CoE框架，将多类型信息编码为统一异构多路网络，利用专用编码器作为领域专家学习各自关系模式，并通过大间隔损失增强区分性。在多个异构数据集上，CoE显著优于现有融合方法，为处理异构多模态信息提供了统一且灵活的解决方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-lz18hxityi/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1709, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lz18hxityi/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1685, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lz18hxityi/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 866, \"height\": 400, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lz18hxityi/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 860, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lz18hxityi/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 807, \"height\": 633, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-lz18hxityi/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1151, \"height\": 768, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lz18hxityi/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 857, \"height\": 513, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lz18hxityi/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lz18hxityi/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1358, \"height\": 1190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lz18hxityi/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1061, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lz18hxityi/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1591, \"height\": 523, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lz18hxityi/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1147, \"height\": 292, \"label\": \"Table\"}]"
motivation: 现有融合方法未能充分处理不同语义空间中的异构模式，导致融合效果欠佳。
method: 提出CoE框架，将信息编码为统一异构多路网络，使用领域专家编码器并引入大间隔损失。
result: 在多个异构数据集上，CoE在分类和聚类任务中大幅超越现有方法。
conclusion: 统一异构网络与专家学习是处理异构信息融合的有效手段。
---

## Abstract
Fusing heterogeneous information remains a persistent challenge in modern data analysis. While significant progress has been made, existing approaches often fail to account for the inherent heterogeneity of object patterns across different semantic spaces. To address this limitation, we propose the **Cooperation of Experts (CoE)** framework, which encodes multi-typed information into unified heterogeneous multiplex networks. By transcending modality and connection differences, CoE provides a powerful and flexible model for capturing the intricate structures of real-world complex data. In our framework, dedicated encoders act as domain-specific experts, each specializing in learning distinct relational patterns in specific semantic spaces. To enhance robustness and extract complementary knowledge, these experts collaborate through a novel **large margin** mechanism supported by a tailored optimization strategy. Rigorous theoretical analyses guarantee the framework’s feasibility and stability, while extensive experiments across diverse benchmarks demonstrate its superior performance and broad applicability.

---

## 论文详细总结（自动生成）

# 中文总结：Cooperation of Experts: Fusing Heterogeneous Information with Large Margin

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：异构信息融合面临对象模式在不同语义空间中的固有异质性挑战，现有方法通常忽略这一点，导致融合效果欠佳。例如，社交网络中不同类型的关系（友谊、工作、家庭）具有截然不同的结构模式，单模型难以同时捕获。
- **整体含义**：本文旨在通过引入“专家合作”范式，将多类型信息编码为统一异构多路网络，使每个专家专注于特定关系模式的建模，并通过大间隔机制实现互补知识的有效整合，提升对复杂异构数据的表示能力和泛化性能。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：
  - 将异构信息（多关系、多模态）建模为异构多路网络，每层网络对应一种关系或模态。
  - 采用**两级专家**架构：低层专家（low-level experts）学习单层网络特有模式；高层专家（high-level experts）通过互信息最大化融合多网络信息，捕获跨层依赖。
  - 引入**置信张量（Confidence Tensor）** 动态调整各专家在最终决策中的权重，取代传统门控机制（竞争），实现专家合作。
  - 设计**大间隔优化**损失函数，最大化正确类别的预测得分与第二高得分之间的间隔，提升专家间一致性并增强鲁棒性。
- **关键技术细节**：
  - **图结构学习（GSL）**：对每层网络使用SGC+KNN重构邻接矩阵，确保结构可靠。
  - **互信息最大化**：通过变分下界（InfoNCE）近似计算网络间互信息，公式为 \( I_{lb}(Z_i; Z_j) = \mathbb{E}[\log \frac{e^{f(z_i,z_{j+})}}{\sum e^{f(z_i,z_j)}}] \)。
  - **两级专家训练损失**：\( L_E = -\sum I(G'_i;Y) - \sum\sum I(G'_i;G'_j) \) 等，最终转化为交叉熵与对比损失。
  - **大间隔损失**：\( M = \sum [Y_i^\top (Y_i \odot S(\Theta g_i)) - \frac{1}{\alpha}\log(\sum e^{\alpha(S(\Theta g_i)-Y_i\odot S(\Theta g_i))_j})] \)，与交叉熵损失 \( C \) 联合优化。
  - **理论保证**：证明了损失函数的部分凸性、Lipschitz连续性、梯度下降收敛性，并推导了基于间隔的泛化界。

## 3. 实验设计
- **数据集与场景**：
  - **多关系网络**（节点分类）：ACM（3层）、DBLP（2层）、Yelp（3层）、MAG（2层，约11.4万节点）、Amazon（3层，约1.2万节点）。
  - **多模态数据**（节点分类）：ESP、Flickr、IAPR、NUS（各包含图像和文本模态，无原始图结构，先通过KNN构建网络）。
- **Benchmark 方法**：
  - 固定结构GNN：GCN、HAN。
  - 有监督GSL：LDS、GRCN、IDGL、ProGNN、GEN、NodeFormer。
  - 无监督GSL：SUBLIME、STABLE、GSR。
  - 无监督多路方法：HDMI、InfoMGF。
  - 图MoE方法：GMoE、Mowst。
  - 多模态方法：DCCAE、CPM-Nets、ECML、MMDynamics、QMF。
- **评价指标**：分类准确率（Accuracy），所有方法重复5次取平均±标准差。

## 4. 资源与算力
- **硬件**：Intel(R) Xeon(R) Gold 5220 CPU + **NVIDIA A800 80GB GPU**。
- **软件**：PyTorch 2.1.1、DGL 2.4.0。
- **训练细节**：使用Adam优化器，超参数通过搜索确定（学习率、隐藏维度、KNN邻居数等）。**未报告具体训练时长**，但MAG和Amazon等大规模数据使用了批处理（batch size 2560）。

## 5. 实验数量与充分性
- **实验组数**：
  - **主要节点分类**：5个多关系网络 + 4个多模态数据集，共9组主实验（表1、表2）。
  - **消融实验**：在5个多关系网络上对比了4种变体（w/o HE、w/o GSL、RF、WRF）（表3）。
  - **鲁棒性分析**：在ACM上加入/删除边扰动（比例0~0.9），对比4种基线（图3）。
  - **超参数敏感性**：对γ和α在{50,100,200,500,1000}上测试（图4），以及对K在{5,10,15,20,25}上测试（附录图5）。
- **充分性评价**：实验较为充分。覆盖了不同规模（小至3025节点，大至11.4万节点）、不同关系类型（同构/异构）、以及有无拓扑结构的多模态场景。消融和鲁棒性实验验证了各模块贡献和抗噪能力。基线方法全面，包括传统GNN、GSL、对比学习、MoE及多模态方法。**但缺乏在大规模图（如百万节点）上的验证**（MAG仅11.4万节点），也未对比近期大规模GNN方法（如GraphSAGE等）。

## 6. 论文的主要结论与发现
- CoE在所有数据集上取得**最佳或接近最佳**的结果，且标准差通常最低，表明稳定性和泛化性优。
- **专家合作优于竞争**：通过置信张量+大间隔机制，所有专家共同贡献，避免了传统MoE只激活少数专家造成的信息丢失。
- **两级专家设计有效**：移除高层专家或移除GSL均导致性能显著下降，其中缺少高层专家影响更大（表3）。
- **鲁棒性强**：即使添加/删除50%边，CoE仍保持较高准确率，优于其他方法（图3）。
- **理论分析支撑**：证明了损失函数的凸性、Lipschitz连续性及收敛性，并给出了基于Rademacher复杂度的泛化界。

## 7. 优点
- **新颖性**：首次将“专家合作”而非“竞争”引入多路网络学习，设计置信张量和大间隔优化机制。
- **框架统一**：可同时处理多关系网络和多模态数据（需先建图），具有广泛适用性。
- **理论扎实**：给出了凸性、Lipschitz、收敛性及泛化界的严格证明，增强了方法的可信度。
- **实验严谨**：在9个数据集上与20+方法对比，消融、鲁棒性、超参数敏感性实验完整，结果统计显著。

## 8. 不足与局限
- **可扩展性验证有限**：最大数据集仅11.4万节点，未在更大规模（如OGBN-Products、Reddit）上测试，批处理策略的实际效率需进一步验证。
- **多模态场景依赖KNN建图**：对模态间交互的建模较间接，可能不如端到端多模态融合方法（如跨注意力）精细。
- **超参数调优成本**：γ、α、K等参数需要网格搜索，未提供自适应选择策略。
- **未讨论异构性程度**：不同层网络的异质性强度对性能的影响没有被量化分析。
- **无消融实验验证大间隔机制相对其他融合策略（如直接平均、加权投票）的优势**：仅对比了RF/WRF，未与动态加权或软投票对比。
- **代码已开源**（GitHub），但未提供详细的复现脚本和模型权重。

（完）
