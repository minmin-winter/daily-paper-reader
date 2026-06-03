---
title: "Can MLLMs Reason in Multimodality? EMMA: An Enhanced MultiModal ReAsoning Benchmark"
title_zh: 多模态大语言模型能进行多模态推理吗？EMMA：增强多模态推理基准
authors: "Yunzhuo Hao, Jiawei Gu, Huichen Will Wang, Linjie Li, Zhengyuan Yang, Lijuan Wang, Yu Cheng"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=v26vwjxOEz"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: EMMA基准测试涵盖多模态推理，涉及数学、物理、化学和编程
tldr: EMMA（增强多模态推理基准）专门评估多模态大语言模型在数学、物理、化学和编程领域的有机多模态推理能力。其任务强调跨模态整合，无法通过单模态推理解决。对现有MLLM的评估揭示了它们在真正多模态推理上的不足。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 842, \"height\": 794, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1733, \"height\": 1729, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 761, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 769, \"height\": 822, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 770, \"height\": 432, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 841, \"height\": 1076, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 843, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 858, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 735, \"height\": 176, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 850, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 853, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 849, \"height\": 641, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 847, \"height\": 322, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1755, \"height\": 850, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 849, \"height\": 354, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 704, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 955, \"height\": 628, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1553, \"height\": 238, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 329, \"height\": 162, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 890, \"height\": 81, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 468, \"height\": 269, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 854, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 797, \"height\": 457, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 299, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 278, \"height\": 400, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 272, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 564, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 409, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 133, \"height\": 119, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 127, \"height\": 114, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 755, \"height\": 102, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 108, \"height\": 97, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1276, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 684, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-035.webp\", \"caption\": \"\", \"page\": 0, \"index\": 35, \"width\": 851, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-036.webp\", \"caption\": \"\", \"page\": 0, \"index\": 36, \"width\": 413, \"height\": 177, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-037.webp\", \"caption\": \"\", \"page\": 0, \"index\": 37, \"width\": 413, \"height\": 176, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-038.webp\", \"caption\": \"\", \"page\": 0, \"index\": 38, \"width\": 359, \"height\": 283, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-039.webp\", \"caption\": \"\", \"page\": 0, \"index\": 39, \"width\": 110, \"height\": 100, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-040.webp\", \"caption\": \"\", \"page\": 0, \"index\": 40, \"width\": 1175, \"height\": 394, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-041.webp\", \"caption\": \"\", \"page\": 0, \"index\": 41, \"width\": 660, \"height\": 332, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-042.webp\", \"caption\": \"\", \"page\": 0, \"index\": 42, \"width\": 1600, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-043.webp\", \"caption\": \"\", \"page\": 0, \"index\": 43, \"width\": 440, \"height\": 215, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-044.webp\", \"caption\": \"\", \"page\": 0, \"index\": 44, \"width\": 1607, \"height\": 321, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-045.webp\", \"caption\": \"\", \"page\": 0, \"index\": 45, \"width\": 1777, \"height\": 1524, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-046.webp\", \"caption\": \"\", \"page\": 0, \"index\": 46, \"width\": 1643, \"height\": 710, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-047.webp\", \"caption\": \"\", \"page\": 0, \"index\": 47, \"width\": 818, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-048.webp\", \"caption\": \"\", \"page\": 0, \"index\": 48, \"width\": 332, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-049.webp\", \"caption\": \"\", \"page\": 0, \"index\": 49, \"width\": 128, \"height\": 113, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-050.webp\", \"caption\": \"\", \"page\": 0, \"index\": 50, \"width\": 815, \"height\": 571, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-051.webp\", \"caption\": \"\", \"page\": 0, \"index\": 51, \"width\": 1189, \"height\": 1306, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-052.webp\", \"caption\": \"\", \"page\": 0, \"index\": 52, \"width\": 1110, \"height\": 744, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-053.webp\", \"caption\": \"\", \"page\": 0, \"index\": 53, \"width\": 1150, \"height\": 728, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-054.webp\", \"caption\": \"\", \"page\": 0, \"index\": 54, \"width\": 1087, \"height\": 446, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-055.webp\", \"caption\": \"\", \"page\": 0, \"index\": 55, \"width\": 537, \"height\": 502, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-056.webp\", \"caption\": \"\", \"page\": 0, \"index\": 56, \"width\": 1004, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-057.webp\", \"caption\": \"\", \"page\": 0, \"index\": 57, \"width\": 1279, \"height\": 1106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-v26vwjxoez/fig-058.webp\", \"caption\": \"\", \"page\": 0, \"index\": 58, \"width\": 1381, \"height\": 1099, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 813, \"height\": 395, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1752, \"height\": 790, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1747, \"height\": 548, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1759, \"height\": 778, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1761, \"height\": 689, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1767, \"height\": 1278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1601, \"height\": 442, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1474, \"height\": 909, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1474, \"height\": 911, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1498, \"height\": 909, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-v26vwjxoez/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1365, \"height\": 911, \"label\": \"Table\"}]"
motivation: 现有基准偏重文本主导推理或浅层视觉线索，未能充分评估真正的跨模态推理。
method: 构建包含数学、物理、化学、编程任务的基准，要求跨模态整合才能解答。
result: 现有MLLM在EMMA上表现不佳，揭示了有机多模态推理能力的不足。
conclusion: 需要更强的多模态推理能力，EMMA可作为有效评估工具。
---

## Abstract
The ability to organically reason over and with both text and images is a pillar of human intelligence, yet the ability of Multimodal Large Language Models (MLLMs) to perform such multimodal reasoning remains under-explored. Existing benchmarks often emphasize text-dominant reasoning or rely on shallow visual cues, failing to adequately assess integrated visual and textual reasoning. We introduce EMMA (Enhanced MultiModal reAsoning), a benchmark targeting organic multimodal reasoning across mathematics, physics, chemistry, and coding. EMMA tasks demand advanced cross-modal reasoning that cannot be addressed by reasoning independently in each modality, offering an enhanced test suite for MLLMs' reasoning capabilities. Our evaluation of state-of-the-art MLLMs on EMMA reveals significant limitations in handling complex multimodal and multi-step reasoning tasks, even with advanced techniques like Chain-of-Thought prompting and test-time compute scaling underperforming. These findings underscore the need for improved multimodal architectures and training paradigms to close the gap between human and model reasoning in multimodality.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：当前多模态大语言模型（MLLMs）是否具备真正的有机多模态推理能力？即能否在同时涉及文本和图像的任务中进行深度、多步、跨模态的推理，而不是仅依赖文本推理或单次视觉感知。
- **研究动机**：现有MLLM推理基准（如MathVista、MMMU等）多侧重于文本主导推理或浅层视觉线索，许多任务可以通过纯文本或简单的图像字幕解决，无法有效评估真正的多模态整合推理。因此需要构建一个专门聚焦于“有机多模态推理”的评测基准。
- **整体含义**：EMMA旨在推动MLLM在视觉与语言深度融合的方向发展，揭示当前模型在空间模拟、多跳视觉推理、跨模态动态推理等方面的显著不足。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：构建一个要求模型必须进行多轮视觉-语言交互推理的评测集，任务设计确保无法通过单模态（仅文本或仅图像）解决。例如，物理中的矢量合成需要视觉分解与模拟，化学中的反应推演需要理解分子结构并模拟电子转移。
- **数据构建流程**：
  1. **源数据筛选**：从现有多模态推理基准（Math-Vision、MathVista、OlympiadBench、EXAMS-V、MMMU等）收集候选问题。
  2. **严格过滤**：利用GPT-4o生成图像字幕，将字幕+文本输入给多个LLM（GPT-4o、Llama-3-70B、Qwen2-72B）进行10次回答；若任一模型在5次及以上答对，则丢弃该问题。这一过滤确保了剩余问题必须依赖深度视觉推理。
  3. **人工扩充**：对于物理、化学等剩余问题极少的学科，手动收集新问题（如从Learn AP Physics、Khan Academy；化学方面利用RDKit分析SMiCRM数据库生成结构计数与识别题；编程题全部从零构建）。
  4. **细粒度分类**：由领域专家或GPT-4o协助标注每个问题的技能类别（如数学的2D变换、3D空间模拟、路径追踪；物理的视觉分解模拟、3D场模拟；化学的结构识别、反应模拟；编程的3D、颜色纹理、对齐等）。

- **关键技术细节**：
  - 评测格式：多选题（72%）和开放短答案（28%），答案可自动检查。
  - 包含4个学科：数学（892题）、物理（156题）、化学（1176题）、编程（564题），总计2788题，其中1796题为全新构建。
  - 设计了EMMA-mini平衡子集（每学科100题，共400题）用于更公平的模型对比和人类评估。

## 3. 实验设计

- **数据集/基准**：EMMA（含EMMA-mini）、对比模型在完整EMMA和EMMA-mini上的表现。
- **对比方法**：
  - 10个SOTA MLLMs：5个闭源（GPT-4o、Claude 3.5 Sonnet、Gemini 2.0 Flash、Gemini 2.0 Flash Thinking、o1）和5个开源（Qwen2-VL-72B、QVQ-72B-Preview、LLaVA-Onevision-72B、InternVL2-76B、InternVL2.5-78B）。
  - 提示策略：直接答案输出 vs. 链式思维（CoT）提示。
  - 测试时计算缩放方法：多数投票（Majority Voting）、最佳N选（Best-of-N）、锦标赛（Tournament），N=1,2,4,8,16。
- **人类基线**：每个学科聘请两位专家，取平均得分作为人类表现。
- **评估指标**：准确率（Accuracy）。

## 4. 资源与算力

论文未明确说明使用的GPU型号、数量或训练时长。所有评价均为零样本推理，使用API（如GPT-4o、Gemini）或在本地加载模型（如Qwen2-VL-72B）进行推理。部分开源模型使用vLLM和Transformers库推理。未提及大规模训练或微调算力开销。

## 5. 实验数量与充分性

- **整体实验量**：在完整EMMA（2788题）上评估了8个模型（不含o1和QVQ因速率限制），在EMMA-mini（400题）上评估了10个模型，并进行了多种测试时缩放方法对比（约3个基础模型 × 3种方法 × 5个N值 ≈ 45组实验）。此外还进行了错误类型分析（分类4类误差，比例统计）和CoT影响分析（按技能类别对比）。
- **消融/分析实验**：对比了CoT vs. 直接提示对封闭/开源模型的不同影响；分析测试时缩放策略在不同奖励模型（自奖励 vs. 更强模型奖励）下的效果；按细粒度技能类别（如2D变换、多跳计数、3D场模拟等）展示各模型准确率。
- **公平性**：使用了统一的提示模板，但模型中o1、QVQ、Gemini Flash Thinking本身内置推理链，因此单独列出。数据集构建采用严格过滤和人工验证，减少噪声。人类专家评测在平衡子集上完成，具备参考价值。
- **充分性评价**：实验覆盖了主要MLLM系列，包含了不同尺度和策略的模型，以及多种推理增强方法。但物理学科问题数量（156题）相对较少，可能影响统计稳定性；化学问题虽多但集中在结构识别和计数，种类不够丰富。总体而言，实验设计较全面，验证了核心论点。

## 6. 论文的主要结论与发现

1. **MLLMs在多模态推理上表现不佳**：最佳模型Gemini 2.0 Flash Thinking-0121在EMMA-mini上仅48.00%，落后人类专家（77.75%）29.75个百分点；o1得分45.75%，表现相近。
2. **测试时计算缩放效果有限**：多数投票、最佳N选、锦标赛等方法在N=16时带来的提升较小（最多7.5%），仍远不及人类；更强基模型（如Gemini Flash Thinking）的Pass@N更高，但自奖励模型不如独立强奖励模型有效。
3. **视觉推理是瓶颈**：错误分析表明，52.83%的错误属于视觉推理错误（如无法模拟3D过程、错误应用物理规则），而非单纯的感知或知识缺失。文本CoT在视觉密集型任务（如2D变换）上反而损害性能，在可语言化的任务（如多跳计数）上才有帮助。
4. **开源与闭源模型对CoT的反应不同**：CoT通常提升闭源模型准确率，但下降开源模型准确率（如Qwen2-VL下降6-7%），表明开源模型难以有效利用语言辅助多模态推理。

## 7. 优点

- **新颖的评测定义**：聚焦“有机多模态推理”，通过严格过滤（图像+文本+字幕）确保问题必须深度整合视觉信息，而非浅层感知。
- **细粒度技能分类**：提供跨学科、跨类别的标签（如2D变换、3D场模拟、结构识别、3D可视化等），支持对模型能力的精细化分析，有助于诊断模型失败原因。
- **人工构建新数据**：化学和编程部分大部分为全新构造，特别是编程题采用多选题形式，避免了传统可视化生成任务中依赖不可靠的LLM作为裁判的问题。
- **全面的评测规模**：2788题覆盖四个学科，大规模新数据补充了物理、化学领域的不足，平衡子集便于快速对比。
- **丰富的实验设计**：不仅比较直接答案，还探索了CoT、测试时缩放、不同奖励模型等，深入分析了视觉推理瓶颈。

## 8. 不足与局限

- **物理学科问题较少**（156题），可能影响统计显著性和结论稳定性，且物理问题种类偏少。
- **化学问题集中在有机化学的结构识别和反应模拟**，缺少无机化学、分析化学等其他分支，限制了领域覆盖的广度。
- **基准构建中存在人工选择偏差**：手动收集和标注可能引入偏好，过滤过程虽严格但可能丢弃一些需要独特视觉推理但文本也能帮助解题的问题。
- **测试时缩放实验仅限于EMMA-mini**（400题），未在完整集上验证；且仅对GPT-4o、Gemini 2.0 Flash和Gemini Flash Thinking进行缩放，未覆盖开源模型。
- **人类专家评测仅在EMMA-mini上进行**，且专家数量有限（每学科2人），可能存在个体差异。
- **计算资源未报告**，影响可复现性评估；开源模型推理超参数设置（如temperature）可能不完全一致（采用默认值0.7），但不同模型默认值不同可能引入变量。
- **伦理风险提示**：多模态推理能力的提升可能被用于生成误导性视觉内容，但当前模型能力远不足以造成实际威胁；基准本身可能被用于过度优化而忽略通用能力。

（完）
