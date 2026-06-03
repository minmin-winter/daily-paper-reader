---
title: Diving into Self-Evolving Training for Multimodal Reasoning
title_zh: 深入多模态推理的自进化训练
authors: "Wei Liu, Junlong Li, Xiwen Zhang, Fan Zhou, Yu Cheng, Junxian He"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=X3ikghfWwD"
tags: ["query:mm-reasoning"]
score: 6.0
evidence: 探索自进化训练提升多模态推理
tldr: 自进化训练在多模态推理中面临性能饱和问题。本文从强化学习角度重新审视该训练范式，识别训练方法、奖励模型等关键因素，提出改进策略。实验表明该方法有效提升了多模态推理能力，为复杂推理任务的数据稀缺提供了新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-x3ikghfwwd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1599, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-x3ikghfwwd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 828, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-x3ikghfwwd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 855, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-x3ikghfwwd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 855, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-x3ikghfwwd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 855, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-x3ikghfwwd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 509, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-x3ikghfwwd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1605, \"height\": 704, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-x3ikghfwwd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 856, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-x3ikghfwwd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 860, \"height\": 410, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-x3ikghfwwd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 803, \"height\": 446, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-x3ikghfwwd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 801, \"height\": 370, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-x3ikghfwwd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1244, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-x3ikghfwwd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1481, \"height\": 1166, \"label\": \"Table\"}]"
motivation: 自进化训练在多模态推理中存在性能饱和问题。
method: 从强化学习角度分析自进化训练，优化训练方法和奖励模型。
result: 改进后的训练方法提升了多模态推理性能，缓解了数据稀缺。
conclusion: 基于强化学习视角可有效改进自进化训练在推理中的效果。
---

## Abstract
Self-evolving training—where models iteratively learn from their own outputs—has emerged as a key approach for complex reasoning tasks, addressing the scarcity of high-quality chain-of-thought data. However, its effectiveness in multimodal reasoning, a domain more intricate than text-only reasoning, remains underexplored, and the understanding of critical factors in this training paradigm remains limited. Furthermore, a central challenge for this training method is performance saturation, which impedes further improvements and scalability. Inspired by reinforcement learning (RL), in this paper, we reframe self-evolving training for multimodal reasoning through the lens of RL, identifying three pivotal factors: $\textit{Training Method}$, $\textit{Reward Model}$, and $\textit{Prompt Variation}$. Through systematic analysis, we establish relatively optimal design principles that significantly enhance multimodal reasoning capabilities. Moreover, delving deeper into training dynamics, we uncover the roots of saturation and propose a new automatic balancing mechanism to mitigate this limitation. Building on these insights, we propose M-STaR (**M**ultimodal **S**elf-evolving **T**r**a**ining for **R**easoning), a framework that achieves consistent performance gains across models of varying sizes and diverse benchmarks. All resources will be made publicly available.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **问题**：多模态推理（如视觉数学推理）在真实应用中至关重要，但高质量多模态思维链（CoT）数据极度稀缺，限制了模型学习。
- **背景**：自进化训练（模型利用自身输出迭代学习）在纯文本推理任务中有效，但在更复杂的多模态推理领域，其有效性、关键设计因素和性能饱和问题尚未被充分探究。
- **目标**：从强化学习（RL）视角重新审视自进化训练，识别并优化核心设计组件（训练方法、奖励模型、提示变化），同时揭示性能饱和根源并引入自动平衡机制，最终提出统一框架 **M-STaR（Multimodal Self-evolving Training for Reasoning）**，以持续提升多模态推理能力。

## 2. 方法论：核心思想、关键技术细节与算法流程

- **核心思想**：将自进化训练形式化为强化学习目标，通过迭代“生成-改进”步骤解耦策略更新，并识别三个关键设计空间。
- **关键技术细节**：
    - **训练方法**：提出 **连续自进化（Continuous Self-Evolving）**——在每次迭代中不仅继承模型权重，还继承优化器状态和学习率调度器，使得迭代训练更接近在线RL；并探究合适的迭代间隔（数据遍历比例）。
    - **奖励模型**：首次引入多模态**过程奖励模型（PRM）** ，使用蒙特卡洛展开从部分前缀生成步骤级标签，并用**min**聚合各步分数。训练后，PRM作为**重排序器**，从所有正确的响应中挑选Top-K个高质量响应用于训练（此处K=2最佳）。
    - **提示变化**：探究是否引入无标注数据，但发现当前PRM对无标注数据泛化能力有限，引入反而有害；仅当有完美奖励信号（如oracle答案）时才有帮助，但结合PRM后效果仍不如仅用标注数据。
- **算法流程（文字描述）**：
    1. **预热阶段**：使用标注数据（问题+答案）让模型生成CoT，筛选正确响应进行SFT训练，获得初始CoT能力。
    2. **迭代阶段**：
        - **生成**：当前策略模型对每个问题采样K个响应（温度可控）。
        - **改进**：对于标注数据，先用答案精确匹配过滤出正确响应；再用PRM对正确响应进行打分，选出Top-2响应；将选出的响应作为训练数据，对模型进行SFT更新。
    3. **动态调节**：每两个迭代，基于验证集上的**Reward-Pass@2**指标（PRM对当前模型生成响应的重排序成功率）自动调整下一轮的采样温度（范围0.3~1.6），以维持探索-利用平衡。

## 3. 实验设计：数据集、Benchmark与对比方法

- **模型**：
    - 主模型：MiniCPM-V-2.5（8B）
    - 扩展验证：Phi-3.5-Vision（4B）、InternVL2（2B）
- **训练数据集**：MathV360K（高质量多模态推理数据集），取一半（180K）作为标注训练集，另一半作为无标注集（部分实验中用于分析）。
- **评估Benchmark**：
    - 域内（ID）：MathV360K分割的750样本测试集。
    - 域外（OOD）：MathVista（testmini分割），涵盖多模态推理任务。
    - 额外扩展：M3CoT、MMStar-R（去除感知子任务）、MMBench-R、AI2D。
- **对比方法**：
    - 基线：SFT、Iterative RFT（每轮从当前或初始模型初始化）、ReST EM（每轮从初始模型初始化）。
    - 本文方法：Continuous Self-Evolving（无PRM）、+PRM Re-Rank、最终M-STaR（动态温度 + PRM）。
    - 额外分析：随机选择正确响应、不同K值、不同阈值α、不同温度固定对比。

## 4. 资源与算力

- 文中**未明确说明**使用了多少GPU型号、数量及具体训练时长。仅在训练设置中提到使用常数学习率1e-6，batch size 128，训练10K步等超参数，但未量化硬件资源和能耗。可能需要读者根据实验规模（多模型、多轮迭代）推测。

## 5. 实验数量与充分性

- **实验数量**：非常丰富。包括：
    - 训练方法对比（7种不同间隔+3种初始化策略）。
    - 奖励模型对比（无PRM、随机选择、Top-K、阈值过滤、不同K值）。
    - 提示变化（有无未标注数据、不同引入时机、有无oracle）。
    - 动态温度调节实验（多种温度固定 vs 自动调节）。
    - 三个模型上的完整结果（表4、表6）。
    - 五个额外Benchmark上验证（表5）。
- **充分性 & 公平性**：
    - 所有控制实验均保持其他设置一致，符合消融分析要求。
    - 对比方法均复现或引用原文设置。
    - 但在小模型（InternVL2-2B）上M-STaR在部分基准上略有下降，作者指出可能因泛化能力有限，实验仍客观呈现了局限性。
    - 总体实验设计系统全面，结论有坚实数据支撑。

## 6. 主要结论与发现

- **训练方法**：连续自进化训练（继承优化器等）显著优于离线迭代方法，且适中的迭代间隔（如25%数据）效果最佳。
- **奖励模型**：多模态PRM尽管作为验证器能力弱（BoN/加权投票不如多数投票），但作为**重排序器**能有效识别更简洁、相关性更高的正确响应，从而提升训练效果。Top-2策略效果最好。
- **提示变化**：当前设置下，引入无标注数据反而损害性能，因为PRM对其泛化差；仅当有完美答案（oracle）时才可能受益。
- **训练动态**：性能饱和源于探索能力下降（Pass@K持续衰减），而**Reward-Pass@2**指标能有效监测探索-利用状态。自动调整采样温度可以缓解探索损失，进一步提升模型性能。
- **最终框架M-STaR**：在三个模型（8B/4B/2B）和五个基准上相较于基线和手工策略均有一致且明显的提升（例如MiniCPM-V-2.5在MathVista上提升6.7个点）。

## 7. 优点：方法与实验设计亮点

- **系统性**：首次对多模态自进化训练的关键组件进行结构化分析，从RL视角统一框架。
- **创新点**：
    - 提出“连续自进化”训练变体，桥接迭代训练与在线RL。
    - 训练并应用多模态过程奖励模型（PRM）作为重排序器，而非通常的验证器。
    - 引入Reward-Pass@2指标并基于其自动调节温度，有效应对探索损失。
- **实验严谨**：大量控制变量实验，多模型、多基准验证，消融充分；揭示PRM实际作用为重排序而非验证，具有洞察力。
- **可复现性**：所有资源即将公开。

## 8. 不足与局限

- **PRM局限性**：当前PRM验证能力弱，仅对已正确过滤的响应有效，无法直接用于无标注数据，限制了场景扩展。
- **小模型效果有限**：InternVL2-2B在某些感知密集型基准上甚至退步，表明自进化训练对较小模型的泛化仍有瓶颈。
- **未标注数据利用不足**：未能有效利用大量未标注多模态数据（与纯文本领域相比），这可能是未来提升空间。
- **资源与成本未报告**：未提供具体计算开销，不利于复现时评估可行性。
- **对比范围**：未与更先进的在线RL方法（如GRPO、PPO）进行直接比较（虽然作者在相关工作中提及，但实验未包含）。
- **只考虑正确答案过滤+重排序**：未尝试使用PRM的分步奖励进行更细粒度的策略梯度训练（作者在附录I中提及未来方向）。

（完）
