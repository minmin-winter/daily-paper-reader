---
title: "DUNIA: Pixel-Sized Embeddings via Cross-Modal Alignment for Earth Observation Applications"
title_zh: DUNIA：通过跨模态对齐实现像素级嵌入用于地球观测
authors: "Ibrahim Fayad, Max Zimmer, Martin Schwartz, Fabian Gieseke, Philippe CIAIS, Gabriel Belouze, Sarah Brood, Aurélien de Truchis, Alexandre d'Aspremont"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=JXCiQteuOv"
tags: ["query:native-multi"]
score: 7.0
evidence: 图像与激光雷达的像素级跨模态对齐
tldr: 针对现有地球观测多模态学习方法仅产生粗粒度面片嵌入、难以与LiDAR等模态集成的问题，本文提出DUNIA，通过对比学习实现图像与全波形LiDAR数据的像素级跨模态对齐。该方法可直接用于零样本环境监测任务，如冠层高度和覆盖度制图，展示了细粒度多模态嵌入在遥感领域的有效性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 858, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1669, \"height\": 1092, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1762, \"height\": 1333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1697, \"height\": 588, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1576, \"height\": 1390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1580, \"height\": 1407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1582, \"height\": 1442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1725, \"height\": 955, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1591, \"height\": 2038, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1574, \"height\": 2002, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1577, \"height\": 2006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1577, \"height\": 2011, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1646, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1778, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1210, \"height\": 350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1711, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 787, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 703, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 461, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 569, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 743, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1305, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 898, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 695, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 696, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 870, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1022, \"height\": 171, \"label\": \"Table\"}]"
motivation: 现有方法只产生粗粒度嵌入，限制了与LiDAR等精细模态的融合。
method: 采用对比学习对齐图像与全波形LiDAR数据，学习像素级嵌入。
result: 在七个零样本环境监测任务上验证了像素级嵌入的有效性。
conclusion: 像素级跨模态对齐可大幅提升遥感多模态模型的细粒度融合能力。
---

## Abstract
Significant efforts have been directed towards adapting self-supervised multimodal learning for Earth observation applications. However, most current methods produce coarse patch-sized embeddings, limiting their effectiveness and integration with other modalities like LiDAR. To close this gap, we present DUNIA, an approach to learn pixel-sized embeddings through cross-modal alignment between images and full-waveform LiDAR data. As the model is trained in a contrastive manner, the embeddings can be directly leveraged in the context of a variety of environmental monitoring tasks in a zero-shot setting. In our experiments, we demonstrate the effectiveness of the embeddings for seven such tasks: canopy height mapping, fractional canopy cover, land cover mapping, tree species identification, plant area index, crop type classification, and per-pixel waveform-based vertical structure mapping. The results show that the embeddings, along with zero-shot classifiers, often outperform specialized supervised models, even in low-data regimes. In the fine-tuning setting, we show strong performances near or better than the state-of-the-art on five out of six tasks.

---

## 论文详细总结（自动生成）

# 论文总结：DUNIA：通过跨模态对齐实现像素级嵌入用于地球观测应用

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：现有的地球观测（EO）自监督多模态学习方法大多产生粗粒度的**面片级（patch-sized）嵌入**，这限制了它们与LiDAR等精细模态的集成能力。同时，现有基础模型即使能处理多模态数据，也主要依赖图像模态，难以理解垂直结构（如冠层高度、全波形LiDAR信号），且在零样本和少样本场景下表现有限。
- **研究动机**：地球观测中，森林监测、碳估算等任务需要高分辨率、细粒度的垂直与水平结构信息。传统监督深度学习依赖大量标注数据，且模型通常为特定任务定制，缺乏泛化性。自监督基础模型（如MAE）虽能缓解标注问题，但大多仍需微调，且无法直接生成像素级预测，难以利用稀疏的LiDAR全波形数据。
- **整体含义**：本文提出**DUNIA**（Dense Unsupervised Nature Interpretation Algorithm），通过**跨模态对齐**（图像与全波形LiDAR）学习**像素级嵌入**，使得模型能够在零样本或少量样本条件下完成多种环境监测任务，包括冠层高度、覆盖度、土地覆盖、树种识别、作物类型、植被面积指数和垂直结构映射。这是首个能在大尺度上从卫星图像生成GEDI全波形的方法。

## 2. 方法论：核心思想、关键技术细节、算法流程

- **核心思想**：利用对比学习，将**水平结构信息**（来自Sentinel-1和Sentinel-2光学/雷达影像）与**垂直结构信息**（来自GEDI空间全波形LiDAR）在像素级别进行对齐。通过两个独立的解码器分别处理水平和垂直结构，使得单个预训练模型可以同时理解两种结构，并支持零样本跨模态检索。
- **整体架构**：一个预训练模型（Transformer编码器 + 两个独立卷积解码器）+ 两个模态特定的自编码器（AE）：
  1. **预训练模型**：以单时相S-1 & S-2合成图像为输入，经过patch嵌入、16层Transformer编码器后，通过**两个独立的解码器**分别生成像素级嵌入 \( O_V \)（用于垂直结构对齐）和 \( O_H \)（用于水平结构对齐）。每个解码器输出经**邻域注意力（Neighborhood Attention）**层增强局部关系。
  2. **波形模型**（垂直AE）：基于VQ-VAE架构，包括波形编码器（ResNet式）、残差向量量化器（RVQ）和波形解码器。将GEDI波形 \( W \) 编码为潜在表示 \( z_e \)，再通过平均池化和线性投影得到 \( O_W \in \mathbb{R}^{D_p} \)，用于与 \( O_V \) 对齐。
  3. **多时相图像模型**（水平AE）：基于ConvLSTM的U-Net结构，处理三个时相的S-1 & S-2合成图像，输出特征图 \( X \)，经时间平均池化后得到 \( O_T \)，用于与 \( O_H \) 对齐。
- **对齐方式**：
  - **像素-波形对齐（Pixel-Waveform）**：使用**Zero-CL**损失（实例级 + 特征级对比损失），在小批量中波形样本较少时表现良好。对齐 \( O_V \) 与 \( O_W \)。
  - **像素-像素对齐（Pixel-Pixel）**：使用**VICReg**损失（方差、不变性、协方差三项），应用于四个解码器层级的 \( O_{H,d} \) 与 \( O_{T,d} \) 之间，实现层次化对齐。
  - **重建损失**：三个MSE损失分别用于波形AE重建、多时相图像AE重建和单时相图像重建，作为正则化。
- **波形生成**：训练一个**潜在扩散模型（LDM）**，以像素嵌入 \( O_{V,\phi,\lambda} \) 为条件，在量化波形潜在空间上生成新波形。推理时先采样潜在表示，再通过冻结的波形解码器输出波形。
- **网络细节**：Transformer编码器16层，8个注意力头，嵌入维度512；解码器维度 \( D_p=64 \)；patch大小8像素；输入图像64×64像素，14个波段。波形编码器将256 bins的波形压缩为16×16潜在表示。多时相AE输入三个时相。扩散模型使用1D UNet，30步推理，使用分类器无关引导（scale=3）。

## 3. 实验设计

- **数据集**：
  - **预训练数据集**：法国全境，使用Sentinel-2 L2A（10m/20m波段，重采样至10m）和Sentinel-1（VV/VH极化，10m），制作叶季合成（2020年4-9月）用于预训练模型，三个4个月合成（2019年10月-2020年9月）用于多时相AE。GEDI（L1B/L2A/L2B）数据2019-2021年，经质量过滤后约1900万个波形，覆盖法国不到1%面积，平均每张64×64图像含26个波形。共836K张64×64图像。
  - **评估数据集**：
    - **PureForest (PF)**：135K个50×50m patch，13个树种，用于树种分类。
    - **CLC+Backbone (CLS+)**：泛欧洲土地覆盖，11个类别，10m分辨率。
    - **PASTIS**：作物映射，18个作物类+1背景，2433张128×128图像。
    - **垂直结构**：使用GEDI导出的冠层高度（RH98）、冠层覆盖度、植被面积指数和完整波形。
- **基准与对比方法**：对比**五个当前最先进的EO基础模型**：SatMAE、DOFA、DeCUR、CROMA、AnySat。所有对比模型均在相同预训练数据集上以相同步数（250K steps）重新训练或使用官方权重，仅在微调时评估（波形生成任务对比方法不支持）。
- **评估指标**：
  - 分类任务：加权F1（wF1）
  - 回归任务：RMSE、Pearson相关系数（r）
  - 波形相似度：Pearson相关系数
- **评估设置**：
  - **零样本分类**：从训练集构建检索数据库，测试集像素作为查询，使用KNN（K=50,5,1）基于余弦相似度检索，距离加权投票。
  - **低样本微调**：冻结预训练网络除最后一个NA层，添加两个1×1卷积输出头，进行微调。
  - 数据量：对于垂直结构产品使用50K个单像素标签；对于CLS+和PASTIS使用500张或1.5K张密集标注图像等。

## 4. 资源与算力

- **文中明确提及**：
  - 预训练：单张**NVIDIA A6000 48GB GPU**，批大小60，训练250K steps。
  - 使用**Lion优化器**（学习率5e-5，权重衰减0.4，5K warmup，余弦退火）。
  - 扩散模型：批大小4096，100K steps，AdamW学习率1e-4。
  - 微调：AdamW学习率2e-4，批大小20，训练至收敛。
  - 使用**Switch EMA（SEMA）** 技术，EMA decay=0.9，每5步更新，每1K步替换网络参数。
  - **未明确说明**训练总时间（小时/天），但算力需求较低（单GPU即可完成预训练）。

## 5. 实验数量与充分性

- **实验组数**：论文包含**7个下游任务**的零样本和微调评估，涉及多个数据集和指标。此外，进行了**大量消融实验**（附录H）：损失函数选择（VICReg vs Zero-CL）、共享解码器 vs 双解码器、层次化VICReg、邻域注意力 vs CNN、嵌入敏感性（交换 \( O_V \) 与 \( O_H \)）、推理运行时、输入尺寸影响、时间稳定性（不同年份）、S-1/S-2单模态 vs 双模态、单日期 vs 中值合成。总计**约12组消融实验**，分布在正文和附录中。
- **充分性与公平性**：
  - 对比方法在相同数据上重新训练（或使用官方权重），且训练步数一致（250K steps），**确保公平比较**。
  - 提供了定性可视化（附图I1-I8）展示地图质量和波形检索/生成效果，增强了说服力。
  - 消融实验设计合理，覆盖架构关键组件和超参数，验证了设计选择的有效性。
  - 零样本结果与多个专业监督模型（如Schwartz et al., Liu et al., Lang et al.等）进行了比较，报告了SOTA数值。
  - **不足**：预训练和评估仅基于法国领土，可能限制地理多样性；波形生成任务没有对比方法（其他模型不支持），但论文本身是首次提出该能力。

## 6. 主要结论与发现

- **零样本性能超越监督模型**：在冠层高度（RMSE=2.0m，r=0.93）、冠层覆盖度（RMSE=11.7%，r=0.89）、植被面积指数（RMSE=0.71，r=0.75）三个垂直结构任务上，DUNIA以KNN=50显著优于现有专业监督模型（高度RMSE改善3.2m，覆盖度改善10.4%）。树种分类（PF）在KNN=5时达到76.0% wF1，超过基线74.6%。
- **微调性能与SOTA持平或更优**：在5/6个任务上达到或超过当前最佳方法。对于垂直结构任务，DUNIA（RMSE=1.3m，r=0.95）远超其他基础模型（AnySat 2.8m, r=0.89）。土地覆盖（CLC+ wF1=90.3%）和树种分类（82.2%）与AnySat相当。
- **新型能力——波形生成与检索**：首次实现从像素输入检索相关GEDI波形（r=0.70）和生成波形（r=0.78），且生成比检索更优。
- **双解码器设计关键**：分离水平和垂直结构理解（表H2显示共享解码器下像素与波形嵌入负相关，而独立解码器达到0.99正相关）。
- **时间稳定性**：在2019-2021三个年份上表现一致（表H8, H9）。
- **中值合成优于单日期**：对作物分类等需要物候信息的任务显著提升（PASTIS wF1从42.3%升至77.0%）。

## 7. 优点

- **像素级细粒度嵌入**：突破现有方法面片级粗粒度限制，实现与LiDAR波形的逐像素对齐，显著提升零样本检索精度。
- **跨模态对齐策略创新**：同时进行像素-像素（水平）和像素-波形（垂直）对齐，使单一模型能同时处理两类任务，而无需针对每类任务单独训练。
- **模块化可扩展设计**：预训练编码器可替换为支持多时相或多分辨率输入的模块，具有良好扩展性。
- **高泛化性能**：在低数据（50K个标签，约0.25%的训练数据）下零样本超越专用监督模型，证明了自监督学习在EO中的强大潜力。
- **波形生成开创性**：首次实现从卫星图像生成GEDI全波形，能直接提供垂直结构信号，为森林监测提供新途径。
- **计算高效**：单GPU即可完成预训练，推理速度（约4.2秒/20.48km²）远快于AnySat（177秒），适合大规模部署。
- **消融实验系统全面**：验证了损失函数选择、解码器分离、层次化对齐、邻域注意力等关键设计的贡献。

## 8. 不足与局限

- **地理覆盖有限**：预训练和所有评估均基于法国，模型可能对其他生物群落（热带、北方森林）泛化能力有限，作者承认需要重新预训练。
- **时间信息利用不足**：模型仅使用中值合成而非完整时间序列，导致在作物类型映射（PASTIS）上表现较差（零样本56.2%，微调77.0%），远低于AnySat（81.1%）。虽然这是设计权衡（减少存储需求），但限制了动态场景的应用。
- **波形质量评估单一**：波形生成仅用Pearson相关系数评估，未使用更专业的波形相似性指标（如RMSE、能量分布差异等）。
- **标注稀缺问题**：虽然零样本性能优秀，但在土地覆盖和作物分类上，当检索数据库较小（5% S）时性能大幅下降（CLC+从80.1%降至70.2%），说明对数据库大小敏感。
- **对比方法可能不公平**：虽然训练步数一致，但对比模型（如AnySat）可能使用更多模态（含1.5m SPOT影像）进行预训练，而微调时仅用S-1 & S-2，可能未充分发挥其潜力。作者已在文中说明。
- **部署风险**：当前模型针对2020年法国设计，时间推移和人为环境变化可能导致需要重新预训练；对云覆盖严重地区（如热带）可能因缺少无云合成而受限。
- **社会影响方面**：虽强调对森林碳汇监测的正面作用，但未讨论误用风险（如用于精准农业或非法监测的逆向工程）（论文有单独伦理声明，但总结中需客观指出）。

（完）
