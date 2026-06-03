---
title: "FlexiReID: Adaptive Mixture of Expert for Multi-Modal Person Re-Identification"
title_zh: FlexiReID：面向多模态行人重识别的自适应专家混合模型
authors: "Zhen Sun, Lei Tan, Yunhang Shen, Chengmao Cai, Xing Sun, Pingyang Dai, Liujuan Cao, Rongrong Ji"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=dewR2augg2"
tags: ["query:balanced-mml"]
score: 8.0
evidence: 自适应专家混合实现动态模态整合
tldr: 现有跨模态行人重识别方法仅支持有限模态组合，缺乏灵活性。本文提出FlexiReID，采用自适应专家混合机制动态融合RGB、红外、素描和文本四种模态特征，支持七种检索模式。在统一数据集上的实验表明，FlexiReID在多种跨模态场景下均取得最优结果，为多模态行人重识别提供了灵活高效的解决方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-dewr2augg2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 717, \"height\": 934, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dewr2augg2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1541, \"height\": 839, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dewr2augg2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 712, \"height\": 293, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dewr2augg2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 715, \"height\": 292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dewr2augg2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 842, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dewr2augg2/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 665, \"height\": 1019, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1774, \"height\": 868, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 894, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1775, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 559, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 485, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1768, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1065, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dewr2augg2/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1061, \"height\": 268, \"label\": \"Table\"}]"
motivation: 现有跨模态行人重识别局限于少数模态组合，无法灵活支持任意查询-检索配对。
method: 提出FlexiReID框架，利用自适应专家混合机制动态融合多种模态特征，并设计跨模态查询融合模块。
result: 在扩展的CIRS-PEDES数据集上，FlexiReID在七个检索模式下均达到最优性能。
conclusion: 自适应专家混合机制有效提升了多模态行人重识别的灵活性和准确性。
---

## Abstract
Multimodal person re-identification (Re-ID) aims to match pedestrian images across different modalities. However, most existing methods focus on limited cross-modal settings and fail to support arbitrary query-retrieval combinations, hindering practical deployment. We propose FlexiReID, a flexible framework that supports seven retrieval modes across four modalities: RGB, infrared, sketches, and text. FlexiReID introduces an adaptive mixture-of-experts (MoE) mechanism to dynamically integrate diverse modality features and a cross-modal query fusion module to enhance multimodal feature extraction. To facilitate comprehensive evaluation, we construct CIRS-PEDES, a unified dataset extending four popular Re-ID datasets to include all four modalities. Extensive experiments demonstrate that FlexiReID achieves state-of-the-art performance and offers strong generalization in complex scenarios.

---

## 论文详细总结（自动生成）

# FlexiReID 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：现有跨模态行人重识别（Re-ID）方法仅支持有限模态组合（如文本→RGB、红外→RGB等），无法灵活处理任意查询-检索配对组合（如同时使用文本+素描+红外进行检索），限制了实际部署中的适应性和信息利用率。
- **研究动机**：在实际监控场景中，经常同时获得多种模态信息（RGB、红外、素描、文本），若仅使用单一模态或固定配对，会浪费多模态信息的互补优势。因此，需要建立一个统一的框架，支持在任意模态组合下进行灵活检索。
- **研究背景**：现有工作包括单模态ReID和跨模态ReID（如文本→RGB、素描→RGB、红外→RGB等），但均局限于特定配对。多模态融合方法（如TriReID）也仅处理特定组合。本文首次提出“灵活检索”概念，涵盖四种模态、七种检索模式。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 2.1 核心思想
- 构建一个统一的双编码器框架（基于CLIP ViT-B/16），所有视觉模态（RGB、红外、素描）共享一个图像编码器，文本模态使用独立的文本编码器。
- 引入**自适应专家分配混合专家（AEA-MoE）**机制，根据输入特征的置信度动态选择不同数量的专家网络，以更好地提取不同模态的特征。
- 设计**跨模态查询融合（CMQF）**模块，利用可学习嵌入特征补偿缺失模态，并融合多模态特征，生成七种组合的融合特征。

### 2.2 关键技术细节
- **AEA-MoE**：
  - 传统Top-K路由固定选择K个专家；AEA-MoE设定一个置信度阈值，首先比较最高专家置信度与阈值，若超过则只激活该专家；否则按置信度降序依次激活专家，直到累计置信度超过阈值。
  - 公式：\( P = \text{Softmax}(W_r \cdot x^T) \)，\( g_i(x) = P_i \) if Adapter i ∈ S else 0，\( y = \sum_i g_i(x) \cdot \text{Adapter}_i(x) \)。
  - 引入自适应损失 \( L_{ada} = -\sum_i P_i \log P_i \) 来约束专家激活的最小集，鼓励稀疏性。
- **CMQF**：
  - 将各模态特征输入各自的Transformer块，其中查询特征由其他模态特征之和生成（如 \( y_s = TL_s((X_{ir}+X_t)W_Q, X_sW_K, X_sW_V) \)）。
  - 对缺失模态使用可学习嵌入特征（LEF）进行补偿。
  - 将所有输出特征拼接后送入共享Transformer块，再通过平均池化得到最终融合特征。
- **优化与推理**：
  - 冻结预训练模型中的Patch Embedding、Word Embedding、Multi-Head Attention，仅训练AEA-MoE、CMQF和可学习嵌入特征。
  - 使用相似性分布匹配（SDM）损失（双向KL散度）进行跨模态对比学习，总损失为七种检索任务的SDM损失之和加上自适应损失。
  - 推理时，对缺失模态分配可学习嵌入特征，计算融合特征与RGB图像特征的相似度，输出Top-K结果。

## 3. 实验设计

### 3.1 使用数据集与benchmark
- **基础数据集**：CUHK-PEDES、ICFG-PEDES、RSTPReid（原始含RGB和文本）、SYSU-MM01（原始含RGB和红外）。
- **扩展为CIRS-PEDES**：通过StyleGAN3生成素描模态，InfraGAN生成红外模态，GPT-4生成文本描述（对SYSU-MM01），使每个数据集覆盖四种模态。
- **评估协议**：采用Rank-k匹配准确率（R@1, R@5, R@10）、平均精度（mAP）和平均逆负惩罚（mINP）。

### 3.2 对比方法
- **文本→RGB任务**：CMPM/C, MIA, ViTAA, NAFS, DSSL, SSAN, Han et al., LBUL+BERT, SAF, TIPCB, CAIBC, AXM-Net, LGUR, IVT, UNIReID, CFine, CSKT。
- **素描→RGB任务**：Sketch Trans+, DALNet, UNIReID。
- **红外→RGB任务**：GUR, SDCL。
- **多模态融合任务（T+S→R等）**：对比UNIReID。
- **SYSU-MM01**：对比SSFT, DDAG, DG-VAE, CICL+IAMA, VCD+VML, MPANet, MCLNet, SMCL, UNIReID等。

### 3.3 消融实验与附加验证
- **消融组件**：对比Zero-shot CLIP、MLP-Adapter、AEA-MoE（有无自适应损失）、CMQF（有无LEF）在R@1上的平均表现。
- **路由策略**：对比Top-K、Soft、Hash路由。
- **特征融合策略**：对比拼接、求和、层次融合。
- **超参数分析**：专家数量（2-10）和阈值置信度（0.1-1.0）的影响。
- **附加实验**：
  - 将AEA-MoE分别应用于图像编码器、文本编码器、两者。
  - 在PKU-Sketch数据集上验证（素描→RGB）。
  - 在Market-1501和MSMT17上验证传统RGB→RGB任务（使用可学习嵌入补偿缺失模态）。

## 4. 资源与算力
- **文中有明确说明**：实验在单个NVIDIA 3090 24GB GPU上进行。
- **训练配置**：Batch size 64，每batch随机选取64个身份，每个身份包含素描、红外、文本、RGB各一个样本。图像尺寸384×128，文本序列长度77。使用Adam优化器，初始学习率1e-5，余弦衰减，训练60个epoch。
- **关键参数**：专家数量n=6，阈值置信度0.6（消融部分调整为0.4），自适应损失权重λ=0.5。

## 5. 实验数量与充分性
- **实验数量充分**：涵盖三个原始文本+RGB数据集（CUHK、ICFG、RSTP）和一个红外+RGB数据集（SYSU-MM01），每个数据集均评估七种检索模式，共约28组性能对比。此外，包含多组消融实验（组件、路由、融合、超参数）、附加实验（PKU-Sketch、Market-1501/MSMT17）。
- **公平性与客观性**：
  - 对比方法均来自权威会议期刊（ECCV、CVPR、AAAI、ICCV等），且尽量复现或引用其官方指标。
  - 消融实验设置了多个对照基线（如Zero-shot CLIP、传统MoE），逐步验证每个模块贡献。
  - 超参数分析通过曲线展示选择依据，避免调参过拟合。
- **不足**：未在更多真实噪声场景（如低分辨率、遮挡严重）下测试；生成数据（StyleGAN3、InfraGAN、GPT-4）的质量可能影响模型真实泛化能力；缺乏与其他多模态框架（如多分支网络）的直接对比。

## 6. 论文的主要结论与发现
- FlexiReID首次实现四种模态任意组合的灵活检索，在七种检索任务上均达到或接近当前最优（SOTA）性能。
- 自适应专家混合机制（AEA-MoE）相比固定Top-K路由，能根据输入特征动态调整专家数量，更高效地提取多模态特征。
- 跨模态查询融合模块（CMQF）结合可学习嵌入特征，有效补偿缺失模态并融合多源信息，使多模态融合检索显著优于单模态检索（如T+S+IR→R的R@1比单模态高约3-20%）。
- 在标准RGB→RGB任务（Market-1501、MSMT17）上，FlexiReID同样取得领先，表明其通用性强。

## 7. 优点
- **创新性**：首次提出“灵活检索”概念，突破传统固定配对限制，开创新研究方向。
- **技术亮点**：自适应专家选择算法（AEA-MoE）动态调整计算资源；CMQF模块利用可学习嵌入解决模态缺失问题，设计简洁有效。
- **实验全面**：覆盖四个主流数据集、七种检索模式、多种消融与附加实验，验证了方法在不同场景下的鲁棒性。
- **资源效率**：仅训练少量模块（冻结大部分预训练权重），在单GPU上即可完成训练，实用性强。

## 8. 不足与局限
- **数据依赖**：素描和红外模态通过生成模型（StyleGAN3、InfraGAN）合成，文本通过GPT-4生成，这些生成数据的风格与真实数据可能存在差异，影响模型在真实场景中的泛化性能。
- **计算复杂度**：AEA-MoE和CMQF增加了额外参数和推理开销（但文中未提供详细计算量对比）。
- **场景覆盖**：实验未考虑极端光照、遮挡、低分辨率等复杂情况；也未测试跨数据集的域迁移性能。
- **对比完整性**：部分多模态融合任务（如T+IR→R）仅与UNIReID对比，缺乏更多基线方法。
- **应用限制**：模型依赖CLIP预训练，对于未见过的新模态（如深度图）无法直接扩展；可学习嵌入特征针对固定四种模态，扩展更多模态需重新设计。

（完）
