---
title: "From Token to Rhythm: A Multi-Scale Approach for ECG-Language Pretraining"
title_zh: 从令牌到节奏：心电图-语言预训练的多尺度方法
authors: "Fuying Wang, Jiacheng Xu, Lequan Yu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=fUjkoGUre0"
tags: ["query:native-multi"]
score: 7.0
evidence: 多尺度心电图-语言对齐预训练
tldr: 针对现有心电图-语言预训练方法未能充分捕捉ECG信号多尺度特性导致表征泛化能力弱的问题，本文提出了一种从令牌到节奏的多尺度预训练框架。该方法同时建模ECG的微观（波形片段）和宏观（节律模式）信息，在多个下游任务上取得了更优的迁移效果。实验证明多尺度对齐能够显著提升ECG语言模型的表示质量和鲁棒性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-fujkogure0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 793, \"height\": 566, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fujkogure0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1663, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fujkogure0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 842, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-fujkogure0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1144, \"height\": 920, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1593, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1691, \"height\": 466, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1681, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1685, \"height\": 543, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1682, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1335, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1684, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1674, \"height\": 156, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 859, \"height\": 110, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1331, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1714, \"height\": 412, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1768, \"height\": 543, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1061, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1574, \"height\": 160, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1677, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1755, \"height\": 160, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1239, \"height\": 726, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-fujkogure0/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1760, \"height\": 366, \"label\": \"Table\"}]"
motivation: 现有ECG-语言预训练方法忽视信号的多尺度特性，难以学到泛化的表示。
method: 提出多尺度预训练框架，同时捕获ECG的局部令牌和全局节奏信息进行跨模态对齐。
result: 在多个下游ECG任务上，多尺度方法优于单尺度基线，表明多尺度对齐的有效性。
conclusion: 多尺度预训练能有效提升ECG语言模型的表示能力和迁移性能。
---

## Abstract
Electrocardiograms (ECGs) play a vital role in monitoring cardiac health and diagnosing heart diseases. However, traditional deep learning approaches for ECG analysis rely heavily on large-scale manual annotations, which are both time-consuming and resource-intensive to obtain. To overcome this limitation, self-supervised learning (SSL) has emerged as a promising alternative, enabling the extraction of robust ECG representations that can be efficiently transferred to various downstream tasks. While previous studies have explored SSL for ECG pretraining and multi-modal ECG-language alignment, they often fail to capture the multi-scale nature of ECG signals. As a result, these methods struggle to learn generalized representations due to their inability to model the hierarchical structure of ECG data. To address this gap, we introduce MELP, a novel Multi-scale ECG-Language Pretraining (MELP) model that fully leverages hierarchical supervision from ECG-text pairs. MELP first pretrains a cardiology-specific language model to enhance its understanding of clinical text. It then applies three levels of cross-modal supervision—at the token, beat, and rhythm levels—to align ECG signals with textual reports, capturing structured information across different time scales. We evaluate MELP on three public ECG datasets across multiple tasks, including zero-shot ECG classification, linear probing, and transfer learning. Experimental results demonstrate that MELP outperforms existing SSL methods, underscoring its effectiveness and adaptability across diverse clinical applications. Our code is available at https://github.com/HKU-MedAI/MELP.

---

## 论文详细总结（自动生成）

# 从令牌到节奏：心电图-语言预训练的多尺度方法 (MELP) – 详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

心电图（ECG）是监测心脏健康、诊断心血管疾病的关键工具。然而，传统深度学习模型严重依赖大规模人工标注，获取标注耗时耗资源。自监督学习（SSL）已成为一个有效替代，但现有ECG-语言多模态预训练方法（如MERL）仅关注全局ECG-文本对齐，忽视了ECG信号固有的**多尺度分层结构**（如图1所示：令牌级对应P波、QRS波等局部波形；心跳级对应单个心动周期；节律级对应整体心电节律）。这种忽视导致模型无法捕获细粒度的局部特征（如P波缺失、QRS宽度等），使得学到的表示泛化能力弱，难以适应多样化的下游任务。为此，论文提出**MELP**（Multi-scale ECG-Language Pretraining），通过层级式跨模态监督，同时对齐ECG信号与临床文本在三个尺度上的信息。

## 2. 方法论：核心思想、关键技术细节

### 2.1 整体框架
MELP采用**双编码器结构**：ECG编码器（基于Wav2Vec 2.0）和文本编码器（基于心脏专科预训练的MedCPT）。模型在三个阶段对ECG-文本对施加监督：
- **令牌级（Token-level）**：生成式报告生成（Captioning Loss）
- **心跳级（Beat-level）**：心跳-句子对比对齐（Local Contrastive Loss）
- **节律级（Rhythm-level）**：全局对比对齐（Global Contrastive Loss）

### 2.2 关键技术细节
1. **心脏专科语言模型预训练**：使用PubMed、Wikipedia和MIMIC-IV-ECG报告组成的心脏病学语料，在MedCPT查询编码器上进行掩码语言建模（MLM）微调，增强模型对临床术语的理解。
2. **令牌级监督**：ECG编码器输出令牌嵌入 \(E \in \mathbb{R}^{L_t \times D}\)，通过含128个可学习查询令牌的注意力池化层得到 \(\tilde{E} \in \mathbb{R}^{128 \times D}\)，随后输入GPT风格的解码器，以自回归方式预测文本报告，损失为交叉熵（公式1）：  
   \[
   L_{\text{LM}}(\zeta) = -\sum_{i=1}^N \log p(w_i | w_{0:i-1}, \tilde{E})
   \]
3. **心跳级监督**：通过注意力池化从令牌嵌入中聚合出10个心跳表示 \(B \in \mathbb{R}^{10 \times D}\)（实际上默认10个心跳，但附录表14显示中位数为12-13，消融实验表明16个最佳）。文本则分割为句子，平均词嵌入得到句子表示 \(S \in \mathbb{R}^{S \times D}\)。计算每个句子与所有心跳的注意力加权心跳表示（公式2-3），再用LogSumExp聚合相似度（公式4），最后采用对比损失 \(L_{\text{Local}}\)（公式5）。  
   \[
   \hat{B}^{(l)} = \sum_{l'} \alpha_{l'} S^{(l')}, \quad \alpha_{l'} = \frac{\exp(\langle S^{(l)}, B^{(l')}\rangle/\tau_1)}{\sum_j \exp(\langle S^{(l)}, B^{(j)}\rangle/\tau_1)}
   \]
   \[
   Z(X,T) = \log\left(\sum_{l=1}^{S} \exp(\langle \hat{B}^{(l)}, S^{(l)}\rangle/\tau_2)\right)^{\tau_2}
   \]
4. **节律级监督**：对所有心跳表示平均池化得到全局ECG嵌入 \(X_g\)，文本[CLS]令牌作为全局文本嵌入 \(T_g\)，应用InfoNCE对比损失 \(L_g\)（公式6）。
5. **总损失**：\(L = L_g + \lambda_1 L_{\text{LM}} + \lambda_2 L_{\text{Local}}\)，其中 \(\lambda_1=2, \lambda_2=0.2\)（通过超参数搜索确定）。

### 2.3 下游任务迁移
- **零样本分类**：直接使用全局嵌入进行检索。
- **线性探测/微调**：提取心跳级嵌入，平均池化后加线性分类器。

## 3. 实验设计

### 3.1 数据集
- **预训练**：MIMIC-IV-ECG v1.0（800,035条记录），经清洗后得到760,618个ECG-文本对。
- **下游评估**：
  - **PTB-XL**（21,837条，500Hz，10秒）：按四个子集（Rhythm, Sub, Form, Super）评测。
  - **CPSC2018**（6,877条，9类标签）。
  - **CSN**（23,026条，38类标签）。

### 3.2 基准与对比方法
对比方法包括14种：SimCLR、BYOL、BarlowTwins、MoCo-v3、SimSiam、TS-TCC、CLOCS、ASTCL、CRT、ST-MEM、HeartLang、ECGFM、MERL（跨模态基线）等。所有实验遵循MERL的划分协议（表1列出各数据集训练/验证/测试样本数）。

### 3.3 任务设定
- **线性探测**：使用1%、10%、100%训练数据，冻结编码器，仅训练线性分类头，评估AUC。
- **零样本分类**：直接使用全局嵌入进行检索，AUC。
- **跨域迁移**：在一个数据集上训练（100%），在另一个数据集上测试（类别匹配，表17）。
- **消融实验**：损失函数、ECG编码器（ResNet-18 vs Wav2Vec 2.0 vs Wav2Vec+CMSC）、语言模型预训练、超参数、心跳数量等。
- **额外任务**：ECG报告生成（BLEU, ROUGE-L, BERTScore）、患者识别（Top-k召回率）。

## 4. 资源与算力
论文明确说明：“All experiments are conducted on four NVIDIA GTX 3090 GPUs.” 预训练100个epoch，每个设备batch size为64。总训练时长未给出，但基于4块3090，预计预训练需数天。

## 5. 实验数量与充分性
- **数量**：主实验18个线性探测设置、6个零样本设置、6个跨域迁移设置；消融实验5组（表5-10、附录表15）、报告生成和患者识别各1组。总计超过30组实验。
- **充分性**：覆盖多尺度监督的每个分量、不同编码器、语言模型预训练影响、超参数敏感性、心跳数量等，分析全面。
- **公平性**：严格遵循MERL的预处理、划分、评测协议，对比方法均使用官方或复现设置，结论可靠。

## 6. 主要结论与发现
1. **性能领先**：MELP在18个线性探测设置中16个取得第一，零样本平均AUC 79.0%（比MERL高3.7%），跨域迁移平均AUC最高。
2. **多尺度监督必要**：消融显示完整多尺度损失（Lg+LLM+LLocal）优于任何单双损失组合，其中全局对比损失（Lg）最关键（缺失时性能骤降）。
3. **低数据场景优势**：仅用1%训练数据时，MELP比第二好方法高出2.46%~7.38%，表明其表征的高效性。
4. **ECG编码器选择**：Wav2Vec 2.0优于ResNet-18和Wav2Vec+CMSC。
5. **语言模型预训练**：提供微小但一致的正向提升（平均+0.35%）。
6. **零样本可视化**：t-SNE显示MELP的嵌入空间更紧致、类别分离更清晰。

## 7. 优点（方法与实验亮点）
- **创新性**：首次在ECG-语言预训练中明确引入令牌、心跳、节律三级别层次化对齐，符合临床诊断逻辑。
- **方法设计**：心跳-句子注意力加权对比机制（公式2-4）有效捕捉局部对应关系；生成式损失促进细粒度理解。
- **实验全面**：不仅覆盖标准分类任务，还包含零样本、跨域、生成、患者识别等多角度评估；消融清晰，超参数探索完整。
- **工程贡献**：代码开源，便于复现和后续研究。

## 8. 不足与局限
- **可解释性**：令牌级监督缺乏显式临床注记（如P波缺失、ST段抬高），仅通过隐式学习，难以用于可解释诊断。作者承认未来可借助外部知识库生成临床意义的描述。
- **文本编码器限制**：当前使用MedCPT（BERT-like），未利用大语言模型的强大推理能力。作者计划未来探索ECG指令微调。
- **心跳数量设定**：默认10个心跳，但中位数实际为12-13（附录表14），虽然消融发现16个最佳，但网格搜索仅在有限值上进行，缺乏自适应方法。
- **数据与偏倚**：仅基于MIMIC-IV-ECG预训练，可能无法覆盖所有种族/设备/场景；尽管预处理去标识化，但隐私和偏倚风险仍需防范。
- **实验覆盖**：报告生成任务仅在500个样本上初步评估（表9），且仅对比PULSE，缺乏与其他ECG生成模型的比较。患者识别任务也未与更多基线对比。

（完）
