---
title: Vision-Language Models Create Cross-Modal Task Representations
title_zh: 视觉语言模型创建跨模态任务表示
authors: "Grace Luo, Trevor Darrell, Amir Bar"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=77ziPGdQct"
tags: ["query:native-multi"]
score: 7.0
evidence: 研究跨模态任务向量，对齐不同模态的表示
tldr: 该论文发现视觉语言模型能够将概念上等价的输入（文本或图像）映射到共享的任务向量，该向量跨模态不变。通过跨模态迁移实验验证了其有效性，表明任务向量可以简化多模态处理，并为表示对齐提供了新视角。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 855, \"height\": 606, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 836, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 840, \"height\": 836, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1301, \"height\": 1224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 779, \"height\": 283, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 774, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 858, \"height\": 1177, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1755, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1425, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1594, \"height\": 1118, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1798, \"height\": 684, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1517, \"height\": 2303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1137, \"height\": 2225, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-77zipgdqct/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1432, \"height\": 1476, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1795, \"height\": 565, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1763, \"height\": 609, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 765, \"height\": 261, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1115, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1342, \"height\": 171, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 869, \"height\": 546, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 799, \"height\": 144, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1446, \"height\": 391, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1522, \"height\": 177, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1573, \"height\": 231, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1498, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1527, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-77zipgdqct/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 793, \"height\": 331, \"label\": \"Table\"}]"
motivation: 多模态模型如何表示任务信息尚不透明，尤其在跨模态情况下。
method: 通过计算跨模态任务向量并测试其跨模态迁移能力来研究表示对齐。
result: 单一任务向量在触发正确生成方面甚至优于完整任务提示，体现了跨模态对齐的有效性。
conclusion: 视觉语言模型自动创建跨模态任务表示，有助于统一多模态处理。
---

## Abstract
Autoregressive vision-language models (VLMs) can handle many tasks within a single model, yet the representations that enable this capability remain opaque. We find that VLMs align conceptually equivalent inputs into a shared task vector, which is invariant to modality (text, image) and format (examples, instruction), and may simplify VLM processing. We measure this alignment via cross-modal transfer--the ability of a task vector derived in one modality to trigger the correct generation in another--on a range of tasks and model architectures. Although the task vector is highly compressed, we find that this single vector outperforms prompting the model with the full task information, unique to this cross-modal case. Furthermore, we show that task vectors can be transferred from a base language model to its fine-tuned vision-language counterpart, and that they can be derived solely from instructions without the need for examples. Taken together, our findings shed light on how VLMs internally process task information, and how they map different modalities into common semantic representations.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：自回归视觉-语言模型（VLMs）能够在单一模型中处理多种任务，但其内部如何表示任务信息仍然不透明。特别是，对于相同任务的不同规格（如文本示例、图像示例、指令），模型是否形成统一的内部表示？
- **研究动机**：理解VLM的内部工作机制，揭示其如何将不同模态（文本、图像）和格式（示例、指令）的输入映射到共享的语义表示空间，从而简化多模态处理。
- **整体含义**：论文发现VLMs能够将概念上等价的输入对齐到一个共享的“任务向量”（task vector），该向量跨模态、跨格式不变。这一发现有助于解释VLM的灵活性和泛化能力，并为模型压缩、跨模态迁移提供新视角。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：VLMs在处理任务规格（如文本示例、指令或图像示例）时，会在特定位置（最后一个查询-答案对之间的分隔符token处）产生一个高维向量，即“任务向量”。该向量编码了任务的摘要信息，并且对于概念等价的不同规格是共享的。论文通过“跨模态修补”（Cross-Modal Patching）来验证这一对齐：从一个模态提取任务向量，然后将其注入到另一模态的查询中，观察能否触发正确的任务生成。
- **关键技术细节**：
  - **激活修补（Activation Patching）**：给定任务规格（如文本示例），在模型前馈过程中，从第 \(l\) 层的最后一个分隔符token处提取任务向量 \(h_{l, txt}\)。然后，对于另一模态的查询（如图像查询 \(x_{img}\)），在相同层和token位置注入该向量，替代原始前馈提供的表示，从而诱导模型执行该任务，而无需在上下文中显式提供任务规格。
  - **任务向量来源**：可来自文本示例、图像示例或纯文本指令。还支持集成（element-wise平均）指令和示例的任务向量以提升样本效率。
  - **跨模态迁移度量**：比较修补后的输出与地面真相标签（精确字符串匹配或GPT-4o评分）。
  - **LLM到VLM迁移**：从基础语言模型（如Vicuna, Mistral）提取任务向量，修补到其对应的微调后VLM（如LLaVA-v1.5, Idefics2）的图像查询上。

## 3. 实验设计：数据集、场景、基准与对比方法

- **数据集/任务**：
  - **主要评估集**：6个自定义任务，每个任务既有文本规格又有图像规格。包括：国家-首都、国家-货币、动物-拉丁名、动物-幼崽、食物-颜色、食物-风味。每个任务分为30个验证样本和100个测试样本。
  - **扩展VQA任务**：从VQAv2（Goyal et al., 2017）中自动构建3个子任务（食物分类、衬衫颜色、男人手持物品），使用图像或密集文本描述作为输入。
  - **任务覆盖实验**：设置4种冲突场景（语义、语法、创意生成、事实回忆），使用VQAv2、OK-VQA、A-OKVQA等。
- **基准方法**：
  - 随机、无上下文（No Context）
  - 图像示例少样本提示/修补（Image Examples Prompt / Patch）
  - 文本示例少样本提示/修补（Text Examples Prompt / Patch）
  - 指令修补（Instruction Patch）
  - 指令+示例集成修补（Ensemble Patch）
  - 系统提示（System Prompt）用于任务覆盖比较
- **对比模型**：
  - LLaVA-v1.5（晚融合，7B）
  - Mantis-Fuyu（早融合，8B）
  - Idefics2（晚融合，8B）
  - 基础语言模型：Vicuna（用于LLaVA）、Mistral（用于Idefics2）

## 4. 资源与算力

- **文中明确说明**：仅在附录A.2中报告了计算开销（runtime和VRAM），但**未明确给出训练所使用的GPU型号、数量、训练时长**。实验部分主要基于预训练模型（Idefics2等）进行推理和修补，未涉及从头训练。
- **结论**：论文未提供详细的训练算力信息。

## 5. 实验数量与充分性

- **实验数量**：论文进行了多组实验，包括：
  - 主跨模态迁移实验（3个模型 × 6个任务 × 3个随机种子，表2）
  - LLM到VLM迁移实验（表3）
  - 指令任务向量与集成实验（图6）
  - 扩展VQA任务实验（表4）
  - 任务覆盖实验（表5）
  - 消融实验：模板格式（表10）、所有模态组合（表12）、鲁棒性（表9）
  - 内部表示分析（t-SNE可视化、logit lens解码、三层阶段性分析）
- **充分性评价**：
  - **覆盖全面**：涵盖多种模型架构（早/晚融合）、多种任务类型（合成/真实VQA）、多种规格（文本/图像/指令）。
  - **统计严谨**：所有结果基于3个种子取均值，报告方差或置信区间。
  - **消融/对照充分**：对比了修补 vs 提示、跨模态 vs 单模态、LLM vs VLM等。
  - **局限性**：任务种类相对有限（主要6个合成任务+3个VQA子集），且图像示例需要视觉识别步骤，可能引入额外噪声。论文本身也承认缺少对更大规模模型（如70B以上）的验证。

## 6. 论文的主要结论与发现

1. **跨模态任务向量存在**：VLMs将概念等价的输入（文本/图像/指令）映射到共享的任务向量空间，该向量聚类按任务而非按模态（图2b）。
2. **跨模态修补优于少样本提示**：将文本示例的任务向量修补到图像查询上，性能显著高于直接少样本提示（表2），且有时优于图像示例修补。
3. **LLM到VLM任务向量可迁移**：基础语言模型的任务向量与微调后VLM的任务向量高度相似（余弦相似度≥0.89），并且从LLM修补到VLM图像查询上的性能与VLM内部修补相当甚至更好（表3）。
4. **任务向量可由指令定义**：纯指令也可生成有效任务向量，与示例向量集成后可提升样本效率（图6）。
5. **跨模态任务覆盖能力**：修补指令向量可有效覆盖或override原任务，优于系统提示（表5）。
6. **表示演化三阶段**：模型在处理多模态输入时，表示经历“输入→任务摘要→答案”三个阶段，与文本ICL过程相似（图8、图13）。

## 7. 优点：方法或实验设计上的亮点

- **新颖性**：首次系统研究VLMs跨模态任务向量的对齐性，提出跨模态修补作为量化工具。
- **方法论简洁有效**：激活修补技术无需额外训练，可在少量推理开销下实现跨模态任务迁移，并显著降低计算成本（附录A.2）。
- **实验设计严谨**：使用合成任务和真实VQA任务，覆盖多种模型架构，进行统计验证和消融。
- **实用价值**：任务向量可用于压缩长上下文（如用单个向量替代30个示例），且在任务覆盖场景中表现出色，有实际应用潜力。
- **提供解释工具**：通过t-SNE、logit lens等揭示了任务向量的聚类性质和解码出来的语义摘要，推动了VLM可解释性。

## 8. 不足与局限：包括实验覆盖、偏差风险、应用限制

- **解释不充分**：论文仅观察到跨模态任务向量的存在，但未深入解释其根本原因（如数据同构性、模型归纳偏好等），作者自己也承认这一点。
- **任务与模型覆盖有限**：仅使用6个合成任务+3个VQA子任务，且模型参数规模均不超过8B，未验证更大模型（如70B+）或更复杂、开放域任务。
- **图像示例存在噪声**：图像示例需要额外视觉识别步骤，导致任务向量可能不如文本示例干净（表6图像ICL解码结果更嘈杂），这可能影响结论的泛化性。
- **评估指标局限**：主要使用精确字符串匹配（表2等），对于开放性任务（如任务覆盖中的创意生成）改用GPT-4o评分，但后者可能引入自动评估偏差。
- **跨模态修补的适用范围**：论文主要针对“文本→图像”的跨模态迁移，并发现“图像→文本”迁移效果较差（表12），说明其不对称性，未深入探讨原因。
- **缺乏对长上下文、多模态对话场景的评估**：仅使用固定5个示例或单条指令，未测试动态交互或复杂指令链。

（完）
