---
title: Re-ranking Reasoning Context with Tree Search Makes Large Vision-Language Models Stronger
title_zh: 通过树搜索重新排序推理上下文，使大型视觉语言模型更强
authors: "Qi Yang, Chenghao Zhang, Lubin Fan, Kun Ding, Jieping Ye, Shiming Xiang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=DJcEoC9JpQ"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 结合树搜索的多模态检索增强生成用于视觉问答推理
tldr: 针对多模态检索增强生成中推理示例稀缺和检索知识响应不稳定的问题，本文提出RCTS框架。通过自洽评估机制构建富含推理模式的知识库，并利用蒙特卡洛树搜索对检索到的上下文进行重排序，为大视觉语言模型提供更准确的推理支持。在VQA基准上，该方法有效提升了答案质量和推理一致性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 827, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1617, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1567, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1568, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 860, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1577, \"height\": 792, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1783, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1783, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1782, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1770, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1803, \"height\": 74, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1777, \"height\": 70, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1770, \"height\": 72, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1739, \"height\": 1487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1737, \"height\": 2017, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1748, \"height\": 1851, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1746, \"height\": 2153, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1703, \"height\": 2195, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djceoc9jpq/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1738, \"height\": 2176, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-djceoc9jpq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 887, \"height\": 307, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djceoc9jpq/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1703, \"height\": 628, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djceoc9jpq/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 854, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djceoc9jpq/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 838, \"height\": 291, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djceoc9jpq/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 821, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djceoc9jpq/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 809, \"height\": 203, \"label\": \"Table\"}]"
motivation: 现有多模态RAG存在推理示例稀缺和检索知识不准确的问题。
method: 构建包含推理模式的知识库，并采用蒙特卡洛树搜索对检索上下文进行重排序以增强LVLM。
result: 在多个VQA数据集上，该框架显著提升了LVLM的答案准确率和推理能力。
conclusion: 通过推理上下文增强和树搜索重排序，多模态RAG系统能有效改善视觉语言模型的推理性能。
---

## Abstract
Recent advancements in Large Vision Language Models (LVLMs) have significantly improved performance in Visual Question Answering (VQA) tasks through multimodal Retrieval-Augmented Generation (RAG). However, existing methods still face challenges, such as the scarcity of knowledge with reasoning examples and erratic responses from retrieved knowledge. To address these issues, in this study, we propose a multimodal RAG framework, termed RCTS, which enhances LVLMs by constructing a Reasoning Context-enriched knowledge base and a Tree Search re-ranking method. Specifically, we introduce a self-consistent evaluation mechanism to enrich the knowledge base with intrinsic reasoning patterns.  We further propose a Monte Carlo Tree Search with Heuristic Rewards (MCTS-HR) to prioritize the most relevant examples.  This ensures that LVLMs can leverage high-quality contextual reasoning for better and more consistent responses. Extensive experiments demonstrate that our framework achieves state-of-the-art performance on multiple VQA datasets, significantly outperforming In-Context Learning (ICL) and Vanilla-RAG methods. It highlights the effectiveness of our knowledge base and re-ranking method in improving LVLMs.

---

## 论文详细总结（自动生成）

# 论文总结：Re-ranking Reasoning Context with Tree Search Makes Large Vision-Language Models Stronger

## 1. 核心问题与整体含义（研究动机和背景）

- **问题背景**：大型视觉语言模型（LVLMs）在视觉问答（VQA）中通过多模态检索增强生成（RAG）取得进展，但面临两个关键挑战：
  1. **推理示例稀缺**：现有知识库中的问答对大多以公式化形式（如“答案为 A”）存储，缺乏内在的推理逻辑模式，无法为 LVLMs 提供有效的推理引导。
  2. **检索质量不稳定**：即使检索到相关示例，其质量参差不齐，可能对生成造成负面影响（指令错位、幻觉）。
- **研究动机**：将多模态 RAG 与上下文学习（ICL）结合，使 LVLMs 不仅“知道”（known），更能“理解推理”（know-how reasoning）。为此需要构建包含推理上下文的知识库，并对检索到的示例进行智能重排序。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
提出 **RCTS（Reasoning Context-enriched knowledge base + Tree Search）** 框架，包含三部分：
1. **构造带推理上下文的知识库**：通过自动生成机制为每个问答对添加详细的推理步骤。
2. **混合嵌入检索**：同时利用文本和图像特征检索相关样本。
3. **蒙特卡洛树搜索与启发式奖励（MCTS-HR）**：对检索到的样本进行重排序，选出最优示例组合。

### 关键技术细节

- **推理上下文生成（Reasoning Context with Self-Consistent Evaluation）**
  - 对知识库中每个问答对 `(Q_kb, A_kb)`，用 LVLM 生成 N_c 个候选推理上下文 `{C_i}`。
  - 用每个 `C_i` 与 `Q_kb` 结合生成预测答案，与真实答案 `A_kb` 对比得到得分 `Score_i`。
  - 选择得分最高的 `C_i` 作为该样本的推理上下文。

- **混合嵌入检索（Hybrid Embeddings Retrieval）**
  - 使用冻结的 BERT-base（文本编码器）和 ViT-L + 2 层 MLP（图像编码器）从 PreFLMR 初始化。
  - 将用户查询的文本和图像编码拼接为混合嵌入 `E_u = [E_Tu, E_Iu]`，知识库同样处理。
  - 计算相关性得分 `r(E_u, E_i) = Σ_j max_k (E_uj · E_ik^T)`，选取 Top-N 样本。

- **蒙特卡洛树搜索与启发式奖励（MCTS-HR）**
  - 将 Top-N 样本作为动作空间 `A`，每个动作包含问答对及其相似度分数 `s_i`。
  - 树搜索过程：选择 → 扩展 → 模拟 → 反向传播。
  - **动作选择**：根据相似度概率分布 `P(a_i) = s_i / Σ s_j` 采样。
  - **启发式奖励**：
    - **自洽奖励（Self-Reward）**：对于分支 i 预测的答案 `~y_i`，用 LVLM 生成 N_s 个不同随机种子下的答案，与原始预测答案计算规则匹配得分 `Q_S`。
    - **互惠奖励（Mutual-Reward）**：从动作空间选 N_m 个样本作为“互惠样本”，用分支 i 的预测作为上下文，让 LVLM 回答这些样本的问题，预测答案与真实答案比较得 `Q_M`。
    - **最终奖励**：`Q_i = α·Q_S + (1-α)·Q_M`（默认 α=0.2）。
  - **反向传播**：更新父节点 Q 值，公式为 `Q'(p) = 1/2 [ (Q(p)·N(p)+Q(c))/(N(p)+1) + max_{i∈Children(p)} Q(i) ]`。
  - 终止条件：最大 rollout 次数（默认 10）或早停策略（零样本与叶子节点答案一致）。

## 3. 实验设计

### 数据集
- **推理型 VQA**：ScienceQA（4241 测试 / 16967 训练+验证）、MMMU（150 开发 / 900 验证）、MathV（304 测试mini / 2736 测试）
- **非推理型 VQA**：VizWiz（4319 验证 / 20523 训练）、VSR-MC（1181 测试 / 4440 训练+验证）
- 确保知识库与评估集无重叠。

### Benchmark 与对比方法
- **基线**：Zero-Shot、ICL（随机检索）、Vanilla-RAG（Top 检索，Lin et al., 2024b）
- **LVLMs**：Qwen2-VL（2B/7B）、InternVL-2（8B），均支持多图像输入

### 主要结果
- 在所有数据集上，RCTS 全面超越对比方法。例如：
  - ScienceQA（Qwen2-VL 2B）：Zero-Shot 67.18%，ICL 70.10%，Vanilla-RAG 71.94%，**RCTS 78.99%**
  - MathV（Qwen2-VL 7B）：Vanilla-RAG 24.67%，**RCTS 28.95%**
  - VizWiz（Qwen2-VL 7B）：Vanilla-RAG 69.89%，**RCTS 71.50%**
  - 平均提升超过 Vanilla-RAG 约 3-4%。

## 4. 资源与算力

- 文中提到：**超过 7B 参数量的 LVLM 通过 AWQ 4-bit 量化在单个 RTX 4090 24GB GPU 上运行**。
- 未明确说明训练时长、总计算消耗或具体 rollout 时间成本。
- 推理上下文生成和 MCTS 多轮模拟会导致额外开销，但论文未给出量化对比（如推理时延或 FLOPs）。

## 5. 实验数量与充分性

- **主实验**：在 5 个数据集 × 3 种 LVLM × 4 种方法（含 RCTS）共约 60 个配置下报告结果（表 2、表 3）。
- **消融实验**：共 4 组：
  - 关键组件消融（表 4）：分别移除推理上下文和 MCTS-HR，验证两者互补。
  - 奖励策略消融（图 5a）：自洽奖励、互惠奖励、混合奖励对比。
  - Rollout 数量影响（图 5b）：4/6/10/18/34 等。
  - 权重 α 敏感性（表 5）：0.0/0.2/0.5/0.8/1.0。
- **可靠性验证**（表 6）：评估生成的推理上下文本身的准确性（在 ScienceQA 上达 100%）。
- **定性分析**：图 6 及附录 D 给出多组可视化案例。
- **充分性评价**：实验覆盖了不同难度、不同领域、不同模型规模，消融全面，对比公平（相同知识库、相同 LVLM）。但缺乏在更大量级 LVLM（如 13B+）上的验证；未与最新 RAG 方法（如 EchoSight）对比。

## 6. 主要结论与发现

1. **推理上下文显著增强**：自动生成的推理上下文能为 LVLMs 提供内在逻辑模式，提升答案准确率。
2. **MCTS-HR 重排序有效**：通过树搜索探索示例组合，优于简单的 top 检索（Vanilla-RAG）。
3. **混合奖励最优**：自洽奖励与互惠奖励结合（α=0.2）在推理型数据集上取得最佳性能。
4. **泛化性好**：在推理和非推理数据集、不同大小 LVLM 上均稳定提升。
5. **依赖性**：提升幅度受知识库中相似样本丰富度影响（MMMU 领域广，提升仅 3% 左右）。

## 7. 优点（亮点）

- **方法新颖性**：首次将推理上下文自动生成与蒙特卡洛树搜索结合用于多模态 RAG 重排序。
- **无需额外训练**：框架完全免微调，可迁移到任意 LVLM 和多领域。
- **自洽与互惠双重奖励**：兼顾单样本预测稳定性和跨样本一致性，设计巧妙。
- **消融实验完整**：对各个组件、奖励形式、超参数进行了系统分析。
- **可视化丰富**：附录 D 提供了大量 MCTS 分支展开的详细案例，直观展示重排过程。

## 8. 不足与局限

- **知识库依赖**：若知识库中缺乏与用户查询高度相似的样本，RCTS 仍可能失败（如附录 Fig.16 案例）。
- **计算开销大**：多轮 LVLM 生成（N_c=10, N_p=10, N_s=5, N_m=5）加上 MCTS rollout（默认 10），推理耗时显著高于 Vanilla-RAG，但论文未给出具体时间/成本对比。
- **领域覆盖局限**：MMMU 数据集跨域广，提升有限，表明方法对领域多样性相对敏感。
- **对比基线有限**：仅对比 ICL 和 Vanilla-RAG，未与同期更先进的多模态 RAG 方法（如 EchoSight, Wiki-LLaVA）直接比较。
- **超参数经验设定**：α、rollout 数等未提供自适应策略，需手动调整。
- **潜在偏差风险**：自洽奖励基于同一 LVLM 生成答案，可能放大模型自身偏差。

（完）
