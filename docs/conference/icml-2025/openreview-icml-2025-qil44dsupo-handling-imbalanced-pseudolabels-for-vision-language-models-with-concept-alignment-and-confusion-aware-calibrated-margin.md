---
title: Handling Imbalanced Pseudolabels for Vision-Language Models with Concept Alignment and Confusion-Aware Calibrated Margin
title_zh: 面向视觉语言模型的伪标签不平衡处理：概念对齐与混淆感知校准边界
authors: "Yuchen Wang, Xuefeng Bai, Xiucheng Li, Weili Guan, Liqiang Nie, Xinyang Chen"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=QIL44dSUPo"
tags: ["query:balanced-mml"]
score: 8.0
evidence: 直接处理视觉语言模型中的伪标签不平衡问题，采用概念对齐方法
tldr: 本文针对视觉语言模型（VLM）使用伪标签进行下游适应时的标签不平衡问题，深入分析了概念不匹配和概念混淆两大成因，并提出了概念对齐与混淆感知校准边界框架。该方法通过增强欠表现概念的对齐和动态调整分类边界，有效缓解了不平衡带来的性能下降。实验证明，该方法在多个基准上优于现有技术，为VLM鲁棒适应提供了新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 752, \"height\": 298, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 837, \"height\": 329, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 850, \"height\": 712, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 858, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1774, \"height\": 691, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 855, \"height\": 309, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 858, \"height\": 314, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 858, \"height\": 351, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 859, \"height\": 356, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 854, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 851, \"height\": 336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1609, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1591, \"height\": 414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1768, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 445, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 856, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qil44dsupo/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1068, \"height\": 434, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-qil44dsupo/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1729, \"height\": 650, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qil44dsupo/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 813, \"height\": 250, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qil44dsupo/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 827, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qil44dsupo/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 829, \"height\": 612, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qil44dsupo/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1589, \"height\": 772, \"label\": \"Table\"}]"
motivation: 视觉语言模型在下游任务中使用伪标签时面临标签不平衡问题，影响性能，且现有方法未充分探究不平衡的根源。
method: 提出概念对齐和混淆感知校准边界机制，通过识别概念不匹配和概念混淆两个因素来减轻伪标签不平衡。
result: 在多个基准数据集上超过现有方法，有效提升了不平衡场景下的VLM适应性能。
conclusion: 所提框架显著缓解了伪标签不平衡问题，为VLM下游适应提供了鲁棒方案。
---

## Abstract
Adapting vision-language models (VLMs) to downstream tasks with pseudolabels has gained increasing attention. 
A major obstacle is that the pseudolabels generated by VLMs tend to be imbalanced, leading to inferior performance.
While existing methods have explored various strategies to address this, the underlying causes of imbalance remain insufficiently investigated.
To fill this gap, we delve into imbalanced pseudolabels and identify two primary contributing factors: concept mismatch and concept confusion. 
To mitigate these two issues, we propose a novel framework incorporating concept alignment and confusion-aware calibrated margin mechanisms. 
The core of our approach lies in enhancing underperforming classes and promoting balanced predictions across categories, thus mitigating imbalance. 
Extensive experiments on six benchmark datasets with three learning paradigms demonstrate that the proposed method effectively enhances the accuracy and balance of pseudolabels, achieving a relative improvement of 6.29\% over the SoTA method. Our code is avaliable at https://github.com/Noahwangyuchen/CAP

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：视觉语言模型（VLM，如CLIP）在下游任务中使用自生成的伪标签进行适应时，伪标签往往呈现严重的**类别不平衡**现象，导致模型性能下降。
- **研究动机**：已有工作采用了一些事后策略（如为每类分配相等数量的伪标签、候选标签集等）来缓解不平衡，但**对不平衡产生的根本原因缺乏深入分析**。本文首次系统性地从语义鸿沟角度出发，识别出导致伪标签不平衡的两个关键因素：
  - **概念不匹配（Concept Mismatch）**：某些类别的文本特征与对应视觉特征存在严重错位，导致即使图像特征聚类良好，零样本预测仍然完全错误。
  - **概念混淆（Concept Confusion）**：相似类别之间的文本特征无法捕获最具区分度的视觉概念，导致预测偏向某一类，造成伪标签不平衡。
- **研究意义**：通过揭示这些内在原因并设计针对性缓解机制，可显著提升VLM在无标注数据上的适应效果，降低标注成本，推动VLM在实际应用中的鲁棒部署。

## 2. 论文提出的方法论

### 核心思想
针对概念不匹配和概念混淆两大问题，分别采用**概念对齐**和**混淆感知校准边界**两大机制，结合独立适配器微调框架，从初始化伪标签生成和训练过程两个层面提升伪标签的准确性与平衡性。

### 关键技术细节

#### （1）概念对齐（Concept Alignment）
- **目标**：消除概念不匹配，为低表现类提供更准确的初始伪标签。
- **步骤**：
  1. **不匹配检测**：使用迭代聚类算法，逐步移除与文本特征对齐良好的类，最终保留可能不匹配的类集 \( Y_{\text{MM}} \)。算法1详细描述了该过程：每次迭代对图像特征做K-means聚类（簇数等于当前剩余类数），计算文本特征与聚类中心之间的相似度，移除置信度最高的（文本、聚类中心）对及其对应图像，直到剩余类别数小于阈值 \( t \)（设为 \( \lceil C/10 \rceil \)）。
  2. **文本增强**：对 \( Y_{\text{MM}} \) 中的每个类，利用LLM（ChatGPT 4o-mini）生成n=5条增强描述。从中选出与聚类中心最相似的描述作为该类的新文本特征。
  3. **伪标签生成**：对于增强后的类，根据新文本特征与图像特征的余弦相似度，选取top-k（k=16）样本作为伪标签样本 \( D_{\text{PL}} \)。

#### （2）混淆感知校准边界（Confusion-Aware Calibrated Margin）
- **目标**：在线训练过程中减轻概念混淆，促进模型在混淆类之间做出更可区分、更平衡的预测。
- **原理**：定义变体交叉熵损失：
  \[
  L_m(y, z) = -\log \frac{e^{z_y}}{e^{z_y} + \sum_{c \neq y} e^{z_c + M_{yc}}}
  \]
  其中 \( M \) 为边际矩阵，由类间相似度矩阵 \( S \) 和类加权度 \( m_c \) 通过哈达玛积得到：
  - 相似度矩阵 \( S \)：计算每个类的视觉原型（平均特征）和文本原型，取两类之间视觉-视觉、文本-文本相似度的最大值。
  - 类加权度 \( m_c = m \times \Delta \times \delta_c \)，其中 \( m \) 为预设尺度（取12），\( \Delta \) 为整体不平衡程度（最大类别倾向差距），\( \delta_c \) 为每类倾向（基于预测置信度超过阈值τ的样本数）。
- **动态更新**：边际矩阵 \( M \) 每轮训练更新一次，以适应模型状态。

#### （3）微调框架
- 使用MaPLe作为提示微调方法，学习文本和视觉分支的上下文提示。
- **独立适配器**：视觉分支上部署**主适配器**（学习 \( D_{\text{PL}} \)）和**伪适配器**（学习 \( D_{\text{UL}} \)），前者生成高质量伪标签用于后者，避免错误累积。
- **损失函数**：总损失 \( L = L_{\text{PL}} + L_{\text{UL}} \)（UL设置），如为SSL/TRZSL则加上 \( L_L \)。计算时均使用混淆感知校准边界损失。

### 算法流程概览
1. 初始化阶段：使用概念对齐生成初始伪标签集 \( D_{\text{PL}} \)。
2. 训练循环：每个epoch，从 \( D_{\text{PL}} \) 取样本通过主适配器计算损失；从 \( D_{\text{UL}} \) 取样本，用主适配器生成伪标签（置信度阈值τ过滤），由伪适配器计算损失；同时更新边际矩阵。
3. 每5个epoch还将高置信度未标注样本扩充至 \( D_{\text{PL}} \)。

## 3. 实验设计

### 数据集与场景
- **6个图像分类数据集**：Flowers102、RESISC45、DTD、EuroSAT、CUB、FGVCAircraft，覆盖遥感、纹理、细粒度、卫星图等多领域。
- **三种学习范式**：
  - **无监督学习（UL）**：仅使用无标注数据。
  - **半监督学习（SSL）**：每类2个标注样本 + 大量无标注数据。
  - **直推式零样本学习（TRZSL）**：可见类有全部标注，不可见类全无标注，比例62:38。

### 基准方法
- zero-shot CLIP（基线）
- FPL（Few Pseudolabels，即UPL）
- GRIP（Grow and Refine Iteratively Pseudolabels）
- CPL（Candidate Pseudo-Labeling，SoTA）

### 评估指标
- 测试集准确率（UL和SSL报告所有类准确率，TRZSL报告可见类与不可见类准确率的调和平均）。

## 4. 资源与算力

论文中未明确说明GPU型号和数量。但在附录D.2中报告了训练时间：
- 在EuroSAT数据集上，CAP方法训练耗时约**29分钟**，而CPL耗时约1小时14分钟，GRIP耗时约1小时42分钟。
- 其他实验细节：使用ViT-B/32作为默认视觉主干，batch size=32，epoch=50。因此推断实验可能在单卡或少量GPU上进行，但未提供具体算力规格。

## 5. 实验数量与充分性

- **主实验**：在6个数据集×3种范式下比较5种方法（含零样本），共18组对比（表1），每组报告3次run的均值和标准差。
- **消融实验**：
  - 分别移除概念对齐（CA）和混淆感知校准边界（CACM）（表2）。
  - 独立适配器（IA）的作用（表3）。
  - 超参数k（每类伪标签数）和τ（置信度阈值）的敏感性分析（图6、图7）。
- **分析实验**：
  - 概念对齐对不匹配类伪标签准确率的影响（图8）。
  - 混淆感知校准边界对局部ECE和混淆组准确率的影响（图9）。
  - 不同边际尺度m的稳定性分析（图10）。
  - 不同数据量比例下的性能变化（图11）。
  - 使用更大主干ViT-L/14的泛化性（表4）。
  - 训练时间对比（附录D.2）。
  - 不匹配类检测数量（附录D.3）。
- **充分性评估**：实验设计系统，覆盖主要对比、组件消融、超参数敏感性、数据规模影响、不同backbone、时间效率等多个维度，对比方法均为当前SoTA。结果客观，多次重复取均值，结果有统计意义。

## 6. 论文的主要结论与发现

1. **概念不匹配和概念混淆是VLM伪标签不平衡的两大根本原因**，通过检测和可视化验证了其存在性。
2. **概念对齐显著提升低表现类的伪标签质量**，使部分类别的伪标签准确率提高60%以上，并最终提升微调后的测试准确率。
3. **混淆感知校准边界有效降低混淆类间的局部校准误差（ECE）**，并提高这些类的下游准确率，同时保持高表现类的性能稳定。
4. **整体框架CAP在UL、SSL、TRZSL三种范式下均超越现有SoTA方法**，在Flowers102、RESISC45、DTD、EuroSAT上平均相对提升6.29%，尤其在EuroSAT上UL设置提升高达7.75%。
5. **方法对超参数k和τ稳健**，对边际尺度m在合理范围内不敏感，且能有效利用有限的无标注数据（约40-60%数据即可达到接近全量的效果）。
6. **训练效率显著优于GRIP和CPL**（约3.5倍加速），因为只需单阶段训练而非迭代多轮。

## 7. 优点

- **问题洞察深刻**：不局限于简单均衡策略，而是从语义鸿沟出发分析了两个具体的、可解释的不平衡原因，为后续研究提供新视角。
- **方法设计精巧**：
  - 概念对齐巧妙结合聚类检测和LLM生成，仅针对少数不匹配类进行增强，避免对全部类做冗余修改。
  - 混淆感知校准边际融合了类间相似度和模型预测动态，实现自适应调整，而非固定边际。
  - 独立适配器机制有效隔离高质量初始伪标签与动态生成伪标签的错误传播，提升了训练稳定性。
- **实验充分且公平**：覆盖多个数据集、三种范式、多种对比方法，消融分析完整，超参数敏感性分析充分，且报告了多次随机种子结果。
- **代码开源**，利于复现和后续研究。

## 8. 不足与局限

- **在CUB和FGVCAircraft数据集上提升有限**：对细粒度数据集，本文方法在UL设置下略低于或持平CPL，仅在SSL上有改进，说明对极度细粒度的概念混淆处理仍不够理想。
- **依赖LLM生成文本描述**：LLM的质量和调用成本限制了方法的可扩展性，且对LLM的依赖可能引入新的偏差。
- **聚类检测环节可能不稳定**：对高维图像特征聚类，结果可能受聚类算法初始化和类别数影响，部分不匹配类可能漏检或误检。
- **未涵盖更多样化的下游任务**：实验仅聚焦图像分类，未在语义分割、目标检测等其他VLM应用上验证。
- **算力细节缺失**：未报告具体GPU型号和数量，影响复现时的资源估算。
- **边际尺度m需人工选择**：虽然实验表明较稳健，但仍需在未知数据集上调节，增加了应用复杂度。

（完）
