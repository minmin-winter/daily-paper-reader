---
title: LLMs can see and hear without any training
title_zh: LLM无需训练即可看和听
authors: "Kumar Ashutosh, Yossi Gandelsman, Xinlei Chen, Ishan Misra, Rohit Girdhar"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=cJeFULIiot"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 无训练多模态迭代推理赋予LLM视觉和音频能力
tldr: 传统多模态模型需要专门训练。MILS提出一种无需训练的迭代推理方法，利用LLM自身多步推理能力，生成候选输出并迭代评分，最终解决多模态任务。在零样本图像、视频和音频字幕任务上取得新最优结果，且可扩展到媒体生成。该方法展示了利用现有LLM进行多模态推理的潜力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 751, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 848, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 838, \"height\": 254, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 855, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 851, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 839, \"height\": 535, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1767, \"height\": 511, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 847, \"height\": 265, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 516, \"height\": 308, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1750, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 799, \"height\": 631, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 802, \"height\": 885, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1760, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cjefuliiot/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 854, \"height\": 525, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-cjefuliiot/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 861, \"height\": 291, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cjefuliiot/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 860, \"height\": 154, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cjefuliiot/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 860, \"height\": 139, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cjefuliiot/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 853, \"height\": 754, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cjefuliiot/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 892, \"height\": 276, \"label\": \"Table\"}]"
motivation: 现有方法需要为每个多模态任务训练专门模型，成本高且泛化差。
method: 提出MILS，通过迭代提示LLM生成候选并评分，以无梯度优化的方式完成多模态任务。
result: 在零样本图像、视频、音频字幕上达到新最优，且适用于媒体生成。
conclusion: 利用LLM自身的推理能力可有效实现多模态理解和生成，无需额外训练。
---

## Abstract
We present MILS: Multimodal Iterative LLM Solver, a surprisingly simple, training-free approach, to imbue multimodal capabilities into
your favorite LLM. Leveraging their innate ability to perform multi-step reasoning, MILS prompts the LLM to generate candidate outputs, each of which are scored and fed back iteratively, eventually generating a solution to the task. This enables various applications that typically require training specialized models on task-specific data. In particular, we establish a new state-of-the-art on emergent zero-shot image, video and audio captioning. MILS seamlessly applies to media generation as well, discovering prompt rewrites to improve text-to-image generation, and even edit prompts for style transfer! Finally, being a gradient-free optimization approach, MILS can invert multimodal embeddings into text, enabling applications like cross-modal arithmetic.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：当前多模态理解与生成任务（如图像、视频、音频字幕、文本到图像生成等）通常需要为每个具体任务训练专门的模型，依赖大量带标注数据。即使所谓的“零样本”方法，也往往在任务特定数据上进行了训练或微调。作者希望探索一种更通用的、无需任何任务特定训练的解决方案，仅利用现有大语言模型（LLM）的推理能力，使其“看”和“听”。
- **核心问题**：如何在不经过任何显式多模态训练的情况下，让LLM完成图像、视频、音频等不同模态的理解与生成任务，同时保持简单性和泛化性。
- **意义**：提出一种训练自由的推理时优化框架MILS（Multimodal Iterative LLM Solver），将LLM视为“生成器”，结合现成的多模态“评分器”，通过迭代优化实现零样本多模态能力，为未来构建更通用、更灵活的AI系统提供了新思路。

## 2. 方法论：核心思想、关键技术细节
- **核心思想**：利用LLM固有的多步推理能力，通过迭代生成候选输出、评分、反馈，逐步逼近任务最优解。整个过程无需梯度计算，完全基于推理时优化。
- **关键技术细节**：
  - **Generator**：通常是一个LLM（文中主要使用Llama 3.1 8B），接收任务描述和上一轮评分反馈，生成新的候选文本（如字幕、提示词等）。对于图像生成任务，Generator可串联LLM与文本到图像模型（如LDM、FLUX）。
  - **Scorer**：一个现成的多模态模型，用于计算候选输出与测试样本之间的相似度或质量分数。例如，图像字幕使用SigLIP计算图像-文本相似度；音频字幕使用ImageBind；图像生成使用PickScore评估人类偏好。
  - **迭代优化流程**：
    1. 初始化候选集（可选，用于字幕任务：从LLM生成30K-50K条通用描述）。
    2. 对每轮，Generator基于当前候选集及其分数（格式化后的文本提示）生成新候选。
    3. Scorer给所有候选评分，保留Top-K并反馈给Generator。
    4. 重复N步（通常10-20步）直至收敛，输出最终结果。
  - **无梯度优化**：与以往基于梯度的零样本方法（如ZeroCap）不同，MILS完全避免反向传播，因此可以轻松扩展到需要离散输出或非可微生成过程的任务（如文本到图像生成、风格迁移）。

## 3. 实验设计
- **数据集与场景**：
  - 图像字幕：MSCOCO Karpathy测试集（5,000张图）。
  - 视频字幕：MSR-VTT（2,990个视频，10-30秒）。
  - 音频字幕：Clotho（音频字幕数据集）。
  - 图像生成：DrawBench（200个提示词），进行人工评估。
  - 风格迁移：自定义图像对，使用Gram矩阵距离。
  - 跨模态算术：结合图像和音频描述生成新图像。
- **基准与对比方法**：
  - 图像字幕：ZeroCap、ConZIC、CLIPRe、MeaCap（含TensorFlow版本）。
  - 视频字幕：Nagrani等（HowTo100M和VideoCC3M训练）。
  - 音频字幕：ZerAuCap。
  - 图像生成：对比原始T2I模型（LDM和FLUX.1 [schnell]）以及MILS增强版本，人工评估质量和文本忠实度。
- **评估指标**：自动指标（BLEU-4、CIDEr、METEOR、SPICE、CLIP相似度、PickScore）和人工评估（Amazon Mechanical Turk，按JUICE协议进行偏好对比）。

## 4. 资源与算力
- **文中未明确说明**：论文未提供具体使用的GPU型号、数量或训练时长（因为MILS是训练无关的，仅有推理时间开销）。作者仅提到使用Llama 3.1 8B、SigLIP等现成模型，并指出优化过程需要多次调用LLM和Scorer，但未详细报告计算成本。实验所用的GPU和耗时属于隐含信息，不具备可复现的详细数值。

## 5. 实验数量与充分性
- **实验数量丰富**：覆盖三大模态（图像、视频、音频）和三类任务（字幕、生成、编辑），包含跨模态算术这一新颖应用。每个任务均有定量对比和定性示例。
- **消融实验充分**：
  - 优化步数的影响（图9）：SCORER输出和下游指标均随步骤改善。
  - 初始候选集大小的影响（图10）：越大越好。
  - Generator和Scorer规模的影响（图12）：更大模型带来更好性能。
  - 不同LLM作为Generator的比较（图16）：Llama 3.1 8B最优，Mistral和Gemma也有效。
  - 不同Scorer（CLIP变体）的比较（表4）：SigLIP最佳。
- **客观性与公平性**：
  - 图像生成使用人工评估，避免了自动指标的偏差，并采用JUICE协议，每组由三人投票。
  - 字幕任务在标准公开数据集上评估，对比方法为官方开源代码或论文报告结果，部分对比（如MeaCap）作者自行运行了代码。
  - 但视频和音频字幕的对比基线较少，且MILS的初始候选集使用了ImageNet/AudioSet类别，可能带来不公平优势？作者在消融中确认了初始集大小的积极影响，但未与完全无初始集的版本对比。

## 6. 主要结论与发现
- MILS在无需任何任务特定训练的情况下，在零样本图像、视频、音频字幕任务上达到或超越了现有专门方法，如MeaCap、Nagrani等，尤其在语义感知指标（METEOR、SPICE）上表现突出。
- 该框架可无缝扩展到文本到图像生成，自动优化提示词，显著提升生成质量（人工评测中MILS增强版比原始模型胜率62%-79%）。
- 支持风格转移和跨模态算术等新颖应用，展现出强大的泛化能力。
- 实验表明MILS的性能随Generator/Scorer规模、初始候选集大小和迭代步数增加而提升，表明其依赖高质量组件但无需训练。

## 7. 优点
- **训练免费**：完全不需要对任何模型进行微调或训练，降低计算和标注成本。
- **通用性极强**：同一框架可处理图像、视频、音频等多种模态，以及理解、生成、编辑等多种任务，仅需更换Generator和Scorer。
- **无梯度优化**：避免了对复杂生成模型（如扩散模型）反向传播的需求，使得应用于文本到图像、视频生成等非可微任务成为可能。
- **简单直观**：代码实现简单，易于复现和扩展（代码已开源）。
- **与现有模型协同**：随着LLM和多模态模型的进步，MILS的性能可自然提升，无需重新设计。

## 8. 不足与局限
- **性能上界受限于组件能力**：MILS依赖Generator的多样性生成和Scorer的准确反馈。若Scorer对某些细粒度属性（如颜色、空间关系）不敏感，或LLM无法提出有效候选，则性能受限。
- **推理效率低**：每步需要多次调用LLM和Scorer，迭代10-20步，导致推理时开销较大。未来可通过更高效的LLM或推理策略改进。
- **初始候选集依赖性**：字幕任务需要大量预生成的候选描述（30K-50K），这本身可能包含来自训练数据的知识，且生成候选集也使用了LLM和类别标签，存在一定的数据依赖性。
- **评估局限性**：
  - 视频和音频字幕实验对比基线较少（仅与1-2个方法比较），且未与当前更先进的视频LLM（如Video-LLaMA）对比（因为那些方法是非零样本的）。
  - 在图像生成中仅使用DrawBench（200个提示）评估，规模较小；人工评估虽然严格但仍可能受主观偏好影响。
- **潜在偏差**：使用的LLM和Scorer本身可能存在社会偏见（如对特定物体、场景的描述偏向），MILS继承了这些偏差，且文中未做专门分析。
- **缺少对失败案例的深入分析**：论文未讨论何时MILS会失败（如Scorer评分失效、LLM产生重复或无关候选等）。

（完）
