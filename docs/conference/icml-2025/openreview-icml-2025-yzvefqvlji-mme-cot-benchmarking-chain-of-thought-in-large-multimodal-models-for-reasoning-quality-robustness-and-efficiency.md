---
title: "MME-CoT: Benchmarking Chain-of-Thought in Large Multimodal Models for Reasoning Quality, Robustness, and Efficiency"
title_zh: MME-CoT：评估大型多模态模型中链式思维推理的质量、鲁棒性与效率基准
authors: "Dongzhi Jiang, Renrui Zhang, Ziyu Guo, Yanwei Li, Yu Qi, Xinyan Chen, Liuhui Wang, Jianhan Jin, Claire Guo, Shen Yan, Bo Zhang, Chaoyou Fu, Peng Gao, Hongsheng Li"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=YZvefQVLJI"
tags: ["query:mm-reasoning"]
score: 9.0
evidence: 系统评估大语言模型在多种领域的链式思维推理能力
tldr: 大语言模型中的链式思维推理已得到广泛研究，但在多模态模型中的评估尚不系统。本文提出MME-CoT基准，涵盖数学、科学、OCR等六个领域，并设计了三项新指标评估推理质量、鲁棒性和效率。实验揭示了不同CoT策略在多模态推理中的表现差异。该基准为多模态推理研究提供了重要评测工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 861, \"height\": 937, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1695, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1741, \"height\": 790, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1105, \"height\": 624, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1769, \"height\": 1234, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 856, \"height\": 1095, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 856, \"height\": 1095, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1770, \"height\": 1004, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 703, \"height\": 706, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1777, \"height\": 1547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1777, \"height\": 1376, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 542, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 742, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 952, \"height\": 1395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1542, \"height\": 1747, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 910, \"height\": 1406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1733, \"height\": 730, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 808, \"height\": 1298, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 399, \"height\": 201, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1465, \"height\": 571, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 427, \"height\": 208, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 64, \"height\": 64, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yzvefqvlji/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 66, \"height\": 70, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 518, \"height\": 643, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 569, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1750, \"height\": 150, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1763, \"height\": 852, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1782, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1769, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 697, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yzvefqvlji/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 788, \"height\": 303, \"label\": \"Table\"}]"
motivation: 链式思维推理在大语言模型中表现优异，但在多模态模型中的评估缺乏系统性。
method: 构建涵盖六个领域的MME-CoT基准，提出三方面评估指标。
result: 揭示了不同CoT策略在多模态推理中的表现差异，为后续研究提供参考。
conclusion: MME-CoT为多模态推理评测提供了标准化工具，推动了该领域的发展。
---

## Abstract
Answering questions with Chain-of-Thought (CoT) has significantly enhanced the reasoning capabilities of Large Language Models (LLMs), yet its impact on Large Multimodal Models (LMMs) still lacks a systematic assessment and in-depth investigation. In this paper, we introduce **MME-CoT**, a specialized benchmark evaluating the CoT reasoning performance of LMMs, spanning six domains: math, science, OCR, logic, space-time, and general scenes. 
As the first comprehensive study in this area, we propose a thorough evaluation suite incorporating three novel metrics that assess the reasoning quality, robustness, and efficiency at a fine-grained level.
Leveraging curated high-quality data and a unique evaluation strategy, we conduct an in-depth analysis of state-of-the-art LMMs, uncovering several key insights: *1)* Models with reflection mechanism demonstrate a superior CoT quality, with Kimi k1.5 outperforming GPT-4o and demonstrating the highest quality results; *2)* CoT prompting often degrades LMM performance on perception-heavy tasks, suggesting a potentially harmful overthinking behavior; and *3)* Although the CoT quality is high, LMMs with reflection exhibit significant inefficiency in both normal response and self-correction phases.
We hope MME-CoT serves as a foundation for advancing multimodal reasoning in LMMs.

---

## 论文详细总结（自动生成）

# 论文总结：MME-CoT：评估大型多模态模型中链式思维推理的质量、鲁棒性与效率基准

## 1. 核心问题与整体含义

- **研究动机**：链式思维（Chain-of-Thought，CoT）已在大语言模型（LLMs）中显著提升推理能力，但在大型多模态模型（LMMs）中，CoT 的适用性、影响程度及潜在副作用尚缺乏系统性评估。现有基准多关注最终答案正确性，忽略了中间推理过程的质量、鲁棒性和效率。
- **核心问题**：
  1. LMMs 的 CoT 中间步骤是否逻辑有效且无幻觉？
  2. CoT 是否干扰感知任务，对推理任务的增强程度如何？
  3. 长链 CoT（尤其是反思步骤）的效率如何？哪些步骤真正有效？
- **整体含义**：本文提出 MME-CoT 基准，为多模态推理评测提供统一、细粒度的评估工具，揭示当前模型的不足，推动 LMMs 推理能力发展。

## 2. 方法论

### 核心思想
- 构建涵盖 6 个领域、17 个子类别的视觉推理数据集，提供人工标注的关键步骤（推理结论 + 图像标注）。
- 设计三维度评估套件：**Quality（质量）**、**Robustness（鲁棒性）**、**Efficiency（效率）**。

### 关键技术细节

#### 2.1 数据集构建
- **数据组成**：1,130 个问题，其中 837 个推理问题（74.1%）、293 个感知问题（25.9%）。包含 3,865 个关键步骤标注，平均每个问题 3.2 个推理结论、1.4 个图像标注。
- **数据来源**：MathVerse、MMMU-Pro、OlympiadBench、MMT-Bench、MuirBench、SciVerse 等 15 个现有基准。
- **两阶段分类**：先通过 GPT-4o 和 Qwen2-VL 对比直接提示与 CoT 提示的性能差异进行初步分类，再由人工专家复核每个问题，划分为推理或感知任务。
- **关键步骤标注**：由 GPT-4o 生成初稿，人工审核修正，确保每个步骤精简（仅保留核心结论和关键视觉描述）。对多解法问题，提供所有可行路径。

#### 2.2 CoT 质量评估
- **Recall（召回率）**：衡量模型预测中覆盖了多少个人工标注的关键步骤。对多解法问题，选择匹配步骤最多的解法计算。
- **Precision（精确率）**：将模型输出分割为原子步骤（逻辑推理、图像描述、背景信息），评估每个步骤的正确性（与标注匹配或逻辑合理）。
- **F1 Score**：作为 CoT 质量的最终指标。

#### 2.3 CoT 鲁棒性评估
- **Stability（稳定性）**：在感知任务上，比较 CoT 提示与直接提示的准确率差异（`Acc_COT - Acc_DIR`）。若为负，说明 CoT 干扰了感知。
- **Efficacy（有效性）**：在推理任务上，比较 CoT 提示与直接提示的准确率差异。正值表示 CoT 有帮助。

#### 2.4 CoT 效率评估
- **Relevance Rate（相关率）**：评估生成步骤中与解决问题相关的内容比例。通过缩放因子放大差异（`(r - α)/(1 - α)`，α=0.8）。
- **Reflection Quality（反思质量）**：识别以“Wait”、“Alternatively”等为标志的反思步骤，判断其对纠正错误或验证结论是否有效。

## 3. 实验设计

### 数据集与场景
- **基准**：MME-CoT，包含 1,130 个问题，6 大领域（数学 29.9%、科学 25.2%、OCR 16.4%、逻辑 9.0%、时空 8.2%、通用场景 11.4%），以及感知任务子集。
- **评测场景**：覆盖推理任务（需多步逻辑）和感知任务（主要测试视觉识别，极少推理）。

### 对比方法
- **早期 LMMs**：LLaVA-OneVision (7B/72B)、Qwen2-VL (7B/72B)、MiniCPM-V-2.6、InternVL2.5 (8B)、DeepSeek-VL2。
- **专门推理模型**：LLaVA-CoT (11B)、Mulberry (8B)、InternVL2.5-MPO (8B/78B)。
- **具有反思能力的模型**：Kimi k1.5（闭源）、QVQ-72B、Virgo-72B。
- **闭源模型**：GPT-4o、Claude-3.5、Gemini-2.0-Flash。
- **总模型数量**：13 个（含不同参数规模变体）。

### 实现细节
- 使用 GPT-4o 进行步骤分割和评估，GPT-4o mini 用于直接答案提取。
- 提示策略：CoT 提示（`Please generate a step-by-step answer...`）和直接提示（`Please directly provide the final answer...`）。
- 超参数遵循 VLMEvalKit 默认设置。

## 4. 资源与算力

- **文中未明确说明**使用的 GPU 型号、数量或训练时长。
- 评估过程主要依赖 GPT-4o 的 API，未涉及大规模模型训练。对于开源模型，推理时可能使用了 A100 等 GPU，但未具体报告。
- **不足**：缺乏算力消耗的量化，可能影响可重复性验证。

## 5. 实验数量与充分性

- **实验数量**：主要实验为一组完整的评测（表 2、表 3），对所有对比模型计算了三项指标的详细得分（共 15+ 指标）。另有人工一致性验证（表 7）、错误类型分布分析（图 11、图 12）。
- **充分性评价**：
  - **优点**：覆盖模型全面（从 7B 到 78B 及闭源模型），指标细粒度，包含人类验证。
  - **局限**：
    - 未进行交叉验证（如不同评判模型的影响）。
    - 未探索不同 CoT 变体（如思维树、自洽性）的影响。
    - 部分模型（如 Mulberry、LLaVA-CoT）在直接提示下仍输出长推理，导致鲁棒性得分不可靠。
    - 数据规模相对较小（1,130 题），可能不足以覆盖所有复杂推理场景。
- **总体**：实验设计合理，在有限资源下较充分，但在泛化性上仍有提升空间。

## 6. 主要结论与发现

1. **反思能力显著提升 CoT 质量**：Kimi k1.5 在 F1 得分上超越 GPT-4o，QVQ 比基座 Qwen2-VL-72B 提升 5.8%。
2. **长 CoT 不一定覆盖关键步骤**：虽然反思模型精确率高，但召回率未与最终准确率对齐，说明可能跳过中间步骤直接得答案。
3. **CoT 干扰感知任务**：多数模型在感知任务上稳定性为负（最大降幅 6.8%，InternVL2.5-8B），表明有害的过度思考行为。
4. **参数规模越大，CoT 助力越明显**：Qwen2-VL-72B 比 7B 版在推理任务上稳定性/有效性更高。
5. **反思步骤常低效**：QVQ 和 Virgo 的反思质量仅约 60%，Kimi k1.5 也有 25% 以上无效反思（重复、错误或未执行）。
6. **在通用场景、时空、OCR 任务上，模型易分心**：生成大量无关图像描述，降低相关率。

## 7. 优点

- **首次系统评估 LMMs 的 CoT 三方面**：质量、鲁棒性、效率，弥补了既往仅关注最终答案的不足。
- **细粒度可解释指标**：Recall/Precision 基于人工标注的关键步骤，避免了“正确答案但错误逻辑”的幻觉评价。
- **关注 CoT 对感知任务的负面影响**：提出稳定性指标，揭示了过度思考的风险，具有实际应用意义。
- **高质量数据集**：经两阶段人工验证的 1,138 道题及 3,865 个关键步骤，可复现且开源。
- **人类一致性验证**：在四个核心指标上均达到 85% 以上一致性，确保评估可靠性。

## 8. 不足与局限

- **计算资源未报告**：无法评估评测成本或复现难度。
- **评判模型依赖单一**：主要使用 GPT-4o 进行步骤判断，可能引入偏差（尽管有人类验证）。
- **数据规模较小**：仅 1,130 题，且各领域分布不均（逻辑 9%、时空 8.2%），可能影响统计显著性。
- **鲁棒性评估瓶颈**：部分模型在直接提示下仍输出推理过程（如 Mulberry、Kimi k1.5），导致稳定性/有效性结果不可靠，需要更严格的“直接输出”约束。
- **未涵盖多语言或复杂图表**：仅英文场景，且排除需要专业领域知识的题目。
- **未探索 CoT 变体**：如思维树（ToT）、自洽性（Self-Consistency）等，仅评估标准逐步推理。
- **反思质量定义依赖表面标记**：仅通过几个关键词检测反思步骤，可能遗漏隐含反思或误判。

（完）
