---
title: Dynamic Mixture of Curriculum LoRA Experts for Continual Multimodal Instruction Tuning
title_zh: 持续多模态指令微调中动态混合课程LoRA专家
authors: "Chendi Ge, Xin Wang, Zeyang Zhang, Hong Chen, Jiapei Fan, Longtao Huang, Hui Xue, Wenwu Zhu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=zpGK1bOlHt"
tags: ["query:balanced-mml"]
score: 8.0
evidence: 直接解决持续多模态指令微调中的模态不平衡
tldr: 持续多模态指令微调中现有方法因固定架构难以适应新任务，面临模态不平衡问题。本文提出动态混合课程LoRA专家（D-MoLE）方法，自动演化模型架构，通过动态调整各模态的专家权重缓解不平衡。实验证明D-MoLE有效提升了持续学习性能，实现了模态间的平衡更新。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-zpgk1bolht/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 840, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zpgk1bolht/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 629, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zpgk1bolht/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1767, \"height\": 753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zpgk1bolht/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 854, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zpgk1bolht/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 517, \"height\": 413, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zpgk1bolht/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1416, \"height\": 845, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zpgk1bolht/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1435, \"height\": 521, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1768, \"height\": 481, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1767, \"height\": 1567, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 481, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1772, \"height\": 943, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1004, \"height\": 1132, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1691, \"height\": 728, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1780, \"height\": 482, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1572, \"height\": 645, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1611, \"height\": 402, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 673, \"height\": 231, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zpgk1bolht/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1058, \"height\": 272, \"label\": \"Table\"}]"
motivation: 持续多模态指令微调中任务架构冲突和模态不平衡阻碍模型适应。
method: 提出D-MoLE方法，动态演化架构，通过混合课程LoRA专家调整模态权重。
result: D-MoLE在持续学习基准上显著提升性能，平衡了模态更新。
conclusion: 动态专家混合有效解决了模态不平衡和任务冲突。
---

## Abstract
Continual multimodal instruction tuning is crucial for adapting Multimodal Large Language Models (MLLMs) to evolving tasks. However, most existing methods adopt a fixed architecture, struggling with adapting to new tasks due to static model capacity. We propose to evolve the architecture under parameter budgets for dynamic task adaptation, which remains unexplored and imposes two challenges: 1) task architecture conflict, where different tasks require varying layer-wise adaptations, and 2) modality imbalance, where different tasks rely unevenly on modalities, leading to unbalanced updates. To address these challenges, we propose a novel Dynamic Mixture of Curriculum LoRA Experts (D-MoLE) method, which automatically evolves MLLM's architecture with controlled parameter budgets to continually adapt to new tasks while retaining previously learned knowledge. Specifically, we propose a dynamic layer-wise expert allocator, which automatically allocates LoRA experts across layers to resolve architecture conflicts, and routes instructions layer-wisely to facilitate knowledge sharing among experts. Then, we propose a gradient-based inter-modal continual curriculum, which adjusts the update ratio of each module in MLLM based on the difficulty of each modality within the task to alleviate the modality imbalance problem. Extensive experiments show that D-MoLE significantly outperforms state-of-the-art baselines, achieving a 15 percent average improvement over the best baseline. To the best of our knowledge, this is the first study of continual learning for MLLMs from an architectural perspective.

---

## 论文详细总结（自动生成）

# 论文《Dynamic Mixture of Curriculum LoRA Experts for Continual Multimodal Instruction Tuning》详细中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究动机**：多模态大语言模型（MLLMs）在实际应用中需要持续适应新任务（持续多模态指令微调，CMIT）。现有方法大多采用固定架构，导致模型容量静止，难以平衡新任务适应与旧知识保持。
- **两大核心挑战**：
  - **任务架构冲突**：不同任务对MLLM不同Transformer层的依赖不同，均匀分配参数效率低。
  - **模态不平衡**：不同任务对文本和视觉模态的依赖程度不同，导致某一模态主导学习，另一模态更新不足。
- **本文目标**：首次从架构演化角度研究MLLM持续学习，提出在受控参数预算下自动演化架构的方法，以动态适应新任务并缓解模态不平衡。

## 2. 方法论：核心思想、关键技术细节与算法流程

### 核心思想
- 提出 **D-MoLE（Dynamic Mixture of Curriculum LoRA Experts）**，通过**动态层专家分配器**和**基于梯度的模态间课程**两个组件，自动在参数预算内演化MLLM架构。

### 关键技术细节

1. **动态层专家分配器（Dynamic Layer-Wise Expert Allocator）**
   - 使用**零成本代理（zero-cost proxies）**：从新任务数据中随机采样1%子集，计算每层梯度范数作为敏感度指标。
   - 依据敏感度排名，在**预定义参数预算**内，仅向最关键的层分配LoRA专家（每个任务一个专家，低秩矩阵 \( \Delta W = BA \)）。
   - 引入**自编码器路由器（Autoencoder Router）**：每个任务有一个轻量2层MLP自编码器，学习该任务的序列嵌入（图像特征+文本特征拼接）。训练阶段用最低重建误差选择最相关的先前专家；推理阶段根据重建误差阈值自动选择专家，若超出所有阈值则回退到预训练主干。

2. **基于梯度的模态间课程（Gradient-based Inter-modal Continual Curriculum）**
   - 对每个新任务，同样利用零成本代理计算LLM和视觉编码器的梯度范数作为“难度分数”。
   - 根据难度分数动态分配参数预算：\[ r_t^M = \frac{Score_t^M}{Score_t^{LLM}+Score_t^{Vision}}, \quad B_t^M = r_t^M \cdot B_{total} \]
   - 使更难模态获得更多LoRA专家，缓解模态不平衡。

3. **算法流程（训练阶段）**
   - 新任务到达 → 采样1%数据 → 计算零成本分数 → 确定模态预算 → 动态分配层专家 → 训练自编码器 → 冻结预训练权重和旧专家 → 仅训练新专家（结合一个最相关的旧专家辅助知识迁移）。
   - 推理阶段：用自编码器重建设别任务，动态路由专家。

## 3. 实验设计

- **数据集/场景**：构建了一个综合CMIT基准，包括9个数据集，涵盖三类任务：
  - **VQA**：VizWiz-VQA、IconQA、OCR-VQA、KVQA、PMC-VQA
  - **图像描述**：VizWiz-Caption、TextCaps、Flickr30k
  - **视觉定位**：SK-VG
  - 任务序列随机排序，交替任务类型以增加难度。
- **对比方法**：
  - 基线包括：Seq-FT（序列微调）、LwF-LoRA、EWC-LoRA、Dense MoLE、Sparse MoLE、MoLA、O-LoRA。
  - 额外对比：Zero-shot、Finetune（单独微调）、Joint-learning（联合训练作为上界）。
  - 所有方法使用LoRA且限制总可训练参数一致。
- **评估指标**：任务特定指标（VQA top-1准确率、图像描述CIDEr、视觉定位IoU>0.5）。持续学习指标：AVG（跨阶段平均）、Last（最终阶段性能）、BWT（后向迁移，负值越低遗忘越严重）。

## 4. 资源与算力

- **模型与硬件**：使用 InternVL2-2B 模型，在 **8 × NVIDIA A100 (40GB) GPU** 上训练。
- **训练时间**：
  - D-MoLE总训练时间约 **12.40小时**（所有9个任务合计）。
  - 对比：Joint-learning 12.83h，Seq-FT 13.15h，O-LoRA 14.87h，MoLA 23.03h。
- **精度**：bfloat16，每个任务训练1或5 epoch（SK-VG和VizWiz-VQA为5 epoch，其余1 epoch）。
- **LoRA配置**：rank=8，总预算 \( B_{total}=24 \)（LLM和视觉编码器各24层，预算比例0.5）。

## 5. 实验数量与充分性

- **实验数量充分**：
  - 主实验在9个数据集上对比8种基线，报告AVG、Last、BWT三个指标（表2）。
  - 额外在通用MLLM基准（MME、MMMU、POPE）上评估知识保留（表3）。
  - 训练效率对比（表4）。
  - 消融实验：4个变体（v1仅微调LLM、v2仅微调视觉编码器、v3移除模态课程、v4移除动态层分配器）（图4）。
  - 阈值敏感性分析（附录G，表7）。
  - 不同参数预算对比（附录I，表11）。
  - 训练时间分解（附录H，表8、9、10）。
  - 可视化动态架构演化与专家激活（附录J，图6、7）。
- **公平性与客观性**：所有基线在相同LoRA参数总量下比较；消融实验系统性地验证每个组件贡献；数据集涵盖多种任务类型和难度。

## 6. 主要结论与发现

- **性能优势**：D-MoLE在所有指标上显著优于SOTA基线：
  - AVG提升15.08%，Last提升20.14%，BWT提升19.82%（相比最佳基线O-LoRA）。
  - 在多个任务上接近甚至超过Finetune和Joint-learning的独立学习上界（如表2中VizWiz-Cap的Last达148.77，而Finetune为151.36，Joint-learning为151.48）。
- **遗忘抑制**：BWT几乎为零（平均-1.49%），远低于其他方法的-20%以上，说明几乎无灾难性遗忘。
- **通用知识保护**：在MME、MMMU、POPE上比Seq-FT和O-LoRA更好地保留原始能力（表3）。
- **训练效率**：比大多数基线更快或相近，由于选择性激活LoRA，减少了反向传播计算量。
- **组件有效性**：消融实验表明动态层分配和模态间课程均不可或缺，单独去除任一组件均导致性能下降。

## 7. 优点

1. **首次从架构演化角度解决MLLM持续学习**：突破了固定架构的限制，动态调整模型容量。
2. **巧妙结合零成本代理和LoRA专家**：无需额外训练开销即可高效识别关键层和模态难度。
3. **自编码器路由实现无任务ID推理**：无需在推理时提供任务标签，实用性强。
4. **轻量级设计**：自编码器仅为2层MLP，零成本计算仅需1%数据一次前向/反向，整体训练时间与基线持平甚至更优。
5. **全面的评估**：涵盖持续学习标准指标、通用知识测试、效率分析、消融及可视化。
6. **理论支撑**：对“任务架构冲突”给出形式化定理证明（附录K），增强说服力。

## 8. 不足与局限

1. **依赖1%数据子集**：虽然采样比例小，但仍需访问当前任务部分数据；在极端数据量少或隐私受限场景可能不适用。
2. **任务边界清晰假设**：自编码器路由器假设任务间有明显分布差异（如不同数据集），对于子任务边界模糊的持续学习场景可能失效（作者在附录F承认此局限）。
3. **仅实验2B模型**：未在更大规模MLLM（如7B、13B）上验证，可扩展性有待检验。
4. **参数预算为超参数**：总预算 \( B_{total} \) 需手动设定，不同预算可能影响性能，但论文只测试了一种预算和一种缩放（附录I仅对比了O-LoRA的预算放大）。
5. **未与其他动态架构方法（如渐进式网络、动态可扩展网络）对比**：仅与基于LoRA的PEFT方法比较，与更广泛的持续学习基线对比不足。
6. **模态间课程基于梯度范数**：梯度范数作为难度代理可能受噪声影响，未与更复杂的课程策略（如动态损失调整）对比。

（完）
