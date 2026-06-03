---
title: "MoHAVE: Mixture of Hierarchical Audio-Visual Experts for Robust Speech Recognition"
title_zh: MoHAVE：层次化音频-视觉专家混合用于鲁棒语音识别
authors: "Sungnyun Kim, Kangwook Jang, Sangmin Bae, Sungwoo Cho, Se-Young Yun"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=ZkybWzxvw9"
tags: ["query:balanced-mml"]
score: 8.0
evidence: 利用专家混合实现音频视觉模态的动态自适应融合
tldr: MoHAVE提出了一种稀疏混合专家框架用于音频-视觉语音识别，通过激活模态特定的专家组实现动态适应，在最小计算开销下有效缩放模型容量。该方法通过专家路由隐式平衡了音频和视觉模态的贡献，直接支持自适应模态平衡需求。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-zkybwzxvw9/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 833, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zkybwzxvw9/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 853, \"height\": 694, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zkybwzxvw9/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1641, \"height\": 1210, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zkybwzxvw9/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1762, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zkybwzxvw9/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1771, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zkybwzxvw9/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1769, \"height\": 921, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zkybwzxvw9/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1422, \"height\": 887, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 857, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 546, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 856, \"height\": 436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1770, \"height\": 784, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1766, \"height\": 502, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1767, \"height\": 259, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 961, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1768, \"height\": 778, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1268, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zkybwzxvw9/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1402, \"height\": 298, \"label\": \"Table\"}]"
motivation: 现有音频视觉语音识别系统难以在不牺牲计算效率的情况下进行扩展。
method: 采用稀疏混合专家架构，激活模态特定的专家组以实现动态适应。
result: 在多个数据集上实现了鲁棒且高效的音频视觉语音识别性能。
conclusion: MoHAVE为多模态系统提供了一种可扩展且平衡的自适应融合方案。
---

## Abstract
Audio-visual speech recognition (AVSR) has become critical for enhancing speech recognition in noisy environments by integrating both auditory and visual modalities. However, existing AVSR systems struggle to scale up without compromising computational efficiency. In this study, we introduce MoHAVE (Mixture of Hierarchical Audio-Visual Experts), a novel robust AVSR framework designed to address these scalability constraints. By leveraging a Mixture-of-Experts (MoE) architecture, MoHAVE activates modality-specific expert groups, ensuring dynamic adaptation to various audio-visual inputs with minimal computational overhead. Key contributions of MoHAVE include: (1) a sparse MoE framework that efficiently scales AVSR model capacity, (2) a hierarchical gating mechanism that dynamically utilizes the expert groups based on input context, enhancing adaptability and robustness, and (3) remarkable performance across robust AVSR benchmarks, including LRS3 and MuAViC transcription and translation tasks, setting a new standard for scalable speech recognition systems.

---

## 论文详细总结（自动生成）

## 论文《MoHAVE: Mixture of Hierarchical Audio-Visual Experts for Robust Speech Recognition》详细中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：音频‑视觉语音识别（AVSR）系统在提高鲁棒性方面至关重要，但现有模型在扩展规模时面临计算效率瓶颈。传统的 AVSR 模型（如 AV‑HuBERT、Auto‑AVSR）通常参数少于 0.5B，远小于纯音频 ASR 模型（如 Whisper 达 1.6B，Seamless 达 2.3B）。增大模型容量主要提升音频语义理解，而视觉处理能力提升有限，且带来更高的延迟和计算开销，难以满足实际部署需求。
- **整体含义**：论文旨在提出一种可扩展且高效的方法，使 AVSR 系统在不显著增加计算成本的前提下提升容量和鲁棒性，尤其在噪声环境下动态利用音频和视觉信息。

### 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：利用稀疏 Mixture‑of‑Experts（MoE）架构，将专家分为音频和视觉两个专门组合（expert groups），并通过**层次化门控机制**（hierarchical gating）动态分配令牌到不同的专家组，实现自适应、低开销的模态融合。
- **关键技术细节**：
  - **Sparse MoE 架构**：在解码器的每个 FFN 层替换为专家模块，每个令牌仅激活 top‑k 专家（默认 k=2，MoHAVE 为每专家组 top‑1，总共 2 个专家）。总参数扩大，但激活参数仅约一半。
  - **层次化门控结构**：
    - **层间路由器（Inter‑modal router）**：根据输入令牌的上下文，学习为音频专家组和视觉专家组分配权重（top‑m 专家组选择，默认 m=2 即两组都激活）。
    - **层内路由器（Intra‑modal router）**：在每个专家组内选择 top‑1 专家（通过 Kronecker delta 硬选择）。
    - 输出为两组专家的加权和。
  - **负载偏置损失（Load Biasing Loss）**：鼓励特定模态的输入（音频只或视频只）尽可能路由到对应的专家组，从而提高专家组的专门化。对于同时包含音频和视频的序列，该损失不施加偏置，由路由器自主学习最优分配。
  - **负载均衡损失**（辅助损失）和 **路由器 z 损失**用于稳定训练和均衡专家负载。
- **公式/算法流程**（文字说明）：
  - 令牌 x 先通过层间路由器得到每组的选择概率 q_i(x)，选择 top‑m 组。
  - 在每个被选中的组内，层内路由器计算专家选择概率 p_{ij}(x)，选择 top‑k 专家（k=1），并取概率最高的专家输出 E_{ij}(x)。
  - 最终输出 y = Σ_i (˜q_i(x) × E_{ij}(x))，其中 ˜q_i 为归一化后的权重。
  - 总损失 L = L_CE + c_B L_B + c_S L_S + c_Z L_Z。

### 3. 实验设计：数据集、基准、对比方法
- **数据集**：
  - **LRS3‑TED**（433 小时，5000+ 说话人）用于鲁棒 AVSR 基准。音频噪声来自 **MUSAN**（babble、speech、music、natural），以 SNR 区间 [‑10, 10] dB 随机添加。额外使用 **DEMAND** 数据集进行真实环境噪声评估。
  - **MuAViC**（1200 小时，8000+ 说话人，9 种语言）用于多语言 AVSR 和 X→英文语音‑文本翻译（AVS2TT）。噪声使用多语言 babble（SNR=0 dB）。
- **基准**：
  - LRS3 上评估：**N‑WER**（四种噪声类型×五个 SNR 的平均 WER）和 **C‑WER**（干净音频 WER）。
  - MuAViC 上评估：AVSR 的 WER 和 AVS2TT 的 BLEU 分数。
- **对比方法**：
  - 基线和消融：AV‑HuBERT（Base/Large）、AV‑MoE（4/8 专家）、硬路由（Hard Routing）、不含负载偏置的 MoHAVE。
  - SOTA 对比：MIR‑GAN、UniVPM、CMA、BRAVEn、XLAVS‑R、Whisper large‑v2 等。
  - 多语言任务：mAV‑HuBERT（Anwar et al., 2023）、XLAVS‑R 300M/2B、Whisper large‑v2。

### 4. 资源与算力
- **文中未明确说明 GPU 型号、数量、训练时长**。仅提到：
  - LRS3 上 finetune 120K steps，前 90K 冻结编码器，仅训练解码器，后 30K 全微调。学习率 5e‑4，每步 8000 帧（约 320 秒语音），beam size 50。
  - MuAViC 上 finetune 120K steps，10K 后解冻编码器。
  - 提供了模型计算量（FLOPs）对比（见表 1）：MoHAVE‑Base 12.1→14.8 GFLOPs/序列，Large 32.2→39.3 GFLOPs，说明计算增加不大。具体硬件资源未报告。

### 5. 实验数量与充分性
- **实验组数较多**：包括 LRS3 上标准噪声（四种类型×五个 SNR）与 DEMAND 真实噪声（18 种环境）的评估；多语言 AVSR（8 种语言）和 AVS2TT（6 种语言）的有/无噪声场景；消融实验（简单 MoE vs 硬路由 vs MoHAVE 有无负载偏置）；专家负载分析（按输入模态、噪声类型/强度、语言）；超参数测试（激活专家数量）；编码器/解码器变体、uptraining；与多篇 SOTA 方法对比。
- **充分性评价**：实验较为充分且客观。消融设计清晰，验证了层次门控和负载偏置的有效性。噪声条件覆盖广泛（合成噪声+真实环境），多语言验证提升了泛化性。公平性方面：与 SOTA 对比时，尽量使用相同编码器（AV‑HuBERT）或相同预训练数据（mAV‑HuBERT from Choi et al.）。但仍存在一些局限（见第8点）。

### 6. 论文的主要结论与发现
- **主要结论**：MoHAVE 通过稀疏 MoE 和层次化门控实现 AVSR 的高效扩展，在保持计算成本接近基线的情况下，显著提升噪声鲁棒性（N‑WER：Base 5.8%，Large 4.5%，相比 AV‑HuBERT 约降低 20‑30% 相对误差）。在 LRS3 和 MuAViC 多项基准上达到 SOTA。
- **关键发现**：
  - 单纯增加 MoE（AV‑MoE）提升有限，专家组专门化（硬路由）是关键。
  - 层次门控（MoHAVE）比硬路由更优，能根据噪声条件自适应调整音频/视觉组权重：噪声高时增加视觉组使用；噪声类型不同（babble vs natural）最优比例不同。
  - 负载偏置损失对于维持专家组专门化至关重要。
  - 在多语言任务中，MoHAVE 进一步降低 WER，提升 BLEU，尤其在高噪声下。

### 7. 优点
- **方法创新**：首次将稀疏 MoE 与层次化门控应用于 AVSR，实现动态模态平衡，是对硬路由的改进。
- **计算高效**：仅激活约一半参数，FLOPs 增加不到 25%，适合部署。
- **全面实验**：覆盖多种噪声、多语言、真实环境，消融充分，与多个 SOTA 比较。
- **可解释性**：通过专家负载分布（图 4‑7）展示了模型自适应行为，验证了设计动机。
- **开源潜力**：代码基于 AV‑HuBERT，易于复现（文中未直接提供代码链接，但声明了模型细节）。

### 8. 不足与局限
- **实验覆盖**：
  - 未进行**大规模预训练**（如从零开始预训练 MoE 编码器，仅使用了 finetune 或 uptraining）。MoE 主要用于解码器，编码器仍为原始 AV‑HuBERT。
  - **未与其他模态（如文本）多模态 MoE 方法直接比较**（如 AVMoE、EVA 等），仅在附录中简要说明不具可比性。
  - **多语言干净环境提升有限**（表 7），表明 MoHAVE 主要增强噪声鲁棒性，干净场景优势不明显。
  - **消融中未对比不同专家数量组合的更多设置**（表 8 仅对 Base 模型测试了有限组合）。
- **偏差风险**：多语言任务使用预训练 mAV‑HuBERT（来自 Choi et al.），可能已包含语言偏差。负载偏置损失假设输入可显式区分为音频/视频/音视频，但实际应用中可能同时存在异步或缺失模态的情况（论文未深入讨论）。
- **应用限制**：当前 MoHAVE 设计为 decoder‑only 的 MoE，编码器未 MoE 化，若需联合编码器 MoE 则需要更多计算和预训练。层次门控计算两个专家组的所有专家，在专家组数量增多时开销可能线性增长。
- **未提供具体资源开销**（GPU 型号、训练时间），难评估实际复现代价。

（完）
