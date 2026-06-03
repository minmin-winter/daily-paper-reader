---
title: "Visual Attention Never Fades: Selective Progressive Attention ReCalibration for Detailed Image Captioning in Multimodal Large Language Models"
title_zh: 视觉注意力永不褪色：面向多模态大模型详细图像描述的选择性渐进式注意力重校准
authors: "Mingi Jung, Saehyung Lee, Eunji Kim, Sungroh Yoon"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=zuXCQRhbl4"
tags: ["query:balanced-mml"]
score: 5.0
evidence: 增强视觉令牌贡献以平衡模态
tldr: 针对多模态大模型在详细图像描述中视觉注意力随文本增长而衰减的问题，本文提出SPARC方法，通过选择性渐进式注意力重校准在解码过程中增强视觉令牌的贡献，以平衡视觉与文本信息的利用。实验表明该方法在不增加训练成本的情况下显著提升了描述的质量和精确度。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 862, \"height\": 331, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 370, \"height\": 281, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 846, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 403, \"height\": 291, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 783, \"height\": 216, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 870, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 866, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 867, \"height\": 322, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 511, \"height\": 516, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 504, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 503, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 472, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1553, \"height\": 2161, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 340, \"height\": 640, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 478, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1734, \"height\": 586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1063, \"height\": 1140, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1147, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1286, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zuxcqrhbl4/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1374, \"height\": 483, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 647, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 713, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 669, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 663, \"height\": 204, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 822, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 846, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1553, \"height\": 2161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 461, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1195, \"height\": 472, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1141, \"height\": 472, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1140, \"height\": 471, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 613, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 796, \"height\": 185, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zuxcqrhbl4/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 848, \"height\": 312, \"label\": \"Table\"}]"
motivation: 多模态大模型在长响应中视觉注意力减弱且噪声增加，导致图像描述质量下降。
method: 提出SPARC，一种无需训练的渐进式注意力重校准方法，选择性增强视觉令牌在解码时的贡献。
result: 实验表明SPARC显著提升了详细图像描述的精确度和召回率。
conclusion: SPARC为改善多模态大模型视觉语言平衡提供了一种高效方案。
---

## Abstract
Detailed image captioning is essential for tasks like data generation and aiding visually impaired individuals. High-quality captions require a balance between precision and recall, which remains challenging for current multimodal large language models (MLLMs). In this work, we hypothesize that this limitation stems from weakening and increasingly noisy visual attention as responses lengthen. To address this issue, we propose SPARC (Selective Progressive Attention ReCalibration), a training-free method that enhances the contribution of visual tokens during decoding. SPARC is founded on three key observations: (1) increasing the influence of all visual tokens reduces recall; thus, SPARC selectively amplifies visual tokens; (2) as captions lengthen, visual attention becomes noisier, so SPARC identifies critical visual tokens by leveraging attention differences across time steps; (3) as visual attention gradually weakens, SPARC reinforces it to preserve its influence. Our experiments, incorporating both automated and human evaluations, demonstrate that existing methods improve the precision of MLLMs at the cost of recall. In contrast, our proposed method enhances both precision and recall with minimal computational overhead.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

多模态大语言模型（MLLMs）在详细图像描述任务中面临一个重要挑战：生成的描述需要在**精确度**（描述内容与图像实际内容一致）和**召回率**（覆盖图像中所有重要元素）之间取得平衡。现有方法往往只关注降低幻觉（提升精确度），却以牺牲召回率为代价，导致描述虽然准确但遗漏细节。论文通过实验发现，MLLMs在生成长文本时，对视觉令牌的注意力会逐渐减弱，同时噪声增加，这是导致描述质量下降的根本原因。因此，论文旨在提出一种无需训练的方法，在不显著增加计算开销的前提下，同时提升精确度和召回率。

## 2. 方法论：核心思想、关键技术细节

### 2.1 核心思想
论文提出**SPARC（Selective Progressive Attention ReCalibration，选择性渐进式注意力重校准）**，一种训练-free的解码增强方法。其核心思想是：在文本生成过程中，**选择性增强关键视觉令牌的贡献**，并**通过累加机制抵消长文本中视觉注意力的自然衰减**。

### 2.2 关键技术细节
- **令牌选择（Token Selection）：使用“相对激活得分”**  
  计算每个视觉令牌当前注意力权重与其指数移动平均（EMA）趋势的**相对变化**，而非绝对大小，以抵抗噪声：  
  \[
  r_{i,j}^{(l)} = \frac{a_{i,j}^{(l)} - \tilde{a}_{i-1,j}^{(l)}}{\tilde{a}_{i-1,j}^{(l)}}
  \]  
  其中 \(\tilde{a}_{i-1,j}^{(l)}\) 是上一层EMA后的平滑注意力。设置阈值 \(\tau\)，得分超过 \(\tau\) 的令牌被选为“关键令牌”。

- **渐进式注意力重校准（Progressive ReCalibration）**  
  维护每个视觉令牌的**选择次数** \(c_{i,j}\)，表示到当前步骤为止该令牌被选中的累积次数。在每一步生成时，对选中令牌的注意力权重进行缩放：  
  \[
  a_{i,j}^{(l)} \leftarrow a_{i,j}^{(l)} \cdot \alpha^{c_{i,j}}
  \]  
  其中 \(\alpha > 1\) 为缩放参数。这确保一直重要的令牌获得持续增强，抵消长上下文中的注意力衰退。实际操作中，可通过直接缩放值向量（Value Vector）实现，利用key-value缓存，无额外内存开销。

- **整体流程**（文字说明）：
  1. 针对当前生成步骤i，计算所有视觉令牌相对激活得分；
  2. 根据阈值筛选出关键令牌集合 \(S_i\)；
  3. 更新每个令牌的选择计数 \(c_{i,j}\)；
  4. 对所有选中的令牌，将其值向量乘以 \(\alpha\)（等价于放大注意力权重）；
  5. 继续正常解码。

## 3. 实验设计

### 3.1 数据集
- **CLAIR评估**：IIW-400（400对）和DOCCI（15K对，评估时随机抽取500样本），提供高度详细、无幻觉的参考描述。
- **CHAIR评估**：MS-COCO 2014验证集，有对象标注。
- **人类评估**：从IIW-400中随机抽取100个样本。

### 3.2 Benchmark
- **CLAIR**：使用GPT-4o评价生成描述与参考描述的对齐质量，得分越高越好。
- **CHAIR**（包括CHAIR_s、CHAIR_i）、精确度、召回率、F1得分。精确度 = 1 - CHAIR_i，召回率 = 正确识别对象比例。
- **人类评估**：由人类标注者比较不同方法在精确度和召回率上的偏好，统计胜率。

### 3.3 对比方法
- **基线**：LLaVA-1.5、LLaVA-Next、Qwen2-VL（均为7B规模）。
- **现有方法**：OPERA、VCD、VOLCANO、PAI（均为幻觉缓解方法）。
- **消融变体**：无令牌选择（全增强）、无EMA（仅用上一步注意力）。

## 4. 资源与算力

论文未明确训练时长（因SPARC无需训练，仅在推理时施加轻量计算）。在效率对比实验中，提到使用**RTX8000 GPU**（单卡）。实际推理时，SPARC额外开销仅为存储每层所有视觉令牌的EMA注意力（约40KB），以及微小的缩放操作。生成时间仅比基线增加约2.8%（从30.37ms/token增至31.21ms/token），远低于其他对比方法（例如OPERA增加961%）。

## 5. 实验数量与充分性

### 实验数量
- **主要表格**：共4个CLAIR对比表（两个数据集×两个模型对比）、1个CHAIR对比表（重复5次随机抽样）、1个人类评估图、1个效率表、1个区域注意力分析表、多个消融表（超参数、组件）。
- **消融实验**：包含4组超参数（层、阈值、平滑系数、缩放因子）的网格搜索，以及组件消融（有无令牌选择、有无EMA）。
- **跨模型验证**：在3个不同架构（LLaVA-1.5、LLaVA-Next、Qwen2-VL）上均获得一致性提升。
- **附录**额外提供定性样例、注意力可视化、多样性分析等。

### 充分性与公平性
- **充分性**：实验覆盖了主流评估指标、多个数据集、多种模型架构、以及详细消融，足够支撑结论。
- **客观公平**：对比方法均按原论文超参数设置；基线重复多次取平均；CHAIR评估重复5次减少随机性；人类评估使用独立标注者。论文承认超参数需针对模型微调（但轻量可调），且方法在部分指标（如CHAIR_s）上未达最优，但整体F1最优，说明权衡合理。

## 6. 主要结论与发现

- **现有方法的缺陷**：现有幻觉缓解方法（OPERA、VCD、VOLCANO、PAI）虽然提升了精确度，但显著降低了召回率（PAI召回率下降约7%），导致F1下降或微弱提升。
- **SPARC的优势**：是唯一**同时提升精确度和召回率**的方法。在LLaVA-1.5上，F1从81.99提升至83.67；在不同模型上CLAIR得分均有提升（+1.36 ~ +6.08）。
- **注意力机制分析**：SPARC成功缓解了长文本中视觉注意力的衰减，并使注意力更聚焦于语义相关区域（相关区域注意力占比从17.85%提升至19.17%，而朴素增强法降至15.50%），同时避免放大注意力沉没（attention sink）令牌。
- **效率**：SPARC计算开销极低（生成时间仅增2.8%），远优于对比方法。
- **无训练**：作为训练-free方法，可直接应用于任何基于注意力的MLLMs。

## 7. 优点

- **平衡精确度与召回率**：解决了一个被忽视的重要矛盾，实际应用价值高。
- **无需训练**：可即插即用，降低部署成本。
- **低计算开销**：仅需存储EMA和进行简单缩放，推理速度几乎不变。
- **理论分析与实验验证一致**：通过注意力多样性、噪声化、衰退三个角度详细论证了现有方法失效的原因，并针对性地设计机制。
- **稳健性**：在三个不同架构和多个数据集上均取得一致改进。
- **人类评估**：验证了方法的实际偏好，增强说服力。

## 8. 不足与局限

- **超参数调整**：关键参数（层、阈值、平滑系数、缩放因子）需针对不同模型微调。虽然轻量（几十次推理即可确定），但仍需用户一定的探索成本。
- **早期幻觉抑制有限**：由于渐进累加机制主要作用于后续生成令牌，对早期出现的幻觉抑制效果有限，导致CHAIR_s指标提升不明显（甚至略高于基线）。论文对此有明确讨论。
- **实验范围**：仅测试了7B规模模型，未在更大/更小模型上验证；仅针对图像描述任务，未在VQA等任务上测试通用性（附录仅有少量POPE实验）。
- **依赖注意力可靠性**：方法有效性建立在注意力权重可信的基础上。若模型注意力本身高度偏移（如严重注意力沉没），选择机制可能受影响（论文通过注意力沉没分析验证了稳健性，但未覆盖极端场景）。
- **仅适用于自回归解码的MLLMs**：不适用于非注意力机制或并行解码模型。

（完）
