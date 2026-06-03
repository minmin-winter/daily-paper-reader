---
title: "Aguvis: Unified Pure Vision Agents for Autonomous GUI Interaction"
title_zh: Aguvis：用于自主GUI交互的统一纯视觉代理
authors: "Yiheng Xu, Zekun Wang, Junli Wang, Dunjie Lu, Tianbao Xie, Amrita Saha, Doyen Sahoo, Tao Yu, Caiming Xiong"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=PlihOwfx4r"
tags: ["query:mm-reasoning"]
score: 6.0
evidence: 纯视觉GUI代理，具备多模态基础推理能力
tldr: 该论文提出Aguvis，一个统一的纯视觉框架用于自主GUI代理。它直接操作屏幕图像，通过内部独白实现结构化推理，并构建大规模多模态基础推理数据集。两阶段训练流程将GUI基础与规划推理分离。实验表明Aguvis在离线和在线基准测试中均达到最先进性能，是首个完全自主的视觉GUI代理。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1679, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 848, \"height\": 755, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 584, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 569, \"height\": 497, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 820, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 520, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1031, \"height\": 550, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 522, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 513, \"height\": 360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 519, \"height\": 801, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 528, \"height\": 596, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 516, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 517, \"height\": 810, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 340, \"height\": 198, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 340, \"height\": 243, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 332, \"height\": 206, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 336, \"height\": 205, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1244, \"height\": 2106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1102, \"height\": 2062, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1118, \"height\": 2131, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1649, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-plihowfx4r/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1641, \"height\": 449, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1468, \"height\": 709, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1781, \"height\": 566, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 820, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 841, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 892, \"height\": 445, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1769, \"height\": 387, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 829, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 557, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 963, \"height\": 773, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1230, \"height\": 476, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1365, \"height\": 441, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1653, \"height\": 531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1622, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1613, \"height\": 1019, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1771, \"height\": 407, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1769, \"height\": 359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1773, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-plihowfx4r/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1769, \"height\": 270, \"label\": \"Table\"}]"
motivation: 现有GUI自动化依赖于文本表示和平台特定动作空间，推理能力有限。
method: 构建纯视觉框架，通过内部独白实现结构化推理，并采用两阶段训练分离基础与推理。
result: 在离线和在线基准中达到最先进性能，成为首个完全自主的视觉GUI代理。
conclusion: 纯视觉方法结合结构化推理能有效实现跨平台GUI自动化。
---

## Abstract
Automating GUI tasks remains challenging due to reliance on textual representations, platform-specific action spaces, and limited reasoning capabilities. We introduce Aguvis, a unified vision-based framework for autonomous GUI agents that directly operates on screen images, standardizes cross-platform interactions and incorporates structured reasoning via inner monologue. To enable this, we construct Aguvis data collection, a large-scale dataset with multimodal grounding and reasoning annotations, and develop a two-stage training pipeline that separates GUI grounding from planning and reasoning. Experiments show that Aguvis achieves state-of-the-art performance across offline and real-world online benchmarks, marking the first fully autonomous vision-based GUI agent that operates without closed-source models. We open-source all datasets, models, and training recipes at https://aguvis-project.github.io to advance future research.

---

## 论文详细总结（自动生成）

好的，作为资深学术论文分析助手，我将基于提供的论文内容，为您生成一份结构化的中文总结。

# 论文《Aguvis: 用于自主 GUI 交互的统一纯视觉代理》总结

## 1. 核心问题与整体含义（研究动机与背景）
- **核心问题**：当前图形用户界面（GUI）的自动化代理面临三大挑战：
    1.  **过度依赖文本表征**：诸如 HTML 或无障碍功能树等文本输入，不仅冗长（通常超过 4K tokens），而且随着界面复杂度增加而增长，限制了泛化能力并增加了计算开销。
    2.  **平台特定的动作空间**：不同平台（Web、移动端、桌面）的动作空间异构，阻碍了跨环境的学习和训练数据的规模化。
    3.  **推理能力有限**：现有方法要么缺乏可靠的视觉定位能力，要么严重依赖闭源大语言模型（LLMs）进行推理，且通常直接生成“反应式”的低级动作，缺乏复杂的规划和推理能力。
- **整体含义**：本文旨在解决上述瓶颈，提出一个**统一的、纯视觉的、完全自主的 GUI 代理框架**，该框架无需依赖平台特定的文本表征或闭源模型，通过模仿人类的视觉感知和结构化推理来操作各类 GUI 环境。

## 2. 方法论：核心思想、关键技术细节与流程
### 核心思想
- **纯视觉观察**：直接操作屏幕截图作为输入，摒弃了 HTML 或无障碍树等文本表征。
- **统一动作空间**：采用 `pyautogui` 库作为基础，并辅以可插拔的插件系统，标准化了跨平台的交互模式。
- **结构化推理（内部独白）**：在训练数据中引入显式的“内部独白”（Thought）和低级指令（Low-level Instruction），让模型在生成动作前先进行规划和推理，模仿人类解决问题的过程。

### 关键技术细节
1.  **统一交互框架**：
    - **观察**：处理 720p 的屏幕图像，保持恒定的 token 成本（约 1196 tokens），远低于文本方法。
    - **动作**：使用 `pyautogui` 命令（如 `click`, `write`）作为通用接口，并通过插件扩展支持移动端手势（如 `mobile.swipe`, `mobile.back`）等平台特定动作。
    - **推理**：在每个步骤中，代理生成一个包含“Thought”（关于当前状态和目标的推理）和“Low-level Instruction”（具体动作描述）的内部独白，再转化为实际的 `pyautogui` 动作。
2.  **数据集构建**：构建了名为 **Aguvis Data Collection** 的大规模多平台数据集，包含两个部分：
    - **基础数据（Grounding Split）**：约 103.6 万个单步轨迹，用于训练 GUI 定位能力。通过整合现有数据集和模板增强生成，涵盖 Web、移动端和桌面。
    - **规划与推理数据（Planning & Reasoning Split）**：约 3.5 万条多步轨迹，用于训练规划和推理能力。通过使用 GPT-4o 对现有轨迹进行增强，生成包含内部独白的结构化推理路径。
3.  **两阶段训练流程**：
    - **阶段 1：基础训练（Grounding Training）**：训练 Aguvis-G 模型，专注于从单张截图进行精准的元素定位和基础交互。采用“基础打包”（grounding packing）策略，将同一张截图上的多个指令-动作对捆绑处理，提高训练效率。
    - **阶段 2：规划与推理训练（Planning & Reasoning Training）**：在 Aguvis-G 基础上训练 Aguvis 模型，利用包含内部独白的轨迹数据，使模型掌握高级决策和推理能力。采用“推理混合”（reasoning mixture）策略，暴露给模型不同复杂度的推理过程。
4.  **模型架构**：基于 **Qwen2-VL** 作为核心视觉语言模型（VLM），利用其 NaViT 风格的动态分辨率处理和 2D-RoPE 位置编码，以高效处理高分辨率、不同尺寸的屏幕截图。同时验证了框架在 **LLaVA-OneVision** 上的可迁移性。

## 3. 实验设计：数据集、基准与对比方法
### 基准与数据集
- **GUI 定位评估**：**ScreenSpot**（1.2K 单步指令，覆盖移动、桌面和 Web 平台，包含文本和图标/控件类型）。
- **离线 GUI 代理评估**：
    - **Multimodal-Mind2Web**：用于评估 Web 导航与交互能力（含跨任务、跨网站、跨领域三个子集）。
    - **AndroidControl**：用于评估移动设备操作能力（区分高级规划任务和低级指令执行任务）。
- **在线 GUI 代理评估**：
    - **Mind2Web-Live**：动态 Web 环境，评估任务逐步完成率。
    - **AndroidWorld**：虚拟 Android 环境（Pixel 6 模拟器）。
    - **MobileMiniWob**：AndroidWorld 中的 MiniWob++ 任务。
    - **OSWorld**：统一桌面操作系统环境，测试跨平台泛化能力。

### 对比方法
- **定位任务**：GPT-4, GPT-4o, CogAgent, SeeClick, Qwen2-VL, UGround, OmniParser。
- **规划任务**：GPT-3.5/4, GPT-4o, PaLM 2S*, 各种方法组合（如 GPT-4o + SeeClick, GPT-4o + UGround, GPT-4o + Aguvis-7B）以及端到端模型（如 SeeClick, UGround）。
- **自演进比较**：Aguvis 与自身变体（移除阶段1/阶段2、移除内部独白等）进行比较。

## 4. 资源与算力
论文在附录 C.2 中明确指出：
- **GPU 型号**：H100-80G
- **Aguvis-7B**：使用 **8 个节点**（具体 GPU 数量未明确，但推测每节点 8 卡即 64 卡），完成基础训练约 5 小时，规划推理训练约 1 小时。
- **Aguvis-72B**：使用 **16 个节点**（推测 128 卡），完成基础训练约 30 小时，规划推理训练约 6 小时。
- 整个训练采用 DeepSpeed、BF16 和梯度检查点技术以节省显存。

## 5. 实验数量与充分性
本实验非常充分且客观：
- **多维度评估**：涵盖了定位、离线规划和在线交互三大类，覆盖了 Web、移动和桌面平台。
- **全面消融研究**：
    - 分析了训练阶段（Stage 1 vs Stage 2 vs 两者组合）的影响。
    - 分析了内部独白（Inner Monologue）的必要性。
    - 分析了跨平台数据训练（Web + Mobile vs Web Only vs Mind2Web Only）带来的泛化收益。
    - 验证了框架在不同模型主干（Qwen2-VL, LLaVA-OneVision）上的有效性。
    - 通过错误分析（50 个样本）深入诊断了失败模式。
- **公平性**：对比了多种最先进的（SOTA）方法，包括闭源模型（如 GPT-4o）、开源模型和混合框架。对于需要公平对比的设置（如 Self-plan 和原始指令），均按照协议进行。

## 6. 主要结论与发现
1.  **性能 SOTA**：Aguvis 在所有评估基准上均达到或超越了当前最先进的性能水平，尤其是在 Multimodal-Mind2Web 上，步骤成功率平均提升 51.9%。
2.  **纯视觉的高效性**：纯视觉方法显著降低了计算和令牌成本（token 成本降低 70%，推理美元成本降低 93%），且性能随界面复杂度提升的扩展性优于文本方法。
3.  **内部独白的关键作用**：引入内部独白不仅显著提升了高级规划任务（如 AndroidControl 高级任务），也意外地改善了低级定位和执行任务（如 ScreenSpot），证明了结构化推理的泛化效益。
4.  **跨平台训练的增益**：在统一的动作空间下融合 Web 和移动端数据进行训练，有效增强了模型在单一平台（如 Web）上的表现，证明了跨环境知识迁移的成功。
5.  **强泛化能力**：仅使用 Web 和移动端数据训练的模型，能够有效泛化到桌面操作系统（OSWorld）任务，表明其学习到了通用的 GUI 交互原则。

## 7. 优点
1.  **开创性**：Aguvis 是首个**完全自主的、基于纯视觉的、且不依赖闭源模型**的 GUI 代理，为未来研究树立了新的标杆。
2.  **高度统一**：在观察和动作层面实现了跨平台统一，极大地简化了训练和部署流程。
3.  **数据驱动与开源**：构建了大规模、带结构化推理标注的数据集，并开源了所有数据集、模型和训练方案，可复现性极强，极大地推动了社区研究。
4.  **技术整合巧妙**：将“内部独白”这一概念成功地融入视觉语言模型（VLM）训练中，实现了模仿人类认知的渐进式推理。
5.  **实验严谨且深入**：不仅展示了 SOTA 性能，还通过大量消融实验和错误分析，深入揭示了模型行为模式和未来改进方向。

## 8. 不足与局限
1.  **错误分析**：论文通过 50 个样本的错误分析发现，**40% 的错误源于指令模糊**（可指向多个定位目标），而 **60% 是定位错误**。模型目前**缺乏拒绝模糊指令或表达不确定性的能力**，这在真实部署中是一个安全风险。
2.  **推理的自动化程度**：尽管模型可以使用内部独白，但在面对“看似简单但需要深层语义理解”的任务时，模型会**默认直接定位而非进行显式规划**。论文提出需要通过外力（Enforced Plan）才能解决 20% 的定位错误。
3.  **在线环境限制**：在 Mind2Web-Live 实验中，某些真实网站（如 kohls, target, united）会主动检测并阻止 Playwright 自动化脚本，导致不可避免的 24 个任务失败。这反映了在线评估环境的固有挑战。
4.  **数据标注依赖**：规划与推理数据的构建依赖于 **GPT-4o 进行生成**（尽管开放，但非完全自主），且人工评估显示 86.7% 数据合格，仍有改进空间。高质量训练数据是其性能的关键，可能存在数据偏差。
5.  **平台覆盖**：虽然框架是跨平台的，但实验主要聚焦于 Web 和移动端，对桌面 OS（仅 OSWorld）和更多元化应用的评估相对有限。

（完）
