---
title: "CLIMB: Data Foundations for Large Scale Multimodal Clinical Foundation Models"
title_zh: CLIMB：大规模多模态临床基础模型的数据基础
authors: "Wei Dai, Peilin Chen, Malinda Lu, Daniel A Li, Haowen Wei, Hejie Cui, Paul Pu Liang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=TcvjOSePic"
tags: ["query:unified-mm"]
score: 5.0
evidence: 大规模统一多模态临床基准
tldr: 为促进大规模多模态临床AI研究，本文提出CLIMB基准，整合了来自2D影像、3D视频、时间序列、图和多种模态的19.01TB数据。该基准覆盖4.51百万患者样本，旨在支持多模态临床基础模型的训练与评估。实验表明，CLIMB能够有效评估多模态方法在临床任务中的表现，为未来研究提供了统一数据平台。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-tcvjosepic/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1729, \"height\": 658, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcvjosepic/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1730, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcvjosepic/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1732, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcvjosepic/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 850, \"height\": 666, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcvjosepic/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 845, \"height\": 292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcvjosepic/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 847, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcvjosepic/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 739, \"height\": 613, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 728, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1765, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 851, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1775, \"height\": 507, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 824, \"height\": 526, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 856, \"height\": 346, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1782, \"height\": 1461, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1694, \"height\": 2138, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1762, \"height\": 2319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1452, \"height\": 707, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1772, \"height\": 156, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1768, \"height\": 1853, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1239, \"height\": 1161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1243, \"height\": 1284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1243, \"height\": 1284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1241, \"height\": 1284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1249, \"height\": 1242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1236, \"height\": 1035, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1244, \"height\": 1284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1238, \"height\": 1290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 850, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 849, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 849, \"height\": 474, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1236, \"height\": 1234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1251, \"height\": 842, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1854, \"height\": 1279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1772, \"height\": 261, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1286, \"height\": 633, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 871, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1046, \"height\": 465, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 879, \"height\": 400, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1403, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 1754, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-035.webp\", \"caption\": \"\", \"page\": 0, \"index\": 35, \"width\": 1763, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcvjosepic/table-036.webp\", \"caption\": \"\", \"page\": 0, \"index\": 36, \"width\": 1467, \"height\": 1311, \"label\": \"Table\"}]"
motivation: 现有临床基准局限于少数模态和任务，阻碍了多模态综合评估。
method: 构建CLIMB基准，统一整合影像、语言、时序和图等多模态临床数据。
result: CLIMB为多模态临床方法提供了全面的评估平台，验证了大规模多模态数据的重要性。
conclusion: 统一的多模态临床基准是推动多模态AI在医疗领域应用的关键基础设施。
---

## Abstract
Recent advances in clinical AI have enabled remarkable progress across many clinical domains. However, existing benchmarks and models are primarily limited to a small set of modalities and tasks, which hinders the development of large-scale multimodal methods that can make holistic assessments of patient health and well-being. To bridge this gap, we introduce Clinical Large-scale Integrative Multimodal Benchmark (CLIMB), a comprehensive clinical benchmark unifying diverse clinical data across imaging, language, temporal, and graph modalities. CLIMB comprises 4.51 million patient samples totaling 19.01 terabytes distributed across 2D imaging, 3D video, time series, graphs, and multimodal data. Through extensive empirical evaluation, we demonstrate that multitask pretraining significantly improves performance on understudied domains, achieving up to 29% improvement in ultrasound and 23% in ECG analysis over single-task learning. Pretraining on CLIMB also effectively improves models' generalization capability to new tasks, and strong unimodal encoder performance translates well to multimodal performance when paired with task-appropriate fusion strategies. Our findings provide a foundation for new architecture designs and pretraining strategies to adavance clinical AI research. Code is released at https://github.com/DDVD233/climb.

---

## 论文详细总结（自动生成）

以下是根据论文《CLIMB: Data Foundations for Large Scale Multimodal Clinical Foundation Models》生成的中文总结。

---

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：当前临床AI的基准和模型大多局限于少数模态（如影像和文本）和少数任务，无法捕捉临床实践中医生综合利用多种医学指标（如影像、时序信号、图表等）进行综合判断的需求。这阻碍了能够对患者健康进行全面评估的大规模多模态基础模型的发展。
- **整体含义**：为了推动下一代多模态临床基础模型的研究，论文构建了**CLIMB**（Clinical Large-scale Integrative Multimodal Benchmark），一个统一、大规模、多样化的多模态临床基准，覆盖影像、语言、时序和图四种数据模态，支持**多任务预训练**和**跨模态融合**，并探索了通用架构和预训练策略对临床任务的影响。

---

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：通过构建一个包含**4.51百万患者样本**、**19.01 TB**数据的大规模多模态临床基准，统一来自33家医疗机构的44个公共数据集，涵盖15种具体模态（2D图像、3D/视频、1D时间序列、图数据、多模态组合），并提供统一的标签空间和QA（CLIMB-QA）版本。在此基础上进行**多任务预训练**、**少样本迁移**和**多模态融合**的系统实验。
- **关键细节**：
  - **数据整合**：对44个数据集进行标准化处理，包括标签统一（合并语义相近的类别，如CheXpert的“Lung Opacity”与VinDr-CXR的“Infiltration”统一）、格式统一（图像保留原始分辨率，时序信号重采样至统一频率）。
  - **多任务预训练**：对每种输入模态（2D/3D视觉、图、EEG、ECG）训练一个统一的编码器，在所有相关任务上联合训练，输出一个聚合的标签词汇表。
  - **少样本迁移**：从CLIMB中剔除目标OOD数据集，用剩余数据进行预训练，再在目标OOD的少量样本（1、8、32个）上微调，评估泛化能力。
  - **多模态融合**：在MIMIC-IV上进行，使用vision、text、time series三个编码器，比较**后期融合**、**MLP融合**和**交叉注意力融合**三种策略。
- **公式/算法流程文字说明**：文中没有给出具体的数学公式，但实验流程可概括为：  
  - 构建统一标签词汇表 \( V = \bigcup_k V_k \)  
  - 训练单一编码器 \( f: X \to \{0,1\}^{|V|} \)  
  - 对于少样本迁移，在OOD数据上微调 \( f \) 的头部  
  - 多模态融合：不同模态的编码器输出 \( h_m \)，通过融合函数 \( g_\theta \) 得到最终预测。

---

### 3. 实验设计：数据集 / 场景、Benchmark、对比方法

- **数据集/场景**：
  - **多任务预训练**：使用CLIMB中所有44个数据集，覆盖13个临床领域（如放射学、心脏病学、皮肤病学等）。
  - **少样本迁移**：针对10个OOD数据集（如COVID-19 CXR、ISIC-2020、BUSI、LNDb、PTB-XL-Finegrained等），这些数据集与训练集无标签重叠或任务粒度不同。
  - **多模态融合**：在MIMIC-IV上评估长度预测（LOS）和48小时院内死亡率预测（48 IHM）两个任务。
- **Benchmark**：CLIMB本身即为统一的多模态临床基准，与现有基准（BenchMD、PMC-VQA、GMAI-MMBench、CARES）对比。
- **对比方法**：
  - **视觉编码器**：MedViT、PMC-CLIP、RAD-DINO（医学专用） vs. ConvNeXtV2、Swin Transformer、EVA-2、InternViT（通用）。
  - **EEG编码器**：SPARCNet、CNNTransformer、FFCL、ContraWR、STTransformer、BIOT（含预训练变体）。
  - **ECG编码器**：ECG-JEPA、UniTS。
  - **图编码器**：GCN、GAT、Graph Transformer。
  - **临床VLM**：LLaVA-Med（零样本和微调）。
  - **多模态融合**：后期融合、MLP融合、交叉注意力融合。

---

### 4. 资源与算力

- 文中明确提到：**所有实验在8×H200 141GB GPU的服务器上运行**（见附录D.4.2）。
- 训练细节：视觉实验使用SOAP优化器，学习率搜索范围1e-5~1e-3；EEG实验使用Adam，lr=1e-3；ECG实验使用Adam，lr=1e-3或1e-4；批次大小根据不同模型为32或512。
- **未明确说明具体训练时长**，但提及保存5个epoch内最低loss的模型。

---

### 5. 实验数量与充分性

- **实验数量**：
  - **RQ1多任务预训练**：在8个视觉编码器、6个EEG模型、2个ECG模型、3个图模型上进行了跨28个视觉数据集+多个EEG/ECG数据集的评估，结果汇总于表3-6和附录表14-31。
  - **RQ2少样本迁移**：9个OOD数据集（视觉、EEG、ECG各多个），对比CLIMB预训练与标准预训练，结果图5-7。
  - **RQ3多模态融合**：3种融合策略 × 2种初始化（CLIMB vs. SoTA） × 2个任务（LOS, 48 IHM） × 2种数据量（全量、8-shot），结果表7。
  - **消融与对比**：还包括标签标准化消融（表12）、自监督预训练消融（表33-35）、与数据集专用SoTA对比（表36）。
- **充分性**：实验设计系统、覆盖多个维度（不同架构、不同数据量、不同任务类型），并附有详细的附录表格。但需要注意的是，部分数据集（如CMMD）因标签问题被排除在实验外，且未在所有模型上测试所有数据集（如视频模型未用于图像任务）。整体上实验设计比较全面，公平性通过统一评价指标和标准化训练流程保障。

---

### 6. 论文的主要结论与发现

1. **多任务预训练显著提升性能**：尤其对研究不充分的领域（如COVID超声AUC提升32.54%，ECG Ga数据集AUC提升23%）。
2. **通用域架构优于专用医疗架构**：ConvNeXtV2在视觉任务上表现最佳；在EEG领域，预训练模型优于从头训练，但更多数据未必更好，数据质量更重要；在ECG领域，专用模型ECG-JEPA优于通用时序模型UniTS。
3. **少样本迁移中，CLIMB预训练优于标准预训练**：在超声（+29.1% AUC）、CT（+28.7%）、ECG（+23%）上效果显著。
4. **多模态融合时，任务复杂度决定最佳融合策略**：复杂任务（LOS）需交叉注意力，简单任务（48 IHM）用MLP融合即可。
5. **临床VLM（LLaVA-Med）在CLIMB上微调后仍大幅落后于专用视觉编码器**（准确率低32.2%），表明当前VLM在细粒度临床理解上仍有不足。

---

### 7. 优点

- **数据规模大、模态全**：4.51M样本，19.01TB，涵盖2D、3D、1D、图、多模态，覆盖33家机构18个国家，包括不发达地区。
- **标准化处理细致**：统一标签、保留元数据、提供QA版本，便于不同模型公平比较。
- **实验设计系统**：三个研究问题环环相扣，从多任务到迁移再到融合，逻辑清晰。
- **开源全面**：代码、预处理脚本、预训练权重全部公开，可复现。
- **对临床AI发展有实际指导意义**：给出了架构选择、预训练策略、融合策略的具体建议。

---

### 8. 不足与局限

- **部分数据集标签问题**：CMMD因标签验证问题被排除在实验外，可能影响乳腺钼靶评估的完整性。
- **OOD数据集验证**：虽然标签无重叠，但部分OOD数据集与训练集在数据来源或任务上仍有相似性，文中通过成员推断实验验证了区分度，但未在所有OOD上验证。
- **未充分探索自监督预训练**：在视觉领域，MAE和对比学习未提升性能，但只在ConvNeXtV2和InternViT上测试，结论可能不普适。
- **多模态融合仅用固定编码器**：没有探索同时联合训练编码器与融合层，融合策略可能未达到最优。
- **临床VLM比较**：只用了LLaVA-Med一个模型，未包含当前更先进的VLM（如Med-Gemini），对比不够全面。
- **潜在偏差风险**：数据集虽涉及不发达地区，但整体仍以欧美为主，地区分布不均可能导致模型偏向；隐私和公平性在论文中仅简要提及，未做定量分析。
- **计算资源未明确**：训练时长、总GPU时数等未报告，影响复现和成本评估。

---

（完）
