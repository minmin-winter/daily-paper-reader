---
title: "Diffuse Everything: Multimodal Diffusion Models on Arbitrary State Spaces"
title_zh: 扩散一切：任意状态空间上的多模态扩散模型
authors: "Kevin Rojas, Yuchen Zhu, Sichen Zhu, Felix X-F. Ye, Molei Tao"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=AjbiIcRt6q"
tags: ["query:native-multi"]
score: 8.0
evidence: 在任意状态空间上原生多模态扩散模型的框架
tldr: Diffuse Everything提出了一种在任意状态空间上构建原生多模态扩散模型的框架，无需外部分词器或变分自编码器进行模态统一。该方法直接联合生成多模态数据，减轻了对编码器-解码器精度的依赖，特别适用于小数据场景。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1598, \"height\": 571, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1343, \"height\": 683, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 372, \"height\": 369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 371, \"height\": 369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 372, \"height\": 369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 789, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1579, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1583, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1578, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 361, \"height\": 2104, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 364, \"height\": 2104, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 362, \"height\": 2112, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 363, \"height\": 2104, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 364, \"height\": 2097, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ajbiicrt6q/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 362, \"height\": 2111, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1775, \"height\": 744, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1640, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1627, \"height\": 403, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1050, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 479, \"height\": 624, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 769, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1240, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1487, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1470, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ajbiicrt6q/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1468, \"height\": 362, \"label\": \"Table\"}]"
motivation: 现有多模态扩散模型依赖外部预处理协议将数据统一为单模态格式，对小数据场景不友好。
method: 提出在任意状态空间上直接构建多模态扩散模型的框架，实现原生多模态生成。
result: 在较少数据下也能有效生成多模态数据，降低了对编码器-解码器精度的依赖。
conclusion: 该框架为构建原生多模态生成模型提供了新范式。
---

## Abstract
Diffusion models have demonstrated remarkable performance in generating unimodal data across various tasks, including image, video, and text generation. On the contrary, the joint generation of multimodal data through diffusion models is still in the early stages of exploration. Existing approaches heavily rely on external preprocessing protocols, such as tokenizers and variational autoencoders, to harmonize varied data representations into a unified, unimodal format. This process heavily demands the high accuracy of encoders and decoders, which can be problematic for applications with limited data. To lift this restriction, we propose a novel framework for building multimodal diffusion models on arbitrary state spaces, enabling native generation of coupled data across different modalities. By introducing an innovative decoupled noise schedule for each modality, we enable both unconditional and modality-conditioned generation within a single model simultaneously. We empirically validate our approach for text-image generation and mixed-type tabular data synthesis, demonstrating that it achieves competitive performance. Code is available at https://github.com/KevinRojas1499/Diffuse-Everything.

---

## 论文详细总结（自动生成）

# 论文核心问题与整体含义（研究动机和背景）

- **研究动机**：现有多模态扩散模型（如 Chameleon、UniDiffuser、OmniFlow 等）通常依赖外部预处理协议（例如 tokenizer 或 VAE）将不同模态的数据统一为单一格式（离散 token 或连续隐向量）。这种“先统一再生成”的范式高度依赖编码器-解码器的精度，在小数据场景下容易引入生成伪影，且不便于扩展到任意模态组合。
- **整体含义**：论文提出一种**原生多模态扩散模型框架**，允许在不同模态的原始状态空间（连续欧氏空间、离散有限空间、黎曼流形等）上直接联合建模，无需额外编码器/解码器统一数据表示。该框架通过为每个模态引入独立的、解耦的噪声时间变量，使单一模型同时支持无条件联合生成和任意模态条件生成。

# 方法论：核心思想、关键技术细节与算法流程

### 核心思想：解耦时间变量的多模态前向过程

- 将数据分布定义在乘积状态空间 \( \mathcal{X}^1 \times \cdots \times \mathcal{X}^n \) 上。
- 为每个模态 \( i \) 独立定义一个 Markov 前向过程（时间变量 \( t_i \)），各过程在给定初始条件下相互独立。
- 前向过程整体记为 \( X_t = (X^1_{t_1}, \dots, X^n_{t_n}) \)，其中 \( t = (t_1, \dots, t_n) \)。

### 关键技术细节

1. **统一学习目标**：论文推广了 Denoising Markov Model 框架，提出了一种**广义显式得分匹配损失（GESM）**，并证明其与可训练的隐式得分匹配损失（IGDSM/IGISM）等价。该损失可直接分解为各模态条件得分匹配损失的求和，学习联合边际分布 \( p(x, t) \)。
2. **连续-离散多模态扩散**：作为实例，论文详细推导了连续空间（欧氏）与离散空间（有限状态）的联合前向/后向过程。
   - 连续部分采用 Ornstein-Uhlenbeck SDE；离散部分采用带屏蔽 token 的 CTMC。
   - 后向过程通过时间反演得到，其中条件得分可简化为各模态自身的条件得分（得益于贝叶斯定理和条件独立性）。
3. **噪声引导（Noisy Guidance）**：利用解耦时间变量的特性，提出了一种新的引导机制——用部分噪声条件（而非完全无条件的评分）作为引导，从而在保持多样性的同时提升生成质量。该引导可视为对 Classifier-Free Guidance 的推广。

### 算法流程（文字说明）

- **无条件联合生成**：从纯噪声（\( t_i = T \)）开始，选择共同的时间参数化 \( u \in [0,T] \)，使各模态时间同步下降，同时模拟后向 SDE 和 CTMC。
- **条件生成**：给定一个模态的干净数据（\( t=0 \)）或部分噪声数据（\( 0<t<T \)），模拟另一模态的后向过程。论文特别指出，利用部分噪声条件进行引导（Noisy Guidance）可提升 FID 等指标。
- **训练**：交替从联合分布中采样噪声水平对 \( (t,s) \)，对连续部分最小化得分匹配损失，对离散部分最小化得分熵损失（实际实现中采用交叉熵损失等价形式）。

# 实验设计：数据集、Benchmark 与对比方法

### 任务一：文本-图像生成

- **训练数据集**：SAM-LLaVA 数据集（由 LLaVA 为 SAM 图像生成描述），含约 1200 万图像-文本对。
- **评估基准**：MS-COCO 30K 验证集上的 FID-30K（文本到图像）。
- **对比方法**：包括专门文本生成图像的方法（DALL-E 2, Imagen, Stable Diffusion, PixArt-α, MMDiT-improved）以及多模态生成模型（Show-o, Transfusion, Chameleon, JetFormer, Versatile Diffusion, UniD3）。
- **评价指标**：FID、CLIP 相似度（额外报告）、以及定性样本展示。

### 任务二：混合类型表格数据合成

- **数据集**：6 个 UCI 真实表格数据集（Adult, Default, Shoppers, Magic, Beijing, News），包含数值和分类特征。
- **对比方法**：GOGGLE, STaSy, CoDi, TabDDPM, TAB SYN。
- **评价指标**：Trend（列相关）、MLE（下游分类/回归 AUC/RMSE）、Shape（列分布）、α-Precision、β-Recall。

### 额外实验：黎曼-离散多模态扩散

- 在 SO(3) × 离散标签的玩具数据上验证框架的通用性。

# 资源与算力

- **文本-图像模型**：总参数量 578M，联合嵌入+单模态约 481M。训练采用 3 阶段策略（600K + 200K + 140K 迭代），批量大小 256→512，使用 AdamW 优化器。
- **表格模型**：约 64K 参数，4 个 DiT 块，隐层维度 24，训练 200 步 warmup，批量大小 2048。
- **未明确说明**：GPU 型号、数量、总训练时长在论文中未明确给出。根据模型规模推断，文本-图像模型可能在 4-8 张 A100 上训练，表格模型可在单张 GPU 上快速完成。

# 实验数量与充分性

### 实验数量

- 文本-图像：在 MS-COCO 上报告 FID-30K 并与 10+ 种方法对比；还报告了 CLIP 相似度和定性样本。
- 表格数据：在 6 个数据集上报告 5 种指标（Trend、MLE、Shape、α-Precision、β-Recall），每个实验重复 20 次给出均值与标准差。
- 消融实验：文本-图像任务中，针对 Noisy Guidance 的不同噪声强度 σ 进行了 FID 对比（图 4）。
- 额外实验：黎曼-离散玩具数据上的条件生成和联合生成可视化。

### 充分性与公平性

- **充分性**：覆盖了两类典型多模态任务，且对比了大量 SOTA 方法。表格实验中重复 20 次确保统计稳健性。
- **公平性**：表格实验中，自己的模型参数量仅为对比方法的 1/100~1/200，展现了极高的参数效率；但文本-图像任务中，自己的 FID 16.16 并非最优（低于 Imagen 7.27、MMDiT 6.79 等），且未使用预训练模型或大容量编码器，因此比较尺度不完全一致。作者也指出训练数据量较小（1200 万 vs 数十亿量级）。
- **客观性**：对比方法的结果大多来自原论文或复现，未发现明显不公。

# 主要结论与发现

1. **核心结论**：提出的通用多模态扩散框架可以在不经数据格式统一的前提下，在任意状态空间上联合生成多模态数据，且训练目标可分解为各模态独立损失的求和。
2. **性能表现**：
   - 文本-图像：在 FID 上达到 16.16（MS-COCO 30K），虽不及顶尖模型，但参数效率更高，且无需额外编码器/解码器。
   - 表格数据：在 Trend 和 MLE 上达到最佳或次佳，且参数量仅约 64K，为最小模型。
3. **噪声引导的有效性**：使用部分噪声条件作为引导（Noisy Guidance）优于传统无条件引导，在 FID 上带来显著提升。
4. **通用性**：在黎曼-离散组合场景（SO(3) × 标签）上同样有效，表明框架可推广到混合状态空间。

# 优点

1. **理论严谨**：从 Markov 过程的生成元出发，给出了多模态扩散模型的统一学习目标，并严格证明了其等价可训练形式。
2. **无需外部编码器**：直接在原始状态空间上进行生成，避免预处理带来的误差和数据需求瓶颈。
3. **任意模态组合**：框架可扩展到任意数量的模态（连续、离散、黎曼等），具有高度通用性。
4. **参数高效**：表格任务中 64K 参数即达到最佳性能，文本-图像模型也远小于同类方法。
5. **单一模型多任务**：一个模型同时支持无条件联合生成、条件生成（任意方向），以及带噪声引导的高质量生成。

# 不足与局限

1. **文本-图像生成质量不及 SOTA**：FID 16.16 远高于当前最优水平（~6-7），主要受限于较小训练数据集（SAM-LLaVA）和未使用预训练文本/图像编码器。
2. **未探索预训练初始化**：论文明确提到“未探索利用预训练单模态扩散模型作为初始化”，若能结合预训练权重，训练效率和性能可能进一步提升。
3. **训练策略较为复杂**：文本-图像模型使用了多阶段训练（3-4 个阶段），需要手动调节训练顺序和冻结策略，缺乏自适应简化方案。
4. **推理效率未详细分析**：文中未讨论采样步数、计算开销等，对于实际应用的可扩展性稍显不足。
5. **应用场景有限**：实验仅涵盖文本-图像和表格数据，未在视频、音频、3D 等更复杂多模态场景上验证。

（完）
