---
title: Reasoning Limitations of Multimodal Large Language Models. A case study of Bongard Problems
title_zh: 多模态大语言模型的推理局限性：基于Bongard问题的案例研究
authors: "Mikołaj Małkiński, Szymon Pawlonka, Jacek Mańdziuk"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=NCZOxhBTrz"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 评估多模态大模型在Bongard问题上的抽象视觉推理能力
tldr: 本文以Bongard问题为案例，系统研究了多模态大语言模型（MLLMs）在抽象视觉推理中的局限性。作者设计了多种适合MLLM的求解策略，并在包含合成和真实图像的三类数据集上测试了8个模型。实验表明，MLLMs在真实世界数据集上取得了一定成功，但在合成数据集上表现不佳。为弥合这一差距，论文提出了Bongard-RWR数据集，用真实世界图像表达合成Bongard概念，为未来研究提供了新基准。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 863, \"height\": 700, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1731, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1629, \"height\": 338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1740, \"height\": 889, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1769, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1774, \"height\": 1187, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1769, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1768, \"height\": 1169, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1758, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1414, \"height\": 2132, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1777, \"height\": 1291, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1059, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 860, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 779, \"height\": 683, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1760, \"height\": 1182, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1434, \"height\": 413, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1437, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 628, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1437, \"height\": 416, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1492, \"height\": 1001, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1331, \"height\": 900, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1493, \"height\": 999, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1333, \"height\": 900, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1493, \"height\": 1000, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1334, \"height\": 902, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1488, \"height\": 1003, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1331, \"height\": 898, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1761, \"height\": 734, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1761, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 850, \"height\": 562, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1742, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nczoxhbtrz/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 861, \"height\": 603, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nczoxhbtrz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1734, \"height\": 441, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nczoxhbtrz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1238, \"height\": 390, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nczoxhbtrz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1631, \"height\": 335, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nczoxhbtrz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1757, \"height\": 1876, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nczoxhbtrz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1199, \"height\": 187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nczoxhbtrz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1201, \"height\": 189, \"label\": \"Table\"}]"
motivation: 多模态大语言模型在抽象视觉推理任务中仍存在显著局限，尤其是在合成Bongard问题上表现不佳，亟需探究其原因并改进。
method: 设计了多种适合MLLM的解决方案策略，并在三个Bongard数据集（包括合成和真实图像）上对4个闭源和4个开源模型进行了系统性评估。
result: MLLMs在真实世界数据集上表现较好，但在合成Bongard问题上普遍失败，揭示了对抽象形状推理的不足。
conclusion: MLLMs在抽象视觉推理上存在严重局限，Bongard-RWR数据集为未来改进提供了重要基准。
---

## Abstract
Abstract visual reasoning (AVR) involves discovering shared concepts across images through analogy, akin to solving IQ test problems. Bongard Problems (BPs) remain a key challenge in AVR, requiring both visual reasoning and verbal description. We investigate whether multimodal large language models (MLLMs) can solve BPs by formulating a set of diverse MLLM-suited solution strategies and testing $4$ proprietary and $4$ open-access models on $3$ BP datasets featuring synthetic (classic BPs) and real-world (Bongard HOI and Bongard-OpenWorld) images. Despite some successes on real-world datasets, MLLMs struggle with synthetic BPs. To explore this gap, we introduce Bongard-RWR, a dataset representing synthetic BP concepts using real-world images. Our findings suggest that weak MLLM performance on classical BPs is not due to the domain specificity, but rather comes from their general AVR limitations. Code and dataset are available at: https://github.com/pavonism/bongard-rwr

---

## 论文详细总结（自动生成）

# 多模态大语言模型的推理局限性：基于Bongard问题的案例研究——论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：Bongard问题（BPs）是一种经典的抽象视觉推理任务，要求从图像中识别共享概念并用自然语言描述，是评估AI类比与抽象推理能力的重要测试。近年来多模态大语言模型（MLLMs）取得了显著进展，但其在抽象视觉推理（AVR）任务上的表现尚未被系统研究。
- **核心问题**：MLLMs能否解决Bongard问题？它们在合成与真实世界两种图像域上的表现有何差异？这种差异是源于领域特殊性还是更根本的AVR局限性？
- **整体含义**：理解MLLMs在AVR上的当前局限，对评估其智能水平、指导未来模型改进具有重要价值。

## 2. 方法论：核心思想、关键技术细节与算法流程

- **核心思想**：针对MLLM特点设计多种求解策略，将Bongard问题转化为自然语言生成或二分类任务，并构建跨域数据集进行对比分析。

- **主要求解策略**（详见Figure 2）：
  - **Direct**：将整个BP矩阵作为单张图像输入，直接要求模型描述左右两侧的差异。
  - **Descriptive**：先对每个图像面板单独生成文本描述（或逐步迭代），再基于所有描述给出最终答案。
  - **Descriptive-iterative**：在单一上下文窗口中逐步看到左侧/右侧所有图像，并不断更新对该侧概念的描述，最后整合两侧描述得出答案。
  - **Descriptive-direct**：在Descriptive基础上，最终步骤同时提供整张矩阵图像。
  - **Contrastive**：分别比较左右侧对应的图像对（例如第一张左与第一张右），生成每对之间的差异描述，然后汇总给出答案。
  - **Contrastive-iterative**：在单一上下文窗口中依次处理图像对，逐步提炼差异，最后给出答案。
  - **Contrastive-direct**：在Contrastive基础上，最后步骤提供整张矩阵图像。

- **评估设置**（Figure 3）：
  - **自然语言生成**：使用MLLM投票（至少2/4专有模型同意）判断生成答案是否与真实概念一致。
  - **二分类设置**：
    - Ground-Truth / Incorrect Label：给模型整张矩阵和一个候选概念，要求判断其是否正确。
    - Images to Sides：给模型两张测试图像（分别来自左右侧，随机打乱），要求正确分配到对应侧。

- **Bongard-RWR数据集生成算法**（Section 4 & Algorithm 1）：
  1. 用GPT-4o对每个合成BP的概念生成\(N=10\)种真实世界文本描述。
  2. 用Pexels API为每种描述下载\(M=15\)张图片。
  3. 用GPT-4o筛选出能正确体现概念且与对立概念可区分的图片，直至获得\(T=3\)组描述，每组含左右各2张图片。
  4. 从不同描述组中抽取图片组装成6张左+6张右的BP实例，避免同类描述导致的简单模式。
  5. 最终通过人工检查与调整，得到60个Bongard-RWR实例（12个自动生成、24个自动+人工调整、24个完全手工构建）。

- **Bongard-RWR变体**：RWR-S（方形裁剪）、RWR-G（灰度）、RWR-SG（方形+灰度），用于分析布局和颜色对模型的影响。

## 3. 实验设计：数据集、Benchmark与对比方法

- **数据集**：
  - 合成BPs：前100个经典Bongard问题（Bongard, 1970）。
  - Bongard HOI：100个真实世界人-物交互问题（来自测试集的分层抽样）。
  - Bongard-OpenWorld：100个开放世界概念问题（测试集分层抽样）。
  - Bongard-RWR：60个由合成概念翻译而来的真实世界问题（本文构建）。

- **模型**：
  - 4个专有模型（通过API）：GPT-4o、GPT-4 Turbo、Gemini 1.5 Pro、Claude 3.5 Sonnet。
  - 4个开源模型（本地NVIDIA DGX A100节点）：InternVL2-8B、LLaVA-1.6 Mistral-7B、Phi-3.5-Vision、Pixtral 12B。
  - 额外缩放实验增加了GPT-4o mini、Gemini 1.5 Flash、InternVL2不同大小（26B/40B/76B）、LLaVA-NeXT系列等。

- **对比方法**：所有7种生成策略 + 3种二分类设置，以及多类概念选择实验（\(k\in\{2,4,8,16\}\)）。另外进行了30名人类受试者的对照实验。

## 4. 资源与算力

- 文中仅明确提到“本地运行的开源模型使用NVIDIA DGX A100节点”，未给出具体GPU型号、数量、训练时长。
- 专有模型通过API调用，算力消耗未提及。
- **结论**：论文未系统报告算力开销，对开源模型仅描述为“本地运行”，缺乏量化信息。

## 5. 实验数量与充分性

- **实验数量**：非常充分。每个模型在4个数据集上执行了7种生成策略 + 3种二分类设置，共计（8模型 × 4数据集 × 10条件）≈ 320组实验，另有额外缩放实验、多类选择实验、Bongard-RWR变体实验，以及人类研究。
- **充分性**：
  - 覆盖了合成与真实世界两个域，并引入Bongard-RWR进行跨域对比，设计巧妙。
  - 消融实验系统比较了-iterative和-direct变体，揭示了上下文窗口和视觉输入的影响。
  - 人类对照实验验证了数据集难度和模型差距。
- **客观性与公平性**：
  - 评估自然语言答案时使用MLLM投票，并通过手动验证调整prompt，减少了单一评估偏差。
  - 二分类任务中提供了随机基线（虚线）。
  - 但开源模型未进行任何微调或超参优化，可能未达到其最佳性能；专有模型后处理细节不透明。

## 6. 主要结论与发现

- **MLLMs在合成BPs上表现极差**：最佳模型（GPT-4o）仅解决22/100题（Direct + Descriptive-direct策略），而二分类任务中部分模型可接近随机水平。
- **真实世界数据集上略有改善**：在Bongard HOI和Bongard-OpenWorld上，最佳模型分别解决45/100和57/100题，但依然远低于人类（人类在Bongard-RWR上平均65%准确率）。
- **Bongard-RWR实验揭示本质局限**：尽管使用真实世界图像，MLLMs仅解决22/60题，远低于人类（平均39.2/60），表明其AVR能力不足并非源于数据域差异，而是根本性推理缺陷。
- **策略对比**：Descriptive策略普遍优于Contrastive策略，且Descriptive-iterative反而降低性能；Contrastive-direct能带来一定提升但不足以超越Descriptive。
- **专有模型显著优于开源模型**，但Pixtral 12B在某些二分类设置中展现出竞争力。
- **模型缩放**：更大模型一般更好，但GPT-4o mini能在部分任务中超过更大开源模型，说明单纯放大参数不足以弥补AVR缺陷。

## 7. 优点：方法与实验设计的亮点

- **系统化的求解策略设计**：覆盖了Direct、Descriptive、Contrastive三类范式及其变体，为MLLM在复杂视觉推理任务上的评估提供了通用框架。
- **跨域对比数据集Bongard-RWR**：创新性地将合成概念翻译为真实世界图像，使得可以直接比较MLLM在两种域上的表现，从而排除领域匹配假象。
- **多维度的评估设置**：不仅包含开放生成，还设计了二分类、多类选择等降级任务，有助于分层次诊断推理能力。
- **人类对照实验**：提供了新数据集的人类基线（39.2/60），清晰量化了人与模型之间的差距。
- **开源贡献**：代码和数据集公开，便于复现和后续研究。

## 8. 不足与局限

- **Bongard-RWR数据集规模小**（仅60个实例），且部分实例需要人工生成与调整，自动生成质量有限，可能限制了统计显著性和泛化结论。
- **未对开源模型进行微调或Prompt优化**，可能低估了其潜力；专有模型的API参数、温度等细节未公开，实验公平性存疑。
- **答案评估依赖MLLM投票**（4个专有模型），尽管经过手动验证，但仍可能引入评估偏差，尤其对于边界案例。
- **算力资源未充分报告**，影响实验可复现性。
- **仅关注Bongard问题**，结论对更广泛的AVR任务（如Raven矩阵、ARC）的适用性需进一步验证。
- **没有探讨模型内部机制或失败原因**（如注意力可视化、错误模式分析），对理解局限性深层根源有限。

（完）
