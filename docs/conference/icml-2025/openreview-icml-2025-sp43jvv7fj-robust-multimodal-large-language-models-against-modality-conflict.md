---
title: Robust Multimodal Large Language Models Against Modality Conflict
title_zh: 鲁棒的多模态大语言模型对抗模态冲突
authors: "Zongmeng Zhang, Wengang Zhou, Jie Zhao, Houqiang Li"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=SP43jVv7fJ"
tags: ["query:balanced-mml"]
score: 10.0
evidence: 直接处理多模态模型中的模态冲突，减轻偏见和幻觉
tldr: 多模态大模型在实际应用中常产生幻觉，现有研究忽视模态输入间的冲突。本文首次从模态冲突角度研究幻觉，定义模态冲突并构建MMMC数据集。提出基于提示工程、微调和强化学习的三种缓解方法，显著减少了由模态冲突导致的幻觉。该工作为构建鲁棒多模态系统提供了重要思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 795, \"height\": 925, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1648, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1654, \"height\": 505, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1686, \"height\": 400, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1678, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 480, \"height\": 482, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1547, \"height\": 1379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 879, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 884, \"height\": 594, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sp43jvv7fj/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 878, \"height\": 591, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 867, \"height\": 431, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1781, \"height\": 1016, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 736, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1779, \"height\": 1022, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1779, \"height\": 1022, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1779, \"height\": 1021, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1665, \"height\": 1255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1667, \"height\": 1367, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sp43jvv7fj/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1664, \"height\": 1305, \"label\": \"Table\"}]"
motivation: 多模态大语言模型中的幻觉常由输入模态间的冲突引起，现有研究关注不足。
method: 定义模态冲突，构建MMMC数据集，提出提示工程、微调和强化学习三种缓解方法。
result: 在多个基准上有效减少了模态冲突导致的幻觉，提升模型鲁棒性。
conclusion: 模态冲突是MLLM幻觉的重要成因，本文的方法为缓解该问题提供了有效方案。
---

## Abstract
Despite the impressive capabilities of multimodal large language models (MLLMs) in vision-language tasks, they are prone to hallucinations in real-world scenarios. This paper investigates the hallucination phenomenon in MLLMs from the perspective of modality conflict. Unlike existing works focusing on the conflicts between model responses and inputs, we study the inherent conflicts in inputs from different modalities that place MLLMs in a dilemma and directly lead to hallucinations. We formally define the modality conflict and construct a dataset named Multimodal Modality Conflict (MMMC) to simulate this phenomenon in vision-language tasks. Three methods based on prompt engineering, supervised fine-tuning, and reinforcement learning are proposed to alleviate the hallucination caused by modality conflict. Extensive experiments are conducted on the MMMC dataset to analyze the merits and demerits of these methods. Our results show that the reinforcement learning method achieves the best performance in mitigating the hallucination under modality conflict, while the supervised fine-tuning method shows promising and stable performance. Our work sheds light on the unnoticed modality conflict that leads to hallucinations and provides more insights into the robustness of MLLMs.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：多模态大语言模型（MLLMs）在实际应用中容易产生**幻觉**（hallucination），即生成与输入事实不符的内容。现有研究主要关注模型输出与输入之间的冲突，却忽视了一个重要根源：**不同模态输入（视觉与文本）之间的内在冲突**（modality conflict）。例如，用户提问“球是什么颜色？”但图片中根本没有球，模型却可能回答“球是绿色的”。
- **研究动机**：即使MLLMs能完美对齐多模态特征，当输入本身存在矛盾时（如文本假设图片中存在某物体而图片中没有），模型仍会陷入两难，直接导致幻觉。本文首次系统性研究这一问题，旨在揭示模态冲突对幻觉的影响并提升MLLMs的鲁棒性。
- **整体含义**：该工作为理解和缓解MLLMs幻觉提供了新视角，强调**输入模态间的一致性检查**是构建可信多模态系统的关键，填补了该领域的研究空白。

## 2. 提出的方法论：核心思想、关键技术细节

本文提出三种方法缓解模态冲突导致的幻觉，均基于条件生成模型 \(A \sim \pi_\theta(A|V, T)\)。

### (1) 模态冲突的正式定义
- **通用形式**：\( \text{Info}(V) \neq \text{Info}(T) \)，具体细分为三类：
  - **物体冲突**：文本中提到图片中不存在的物体（如“猫”不在图中）。
  - **属性冲突**：文本与图片描述同一物体但属性不同（如“红苹果” vs “绿苹果”）。
  - **关系冲突**：文本与图片描述同一对物体但关系不同（如“猫在桌上” vs “猫在地板上”）。

### (2) 数据集MMMC构建
- 基于Visual Genome图像，利用GPT-4o-mini对原始问题中的关键组件（物体、属性、关系）进行**替换**，生成与图像内容冲突的新问题，并基于纯文本生成正确答案（避免引入多模态幻觉）。经人工验证后得到20K三元组（18K训练/2K测试）。

### (3) 三种缓解方法
- **提示工程（PE）**：在问题前加上指令“请检查图像是否包含所提及的信息，然后回答问题：”，不更新模型参数。
- **监督微调（SFT）**：在MMMC数据集上使用语言建模目标微调模型（最小化负对数似然），1个epoch，10000训练样本。
- **强化学习（RL）**：将生成过程建模为MDP，使用REINFORCE++算法优化期望奖励。奖励函数在生成结束时依据语义一致性给予+1或-1（使用Llama-3.3-70B作为奖励模型），训练1000样本。

## 3. 实验设计

- **数据集**：主要使用自建的**MMMC**（20K样本，含3类冲突）；用于评估对齐税（alignment tax）的基准包括HallusionBench、MMBench、MMStar、MMMU、MathVista、OCRBench、AI2D、MMVet、MME。
- **基准模型**：InstructBLIP-7B、LLaVA-v1.5-7B、LLaVA-NeXT-7B、Qwen2-VL-Instruct（2B和7B）、GPT-4o。
- **对比方法**：Baseline（原始模型）、Prompt Engineering (PE)、Supervised Fine-Tuning (SFT)、Reinforcement Learning (RL)。
- **评估指标**：
  - **ROUGE-L**：与参考答案的序列重叠。
  - **Hallu-Rate**（幻觉率）：由LLM判断模型是否“假装看到”图像中不存在的物体/属性/关系。
  - **LLM-Judge**（整体质量分数0-4）：由GPT-4o和Llama-3.3-70B分别评估。
- **实验数量与充分性**：非常充分。
  - 主实验：6个模型 × 4种设置（Base/PE/SFT/RL），每个SFT和RL重复3次随机种子。
  - 消融与分析：
    - 三类冲突的子集性能分解（物体、属性、关系）。
    - 对齐税分析（9个通用基准上的性能变化）。
    - 训练稳定性分析（损失、奖励、响应长度、KL散度曲线）。
    - 训练轮数对RL性能的影响。
  - 所有实验均使用两个不同的LLM评判器（GPT-4o和Llama-3.3-70B）以保证结果可靠性。

## 4. 资源与算力

- 论文中**未明确说明GPU型号和数量**，但提及使用“MCC Lab of Information Science and Technology Institution, USTC”提供的GPU集群。
- 训练细节：SFT使用Adam优化器，lr=5e-6，batch size=8，1 epoch（10000样本）；RL使用Adam优化器，lr=9.65e-6，batch size=8，1000样本，KL系数0.01，最大响应长度128。所有微调均采用LoRA（低秩适应）。
- 奖励模型使用**Llama-3.3-70B-Instruct**（需额外推理资源）。
- 总体算力需求中等（LoRA微调+小型数据集），但未提供具体GPU小时数。

## 5. 实验数量与充分性评估

- **实验数量**：超过10组主实验 + 多组消融实验，覆盖5种不同架构的MLLM，每种配置重复3次。还包含定性示例分析（附录D）。
- **充分性**：非常充分。
  - 消融涵盖冲突类型、训练轮数、对齐税、训练稳定性等多个维度。
  - 使用两个独立LLM评判器交叉验证，消除单一评判偏差。
  - 公平性：所有方法在同一MMMC数据集上评估；对齐税分析在9个公认的公开基准上进行，基线与微调后模型相同。
- **客观性**：结果统计报告均值和标准差，可视化清晰，结论有数据支撑。

## 6. 论文的主要结论与发现

1. **模态冲突是MLLMs幻觉的重要诱因**：所有基线模型（包括GPT-4o）在MMMC上的幻觉率均超过40%，表明现有模型普遍缺乏识别模态冲突的能力。
2. **三种方法均有效，但RL最佳**：
   - RL使幻觉率降低10%~50%（如LLaVA-v1.5-7B从93.25%降至33.87%），整体质量提升0.4~0.9分。
   - SFT性能稳定，但对某些模型（如InstructBLIP）效果有限。
   - PE简单但依赖基础模型，有时甚至恶化结果。
3. **模型在处理不同冲突类型时表现差异**：物体冲突最容易，属性冲突次之，关系冲突最难（幻觉率最高）。
4. **对齐税普遍存在但可控**：对一些模型（如Qwen2-VL-7B）几乎无影响，对另一些（如InstructBLIP）影响较大；但部分基准（如LLaVA-NeXT在HallusionBench上）反而提升，表明冲突识别能力可迁移。
5. **RL训练不稳定**：训练曲线中奖励和响应长度波动明显，InstructBLIP甚至出现模型崩溃；SFT则更稳定。

## 7. 优点

- **问题定义创新**：首次从模态冲突角度系统定义并分类幻觉来源，提供形式化框架。
- **数据集精心设计**：基于Visual Genome，使用大模型自动生成冲突问题+人工验证，保证了质量和规模（20K）。
- **方法多样性**：涵盖无训练、监督微调、强化学习三种范式，便于对比分析。
- **评估全面严谨**：使用两种LLM评判器、多个指标（ROUGE-L、Hallu-Rate、LLM-Judge），并对齐税和训练稳定性进行深度分析。
- **实验充分**：覆盖多种主流MLLM架构（InstructBLIP, LLaVA, Qwen2-VL, GPT-4o），重复三次随机种子，结果可靠。
- **实用价值**：提示工程方法简单即用，RL方法效果强大，为实际部署提供不同成本的选择。

## 8. 不足与局限

- **数据集覆盖有限**：仅基于Visual Genome（静态图片+简单问答），缺乏真实世界复杂场景（如动态视频、常识推理）。冲突类型仅三种，可能遗漏其他冲突形式（如情感、抽象概念）。
- **RL稳定性问题**：RL训练容易导致模型崩溃（尤其对InstructBLIP），且需要精心调参，实际应用中部署风险较高。
- **对齐税未完全解决**：某些模型在部分通用基准上性能下降（如InstructBLIP在MMBench下降50%），说明模态冲突识别能力与通用能力存在权衡。
- **评估偏差风险**：虽使用LLM评判，但评判模型本身可能对某些回答存在偏好；幻觉率定义依赖“假装看到”，但模型可能以其他方式表达否认（如“我不确定”），判决可能不准确。
- **可扩展性**：仅测试7B及以下模型，更大模型（如70B、GPT-4V）表现如何未知；LoRA微调可能限制模型能力上限。
- **缺少与其他缓解方法的对比**：未与现有的去偏见解码方法（如VCD、OPERA）或DPO等方法比较，无法确定本文方法是否优于已有技术。

（完）
