---
title: "Divide and Conquer: Exploring Language-centric Tree Reasoning for Video Question-Answering"
title_zh: 分治策略：探索面向视频问答的语言中心树推理
authors: "Zhaohe Liao, Jiangtong Li, Siyu Sun, Qingyang Liu, Fengshun Xiao, Tianjiao Li, Qiang Zhang, Guang Chen, Li Niu, Changjun Jiang, Liqing Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=yTpn3QY9Ff"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 基于语言中心树推理的视频问答，结合视觉和文本理解
tldr: 本文针对视频问答中推理过程不可控且不透明的问题，提出语言中心树推理（LTR）框架。该框架递归地将复杂问题分解为逻辑上可管理的子问题，逐步解决，从而增强现有多模态大模型的推理能力和可解释性。在视频问答任务上验证了其有效性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ytpn3qy9ff/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 847, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ytpn3qy9ff/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1767, \"height\": 803, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ytpn3qy9ff/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1776, \"height\": 1393, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1770, \"height\": 707, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1768, \"height\": 547, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 859, \"height\": 474, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 860, \"height\": 584, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 860, \"height\": 392, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1421, \"height\": 809, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1251, \"height\": 599, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ytpn3qy9ff/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 978, \"height\": 521, \"label\": \"Table\"}]"
motivation: 现有MLLM在视频问答中推理过程不透明且不可控，需要增强推理能力。
method: 提出LTR框架，先通过语言生成逻辑树，递归分割复杂问题，再逐步解答。
result: 在视频问答任务上提升了推理能力和可解释性。
conclusion: 语言中心树推理是提升视频问答推理能力的有效方法。
---

## Abstract
Video Question-Answering (VideoQA) remains challenging in achieving advanced cognitive reasoning due to the uncontrollable and opaque reasoning processes in existing Multimodal Large Language Models (MLLMs). To address this issue, we propose a novel Language-centric Tree Reasoning (LTR) framework that targets on enhancing the reasoning ability of models. In detail, it recursively divides the original question into logically manageable parts and conquers them piece by piece, enhancing the reasoning capabilities and interpretability of existing MLLMs. Specifically, in the first stage, the LTR focuses on language to recursively generate a language-centric logical tree, which gradually breaks down the complex cognitive question into simple perceptual ones and plans the reasoning path through a RAG-based few-shot approach. In the second stage, with the aid of video content, the LTR performs bottom-up logical reasoning within the tree to derive the final answer along with the traceable reasoning path. Experiments across 11 VideoQA benchmarks demonstrate that our LTR framework significantly improves both accuracy and interpretability compared to state-of-the-art MLLMs. To our knowledge, this is the first work to implement a language-centric logical tree to guide MLLM reasoning in VideoQA, paving the way for language-centric video understanding from perception to cognition.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有多模态大模型（MLLMs）在视频问答（VideoQA）中的推理过程不可控、不透明，难以实现系统2（System-2）认知推理。例如，复杂问题涉及多个时间视觉线索时，模型可能给出错误答案且不揭示推理路径，导致结果不可信。
- **研究动机**：从“感知”到“认知”是视频理解的关键挑战。低层感知需理解时空特征（物体、动作、场景），高层认知则需理解视频与问题的内在逻辑并执行推理。现有MLLMs虽能提供一定解释，但推理过程缺乏可控性和可追溯性。
- **整体含义**：提出一种**语言中心树推理（LTR）框架**，以语言为驱动力，通过递归分解复杂问题为简单感知问题，再自底向上推理，同时增强推理能力与可解释性，推动视频问答向可验证的认知推理发展。

## 2. 论文提出的方法论

### 核心思想
- 采用**分治策略**：第一阶段（Divide）递归地将原始问题分解为语言中心的逻辑树；第二阶段（Conquer）借助视频内容自底向上推理，得出最终答案及完整的推理路径。
- 以**语言为中心**：逻辑树基于问题本身的逻辑结构生成，而非直接依赖视觉特征；视觉信息在第二阶段辅助推理，但不能主导逻辑结构。

### 关键技术细节
1. **第一阶段：Divide with Top-down Recursive Checking**
   - **问题分解（Question Division）**：利用 MLLM 对给定问题与视频进行递归分解，将复杂认知问题拆分为多个更简单的子问题。借助**检索增强生成（RAG）**：从 AGQA-Decomp 数据集中检索最相似的“问题-子问题”元组作为少样本示例，指导分解过程。
   - **递归感知检查（Recursive Perceptual Checking）**：对每个子问题，结合视频内容判断其是否足够简单（即“可感知”），可直接通过现有 MLLM 的感知能力回答。只有不可感知的问题才继续分解。当所有叶子节点均为感知问题时，递归停止，生成完整的逻辑树。

2. **第二阶段：Conquer with Bottom-up Tree Reasoning**
   - **感知叶子问题回答（Perceptual Question Answering）**：利用 MLLM 回答所有叶子节点问题（简单感知问题）。
   - **视频辅助逻辑推理（Video-aided Logical Reasoning）**：针对每个非叶子节点（父问题），输入子问题的答案、父问题描述以及视频内容，让 MLLM 进行逻辑推理并输出答案。这一步可弥补分解过程中可能的模糊性或子问题答案的错误。
   - **过程中答案验证（In-process Answer Verification）**：对每个中间节点的答案，从两个维度验证：① 逻辑一致性（从子问题到父问题的推理是否合理）；② 视觉一致性（答案是否与视频内容冲突）。如发现冲突，则重新执行视频辅助逻辑推理以修正。

### 算法流程（文字说明）
1. 输入：原始问题 + 视频。
2. 第一阶段：调用 MLLM（结合 RAG 检索）生成并递归扩展逻辑树，直到所有叶子节点判定为可感知。
3. 第二阶段：a) 用 MLLM 获取所有叶子节点的答案；b) 自底向上对每个中间节点进行视频辅助逻辑推理，得到父问题答案；c) 对每个中间节点进行答案验证，必要时修正。
4. 输出：根节点（原始问题）的答案及完整推理路径（树结构）。

## 3. 实验设计

- **数据集（11个VideoQA benchmarks）**：
  - 开放型：MSVD-QA、MSRVTT-QA、TGIF-QA、ActivityNet-QA、AGQA-Decomp（含组合一致性评估）
  - 选择题型：Causal-VidQA、NExT-QA、STAR、Ego-Schema、Video-MME、MVBench
  - 覆盖简单感知任务到复杂认知推理（因果、时序、反事实等），以及长视频理解。

- **基准方法与对比**：
  - 选择4个MLLM作为基线：VideoLLaMA3、VideoChat2、Qwen2-VL、LLaVA-OneVision。
  - 对比方法包括：Video-LLaVA、LLaMA-VID、Chat-UniVi、VideoChat、MiniGPT4-Video、VoT、VLAP等（部分来自原文引用）。
  - 评估指标：准确率（accuracy）、得分（score）、组合一致性指标（cP, cR, cF1）源自VA³。

- **实验设置**：
  - 视频分辨率：336×336，均匀采样16帧。
  - 最大生成长度：2048 tokens。
  - 其他设置遵循各基线模型的零样本推荐配置。

## 4. 资源与算力

- **论文未明确说明使用的GPU型号、数量、训练时长**等具体算力信息。由于LTR框架是**训练无关（training-free）**，仅需推理阶段的MLLM计算，因此未涉及额外训练成本。但基线模型的推理计算资源未被详细披露。

## 5. 实验数量与充分性

- **实验数量**：共进行多组实验，包括：
  - 11个基准数据集上的零样本评估（主实验）。
  - 在AGQA-Decomp上额外报告组合一致性指标。
  - 消融实验（表5）：在Causal-VidQA和NExT-QA上，对第一阶段（有无RAG、有无视频）和第二阶段的三个组件（答案验证、完美感知答案、无视频推理）进行剖析。
  - 多个基线（4种MLLM）的对比，且在多个数据集上重复。
  - 附录中还包含更多数据集（MSVD-QA、MSRVTT-QA、TGIF-QA、ActivityNet-QA、STAR、Ego-Schema、Video-MME）的补充实验。
- **充分性评价**：实验设计较充分，覆盖了多种视频问答子任务（简单感知、因果、反事实、长视频等），并与多个SoTA方法对比。消融实验验证了各组件的贡献。但注意，所有实验均基于同一组超参数（16帧、336分辨率），未探索帧数或分辨率的影响。此外，由于框架是零样本的，尚未与微调后的方法直接比较（但论文目标是零样本增强）。

## 6. 论文的主要结论与发现

1. **LTR框架显著提升了多个MLLM在11个VideoQA基准上的准确率**，尤其在复杂认知推理任务（反事实、因果、时序）上的提升比简单感知任务更明显。
2. **LTR增强了推理的可解释性和可追溯性**：通过显式的逻辑树和中间验证步骤，用户可追踪推理路径，定位错误来源（感知错误还是逻辑错误）。
3. **分治策略的有效性**：递归分解降低问题复杂度，视频辅助推理弥补分解和子问题答案的不准确性，验证机制减少错误传播。
4. **语言中心优于视觉中心**：优先构建语言逻辑结构，视频信息仅起辅助作用，避免了视觉主导带来的逻辑偏差。
5. **AGQA-Decomp上的组合一致性大幅提升**（cF1提升超过10%），说明LTR能更好地保持主问题与子问题间的推理一致性。

## 7. 优点

- **方法设计创新**：首次在VideoQA中提出显式的语言中心逻辑树推理，将问题分解与分治推理结合，符合人类认知模式。
- **训练无关、模型无关**：即插即用，无需重新训练或微调MLLM，适用于多种现有模型，实用性强。
- **可解释性强**：生成清晰的推理路径，便于错误诊断和人类信任。
- **误差容忍度高**：相比传统模块化网络（如NMNs）的硬性程序执行，LTR通过视频辅助推理和验证步骤，能纠正部分分解或感知错误，提升鲁棒性。
- **实验全面**：覆盖11个多样化基准，并与多个基线模型对比，消融实验验证了各组件贡献。

## 8. 不足与局限（包括实验覆盖、偏差风险、应用限制）

- **长视频理解局限**：由于框架固定采样16帧，在处理长视频（如Ego-Schema、Video-MME长视频子集）时性能增益较小，因为叶子节点问题可能因信息稀疏而回答不准。
- **对基座MLLM感知能力的依赖**：若基座模型在简单感知问题上表现差，LTR的推理性能会受到显著影响（消融实验显示无正确感知答案时大幅下降）。
- **计算开销**：递归分解和多次MLLM调用（每个节点至少一次推理）增加了延迟，不太适合实时或低延迟应用。
- **零样本上限**：零样本方式未充分利用任务特定数据，可能不如微调方法在特定基准上效果好（但论文目标是通用增强）。
- **未对比最先进的微调模型**：实验中对比的基线和VoT等方法多为零样本或简单微调，未与例如借助AGQA-Decomp训练的高精度模型（如VA³等）在AGQA上直接比较，但VA³已被引用。
- **缺乏对超参数（如帧数、树深度）的敏感性分析**：实验未改变这些参数，可能影响泛化结论。
- **公平性风险**：逻辑树的生成依赖RAG检索自AGQA-Decomp，若目标域数据分布差异大，检索质量可能下降，导致分解不准确。

（完）
