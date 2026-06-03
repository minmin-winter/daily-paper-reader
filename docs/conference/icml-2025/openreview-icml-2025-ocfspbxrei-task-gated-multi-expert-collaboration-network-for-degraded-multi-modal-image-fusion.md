---
title: Task-Gated Multi-Expert Collaboration Network for Degraded Multi-Modal Image Fusion
title_zh: 任务门控多专家协作网络用于退化多模态图像融合
authors: "Yiming Sun, Xin Li, Pengfei Zhu, Qinghua Hu, Dongwei Ren, Huiying Xu, Xinzhong Zhu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=OcFsPBXREI"
tags: ["query:balanced-mml"]
score: 8.0
evidence: 多模态图像融合中的任务门控多专家协作实现均衡融合
tldr: 本文针对退化环境下的多模态图像融合问题，提出了任务门控多专家协作网络TG-ECNet，通过退化感知门控动态分配专家进行前处理恢复，并利用任务门控进行自适应融合。该方法能处理噪声、模糊、条纹等多种退化，在多个基准上取得了最优融合效果，增强了感知能力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 860, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1765, \"height\": 724, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 851, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1737, \"height\": 721, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1776, \"height\": 1029, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1772, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1774, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 893, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1782, \"height\": 611, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1775, \"height\": 487, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 458, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1765, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1771, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1521, \"height\": 119, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 856, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 859, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1767, \"height\": 495, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1767, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1769, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1765, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1768, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1767, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1766, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1768, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1767, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1327, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1327, \"height\": 431, \"label\": \"Table\"}]"
motivation: 真实多模态图像融合常受退化（噪声、模糊等）影响，现有方法未考虑退化类型差异。
method: 提出任务门控多专家协作网络，通过退化感知门控动态分配专家组进行恢复，再基于任务门控进行融合。
result: 在多个退化场景下实现了高质量融合，优于现有方法。
conclusion: TG-ECNet通过任务感知门控有效提升了退化多模态图像的融合质量。
---

## Abstract
Multi-modal image fusion aims to integrate complementary information from different modalities to enhance perceptual capabilities in applications such as rescue and security. However, real-world imaging often suffers from degradation issues, such as noise, blur, and haze in visible imaging, as well as stripe noise in infrared imaging, which significantly degrades model performance. To address these challenges, we propose a task-gated multi-expert collaboration network (TG-ECNet) for degraded multi-modal image fusion. The core of our model lies in the task-aware gating and multi-expert collaborative framework, where the task-aware gating operates in two stages: degradation-aware gating dynamically allocates expert groups for restoration based on degradation types, and fusion-aware gating guides feature integration across modalities to balance information retention between fusion and restoration tasks. To achieve this, we design a two-stage training strategy that unifies the learning of restoration and fusion tasks. This strategy resolves the inherent conflict in information processing between the two tasks, enabling all-in-one multi-modal image restoration and fusion. Experimental results demonstrate that TG-ECNet significantly enhances fusion performance under diverse complex degradation conditions and improves robustness in downstream applications. The code is available at https://github.com/LeeX54946/TG-ECNet.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义（研究动机和背景）

- **问题**：多模态图像融合（如可见光与红外）在救援、安防等应用中至关重要，但真实成像常受噪声、模糊、雾霾、条纹噪声等多种退化干扰，严重降低融合质量。现有方法要么级联恢复和融合（恢复可能丢失融合有用特征，融合可能放大恢复错误），要么仅针对特定退化（如单一雾或噪声），缺乏统一处理多种复合退化的能力。
- **动机**：提出一个能够自适应识别退化类型并同时完成恢复与融合的端到端框架，以提升在复杂退化环境下的鲁棒性和融合质量。

### 2. 方法论：核心思想、关键技术细节

- **核心思想**：任务门控多专家协作网络（TG-ECNet），通过**退化感知门控**动态分配专家组进行图像恢复，再通过**融合感知门控**引导多模态特征选择性融合，采用**两阶段训练策略**消除恢复与融合任务之间的信息冲突。
- **技术细节**：
  - 骨干网络：基于U-shape Transformer（Restormer）的编码器-解码器结构，红外和可见光分支共享权重。
  - 第一阶段（恢复）：输入退化图像，经退化感知门控（基于全局平均池化+SoftMax生成任务提示）动态选择K个专家（MoE）处理，输出恢复图像。
  - 第二阶段（融合）：冻结第一阶段恢复部分参数，将恢复后的可见光与红外特征用可学习权重（α, β）融合，再经融合感知门控和MoE模块进行特征整合，输出最终融合图像。
  - 损失函数：第一阶段：恢复损失（L1）+ 梯度损失 + 加载损失；第二阶段：像素损失 + 梯度损失 + 加载损失。
  - 专家数量N=11，选定K=6（经实验确定）。

### 3. 实验设计：数据集、Benchmark、对比方法

- **数据集**：
  - **DeMMI-RF**（自建）：包含26,631训练样本和9,895测试样本，涵盖6种退化类型（高斯噪声σ=15/25/50、雾、离焦模糊、条纹噪声），包括城市街景和低空无人机视角。
  - **EMS**：公开数据集，用于跨数据集验证。
  - **AWMM**：真实世界雾天数据，用于定性评估。
- **对比方法**：
  - 联合恢复与融合方法：AWFusion、DRMF、Text-IF。
  - 纯融合方法：DenseFuse、SwinFuse、CDDFuse、SeAFusion、MGDN、EMMA（这些方法先用通用恢复模型AdaIR预处理退化图像）。
- **评估指标**：CC、MSE、PSNR、Nabf、MS-SSIM。下游任务：YOLOv5目标检测（mAP50、AP(0.5:0.95)）、Grounded-SAM语义分割。

### 4. 资源与算力

- **硬件**：6块NVIDIA GeForce RTX 4090 GPU。
- **软件**：PyTorch 1.12.0，Adam优化器，初始学习率1e-4，余弦退火策略。
- **训练设置**：图像随机裁剪至128×128，每阶段30个epoch（共60 epoch），批量大小未明确提及，但典型设置下总训练时间约为数十小时量级（论文未给出具体时钟时间）。

### 5. 实验数量与充分性

- **实验组数**：涵盖5种单一退化（噪声3种、雾、模糊、条纹）、9种退化组合、无退化场景、真实世界场景，以及下游检测和分割共约15+组定量对比，加上消融实验（5组），以及专家超参数优化（2组）。总计约20+组实验。
- **充分性**：实验设计全面，覆盖了单退化、多退化、无退化、真实数据，并在两个数据集上验证跨域泛化性。消融实验逐一验证了门控、MoE、两阶段训练的关键性。对比方法覆盖了主流SOTA，且对无恢复能力的融合方法采用了统一恢复预处理以公平比较。实验结论客观、有说服力。

### 6. 主要结论与发现

- TG-ECNet在所有退化场景（单任务及多任务混合）下均取得最优或接近最优的融合质量（PSNR、MS-SSIM等指标显著超越对比方法）。
- 在下游任务（检测、分割）中，TG-ECNet生成的融合图像提升了目标检测mAP50（0.969）和分割准确性（更精确的轮廓），验证了实际应用价值。
- 两阶段训练策略有效消除了恢复与融合间的冲突，消融实验表明每项组件（门控、MoE、两阶段）均对最终性能有贡献。

### 7. 优点

- **方法亮点**：
  - 统一处理多种退化类型，无需提前知道退化类型。
  - 任务门控机制动态调整专家分配，实现自适应恢复与融合。
  - 两阶段训练解耦任务，避免信息冲突。
  - 构建了大规模多退化多模态数据集DeMMI-RF，填补了领域空白。
- **实验亮点**：
  - 对比方法覆盖全面，且对纯融合方法采用统一恢复预处理以公平比较。
  - 下游任务验证（检测、分割）增强了方法的实际意义。
  - 附带了专家超参数消融分析，证明设计选择合理。

### 8. 不足与局限

- **计算开销**：模型参数量约160M，FPS仅1.03（4090），略低于部分轻量融合方法（如DenseFuse 1.64 fps），但优于DRMF（0.2 fps）。在实时应用中可能受限。
- **专家数量依赖启发式**：N=11, K=6通过实验确定，缺乏理论指导，且选择过程可能随退化类型增多需要重新调整。
- **真实退化测试有限**：仅用AWMM一个真实数据集定性验证，未在更广泛真实场景（如不同传感器、天气条件）定量评估。
- **退化类型覆盖**：当前数据集仅包含6种退化，实际场景中可能存在其他退化（如运动模糊、低光照、低对比度等），模型泛化到未知退化类型的能力未经测试。
- **两阶段训练繁琐**：需要交替冻结参数，流程较复杂，且损失函数超参数（加权系数）未详细讨论。

（完）
