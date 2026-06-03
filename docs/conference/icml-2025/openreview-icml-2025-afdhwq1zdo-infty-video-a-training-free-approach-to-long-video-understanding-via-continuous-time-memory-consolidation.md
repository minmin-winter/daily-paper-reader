---
title: "$\\infty$-Video: A Training-Free Approach to Long Video Understanding via Continuous-Time Memory Consolidation"
title_zh: ∞-Video：通过连续时间记忆巩固的无训练长视频理解方法
authors: "Saul Santos, António Farinhas, Daniel C McNamee, Andre Martins"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=afDHwQ1ZDO"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 提出基于连续时间记忆的长视频理解方法，实现视频内容的推理
tldr: ∞-Video通过连续时间长期记忆巩固机制，无需额外训练即可处理任意长度视频。该方法通过连续注意力动态聚焦相关视频片段，形成随时间演变的粘性记忆，显著提升了视频语言模型在长视频理解和推理任务上的表现，直接服务于视频内容理解与推理需求。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1729, \"height\": 904, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 775, \"height\": 664, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1388, \"height\": 282, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1537, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1732, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1065, \"height\": 785, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1595, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-afdhwq1zdo/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1747, \"height\": 1067, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-afdhwq1zdo/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 861, \"height\": 538, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-afdhwq1zdo/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 852, \"height\": 368, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-afdhwq1zdo/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1642, \"height\": 670, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-afdhwq1zdo/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1770, \"height\": 236, \"label\": \"Table\"}]"
motivation: 当前视频语言模型受限于有限上下文长度和稀疏帧采样，长视频理解困难。
method: 引入连续时间长期记忆机制，通过连续注意力动态分配细粒度到最相关视频段。
result: 在Video-LLaMA和VideoChat2等模型上验证了长视频推理性能的提升。
conclusion: ∞-Video提供了一种无需训练的长视频理解方案，拓展了多模态推理的能力边界。
---

## Abstract
Current video-language models struggle with long-video understanding due to limited context lengths and reliance on sparse frame subsampling, which often leads to information loss. In this paper, we introduce $\infty$-Video, which is able to process arbitrarily long videos through a continuous-time long-term memory (LTM) consolidation mechanism. Our framework augments video Q-formers by making them able to process unbounded video contexts efficiently and without requiring additional training. Through continuous attention, our approach dynamically allocates higher granularity to the most relevant video segments, forming "sticky" memories which evolve over time. Experiments with Video-LLaMA and VideoChat2 demonstrate improved performance in video question-answering tasks, showcasing the potential of continuous-time LTM mechanisms to enable scalable and training-free comprehension of long videos.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：当前视频语言模型（Video-LLM）受限于固定上下文长度和稀疏帧下采样策略，无法有效处理超长视频（如1小时以上），导致信息丢失和推理能力不足。
- **研究动机**：受人类认知中记忆巩固机制的启发——人类大脑能够动态地将重要情节整合到长期记忆中，且工作记忆模型从“离散槽位”转向“连续共享资源”。作者希望让预训练的短上下文多模态大模型无需额外训练即可处理任意长度的视频。
- **整体含义**：提出一种训练无关（training-free）的框架，通过连续时间长期记忆（LTM）机制，使视频Q-Former能够高效处理无限视频上下文，动态分配更高粒度给最相关的视频片段，形成“粘性记忆”。

## 2. 论文提出的方法论
- **核心思想**：在现有视频Q-Former的交叉注意力中引入连续时间长期记忆（LTM），与原有的短期记忆（STM）加权融合。LTM通过连续注意力（continuous attention）对过去所有视频块的信息进行压缩和巩固，并根据历史注意力密度动态分配采样位置（粘性采样）。
- **关键技术细节**：
  - **连续信号表示**：将离散帧序列通过基函数线性组合转化为连续信号 \( x(t) = B^\top \psi(t) \)，其中系数矩阵 \( B \) 通过岭回归（ridge regression）计算。
  - **连续注意力**：用Gibbs概率密度函数（PDF）替代离散softmax，积分近似期望值作为上下文表示。
  - **记忆巩固（Memory Consolidation）**：每处理一个新视频块时，先“收缩”旧LTM（乘以遗忘因子 \(\tau\)），再拼接新块，重新拟合连续信号，从而实现信息压缩和遗忘。
  - **粘性记忆（Sticky Memories）**：根据历史注意力密度分布（直方图）采样 \( T \) 个位置，使得重要区域获得更多“记忆空间”，类似于大脑中的记忆重放和再巩固。
  - **最终上下文**：输出为 \( Z = \alpha Z_{\text{STM}} + (1-\alpha) Z_{\text{LTM}} \)，其中 \(\alpha\) 平衡长短记忆。对所有视频块输出的视觉token取运行平均（running average）后送入LLM。
- **无需训练**：所有参数（投影矩阵等）继承自预训练模型，仅在前向推理中增加LTM计算。

## 3. 实验设计
- **数据集与场景**：
  - **NeXT-QA**（短视频，44秒平均时长，多项选择）
  - **EgoSchema**（中长视频，3分钟，多项选择）
  - **Video-MME**（超长视频，最长1小时，多项选择）
  - **MovieChat-1K**（长视频，平均8分钟，开放式问答）
- **Benchmark**：对比三类方法：
  1. **基于GPT-4的后端方法**：LLoVi、VideoAgent、VideoTree（需多次调用GPT-4）。
  2. **与∞-Video同架构的训练无关方法**：Video-LLaMA、MovieChat、MovieChat+。
  3. **更强短视频模型**：VideoChat2及其变体。
- **对比方法**：包括ST-LLM、Video-LLaVA、ShareGPT4Video、Chat-UniVi-v1.5、Qwen-VL-Chat等，以及原版Video-LLaMA和VideoChat2。
- **评估指标**：多项选择用准确率；开放问答用GPT-3.5评分（正确性、细节、上下文理解等），以及二元正确判断。

## 4. 资源与算力
- **论文未明确说明GPU型号、数量、训练时长**（因其为训练无关方法，仅需推理计算）。但提到了模型规模：Video-LLaMA使用ViT-G/14（EVA-CLIP）和Vicuna-7B；VideoChat2使用UMT-L和Mistral-7B。所有实验在推理阶段完成，未报告具体耗时或硬件配置。

## 5. 实验数量与充分性
- **实验数量**：在4个数据集上进行了多项选择和开放问答评估，共约7组主实验（包括不同α、不同采样策略、有无LTM的变体）。此外，还进行了消融实验（变化α、基函数数量N、采样方式）和定性分析（注意力密度可视化）。
- **充分性与公平性**：
  - 对比了多种训练无关和训练依赖的方法，涵盖从GPT-4后端到轻量模型。
  - 消融实验系统分析了α和N的影响，验证了粘性采样优于均匀采样。
  - 但存在不足：①Video-LLaMA在Video-MME上表现过差（随机猜测水平）被排除，未提供完整对比；②对于VideoChat2，改进幅度较小（尤其NeXT-QA上几乎持平），作者解释为原模型已经接近饱和，但仍需更多证据；③仅在英伟达硬件上？未报告。

## 6. 论文的主要结论与发现
- **主要结论**：∞-Video通过连续时间LTM巩固机制，能够以训练无关方式将短视频模型扩展到超长视频理解，且在多个数据集上提升显著。
- **关键发现**：
  - 粘性记忆（sticky）普遍优于均匀采样和仅使用STM（α=1），尤其在Video-LLaMA上提升明显（NeXT-QA +3.5%，EgoSchema +6%，MovieChat准确率+4.2%）。
  - 对于原本就较强的VideoChat2，提升幅度有限，但在超长视频（Video-MME）上仍有微弱改进。
  - 单独使用LTM（α=0）效果不如STM+LTM组合，说明长短记忆的加权融合至关重要。
  - 注意力密度图显示粘性记忆能聚焦于关键帧（如重要场景），而均匀记忆则可能浪费资源在无关帧（如片尾字幕）。

## 7. 优点
- **方法创新**：首次将连续注意力机制和粘性采样引入视频Q-Former，模拟人类记忆巩固和重放，具有强生物可解释性。
- **训练无关**：不需额外训练或微调，直接应用于现有预训练模型，节省大量计算资源。
- **单次前向**：只需一次全视频遍历，不依赖问题后回溯，效率高。
- **可扩展性**：理论上可处理任意长度视频，内存开销由基函数数量N决定（而非帧数），具有线性复杂度。
- **实验全面**：覆盖短、中、长多种视频时长，包含多项选择和开放生成，且进行了详细的消融和定性分析。

## 8. 不足与局限
- **实验覆盖**：未在更多视频理解benchmark（如ActivityNet-QA、MSVD-QA）上验证；VideoChat2的改进较小，需更严谨的统计显著性检验。
- **偏差风险**：评估开放问答依赖GPT-3.5打分，可能存在Prompt敏感性和评分偏差；模型本身可能继承预训练数据中的社会偏见。
- **应用限制**：连续信号压缩依赖于基函数选择（矩形函数），可能损失精细时空信息；遗忘因子τ和采样点数T为超参数，需要手动调优，未探索自适应策略。
- **算力未报告**：虽无训练成本，但推理时积分计算（1000个采样点）可能增加延迟，实际部署性能未量化。
- **对比公平性**：与GPT-4后端方法比较时，其调用成本高，但∞-Video为单次轻量推理，直接比较准确率可能忽略成本差异。
- **理论分析**：缺乏对连续注意力近似误差的理论界，以及收敛保证分析。

（完）
