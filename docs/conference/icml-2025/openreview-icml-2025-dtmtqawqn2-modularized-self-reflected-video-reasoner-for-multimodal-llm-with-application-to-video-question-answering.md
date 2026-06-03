---
title: Modularized Self-Reflected Video Reasoner for Multimodal LLM with Application to Video Question Answering
title_zh: 面向多模态大模型的模块化自反思视频推理器及其在视频问答中的应用
authors: "Zihan Song, Xin Wang, Zi Qian, Hong Chen, Longtao Huang, Hui Xue, Wenwu Zhu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=dtmTQawQN2"
tags: ["query:mm-reasoning"]
score: 9.0
evidence: 为视频问答提供显式推理路径，直接处理视频内容理解与推理
tldr: 现有多模态大模型在视频问答中缺乏可解释性，无法提供推理路径。本文提出MSR-ViR，首次将模块化网络集成到多模态大模型中，通过模组化时空定位和自反思机制生成显式推理路径。实验表明该方法在提升可解释性的同时保持了优异的问答性能。该工作推动了视频理解中可解释推理的发展。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1596, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1546, \"height\": 942, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 777, \"height\": 685, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1595, \"height\": 1047, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1482, \"height\": 2135, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1498, \"height\": 2045, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1592, \"height\": 840, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1590, \"height\": 894, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1599, \"height\": 648, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-dtmtqawqn2/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1645, \"height\": 653, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 690, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 714, \"height\": 383, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 844, \"height\": 459, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 792, \"height\": 618, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 752, \"height\": 638, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1354, \"height\": 480, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1510, \"height\": 676, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1265, \"height\": 538, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-dtmtqawqn2/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1326, \"height\": 236, \"label\": \"Table\"}]"
motivation: 多模态大模型在视频问答中缺乏可解释性，无法展示推理过程。
method: 将模块化网络集成到多模态大模型中，提出模组化时空定位和自反思机制生成显式推理路径。
result: 在VideoQA基准上取得竞争性能，同时提供可解释推理路径。
conclusion: MSR-ViR为视频问答提供了可解释的推理框架，平衡了性能与可解释性。
---

## Abstract
Multimodal Large Language Models (Multimodal LLMs) have shown their strength in Video Question Answering (VideoQA). However, due to the black-box nature of end-to-end training strategies, existing approaches based on Multimodal LLMs suffer from the lack of interpretability for VideoQA: they can neither present reasoning paths nor indicate where the answers are derived from the video. To address this issue, we propose **MSR-ViR** (**M**odularized **S**elf-**R**eflected **Vi**deo **R**easoner), which for the first time integrates modular networks to Multimodal LLMs, capable of providing VideoQA with explicit reasoning paths for more interpretability. Specifically, a **MoST-Grounding** (Modularized Spatial-Temporal Grounding) network is proposed to decompose complex questions via tree-structured policies, localizing relevant temporal and spatial segments within videos through step-by-step reasoning. The proposed MoST-Grounding network provides explicit visually grounded information for Multimodal LLMs with clear reasoning paths, thus enhancing interpretability for the predicted answers. To further improve the reasoning quality, we design an **Alternate Self-reflection Training Strategy** to jointly optimize policy generation and Multimodal LLMs. Experiments on real-world datasets demonstrate the superiority of our proposed MSR-ViR framework in video understanding, reasoning transparency, and providing explicit localization evidence for answers.

---

## 论文详细总结（自动生成）

## 中文总结：MSR-ViR — 面向多模态大模型的模块化自反思视频推理器

### 1. 核心问题与研究动机

- **背景**：多模态大模型（Multimodal LLMs）在视频问答（VideoQA）中表现出色，但现有端到端训练方法本质上是“黑箱”，缺乏可解释性——既无法展示推理路径，也不能指出答案来源于视频的哪些具体时空片段。
- **核心问题**：如何在保持高性能的同时，为 VideoQA 提供**显式的、可解释的推理路径**以及**可视化的定位证据**？
- **整体含义**：本文首次将模块化网络与多模态大模型相结合，提出 MSR-ViR 框架，在实现可解释推理的同时，不牺牲甚至提升了问答准确率，推动了视频理解领域向透明化、可审计方向发展。

### 2. 方法论

- **核心思想**：通过一个**问题解析器（Question Parser）** 将复杂问题分解为树状结构的执行策略，然后由**模块化时空定位网络（MoST-Grounding）** 逐步在视频中定位相关的时间段和空间区域，最后将这些显式的定位信息与全局视频表示一起送入多模态大模型进行答案生成。
- **关键组件**：
  - **Question Parser**：基于大语言模型（Qwen2-7B），利用上下文学习，将原始问题转换为 JSON 格式的模块化执行策略。
  - **MoST-Grounding 模块**：包含时间定位器（Temporal Localizer，如 UniVTG）和空间定位器（Spatial Localizer，如 YOLO-World），共 **7 个小模块**（如 DetectAct、LocateObj、TemporalBetween 等），根据策略动态组装，递归执行时空定位。
  - **多模态大模型回答器**：接收三种视觉输入——全局视频表示（均匀采样帧的池化）、时间定位帧、空间定位帧，以及带指示的提示模板，通过监督微调（SFT）训练。
- **自反思训练策略（Alternate Self-reflection Training）**：
  - **交替优化**：先对多模态大模型进行 SFT（公式 5：交叉熵损失）；然后冻结大模型，对 Question Parser 进行**直接偏好优化（DPO，公式 6）**，以多模态大模型的损失为反馈，区分正负策略（损失较小的策略为正）。
  - **周期交替**：每 200 步切换一次训练对象，梯度累积步数为 16。
- **计算复杂度**：理论证明了 MSR-ViR 的复杂度上界为 \(O(c_1 T H^2W^2 + c_2 T^2 + C_1 H^2W^2 + C_2 L^2 + C_3 l_p^2)\)，额外开销主要来自 Question Parser，且与视频长度无关，可被严格约束。

### 3. 实验设计

- **数据集**：
  - **VideoQA**：NExT-QA（含 Temporal、Causal、Descriptive 子集）、STAR（取 Interaction、Sequence 子集，记为 STAR-sub）。
  - **长视频 QA**：EgoSchema（子集与全集）、VideoMME（按视频长度分 Short、Medium、Long 子集）。
  - **带定位的 VideoQA**：NExT-GQA（含 ground-truth 时间片段，评估 mIoU、IoU@0.3/0.5、Acc@GQA）。
- **基准方法**：
  - 小模型：ATP、MIST、CoVGT、HiTeA、InternVideo 等。
  - 多模态大模型：BLIP-2、InstructBLIP、Qwen-VL、LLaVA-NeXT、Qwen2-VL、LLaVA-Video。
  - 基于定位的方法：TGB、SeViLa、GCG。
  - 模块化方法：LLoVi、MoReVQA、LangRepo。
- **对比场景**：
  - **监督微调**：在 NExT-QA 和 STAR 上训练并测试。
  - **零样本**：在 EgoSchema、VideoMME、NExT-GQA 上测试（其中 NExT-GQA 为微调后测试）。
- **消融实验**：
  - 移除自反思训练（w/o SR）。
  - 移除空间定位模块（w/o ms）。
  - 移除提示模板（w/o prompts）。
  - 移除全局表示（w/o gv）。
  - 仅用全局表示（only w/ gv）。
  - 移除推理路径（w/o RP，直接用原始问题做定位）。
  - 更换时间定位模型（UniVTG vs R2-Tuning vs Moment-DETR）。
  - 帧采样策略对比。

### 4. 资源与算力

- 论文**未明确说明**使用的 GPU 型号、数量及总训练时长。
- 但文中提及：推理速度测试在一张 NVIDIA A100 GPU 上进行。
- 模型大小：Question Parser 为 Qwen2-7B（约 7B 参数），多模态大模型基于 Qwen-VL（9.6B）或 LLaVA-NeXT（7.1B），MSR-ViR 总参数量约 16.7B（Q 版）或 14.2B（L 版）。
- **不足**：未提供训练所需的具体算力成本，读者难以复现或评估部署开销。

### 5. 实验数量与充分性

- **实验数量**：覆盖 5 个数据集（NExT-QA、STAR-sub、EgoSchema、VideoMME、NExT-GQA），涉及监督微调和零样本两种设置，共呈现 **10+ 张表格**和 **多组消融实验**。
- **充分性**：
  - 与多种类型基线（小模型、多模态大模型、定位法、模块法）进行了对比，且对每种子类型（如 Temporal、Descriptive、Interaction）分别报告结果。
  - 消融实验覆盖了主要设计（自反思、空间模块、提示、全局表示、推理路径、定位模型、帧采样）。
  - 在 Grounded VideoQA 上还评估了定位精度（mIoU、IoU@0.5、Acc@GQA）。
- **公平性**：
  - 与直接基线（Qwen-VL、LLaVA-NeXT 等）均使用相同的骨干网络和参数设置。
  - 对于 LLoVi 和 MoReVQA 等使用更大 LLM（GPT-4、PaLm-2）的方法，在对比中做了淡化处理（灰色行），保证了同规模比较的公平性。
- **结论**：实验设计较为充分，对比客观，但缺少训练成本的详细报告，以及跨不同随机种子的稳定性分析。

### 6. 主要结论与发现

- **性能提升**：MSR-ViR 在所有数据集上均显著优于其直接基线（如 Qwen-VL、LLaVA-NeXT），并在多个子集上达到 state-of-the-art（如 NExT-QA Temporal 子集、NExT-GQA 定位指标）。
- **可解释性**：通过树状策略和时空定位结果，模型能够显式展示“如何从问题推导出答案”，并输出对应的视频片段和边框作为证据。
- **自反思训练的有效性**：移除自反思训练后，NExT-QA 平均准确率下降 1.5%，NExT-GQA 定位指标也下降；且自反思能改善策略质量（对比图 4 示例）。
- **空间定位的重要性**：移除空间定位模块后，准确率下降 1.4%，说明不仅需要时间定位，空间定位同样关键。
- **长视频优势明显**：在 VideoMME 的 Long 子集上，MSR-ViR 相比基线提升最为显著（如 MSR-ViR LV 比 LLaVA-Video 提升 3.3%），说明模块化推理在长视频复杂场景下更有优势。

### 7. 优点

- **首次融合模块化网络与多模态大模型**：在 VideoQA 领域开创性地实现显式推理路径与视觉定位证据。
- **自反思交替训练**：通过 DPO 利用大模型自身的损失反馈优化问题解析器，无需额外奖励模型，训练稳定。
- **计算复杂度可控**：理论证明了额外开销严格有界，且主要来自固定的提示长度，与视频长短无关。
- **全面的评估体系**：同时衡量问答准确率、定位精度（IoU/IoP）和定位-答案联合指标（Acc@GQA），充分验证了可解释性和性能的平衡。
- **跨数据集泛化能力**：在多个不同风格（短时/长时、第三人称/第一人称）的数据集上均取得一致提升。

### 8. 不足与局限

- **计算开销**：尽管复杂度上界可控，但相较于纯端到端模型，MSR-ViR 的推理时间约为基线的 2~3 倍（如 MSR-ViR L 为 4.96 s/sample vs LLaVA-NeXT 的 2.19 s/sample），在实际部署中可能成为瓶颈。
- **依赖外部模块**：MoST-Grounding 依赖 UniVTG 和 YOLO-World 等预训练小模型，这些模型的性能上限直接影响框架的整体表现；且更换新域可能需要重新训练或适配这些模块。
- **问题解析器依赖上下文学习**：虽然通过自反思训练可以提升策略质量，但初始策略生成仍依赖于精心设计的提示模板，对模板变化的鲁棒性未作探讨。
- **实验覆盖不完整**：
  - 未报告训练阶段的 GPU 小时数或能耗。
  - 未提供不同随机种子下的方差。
  - 仅在英文数据集上验证，未考虑多语言场景。
- **应用限制**：框架适用于“需要时空推理”的 VideoQA 任务，对于预测性或可行性类问题（如 STAR 中被排除的 Prediction 和 Feasibility）不适用。

---
（完）
