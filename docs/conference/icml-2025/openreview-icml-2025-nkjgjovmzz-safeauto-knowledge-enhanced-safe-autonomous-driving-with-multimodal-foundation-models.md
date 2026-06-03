---
title: "SafeAuto: Knowledge-Enhanced Safe Autonomous Driving with Multimodal Foundation Models"
title_zh: SafeAuto：基于知识增强的多模态基础模型安全自动驾驶
authors: "Jiawei Zhang, Xuan Yang, Taiqi Wang, Yu Yao, Aleksandr Petiushko, Bo Li"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=nKJGjovmZz"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 使用多模态大语言模型进行自动驾驶推理，融合视觉和文本数据
tldr: SafeAuto框架通过结合结构化和非结构化知识来增强基于多模态大语言模型的自动驾驶系统。提出位置依赖交叉熵损失(PDCE)改进低层控制信号预测。该方法解决了安全知识嵌入MLLM的挑战，实现了高层推理与低层控制的统一。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1741, \"height\": 817, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 855, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 750, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1053, \"height\": 1051, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1747, \"height\": 810, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1753, \"height\": 1024, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1748, \"height\": 963, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjgjovmzz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1719, \"height\": 1152, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 741, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 736, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1769, \"height\": 389, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 857, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 857, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 976, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 896, \"height\": 671, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1771, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1771, \"height\": 365, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjgjovmzz/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 627, \"height\": 286, \"label\": \"Table\"}]"
motivation: 传统自动驾驶系统难以结合高层推理与低层控制，MLLM的引入面临安全知识嵌入困难。
method: 提出PDCE损失改进控制信号预测，并融合非结构化和结构化知识增强MLLM。
result: 在自动驾驶任务中实现了更安全的行为，验证了知识增强MLLM的有效性。
conclusion: 所提框架有效连接了高层推理与低层控制，提升了自动驾驶安全性能。
---

## Abstract
Traditional autonomous driving systems often struggle to connect high-level reasoning with low-level control, leading to suboptimal and sometimes unsafe behaviors. Recent advances in multimodal large language models (MLLMs), which process both visual and textual data, offer an opportunity to unify perception and reasoning. However, effectively embedding precise safety knowledge into MLLMs for autonomous driving remains a significant challenge.
To address this, we propose SafeAuto, a framework that enhances MLLM-based autonomous driving by incorporating both unstructured and structured knowledge. First, we introduce a Position-Dependent Cross-Entropy (PDCE) loss to improve low-level control signal predictions when values are represented as text. Second, to explicitly integrate safety knowledge, we develop a reasoning component that translates traffic rules into first-order logic (e.g., "red light => stop") and embeds them into a probabilistic graphical model (e.g., Markov Logic Network) to verify predicted actions using recognized environmental attributes.
Additionally, our Multimodal Retrieval-Augmented Generation (RAG) model leverages video, control signals, and environmental attributes to learn from past driving experiences. Integrating PDCE, MLN, and Multimodal RAG, SafeAuto outperforms existing baselines across multiple datasets, enabling more accurate, reliable, and safer autonomous driving. The code is available at https://github.com/AI-secure/SafeAuto.

---

## 论文详细总结（自动生成）

好的，作为一名资深学术论文分析助手，我将严格按照您的要求，使用中文、以Markdown形式，对论文《SafeAuto: Knowledge-Enhanced Safe Autonomous Driving with Multimodal Foundation Models》进行结构化、深入、客观的总结。

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：传统的自动驾驶系统通常将高层推理（例如“汽车应该减速并停止”）与低层控制（例如预测具体的速度和转向角度）分离为不同模块，忽略了两者间的内在关联，导致驾驶行为不连贯、效率低下甚至不安全。尽管多模态大语言模型（MLLM）的出现为统一感知与推理带来了机遇，但如何将精确的驾驶安全知识有效地嵌入到MLLM中，仍然是一个重大挑战。
- **研究动机**：当前基于MLLM的自动驾驶方法主要存在两个局限：其一，在数值控制信号预测上，无论是将其作为文本序列生成，还是通过线性层解码，都无法同时兼顾数值精度和语言模型的文本生成能力（即回答问题、解释行为的能力）。其二，这些方法本质上是数据驱动的，未能有效利用结构化的交通规则和安全约束来保证行为的合规性，MLLM的幻觉倾向可能导致它生成不安全或违法的驾驶行为。
- **整体含义**：为了解决上述问题，论文提出了SafeAuto框架，旨在通过融合结构化知识（如明确表示的交通规则）和非结构化知识（如从过去驾驶经验中获取的上下文信息），来增强基于MLLM的自动驾驶系统，实现更安全、更准确、更可靠的行为。

## 2. 方法论：核心思想、关键技术细节、非公式化算法流程

- **核心思想**：SafeAuto框架在MLLM的基础上集成了三个核心模块，分别解决数值精度、安全合规和经验学习问题：
    1.  **位置依赖交叉熵损失（PDCE Loss）**：改进MLLM对低层级控制信号的数值预测精度。
    2.  **知识增强的后安全性验证（Knowledge-Enhanced Post-Safety Verification）**：利用马尔可夫逻辑网络（MLN）对MLLM的高层动作进行显式的安全规则校验和纠正。
    3.  **多模态检索增强生成（Multimodal RAG）**：通过训练一个统一嵌入空间，从历史驾驶经验中检索与当前场景相似的上下文，辅助决策。

- **关键技术细节**：
    1.  **PDCE损失**：
        - **问题**：传统交叉熵（CE）损失在预测数值“12.46”时，将每个数字（如“1”， “2”， “4”， “6”）的预测视为独立事件，未考虑预测值“12.40”与“11.46”在数值上与真实值的接近程度不同，导致预测分布不集中。
        - **解决方案**：设计了一个新损失函数，遵循两个原则：
            - **数字级接近性**：对于同一位置上的数字（如小数点后第一位），预测结果越接近真实数字（如预测“5”接近真实“6”），损失越小。
            - **位级重要性**：数字越靠左（如百位、十位），其在损失计算中的权重越高。
        - **实施手段**：
            - **软目标**：将传统的one-hot硬标签替换为以目标数字为中心的高斯分布 `D(μ, σ)`，例如预测“4”时，其周围的“3”和“5”也获得一定的概率。
            - **位级权重**：将所有数字权重的乘积作为权重（如数字“12.46”中，最高位“1”的权重最高，后续每个数字的权重递减），并与KL散度损失结合。公式为：`PDCE loss = Σ wi · KL(Pi || D(μi, σ))`。
            - **实践**：在训练过程中，σ从小的初值（0.01）逐渐增大到预设值（0.35），以稳定训练。同时，所有数值统一格式化（如8.1表示为“08.100”）。
    2.  **后安全性验证（MLN）**：
        - **建模**：将交通规则（如“红灯=>不加速”）转化为一阶逻辑公式（`SolidRedLight(x) => ¬Accelerate(x)`），并用马尔可夫逻辑网络（MLN）来建模，每个公式带有一个权重。MLN定义了一个联合概率分布。
        - **预测与观察**：MLN中的谓词分为：
            - **未观察谓词**：代表驾驶动作（如 `Accelerate(x)`, `Stop(x)`），是需要推断的变量。
            - **观察谓词**：
                1.  **MLLM动作谓词**：从MLLM生成的高层动作描述中提取（如`MLLMAccelerate(x)`）。
                2.  **环境谓词**：通过YOLOv8等对象检测器从视频中提取（如`StopSign(x)`， `SolidRedLight(x)`）。
                3.  **历史控制信号谓词**：从历史控制信号中提取（如`HCSTurnLeft(x)`）。
        - **推理与安全验证**：给定观察到的谓词，MLN通过最大化条件概率`P(未观察谓词 | 观察谓词)`来推断最安全的动作。如果MLN推断的动作与MLLM建议的动作相矛盾（例如，MLN认为应`Stop`，但MLLM认为应`Accelerate`），则用MLN的结果覆盖MLLM的原始动作，并重新提示MLLM生成新响应。
    3.  **多模态RAG**：
        - **目标**：训练一个统一的嵌入空间，将当前驾驶场景（视频、历史控制信号、环境谓词）嵌入到一个向量中。
        - **训练逻辑**：利用文本描述（如“汽车因前方红灯而减速停车”）的嵌入作为锚点。因为该文本描述已完美概括了所有模态的信息。通过最大化当前场景统一嵌入`Zu`与文本嵌入`Zt`的相似性矩阵对齐，来训练各模态的编码器（LanguageBind, MLP）。
        - **优势**：在推理时，无需文本描述，即可通过计算`Zu`的相似度，从训练数据库中检索最相似的`K`个驾驶经验，作为上下文输入给MLLM。实验表明，包含明确的二值环境谓词向量能显著提高检索性能。

- **非公式化算法流程**：
    1.  **训练阶段**：
        a. 使用**PDCE损失**和**RAG检索到的上下文**，端到端地微调MLLM，使其能同时准确预测高层动作、理由和低层控制信号。
        b. 训练**多模态RAG**的投影器（projectors），使多模态统一嵌入与该场景文本描述的嵌入空间对齐。
        c. 使用真实和模拟数据训练**MLN**的公式权重。
    2.  **评估阶段**：
        a. 对于当前驾驶场景，检索Top-K个最相似的历史经验作为上下文。
        b. 将当前视频、历史控制信号和检索到的上下文一起输入MLLM，生成高层动作、理由和低层控制信号。
        c. 提取MLLM生成的高层动作谓词以及从视频中提取的环境谓词。
        d. 将这些观察谓词输入训练好的**MLN**进行推理。若MLN推断的安全动作与MLLM的原始输出矛盾，则使用MLN的结果修正MLLM的输出。

## 3. 实验设计：数据集、基准、对比方法

- **数据集**：
    1.  **BDD-X**：用于评价高层动作/理由生成和低层控制信号预测。
    2.  **DriveLM**：基于nuScenes数据集，主要用于评价高层行为预测和低层轨迹预测。
- **基准**：
    - **BDD-X数据集**：
        - **ADAPT**: 基于视频Transformer的独立分支预测方法。
        - **TimeLLM**: 将LLM用于时间序列预测。
        - **DriveGPT4**: 首个端到端MLLM方法。
        - **RAGDriver**: 使用三元组损失的多模态检索方法。
    - **DriveLM数据集**：
        - **UniAD**: 纯低层预测的SOTA基线（包含使用完整视频的 Full 版本和单帧的 Single 版本）。
        - **BLIP-RT-2**: 使用BLIP-2结合RT-2的轨迹分词方法。
        - **DriveLM-Agent**: 使用图状VQA的高层行为预测SOTA方法。
- **对比方法**：实验在BDD-X和DriveLM两个数据集上，针对高层（动作、理由/行为）和低层（控制信号/轨迹）预测任务，分别与上述多个强基线进行了比较。

## 4. 资源与算力

- **实验硬件**：所有实验在**8张NVIDIA A6000 GPU**上完成。
- **训练详情**：
    - BDD-X: 微调2个epoch，批大小128，学习率5×10⁻²。
    - DriveLM: 微调4个epoch，批大小64，学习率5×10⁻²。
    - RAG投影器：训练100个epoch，BDD-X批大小2048，DriveLM批大小512。

## 5. 实验数量与充分性

- **实验组数**：论文进行了非常充分且多角度的实验，包括：
    - **主要结果**：在2个数据集、2个主要任务（高层、低层）上的性能对比。
    - **消融实验**：
        - 每个模块（PDCE, MLN, RAG）的单独贡献分析（BDD-X和DriveLM都做了）。
        - PDCE损失中不同σ值的敏感性分析。
        - RAG中是否包含环境谓词（EP）以及不同Top-K数量的影响。
        - 谓词选择（MLLM谓词、不同数量的环境谓词）的影响。
        - 各模块对交通规则违反率的影响。
        - 预测分布的定性展示（图2， 图7）。
    - **案例研究**：提供了高层动作预测、低层动作预测、MLN安全性验证的具体案例（图5， 6, 8）。
- **充分性评估**：
    - **客观与公平**：实验设计非常严谨。
        1.  **多数据集验证**：在BDD-X和DriveLM两个不同特点的数据集上评估，增加了结论的泛化性。
        2.  **多维度指标**：高层任务采用了BLEU-4， CIDEr， METEOR， 低层任务采用了RMSE， Aδ以及ADE， 并能通过引入“动作谓词准确率”这种更客观的指标来弥补传统NLP指标的不足。
        3.  **全面的消融**：对三个核心组件的贡献进行了清晰的量化分析，证明了每个组件的必要性。超参数分析（σ, K, 谓词选择）也使得实验结论非常坚实。
        4.  **公平性**：使用的基线是最新的SOTA方法，结果表格清晰展示了SafeAuto的优势。
    - **因此，可以认为实验设计是充分、客观且公平的。**

## 6. 主要结论与发现

- **提升低层预测精度**：PDCE损失能显著提升MLLM对数值控制信号的预测精度，使其误差更小、分布更集中，且能保留MLLM的语言生成能力。
- **增强高层动作安全性**：基于MLN的后安全校验能有效纠正MLLM提出的一系列危险或不合法的高层动作，降低规则违反率。
- **有效利用经验知识**：多模态RAG能有效从历史驾驶经验中学习，显著提升高层动作预测的准确性和上下文感知能力。其中，包含二值环境谓词是提升检索效果的关键。
- **整体性能突破SOTA**：集成了三个模块的SafeAuto在几乎所有指标上都优于现有SOTA方法。例如，在BDD-X上，速度预测RMSE额外降低5.8%，高层动作CIDEr提升28%；在DriveLM上，运动预测ADE降低44.4%，高层行为准确率提升13%。

## 7. 优点：方法或实验设计上的亮点

1.  **PDCE损失的设计**：这是一个优雅且创新的损失函数，它成功地将适合回归任务的MSE损失的性质（数值接近性）融入到了适合语言模型的CE损失中。它保留了MLLM的文本生成能力（用于QA），同时解决了数值预测准确性的问题，这是对当前MLLM+AD领域一个关键技术瓶颈的有效解决。
2.  **结构化和非结构化知识的融合**：SafeAuto并不仅仅是“使用MLLM”，而是创造性地将结构化的交通规则（通过MLN）和非结构化的经验知识（通过RAG）有机结合，形成了一套完整的“感知-推理-校验-学习”的闭环，比单纯的数据驱动方法更具鲁棒性和安全性。
3.  **模块化与即插即用**：如论文所述，这三个模块（PDCE, MLN, RAG）在设计上具有高度的模块化特性，可以方便地被集成到任何其他基于MLLM的自动驾驶框架中，具有很强的可扩展性和泛化性。
4.  **安全是第一性**：将“安全”作为框架设计的核心考量，通过MLN实现显式的、可解释的安全校验，而非仅依赖模型的内隐学习。这在安全攸关的自动驾驶领域至关重要。

## 8. 不足与局限

1.  **PDCE损失的优化空间**：论文本身承认，用于生成软目标的高斯分布 `D(μ, σ)` 是简单有效的，但可能存在更优的分布函数（如非对称分布）来进一步提升性能。超参数σ需要人工设定和调整。
2.  **谓词提取的瓶颈**：后安全校验（MLN）的有效性高度依赖谓词提取的准确性。当前使用的YOLOv8和GPT4o虽然强大，但并非完美。在场景复杂、光照差、或被遮挡的情况下，谓词提取可能失败，导致MLN的推理结果不可靠。
3.  **RAG检索的局限性**：RAG模块的性能依赖于检索到的经验与当前场景的相关性。当出现训练数据中没有遇到过的新型或边缘场景时，检索到的经验质量可能不高，甚至会引入噪声。论文也提出了未来可以加上一个二次重排序或过滤机制来缓解这个问题。
4.  **环境依赖性**：MLN中的交通规则是基于加州驾驶手册构建的，这使得SafeAuto的知识具有很强的地域局限性。将模型部署到其他国家和地区时，需要重新构建和训练MLN的规则和权重。
5.  **计算资源**：使用8张A6000 GPU进行实验，这表明整个模型的计算开销较大，在车端部署可能面临算力和实时性的挑战。

（完）
