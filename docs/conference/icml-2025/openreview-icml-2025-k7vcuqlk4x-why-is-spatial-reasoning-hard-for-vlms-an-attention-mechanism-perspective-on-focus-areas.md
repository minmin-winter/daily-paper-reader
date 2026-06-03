---
title: Why Is Spatial Reasoning Hard for VLMs? An Attention Mechanism Perspective on Focus Areas
title_zh: 为何空间推理对VLM如此困难？注意力机制视角下的关注区域分析
authors: "Shiqi Chen, Tongyao Zhu, Ruochen Zhou, Jinghan Zhang, Siyang Gao, Juan Carlos Niebles, Mor Geva, Junxian He, Jiajun Wu, Manling Li"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=k7vcuqLK4X"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 分析VLM在空间推理任务中的注意力分配
tldr: 该论文通过机制可解释性视角，深入分析大视觉语言模型在空间推理任务中图像与文本token的注意力交互。研究发现模型对图像和文本的注意力分配存在显著差异，这种不平衡导致了空间推理错误。论文通过追踪中间层注意力分数揭示了错误模式，为理解多模态推理的局限性提供了新见解。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1773, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 790, \"height\": 418, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 699, \"height\": 343, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 511, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1755, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 875, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 850, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1724, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1758, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1758, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1618, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1622, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1572, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1285, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1770, \"height\": 602, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 561, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 580, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 711, \"height\": 336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1762, \"height\": 765, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1765, \"height\": 766, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1765, \"height\": 787, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1772, \"height\": 788, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1764, \"height\": 788, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1765, \"height\": 789, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1584, \"height\": 969, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1819, \"height\": 343, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k7vcuqlk4x/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 516, \"height\": 358, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1770, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 859, \"height\": 532, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 851, \"height\": 419, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 857, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 785, \"height\": 367, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1380, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 860, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 892, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 856, \"height\": 132, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 863, \"height\": 131, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k7vcuqlk4x/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1159, \"height\": 266, \"label\": \"Table\"}]"
motivation: 当前VLM在简单空间推理任务中表现不佳，但内部机制尚不明确。
method: 通过打开模型分析注意力行为，对比图像与文本token的注意力分配。
result: 发现VLM对图像和文本的注意力分配存在显著差异，并观察到错误模式。
conclusion: 注意力不平衡是空间推理困难的重要原因，为改进多模态推理提供了方向。
---

## Abstract
Large Vision Language Models (VLMs) have long struggled with spatial reasoning tasks. Surprisingly, even simple spatial reasoning tasks, such as recognizing “under” or “behind” relationships between only two objects, pose significant challenges for current VLMs. We believe it is crucial to use the lens of mechanism interpretability, opening up the model and diving into model’s internal states to examine the interactions between image and text tokens during spatial reasoning. Our analysis of attention behaviors reveals significant differences in how VLMs allocate attention to image versus text. By tracing the areas of images that receive the highest attention scores throughout intermediate layers, we observe a notable pattern: errors often coincide with attention being misdirected towards irrelevant objects within the image. Moreover, such attention patterns exhibit substantial differences between familiar (e.g., “on the left side of ”) and unfamiliar (e.g.,“in front of ”) spatial relationships. Motivated by these findings, we propose ADAPTVIS based on inference-time confidence scores to sharpen the attention on highly relevant regions when the model exhibits high confidence, while smoothing and broadening the attention window to consider a wider context when confidence is lower. This training-free decoding method shows significant improvement (e.g., up to a 50 absolute point improvement) on spatial reasoning benchmarks such as WhatsUp and VSR with negligible additional cost.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：大型视觉语言模型（VLMs）在空间推理任务中表现严重不足，即使是最简单的双物体空间关系（如“under”“behind”）也难以正确识别。例如，LLaVA将“书在蜡烛后面”错误地描述为“书在蜡烛左边”。
- **研究动机**：现有工作多从视觉编码器（如CLIP）角度分析，但忽略了视觉与文本token在模型内部如何交互以构建几何理解的机制。作者认为，空间推理是研究VLM内部处理视觉信息的理想“透镜”，因为该任务要求同时识别物体并维护几何上下文。
- **整体含义**：揭示VLM内部注意力分配的失衡是空间推理困难的根本原因，并提出无需训练的推理时干预方法，显著提升性能，为理解多模态推理瓶颈提供新视角。

## 2. 论文提出的方法论
### 核心思想
- 通过机制可解释性分析，发现VLM对图像token分配的注意力远少于文本token（图像占序列长度90%却仅获约10%注意力），且简单增加图像注意力无效。关键在于注意力在图像上的**几何分布**：正确回答时注意力聚焦于相关物体，错误时则分散到无关区域。
- 基于模型自身**置信度**（生成概率）动态调整注意力温度：高置信度时锐化分布（强化对当前聚焦区域的关注），低置信度时平滑分布（鼓励探索更广上下文）。

### 关键技术细节
- **S CALING VIS（固定温度缩放）**：对图像token的注意力logits乘以系数α（公式2）。α>1锐化，α<1平滑。在合成数据上α<1更优，真实数据上α>1更优。
- **A DAPT VIS（自适应温度缩放）**：引入置信度阈值β，根据置信度C选择不同系数（公式3）：
  - 若C < β，使用α1<1平滑分布（公式3a）；
  - 若C > β，使用α2>1锐化分布（公式3b）。
- 干预仅作用于最后一个输入token对图像token的注意力，且统一应用于所有层和所有注意力头，避免复杂超参数搜索。

### 算法流程（文字说明）
1. 用模型生成答案，同时记录生成该token的置信度（概率）。
2. 比较置信度与预设阈值β：
   - 若置信度低，对图像注意力logits乘以小于1的系数（如0.5），使分布更均匀；
   - 若置信度高，乘以大于1的系数（如2.0），使分布更尖锐。
3. 重新计算softmax，用调整后的注意力分布生成最终输出。

## 3. 实验设计
### 数据集与场景
- **WhatsUp**：包含合成数据（Controlled A/B：干净背景，两物体）和真实数据（MS COCO和Visual Genome的子集：复杂背景，单/双物体）。每个子集设4或6选项（left/right/on/under/behind/front）。
- **VSR**：1223个image-caption对，布尔标签，改编为QA格式。
- 额外通用基准：POPE（物体幻觉检测）、GQA、TextVQA、VQAv2。

### Benchmark与对比方法
- 主要模型：LLaVA-1.5、LLaVA-1.6，附录还包括Qwen2-VL。
- 对比基线：
  - 贪心解码（基线）
  - VCD（视觉对比解码）
  - DoLa（对比层输出）
  - S CALING VIS（固定温度缩放）
  - A DAPT VIS（自适应温度缩放）

### 评估指标
- 准确率（Exact Match）、Pair Accuracy（成对图像均正确）、Set Accuracy（一组四个方向均正确）、F1分数（VSR）。

## 4. 资源与算力
- 论文未明确说明使用的GPU型号、数量或训练时长。由于A DAPT VIS是推理时方法（training-free），不涉及训练阶段。
- 附录E.9提供了推理时间对比：S CALING VIS仅增加约2%时间，A DAPT VIS增加约64%时间（因需计算阈值）。

## 5. 实验数量与充分性
- **主要实验**：表1（WhatsUp 6个子集，2种模型，对比4种方法）、表2（VSR，2种模型，对比4种方法）。
- **消融与鲁棒性**：
  - 不同α/β选择（附录E.3）；
  - OOD测试：将Controlled A/B上优化的超参数应用到COCO子集，仍有效（附录表8）；
  - Prompt敏感性：改变选项数量（2/6选项），方法仍稳定（附录图27）；
  - Reverse curse测试：交换问题中物体顺序，性能下降但方法仍能改善（附录图28）。
- **其他模型验证**：Qwen2-VL上一致提升（附录表3、4、6）。
- **通用任务测试**：POPE、GQA、TextVQA上轻微正向或持平（附录表10）。
- **注意力分析**：AUROC、熵、偏度等额外可视化（附录E.5、E.4）。

**充分性评价**：实验覆盖多种数据集（合成/真实）、多种模型（LLaVA-1.5/1.6、Qwen2-VL）、多种基线，并包含消融、鲁棒性、通用测试，设计较为全面客观。但未对比更多最新VLM（如GPT-4V）且主要聚焦于LLaVA系列，可能存在一定选择性偏差。

## 6. 论文的主要结论与发现
1. **注意力分配严重失衡**：图像token占输入序列长度约90%，但仅获约10%注意力；文本token获取约90%注意力。
2. **注意力位置比数量更重要**：简单提升所有图像注意力无效，正确执行空间推理需要注意力对准物体位置。
3. **中间层是处理关键**：AUROC分析显示中间层（如17-18层）注意力与物体标注重叠度最高，是信息处理核心。
4. **置信度可指示注意力可靠性**：模型对熟悉关系（如“left/right”）置信度更高，正确率也更高；对不熟悉关系（如“behind”）置信度低，错误多。
5. **A DAPT VIS显著提升**：在WhatsUp上最高提升50个绝对百分点，在VSR上F1提升达11.2%。且在合成和真实数据上均有效。

## 7. 优点
- **机制可解释性深度**：首次从注意力分布几何角度系统分析VLM空间推理失败原因，提供清晰内部机理。
- **方法简洁高效**：基于置信度的推理时干预，无需训练、无需额外数据或模型修改，仅微调推理过程。
- **结果显著**：在多个基准上取得大幅提升（如Controlled A从60.3%升至84.9%），且计算开销极小（仅推理时间增加2-64%）。
- **泛化性好**：在LLaVA-1.5/1.6、Qwen2-VL上均有效，在通用QA任务上也不减性能。
- **实验设计周全**：包括消融、鲁棒性、OOD测试、逆向提示、多选项数量，验证了方法的稳健性。

## 8. 不足与局限
- **依赖验证集调参**：α和β需要根据验证集选择，无法完全免调参，且不同分布可能需要不同参数。
- **仅解决模型端问题**：无法处理视觉编码器（如CLIP）本身对空间信息的错误编码（如Tong et al.指出的CLIP局限）。
- **数据集偏差**：真实数据中“left/right”占比远高于其他关系，模型已训练先验，可能高估提升的有效性。
- **未与最强VLM对比**：实验主要基于开源模型（LLaVA、Qwen2-VL），未评估GPT-4V等商业闭源模型。
- **通用任务提升有限**：在POPE、GQA等非空间任务上仅轻微提升甚至持平，说明方法专为空间推理设计，通用性有限。
- **置信度定义简单**：仅使用生成概率作为置信度，可能受输出格式影响（如多选项分布），未探索更复杂的不确定性估计方法。

（完）
