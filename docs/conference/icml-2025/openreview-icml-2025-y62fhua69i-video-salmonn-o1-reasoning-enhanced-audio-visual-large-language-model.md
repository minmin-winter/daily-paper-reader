---
title: "video-SALMONN-o1: Reasoning-enhanced Audio-visual Large Language Model"
title_zh: video-SALMONN-o1：推理增强的音频-视觉大语言模型
authors: "Guangzhi Sun, Yudong Yang, Jimin Zhuang, Changli Tang, Yixuan Li, Wei Li, Zejun MA, Chao Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=y62fhuA69I"
tags: ["query:mm-reasoning"]
score: 9.0
evidence: 推理增强的音频-视觉大语言模型用于通用视频理解
tldr: 现有推理优化工作局限于数学和视觉图形，忽略了通用视频理解。本文提出video-SALMONN-o1，首个开源推理增强的音频-视觉大语言模型。通过构建包含挑战性音频-视觉问题的推理数据集，并设计过程直接偏好优化（pDPO）进行步骤级奖励，显著提升了视频理解中的推理能力。实验结果在多个视频问答基准上取得新高度。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 856, \"height\": 659, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 854, \"height\": 406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1505, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 854, \"height\": 401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 774, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1218, \"height\": 284, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1227, \"height\": 306, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1229, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 581, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1224, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1413, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1409, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1226, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1238, \"height\": 664, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1230, \"height\": 186, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1233, \"height\": 715, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1415, \"height\": 212, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1414, \"height\": 211, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-y62fhua69i/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1402, \"height\": 462, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 818, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1782, \"height\": 661, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1607, \"height\": 430, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1368, \"height\": 322, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1530, \"height\": 625, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1335, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1351, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-y62fhua69i/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1607, \"height\": 193, \"label\": \"Table\"}]"
motivation: 现有推理优化方法未覆盖通用视频理解中的音频-视觉推理。
method: 构建推理密集型音频-视觉数据集，并提出过程直接偏好优化（pDPO）进行步骤级奖励。
result: 在多个视频理解基准上取得最佳性能，证明了推理增强的有效性。
conclusion: 推理增强和合理的步骤级优化是提升视频理解模型中音频-视觉推理的关键。
---

## Abstract
While recent advancements in reasoning optimization have significantly enhanced the capabilities of large language models (LLMs), existing efforts to improve reasoning have been limited to solving mathematical problems and focusing on visual graphical inputs, neglecting broader applications in general video understanding. This paper proposes video-SALMONN-o1, the first open-source reasoning-enhanced audio-visual LLM designed for general video understanding tasks. To enhance its reasoning abilities, we develop a reasoning-intensive dataset featuring challenging audio-visual questions with step-by-step solutions. We also propose process direct preference optimization (pDPO), which leverages contrastive step selection to achieve efficient step-level reward modelling tailored for multimodal inputs. Additionally, we introduce RivaBench, the first reasoning-intensive video understanding benchmark, featuring over 4,000 high-quality, expert-curated question-answer pairs across scenarios such as standup comedy, academic presentations, and synthetic video detection. video-SALMONN-o1 achieves 3-8% accuracy improvements over the LLaVA-OneVision baseline across different video reasoning benchmarks. Besides, pDPO achieves 6-8% improvements compared to the supervised fine-tuning model on RivaBench. Enhanced reasoning enables video-SALMONN-o1 zero-shot synthetic video detection capabilities.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **背景**：大语言模型（LLM）的推理优化（如思维链 CoT、过程奖励模型 PRM）在文本数学和代码任务上取得了显著进展，但在多模态领域，现有工作主要聚焦于**图像上的数学推理**，忽略了更广泛的**通用视频理解**任务。通用视频理解需要同时处理音频、视觉和文本模态，且推理过程常涉及对时间、因果、物理规则等复杂逻辑的理解。
- **核心问题**：如何为音频-视觉大语言模型（AV-LLM）设计有效的推理增强方法，使其能够处理一般性视频中的逻辑推理（如理解学术演讲中的概念、分析喜剧中的笑点、检测合成视频中的异常），并弥补现有开源模型在此类任务上的空白。
- **整体含义**：本文提出 **video‑SALMONN‑o1**，首个开源的推理增强型音频-视觉大语言模型，旨在将推理能力从文本/图像推广到通用视频理解，填补了该领域的研究缺口。

### 2. 论文提出的方法论

- **核心思想**：通过**推理密集型监督微调（SFT）** 先让模型学习结构化推理路径，然后利用**过程偏好优化（pDPO）** 进行步骤级强化学习，精细调整推理过程。
- **关键技术细节**：
  - **模型结构**：基于 video‑SALMONN 2 架构，包含独立的视觉编码器（SigLIP）、音频编码器（Whisper‑Large‑v3）和模态对齐器，通过**交错同步模块**按时间顺序拼接视觉与音频 token 后送入 LLM（Qwen‑2‑7B），使用 LoRA 微调。
  - **推理密集型 SFT 数据构建**：
    1. 利用 **Gemini‑1.5‑pro** 从训练视频（含音频）生成问题、答案及**逐步推理步骤**。
    2. 使用 **GPT‑4o** 进行质量检查，丢弃不合格样本并重新生成，避免单一模型偏差。
    3. 数据包含约 **30k** 个具有挑战性的 QA 对，每个 QA 均配有 6‑10 步推理链（图 4 显示分布）。
  - **过程直接偏好优化（pDPO）**：
    - **核心公式**（基于 Bradley‑Terry 模型）：
      \[
      L = -\mathbb{E}\left[ \alpha_k \log p(s_k \succ s'_k) + (1-\alpha_k)\log p(s'_k \succ s_k) \right]
      \]
      其中 \(p(s_k \succ s'_k) = \sigma(r(s_k) - r(s'_k))\)，\(r(s_k) = \beta \log \frac{\pi_\theta(s_k|s_{<k}, H_{AV})}{\pi_{\text{ref}}(s_k|s_{<k}, H_{AV})}\)，\(\alpha_k\) 通过 rollout 的预期正确性决定（可硬标签或软标签）。
    - **对比步骤选择**：对每个中间步骤 \(s_k\)，对输入视频施加微小扰动，计算归一化 KL 散度 \(d_{s_k}\)（公式略），衡量该步骤对输入变化的敏感度。选择 **Top‑T** 高敏感度步骤进行 rollout（图 3），因为这些步骤更易出现视频内容误解或幻觉，从而聚焦优化关键错误点。
    - **训练流程**：SFT 后，从错误推理路径中采样，对完整路径使用 PPRM（完整路径偏好），对选中的关键步骤使用 pDPO 进行步骤级偏好训练，共生成约 200k 偏好对（100k 完整路径 + 100k 步骤级）。

### 3. 实验设计

- **数据集与 Benchmark**：
  - **RivaBench**：新构建的推理密集型视频理解基准，包含 **4,000+** 人类专家标注的 QA 对，覆盖三个场景：
    - **单口喜剧（StandUp）**：需结合语调、表情和手势分析笑点成因，2,128 个 QA。
    - **学术演讲（Academic）**：基于 M³AV 测试集，需理解专业内容并推理因果关系，1,912 个 QA。
    - **合成视频检测（SynthDec）**：利用 Hunyuan‑large 生成合成视频，需判断视频真实性，200 个 QA。
  - **额外基准**：Video‑MME（音频-视觉）和 NExT‑QA（视觉），用于评估通用视频理解。
- **对比方法**：
  - **专有模型**：GPT‑4o（视觉仅）、Gemini‑1.5‑pro（音频+视觉），并测试其是否使用 CoT 推理。
  - **开源模型**：LLaVA‑OneVision（视觉）、video‑SALMONN、Video‑LLaMA 2.1（音频+视觉）。
  - **消融变体**：不同 SFT 数据设置（有无推理部分）、不同奖励模型（ORM、PRM、PPRM、pDPO 变体）。

### 4. 资源与算力

- **SFT 阶段**：使用 **16 块 A100 GPU**，训练 **48 小时**。
- **pDPO 阶段**：使用 **8 块 A100 GPU**，训练 **24 小时**。
- 视觉编码器、音频编码器和 LLM 主干在训练期间冻结，仅训练音频对齐器、模态对齐器和 LoRA 模块（r=64, α=256）。

### 5. 实验数量与充分性

- **实验组数**：论文在 **3 个主要基准**（Video‑MME、NExT‑QA、RivaBench）上报告了结果，并进行了多组消融实验：
  - **SFT 数据消融**（表 3）：比较完整 SFT 数据、移除推理部分、仅推理部分等 6 种设置。
  - **奖励模型消融**（表 4）：比较 SFT 1‑best、Majority Voting、ORM、PRM、pDPO（含不同步骤选择）共 7 种配置。
  - **步骤选择消融**（图 5）：比较仅完整路径、完整路径+Top‑3 步骤、完整路径+所有步骤。
  - **异常检测案例**：展示了 LLaVA‑OneVision、GPT‑4o、Gemini‑1.5‑pro 与 video‑SALMONN‑o1 的定性对比（附录 G、H）。
- **充分性与公平性**：实验较为充分，覆盖主流基准和新构建的复杂场景；对比方法包括同架构变体（LLaVA‑OneVision）和音频-视觉同类模型（video‑SALMONN、Video‑LLaMA 2.1），且控制推理策略（是否 CoT）；但未与其他近期 o1‑like 多模态模型（如 Virgo、MAmmoTH‑VL）对比，可能因时间限制。

### 6. 论文的主要结论与发现

1. **推理增强有效**：video‑SALMONN‑o1 在 Video‑MME、NExT‑QA、RivaBench 上比 LLaVA‑OneVision 基线**绝对提升 3‑8%**，比 SFT 模型提升 **6‑8%**（表 2）。
2. **pDPO 优于传统奖励模型**：pDPO 的 1‑best 结果（65.6% Video‑MME）显著优于 ORM（62.7%）和 PRM（63.5%）的 best‑of‑20 结果（表 4），表明步骤级成对偏好建模比绝对分数预测更适合通用视频推理。
3. **对比步骤选择带来提升**：选择 Top‑3 敏感步骤进行 pDPO 训练比仅使用完整路径或所有步骤更优（图 5），说明聚焦视频相关错误步骤是高效的。
4. **零样本合成视频检测能力**：pDPO 模型在 SynthDec 上获得 17.8% F1（精确率 87%），而其他开源模型几乎全预测为“真实”，展示了推理增强带来的**涌现能力**。
5. **推理密集型 SFT 数据的重要性**：移除该部分数据后，推理性能明显下降（表 3 行 4 vs 行2）；但仅使用推理数据会导致基础感知能力不足（行 5），需平衡。

### 7. 优点

- **方法创新**：首次将过程偏好优化（pDPO）与对比步骤选择结合到通用视频理解中，无需外部奖励模型，训练高效。
- **数据质量**：推理密集型 SFT 数据采用双模型（Gemini + GPT‑4o）生成和校验，减少偏差，且包含真实人类专家标注的 RivaBench 基准。
- **任务覆盖广**：除传统问答外，涵盖**合成视频检测**这一新兴且高难度任务，展示推理能力对实际应用的帮助。
- **开源与可复现**：承诺公开代码、模型、数据，有利于社区验证和后续发展。
- **公平对比**：考虑了推理策略（是否 CoT）对结果的影响，并分析视觉仅模型（GPT‑4o）因缺乏音频而表现更差的现象。

### 8. 不足与局限

- **计算资源需求高**：SFT 需 16×A100 训练 48 小时，pDPO 需 8×A100 训练 24 小时，小规模团队可能难以复现。
- **推理性能依赖数据质量**：SFT 数据依赖 Gemini‑1.5‑pro 生成，可能存在长尾分布覆盖不充分；pDPO 的 rollout 次数有限（文中为 6 次），过程标签估计有噪声。
- **偏差风险**：预训练编码器（Whisper、SigLIP）可能对特定人口群体表现不佳；LLM 主干（Qwen‑2）可能继承社会偏见；RivaBench 的学术和喜剧场景主要来自英语演讲和西方文化，多样性受限。
- **应用限制**：合成视频检测仅测试了同类型生成模型（Hunyuan‑large），对其他篡改或生成方式（如 Deepfake 换脸）的泛化性未知；模型可能被滥用于监控或窃听，论文虽提及 legal expert 咨询，但未给出具体防护措施。
- **实验覆盖**：未与近期 o1‑like 多模态推理模型（如 Virgo、MAmmoTH‑VL）直接对比；RivaBench 中 Academic 和 StandUp 场景的模型表现仍远低于人类水平，推理能力尚未饱和。

（完）
