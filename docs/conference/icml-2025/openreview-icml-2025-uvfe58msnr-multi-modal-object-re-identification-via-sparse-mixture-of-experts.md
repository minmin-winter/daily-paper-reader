---
title: Multi-Modal Object Re-identification via Sparse Mixture-of-Experts
title_zh: 基于稀疏混合专家的多模态物体重识别
authors: "Yingying Feng, Jie Li, Chi Xie, Lei Tan, Jiayi Ji"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=uvFE58mSnR"
tags: ["query:balanced-mml"]
score: 9.0
evidence: 平衡多模态重识别中的共享与特有特征
tldr: 现有方法在多模态物体重识别中难以平衡模态共享和特有特征。本文提出MFRNet，包含特征融合模块实现细粒度像素级交互，特征表示模块高效提取并组合共享和特有特征。实验表明该方法在多个数据集上取得最优结果，有效解决了模态不平衡问题。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-uvfe58msnr/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 852, \"height\": 582, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uvfe58msnr/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1748, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uvfe58msnr/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 827, \"height\": 900, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 848, \"height\": 757, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 851, \"height\": 1085, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1767, \"height\": 420, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 778, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 836, \"height\": 246, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 771, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 774, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 777, \"height\": 452, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 776, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uvfe58msnr/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 773, \"height\": 282, \"label\": \"Table\"}]"
motivation: 当前方法缺乏像素级跨模态交互且难以平衡模态共享与特有特征，限制了多模态重识别性能。
method: 设计特征融合模块和特征表示模块，分别实现细粒度交互和平衡特征组合。
result: 在多个公开数据集上达到最先进性能，验证了平衡策略的有效性。
conclusion: MFRNet通过显式平衡模态特征，显著提升了多模态物体重识别的鲁棒性。
---

## Abstract
We present MFRNet, a novel network for multi-modal object re-identification that integrates multi-modal data features to effectively retrieve specific objects across different modalities. Current methods suffer from two principal limitations: (1) insufficient interaction between pixel-level semantic features across modalities, and (2) difficulty in balancing modality-shared and modality-specific features within a unified architecture. To address these challenges, our network introduces two core components. First, the Feature Fusion Module (FFM) enables fine-grained pixel-level feature generation and flexible cross-modal interaction. Second, the Feature Representation Module (FRM) efficiently extracts and combines modality-specific and modality-shared features, achieving strong discriminative ability with minimal parameter overhead. Extensive experiments on three challenging public datasets (RGBNT201, RGBNT100, and MSVR310) demonstrate the superiority of our approach in terms of both accuracy and efficiency, with 8.4% mAP and 6.9% accuracy improved in RGBNT201 with negligible additional parameters.

---

## 论文详细总结（自动生成）

# 论文总结：基于稀疏混合专家的多模态物体重识别（MFRNet）

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：多模态物体重识别（Multi-modal Object ReID）利用RGB、近红外（NIR）、热红外（TIR）等多种模态的互补信息，在复杂场景（如光照不足、阴影）下提升识别能力。但现有方法存在两大局限：
  - **交互不足**：仅在高层次语义空间进行模态交互，忽略了多模态图像固有的像素级对齐特性，缺乏细粒度跨模态信息交换。
  - **特征失衡**：难以在统一网络中平衡模态共享特征与模态特有特征。共享参数的单骨干网络会丢失模态特有信息，而独立骨干网络则参数冗余、计算量大。
- **整体含义**：本文提出MFRNet，通过引入稀疏混合专家（Sparse Mixture-of-Experts, MoE）范式，同时解决像素级交互和特征平衡问题，实现高效、准确的多模态物体重识别。

## 2. 论文提出的方法论
### 核心思想
- 继承MoE思想，将“专家”分别用于特征生成（融合）和特征表示（提取）。
- 设计两个核心模块：**特征融合模块（FFM）** 和 **特征表示模块（FRM）**，两者均采用MoE结构，实现自适应、细粒度的多模态交互与平衡特征学习。

### 关键技术细节
#### （1）特征融合模块（FFM）
- **目标**：实现像素级跨模态交互，利用多模态图像的空间对齐特性。
- **方法**：
  - 对每个模态（如RGB），利用其他两个模态（NIR、TIR）通过生成专家（Generation Expert）重建成当前模态特征。
  - 每个生成专家是一个简单的卷积层序列（`conv1 -> drop -> conv2`）。
  - 使用MoE组合多个简单生成专家：每个输入token通过余弦路由选择最佳专家（Top-1），生成跨模态特征。
  - 加权融合：通过全局平均池化+线性层生成每个模态的权重（`w(·)`），并经Softmax归一化，与原始特征加权求和。
  - 公式示例（RGB模态重建）：
    \[
    I_g^R = \lambda I^R + w_N(I^N) \cdot g_N(I^N) + w_T(I^T) \cdot g_T(I^T)
    \]
    其中 \(\lambda\) 控制自保留比例（实验中设为0.5）。
  - **模态缺失处理**：若某模态缺失，则其重建仅依赖可用模态生成，无需专门训练。

#### （2）特征表示模块（FRM）
- **目标**：在统一ViT骨干中高效提取模态共享和模态特有特征。
- **方法**：
  - 基于RepAdapter（轻量适配器）插入到ViT残差注意力层之后。
  - 将RepAdapter作为基础专家，使用MoE扩展：多个RepAdapter专家，通过余弦路由（Top-1）动态选择。
  - 公式：\( Z = Y + \text{lmoe\_Ada}(Y_{\text{lnorm}}) \)，其中`lmoe_Ada`是MoE增强的RepAdapter层。
  - 辅助损失 \(L_{\text{aux}}\)（重要损失+负载损失）平衡各专家激活频率，防止专家坍塌。

#### （3）整体损失函数
- 基础损失：标签平滑交叉熵损失 + 三元组损失。
- 两个MoE辅助损失（FFM和FRM各一个）：
  \[
  L = L_{\text{ViT}}^{\text{ce}} + L_{\text{ViT}}^{\text{tri}} + L_{\text{aux}}^{\text{moe1}} + L_{\text{aux}}^{\text{moe2}} + L_{\text{aux}}^{\text{Ada}}
  \]

## 3. 实验设计
### 数据集
- **RGBNT201**：多模态行人重识别，201个身份，4787个三元组（RGB/NIR/TIR）。
- **RGBNT100**：大规模多模态车辆重识别，17250个三元组。
- **MSVR310**：小规模多模态车辆重识别，2087个三元组。

### 评估指标
- mAP, Rank-1/5/10准确率，参数量（Params），计算量（FLOPs）。

### 对比方法
- **单模态方法**：MUDeep, HACNN, MLFN, PCB, OSNet, CAL, TransReID, AGW 等。
- **多模态方法**：HAMNet, PFNet, IEEE, DENet, UniCat, HTT, EDITOR, RSCNet, TOP-ReID, CCNet 等。

## 4. 资源与算力
- 论文明确说明实验在一张NVIDIA V100 GPU上进行，但**未披露具体训练时长**（如小时数）或使用的GPU数量（可能为单卡）。
- 模型参数量为57.1M，FLOPs为22.1G，相比同类模型（如TOP-ReID 278.2M参数）显著更轻量。

## 5. 实验数量与充分性
- **实验充分性评估**：非常充分。
  - **三大数据集全量对比**：在RGBNT201、RGBNT100、MSVR310上与大量方法进行性能对比，并报告mAP和Rank-k。
  - **缺失模态实验**：设计6种模态缺失场景（单模态缺失、双模态缺失），并与TOP-ReID等对比，验证了FFM的模态互补能力。
  - **消融实验**：共11组以上，包括：
    - 模块有效性（基线 vs +FFM vs +FRM vs MFRNet）。
    - FRM专家数量（3/6/9）、位置（第10/11/12层等）。
    - FFM专家数量（1~12）、参数λ（0~1）、位置（0层/3/6/9/12层）。
  - **计算量对比**：与HTT、EDITOR、TOP-ReID对比Params和FLOPs。
  - **专家可视化**：通过热图展示FRM各专家聚焦的语义区域。
- **公平性**：对比方法均为公开基准，代码已开源；使用相同的预训练CLIP-ViT骨干，超参数对齐主流设置。

## 6. 论文的主要结论与发现
- MFRNet在三个数据集上均达到**最先进水平**：
  - RGBNT201：mAP 80.7%（+8.4%），Rank-1 83.5%（+6.9%）。
  - RGBNT100：mAP 88.2%（+5.9%），Rank-1 97.4%。
  - MSVR310：mAP 50.6%（+11.1%），Rank-1 64.8%。
- 在**模态缺失场景**下，MFRNet无需专门训练即可自适应补偿，平均mAP较TOP-ReID提升4.7%。
- **参数效率**：参数量仅57.1M（< TOP-ReID的1/4），FLOPs仅22.1G。
- **FRM可视化**显示：不同专家自动学习共享语义（如行人区域）或模态特有特征（如特定模态的背景），验证了平衡机制的生效。

## 7. 优点
1. **创新性强**：将稀疏MoE首次系统性地引入多模态重识别的特征融合与表示，解决了两大核心挑战（像素级交互与特征平衡）。
2. **设计精巧**：FFM利用模态间线性变换特性，用简单生成专家组合实现复杂跨模态生成，参数高效；FRM通过轻量RepAdapter专家，在保持共享表示的同时保留模态特异性。
3. **鲁棒性**：自然适应模态缺失场景，无需额外训练或架构调整，实用价值高。
4. **实验结果全面**：提供了大量消融、参数分析和可视化，验证了各模块的有效性。
5. **计算成本低**：与同类ViT方法相比，参数和FLOPs显著减少，便于实际部署。

## 8. 不足与局限
1. **实验覆盖**：仅验证了RGB、NIR、TIR三种特定模态，未涵盖深度图、事件相机等其他常见模态；数据集规模相对较小（最大1.7万样本），泛化性需在更大规模多模态数据集（如多模态行人重识别大规模基准）中进一步验证。
2. **偏差风险**：专家分配依赖路由机制，可能存在对某些模态或语义的偏好（虽通过辅助损失平衡，但未完全消除）；在极其类间相似度高的场景（如同款同色车辆），仅凭模态融合可能仍不足。
3. **缺少训练时间统计**：未明确报告训练所需时间或收敛速度，影响算力需求评估。
4. **应用限制**：假设多模态图像已严格对齐（像素级对齐），实际应用中可能存在配准误差；FFM的生成专家依赖简单卷积，对于复杂场景（如强遮挡、大视角变化）的跨模态生成能力可能有限。
5. **消融分析中**：FRM专家数6时最优，但未给出专家数大于6后性能下降的深入解释（论文仅推测可能过度关注特异性而损失共享知识），可进一步分析路由分布。

（完）
