---
title: A Closer Look at Multimodal Representation Collapse
title_zh: 多模态表示坍塌的深入分析
authors: "Abhra Chaudhuri, Anjan Dutta, Tu Bui, Serban Georgescu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Vf9f7eNX6T"
tags: ["query:balanced-mml"]
score: 9.0
evidence: 直接研究多模态融合中的模态坍塌和不平衡问题
tldr: 该论文深入研究了多模态融合中的模态坍塌现象，即模型倾向于忽略部分模态。作者揭示了坍塌机制，并证明跨模态知识蒸馏可以解缠表示、缓解不平衡，为平衡多模态学习提供了理论基础和方法指导。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 857, \"height\": 650, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1693, \"height\": 835, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1774, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1781, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1782, \"height\": 446, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 867, \"height\": 669, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 867, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 877, \"height\": 670, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 877, \"height\": 670, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vf9f7enx6t/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1768, \"height\": 440, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1419, \"height\": 542, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 855, \"height\": 388, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 886, \"height\": 485, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 846, \"height\": 536, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 708, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 712, \"height\": 412, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 686, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1040, \"height\": 471, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 299, \"height\": 258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 927, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vf9f7enx6t/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1110, \"height\": 570, \"label\": \"Table\"}]"
motivation: 多模态融合模型常常依赖于部分模态而忽略其他，导致性能下降，缺乏对模态坍塌机制的理解。
method: 通过理论分析证明模态坍塌源于融合头共享神经元导致的噪声纠缠，并利用跨模态知识蒸馏解缠表示。
result: 实验表明跨模态蒸馏有效缓解了模态坍塌，提升了多模态融合性能。
conclusion: 该工作从理论上解释了模态坍塌的原因，并提出了一种有效的缓解方法。
---

## Abstract
We aim to develop a fundamental understanding of modality collapse, a recently observed empirical phenomenon wherein models trained for multimodal fusion tend to rely only on a subset of the modalities, ignoring the rest. We show that modality collapse happens when noisy features from one modality are entangled, via a shared set of neurons in the fusion head, with predictive features from another, effectively masking out positive contributions from the predictive features of the former modality and leading to its collapse. We further prove that cross-modal knowledge distillation implicitly disentangles such representations by freeing up rank bottlenecks in the student encoder, denoising the fusion-head outputs without negatively impacting the predictive features from either modality. Based on the above findings, we propose an algorithm that prevents modality collapse through explicit basis reallocation, with applications in dealing with missing modalities. Extensive experiments on multiple multimodal benchmarks validate our theoretical claims. Project page: https://abhrac.github.io/mmcollapse/.

---

## 论文详细总结（自动生成）

好的，请查收基于您提供的论文内容生成的详细中文总结。

## 论文详细中文总结

### 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：多模态融合模型在训练过程中，常常会过度依赖某个或某几个模态，而忽略甚至“遗忘”其他模态。这种现象被称为**模态坍塌（Modality Collapse）**。模态坍塌会严重影响模型在测试时面对缺失模态场景的鲁棒性，例如，若模型仅依赖的模态缺失，模型可能完全失效。
- **研究动机**：现有工作大多基于经验观察或推测来解释模态坍塌的原因（如梯度冲突、数据分布与融合策略的交互），**缺乏对背后学习理论机制的深入理解**。本文旨在填补这一空白，从底层机制出发，建立模态坍塌的理论基础。

### 2. 方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：
    1. **模态坍塌的成因**：模态坍塌源于融合头中**多语义神经元（Polysemantic Neurons）** 导致的**跨模态特征纠缠**。具体来说，一个模态的**噪声特征**会与另一个模态的**预测特征**通过共享的神经元纠缠在一起。这种纠缠使得噪声特征掩盖了前一个模态预测特征的正面贡献，导致该模态的预测能力“崩塌”。
    2. **关键理论机制**：
        - **引理1**：随着模态数量增加，跨模态多语义神经元的比例呈**二次方增长**。
        - **定理1（干扰）**：跨模态多语义碰撞增加，会导致预测特征对损失函数减少的边际贡献下降。
        - **引理2 & 定理2（秩瓶颈）**：SGD梯度更新的秩会收敛到一个低秩流形，这与神经网络的**低秩简单性偏差**有关。模型倾向于学习低秩的多语义神经元，而非高秩的单语义神经元，从而加剧了跨模态的噪声-预测特征纠缠。
    2. **解决方案**：
        - **隐式解缠：跨模态知识蒸馏**。**定理3**证明，将幸存模态的知识蒸馏给已崩塌模态的编码器，可以隐式地“释放秩瓶颈”，使得模型能够沿着新的、独立的维度去“去噪”，从而解缠表示，允许所有模态的预测特征都被充分利用。
        - **显式解缠：显式基重分配**。基于理论，提出 **EBR** 算法，通过对抗训练的方式，显式地解缠和去噪，以达到更高效、可控的防止模态坍塌效果。

- **关键技术细节：显式基重分配（EBR）算法流程**：
    1. 在每个模态编码器 *fi* 上附加一个编码器-解码器结构 *h-i · h⁻¹-i*，实现一个可逆的投影。
    2. 定义一个模态判别器网络 ψ，用于根据编码后的特征 *gi(x)* （即 *fi·hi* 的输出）预测模态标签。
    3. **联合优化两个损失**：
        - **模态判别损失 Lmd**：交叉熵损失，判别器 ψ 试图正确预测模态来源。
        - **语义损失 Lsem**：最终多模态预测任务的交叉熵损失。
    4. **更新规则**：
        - 判别器 ψ 更新以最小化 Lmd。
        - 编码器 *gi* 更新以**最小化语义损失 Lsem**，同时**最大化模态判别损失 Lmd**（通过梯度上升），这一步旨在使不同模态的表示在语义相关的同时，尽可能接近（在距离度量 d 下），从而解缠。
        - 解码器 *h⁻¹-i* 更新以最小化语义损失。
    5. **对抗性解缠**：通过 *gi* 最大化 Lmd 和 ψ 最小化 Lmd 的对抗过程，实现了不同模态特征的显式解缠。最终通过 *h⁻¹-i* 将解缠后的表示映射回原始维度，得到去噪后的表示。

### 3. 实验设计：数据集、基准与对比方法

- **数据集**：
    - **MIMIC-IV**：大型医疗电子健康记录数据集，包含临床笔记、实验室值、人口统计学信息、诊断、用药等多个模态。任务：**死亡率预测**和**再入院预测**。
    - **avMNIST**：包含图像和音频的MNIST数字识别数据集。任务：**数字分类**。
- **基准（Benchmark）**：
    - 在MIMIC-IV上，主要基准是 **MUSE** (ICLR‘24) 及其同类模型。
    - 在avMNIST上，遵循Wang et al. (2023)的设置，与多个SOTA方法比较。
- **对比方法**：
    - **缺失模态处理方法**：CM-AE, SMIL, MT, Grape, M3Care, ShaSpec, MUSE等。
    - 在消融实验中，对比了**无任何干预的“Vanilla”多模态模型**、**使用KD进行隐式基重分配的模型**，以及**使用EBR进行显式基重分配的模型**。

### 4. 资源与算力

- 论文**未明确说明**使用的GPU型号、数量以及训练时长。在实现细节部分，仅提到了训练轮数（1200 epochs）及学习率调度等参数，但未提及硬件资源。因此，无法从文中获知具体的算力成本。

### 5. 实验数量与充分性

- **实验数量与类型**：论文进行了大量且全面的实验，覆盖了多个方面：
    - **跨模态多语义干扰验证**（图4）：分析了被消除模态的语义损失曲线。
    - **秩瓶颈存在性验证**（图5 a, c）：展示了多模态表示的秩随模态强度β的变化。
    - **基重分配有效性**（图5 b, d；图6；图7；表2）：从秩、相似性、损失动力学、抗噪性等角度评估KD和EBR。
    - **缺失模态处理**（表1, 3）：在不同缺失率下与SOTA方法比较。
    - **融合策略无关性**（表2, 4）：将EBR应用于不同基础融合模型（如Grape, M3Care, MUSE）的编码器。
    - **蒸馏顺序的影响**（表5）。
    - **可替代性分析**（表6）。
    - **统计显著性检验**（表8）：Wilcoxon秩检验。
    - **对比与生成模型**（表10, 11）：分析了MMVAE和GMC中的秩瓶颈。
    - **多模态共线性**（表7）。
    - **多语义性直接测量**（表9）。
- **充分性评价**：实验非常充分且客观。不仅验证了核心理论（秩瓶颈、多语义纠缠），还检验了所提方法（KD, EBR）在不同场景（噪声、不同缺失率、不同融合策略）下的有效性，并与多个SOTA方法进行了公平比较，同时进行了统计检验。实验设计严谨，结论可靠。

### 6. 主要结论与发现

1. **根本原因**：模态坍塌的根本原因是低秩的梯度更新迫使融合头神经元以多语义的方式纠缠不同模态的噪声与预测特征，导致模态塌陷。
2. **有效缓解**：跨模态知识蒸馏通过隐式释放秩瓶颈，解缠表示并去噪，从而有效防止模态坍塌。
3. **显式方法更优**：提出的显式基重分配（EBR）算法能更系统、高效地进行解缠和去噪，在缺失模态任务上达到了SOTA性能。
4. **通用性**：EBR方法不依赖特定的融合策略，可以作为一个通用工具应用于各种多模态模型。

### 7. 优点（亮点）

1. **理论创新性**：首次从**多语义性（Polysemanticity）** 和**低秩简单性偏差（Low-Rank Simplicity Bias）** 的视角，为模态坍塌现象提供了严格的、机理性的理论解释，超越了以往的经验假设。
2. **方法通用性**：提出的EBR算法仅在单模态编码器端进行修改，与下游融合算子无关，因此具有很好的通用性和可迁移性，可以即插即用地应用于现有SOTA模型。
3. **实验全面性**：实验覆盖了理论验证、多任务、多数据集、多种缺失率、多种融合策略、统计检验等多个维度，论证链条完整，结果具有说服力。
4. **实际应用价值**：通过解决模态坍塌，有效提升了模型在测试时缺失模态场景下的鲁棒性，对于医疗诊断、自动驾驶等关键应用具有重要的实际意义。

### 8. 不足与局限

1. **理论假设条件**：定理2和3的有效性依赖于所有特征提供的条件交叉熵减少量相同（即 `I(x; y|z1)=I(x; y|z2)=...`）这一条件。当特征重要性不均时，理论边界需要进一步扩展。
2. **额外参数开销**：EBR引入了h, h⁻¹, ψ 等模块（简单的两层MLP），虽然作者声明参数开销最小，但仍增加了模型的复杂度。
3. **实验场景限制**：实验主要集中于医疗（MIMIC-IV）和简单视觉音频（avMNIST）数据集。在更复杂、模态更多样（如视频+文本+语音）或规模更大的真实场景下的表现有待进一步验证。
4. **计算资源未报告**：缺乏对训练资源（GPU型号、时间）的详细报告，这使得其他研究者难以复现和评估算法的实际成本。
5. **潜在偏差风险**：模态替代策略依赖于对模态相似性的排序，如果模型的 latent factors 没有被完全且无偏地学到，替代效果可能有偏差。虽然提到了需要满足可识别性条件，但实际中无法完美保证。
6. **局限性讨论**：作者在结论中承认，对于特征条件互信息不同的情况，以及将EBR导致凸损失景观的内在机制的理论化探索是未来工作，表明当前工作在这些方面存在局限。

（完）
