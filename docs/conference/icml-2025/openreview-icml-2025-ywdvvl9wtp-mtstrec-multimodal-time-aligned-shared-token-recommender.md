---
title: "MTSTRec: Multimodal Time-Aligned Shared Token Recommender"
title_zh: MTSTRec：多模态时间对齐共享令牌推荐器
authors: "Ming-Yi Hong, Yen-Jung Hsu, Miao-Chen Chiang, Che Lin"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=yWDvVl9Wtp"
tags: ["query:unified-mm"]
score: 6.0
evidence: 时间对齐的共享令牌实现推荐中的高效跨模态融合
tldr: 本文针对现有推荐方法忽略多模态数据时间对齐的问题，提出多模态时间对齐共享令牌推荐器（MTSTRec）。为每个产品生成单一时间对齐的共享令牌，高效融合文本、视觉和价格信息。实验表明MTSTRec达到最先进效果。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ywdvvl9wtp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1258, \"height\": 885, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ywdvvl9wtp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 702, \"height\": 260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ywdvvl9wtp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1540, \"height\": 359, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1266, \"height\": 731, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1774, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1622, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1759, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 683, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1609, \"height\": 523, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 825, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 641, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 634, \"height\": 170, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 787, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1613, \"height\": 175, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1296, \"height\": 335, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 901, \"height\": 145, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ywdvvl9wtp/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 997, \"height\": 145, \"label\": \"Table\"}]"
motivation: 现有推荐模型忽略了用户浏览序列中多模态数据的时间对齐。
method: 提出时间对齐的共享令牌，实现跨模态高效融合。
result: 在推荐任务上达到最先进性能。
conclusion: 时间对齐的多模态融合有效提升推荐质量。
---

## Abstract
Sequential recommendation in e-commerce utilizes users' anonymous browsing histories to personalize product suggestions without relying on private information. Existing item ID-based methods and multimodal models often overlook the temporal alignment of modalities like textual descriptions, visual content, and prices in user browsing sequences. To address this limitation, this paper proposes the Multimodal Time-aligned Shared Token Recommender (MTSTRec), a transformer-based framework with a single time-aligned shared token per product for efficient cross-modality fusion. MTSTRec preserves the distinct contributions of each modality while aligning them temporally to better capture user preferences. Extensive experiments demonstrate that MTSTRec achieves state-of-the-art performance across multiple sequential recommendation benchmarks, significantly improving upon existing multimodal fusion. Our code is available at https://github.com/idssplab/MTSTRec.

---

## 论文详细总结（自动生成）

# MTSTRec 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：现有的序列推荐系统（SRS）主要依赖单一模态数据（如产品ID），忽略了多模态信息（文本描述、图像、价格等）的丰富性。更重要的是，现有多模态融合方法（早期融合、晚期融合）未能有效处理不同模态在用户浏览序列中的**时间对齐**问题，导致跨模态交互受限，无法充分利用各模态的互补信息。
- **核心问题**：如何在序列推荐中实现多模态特征的高效、时间对齐的融合，以更准确地捕捉用户偏好。
- **整体含义**：提出MTSTRec框架，通过**时间对齐的共享令牌（Time-aligned Shared Token, TST）** 在每个时间步对齐不同模态的特征，保留各模态独有贡献的同时促进跨模态交互，从而显著提升推荐性能。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
- 为每个产品在序列的每个时间步分配一个**共享令牌**，该令牌负责跨模态的信息交换，且保持时间顺序一致性（即同一时间步的不同模态对应同一个产品）。
- 采用**中期融合（Mid-fusion）** 策略：先让各模态独立通过自注意力编码器提取模态特定特征，再通过TST模块进行跨模态交互，最后融合输出。

### 关键技术细节
1. **特征提取器**：
   - **ID提取器**：嵌入矩阵查找。
   - **风格提取器**：使用VGG-19的前两层计算Gram矩阵，捕获图像纹理和颜色模式，再通过最大池化压缩为512维风格嵌入。
   - **文本提取器**：使用Llama 3.1将产品标题和描述编码为4096维嵌入，再通过线性投影降维。
   - **提示文本提取器**：利用LLM（Llama 3.1或GPT-4o-mini）通过5种不同提示（如释义、标签、猜测、推荐释义、推荐标签）生成额外文本，并通过门控网络（Gating Network）动态加权融合。
   - **价格提取器**：采用SCANE方法（可缩放数值嵌入），将价格归一化后乘以嵌入矩阵。

2. **多模态Transformer与TST融合**：
   - 每个模态独立经过自注意力编码器（Transformer块），包含多头自注意力、层归一化、MLP和残差连接。
   - 在每个时间步，模态特定令牌（`z_mod`）与共享令牌（`z_sh`）拼接后输入自注意力层。
   - 共享令牌在每层结束后通过**平均所有模态的对应令牌**更新，从而传递跨模态信息。
   - 最终预测时，各模态的CLOZE令牌（`zcz`）拼接形成联合表示，用于计算与目标及负样本的余弦相似度。

3. **损失函数**：二元交叉熵损失（BCE），最大化与正样本的余弦相似度，最小化与负样本的相似度。

### 公式/算法流程（文字说明）
- 输入：用户历史序列S，每个物品含ID、图像、文本、价格。
- 步骤：
  1. 各模态特征提取器生成嵌入矩阵（E_id, E_style, E_text, E_pt, E_price）。
  2. 添加位置编码和CLOZE令牌，得到Z_id, Z_style, ...。
  3. 各模态独立经过自注意力编码器。
  4. 进入TST融合编码器（L层）：每层中，模态特定令牌与共享令牌拼接后自注意力，然后更新模态令牌和共享令牌（共享令牌取所有模态平均）。
  5. 将各模态的CLOZE令牌拼接得到z_output。
  6. 计算余弦相似度与BCE损失。

## 3. 实验设计

### 数据集
- **Food E-commerce**（专有，公开）：食品电商，770个产品，216,576个会话，平均会话长度4.693。
- **House-Hold E-commerce**（专有，公开）：家居电商，2,464个产品，12,345个会话。
- **H&M (Trousers)**（公开）：服装（裤子）购买记录，11,150个产品，416,794个会话。
- 所有数据按时间顺序划分：75%训练、12.5%验证、12.5%测试。

### Benchmark方法
- **单模态基线**：SASRec、BERT4Rec（仅ID）。
- **多模态基线**：
  - SASRec+、BERT4Rec+：早期融合，将MTSTRec提取的文本和图像特征在输入前拼接。
  - MMMLP：晚期融合，使用特征混合器、融合混合器。
  - MMMLP+：增强版，使用与MTSTRec相同的5个特征（ID、文本、提示文本、图像风格、价格）。

### 评估指标
NDCG@5/10、HR@5/10、MRR@5/10（针对多标签任务调整）。

## 4. 资源与算力

- **文中提及**：在附录M中给出参数数量和运行时间统计（House-Hold E-commerce数据集上，MTSTRec参数59.24M，训练时间83分钟，推理时间12.43秒），但**未明确说明使用的GPU型号和数量**。因此无法获得完整算力信息。
- 作者感谢国家高性能计算中心提供计算和存储资源，但未给出具体硬件配置。

## 5. 实验数量与充分性

- **主要对比实验**：在3个数据集上与7个基线模型全面对比（表1）。
- **消融实验**：
  - 不同模态的贡献：移除ID、文本、提示文本、风格、价格（表2）。
  - 融合策略对比：TST vs 早融合 vs 晚融合（表3）。
  - 共享令牌配置：1:1、1:2、1:4、Bottleneck（表4）。
  - 语言模型对比：BERT、OpenAI、Llama 3、Llama 3.1（表5）。
  - 提示策略与LLM生成质量（表7、8、9）。
  - CLOZE令牌影响、共享令牌是否加入输出（表13、14）。
- **充分性评估**：实验设计非常全面，覆盖了方法的核心组件、参数敏感性和公平性（为基线对齐输入特征）。结果有标准差（多次运行），统计严谨。但仍有部分细节（如随机种子次数）未说明，总体是充分的。

## 6. 论文的主要结论与发现

- **MTSTRec在所有三个数据集上均取得最佳性能**，特别是在H&M数据集上NDCG@5比第二好模型高约31.5%~43.7%。
- **TST中期融合策略显著优于早融合和晚融合**，验证了时间对齐的跨模态交互的重要性。
- **ID模态在小产品空间（<2500产品）至关重要**，移除后性能大幅下降；但在大产品空间（>11000产品）移除ID反而提升，说明此时其他模态信息更能弥补ID的稀疏性。
- **文本和提示文本是第二重要的模态**，尤其在某些场景下贡献显著。
- **风格（图像）和价格贡献相对较小**，但仍有正面影响。
- **Llama 3.1作为文本编码器效果最佳**；提示文本策略中“标签型”提示权重最高。

## 7. 优点：方法或实验设计上的亮点

- **创新性**：提出**时间对齐共享令牌**，巧妙地将序列推荐中的时间顺序约束引入多模态融合，保证了同一时间步跨模态交互的精确性。
- **特征提取精细**：图像使用Gram矩阵提取风格而非分类，文本利用LLM增强并通过门控融合多种提示，价格采用SCANE或直接扩展，各有针对性。
- **实验设计公平**：为基线模型加入相同多模态特征（SASRec+、BERT4Rec+、MMMLP+），确保对比聚焦于融合架构差异。
- **消融实验全面**：不仅分析各模态贡献，还比较不同融合策略、共享令牌配置、语言模型和提示方法，结论可靠。
- **代码开源**：提供GitHub仓库，便于复现和应用。

## 8. 不足与局限

- **实验覆盖的局限性**：
  - 仅在三个电商数据集上验证（食品、家居、服装），缺乏其他领域（如视频、新闻、音乐）的泛化性测试。
  - 数据集产品数量差异较大，但未在不同规模数据集上系统分析模型可扩展性。
- **计算资源未明示**：缺乏GPU型号和训练总时长（仅给出单一数据集时间），难以评估实际部署开销。
- **部分结果矛盾**：H&M数据集上移除ID后性能提升，而其他数据集相反，论文解释为产品空间差异，但未深入分析ID过度拟合或噪声问题。
- **价格模态表现弱**：价格对精度几乎没有贡献，可能需要更复杂的编码方式（如相对价格比等），而非简单归一化。
- **应用限制**：方法依赖LLM生成文本和VGG提取风格，对实时性要求高的场景可能成本过高；且提示文本需要人工设计，自动化程度不足。
- **公平性风险**：未讨论多模态数据可能引入的偏见（如图像风格导致性别/种族偏见），以及隐私问题（虽然声称仅用匿名浏览历史）。

（完）
