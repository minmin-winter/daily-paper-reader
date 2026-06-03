---
title: "CoMemo: LVLMs Need Image Context with Image Memory"
title_zh: CoMemo：视觉语言模型需要图像上下文与图像记忆
authors: "Shi Liu, Weijie Su, Xizhou Zhu, Wenhai Wang, Jifeng Dai"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Hw6MDsaor9"
tags: ["query:mm-reasoning"]
score: 7.0
evidence: 双路径架构缓解视觉语言模型中的注意力不平衡
tldr: 本文指出现有大型视觉语言模型存在两个子优问题：随着上下文增长中间视觉内容被逐渐忽略，以及传统位置编码无法保持2D结构。为此提出CoMemo双路径架构，通过上下文图像路径和图像记忆路径并行处理视觉信息，有效缓解了注意力分配不均和结构信息丢失问题。实验表明CoMemo提升了模型在多种视觉语言任务上的表现。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-hw6mdsaor9/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1759, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hw6mdsaor9/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 828, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hw6mdsaor9/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 858, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hw6mdsaor9/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 852, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hw6mdsaor9/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1186, \"height\": 604, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-hw6mdsaor9/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 840, \"height\": 539, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1772, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 863, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 860, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 859, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 860, \"height\": 159, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 861, \"height\": 144, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1769, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1242, \"height\": 697, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1633, \"height\": 648, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1724, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-hw6mdsaor9/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1840, \"height\": 1267, \"label\": \"Table\"}]"
motivation: LVLMs存在视觉内容注意力分配不均和2D位置编码不足的问题。
method: 提出双路径架构CoMemo，包含上下文图像路径和图像记忆路径以改进视觉特征处理。
result: 在多个LVLM基准上，CoMemo显著提升了视觉语言任务的性能。
conclusion: 双路径视觉处理机制有效解决了LVLM中的注意力偏差和结构感知缺陷。
---

## Abstract
Recent advancements in Large Vision-Language Models built upon Large Language Models have established aligning visual features with LLM representations as the dominant paradigm. 
However, inherited LLM architectural designs introduce suboptimal characteristics for multimodal processing. 
First, LVLMs exhibit a bimodal distribution in attention allocation, leading to the progressive neglect of middle visual content as context expands. 
Second, conventional positional encoding schemes fail to preserve vital 2D structural relationships when processing dynamic high-resolution images. 
To address these limitations, we propose **CoMemo** - a dual-path architecture that combines a **Co**ntext image path with an image **Memo**ry path for visual processing, effectively alleviating visual information neglect. 
Additionally, we introduce RoPE-DHR, a novel positional encoding mechanism that employs thumbnail-based positional aggregation to maintain 2D spatial awareness while mitigating remote decay in extended sequences. 
Evaluations across seven benchmarks,including long-context comprehension, multi-image reasoning, and visual question answering, demonstrate CoMemo's superior performance compared to conventional LVLM architectures.
Project page is available at [https://lalbj.github.io/projects/CoMemo/](https://lalbj.github.io/projects/CoMemo/).

---

## 论文详细总结（自动生成）

### 论文总结：CoMemo: LVLMs Need Image Context with Image Memory

#### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：现有大型视觉语言模型（LVLMs）在继承大语言模型（LLMs）架构时表现出两个子优特性：
  1. **注意力分布双峰性**：因果自注意力机制导致模型倾向于关注序列首尾的 token，而中间位置的视觉内容（尤其是多张图像或高分辨率切片）被逐渐忽略，即“lost in the middle”现象。
  2. **位置编码失效**：传统的RoPE位置编码在动态高分辨率（DHR）场景下，因 token 数量激增而产生严重的远程衰减（remote decay），且一维增量编码无法保留图像的二维空间结构关系。
- **整体含义**：上述问题限制了 LVLMs 在长上下文理解、多图像推理、长文本生成等任务中的性能。论文提出了一种新型双路径架构 **CoMemo** 来缓解视觉信息被忽视的问题，并通过 **RoPE-DHR** 位置编码机制保持二维空间感知并抑制远程衰减，从而提升模型在多模态任务上的综合表现。

#### 2. 论文提出的方法论：核心思想、关键技术细节、算法流程
- **核心思想**：引入一个不受上下文长度影响的额外图像处理路径（记忆路径），与原有的全自回归路径（上下文路径）并行处理视觉特征，使模型在生成过程中始终能访问到完整的图像信息。
- **关键技术细节**：
  - **双路径架构**：
    - **上下文路径（Context Path）**：与 LLaVA 类似，将图像 token 与文本 token 拼接作为输入序列进行全自回归处理，作为主要的图像上下文引入方式。
    - **记忆路径（Memory Path）**：通过交叉注意力（跨模态注意力）机制，将图像 token 作为“记忆”与输入序列的隐藏状态交互。该路径在解码时只需单步计算当前 token 与缓存的视觉记忆，不增加 KV cache 长度。
  - **RoPE-DHR 位置编码**：
    - 针对动态高分辨率（DHR）场景，将图像缩略图（thumbnail）的 patch token 分配连续位置 ID，然后将高分辨率子图（tiles）的 patch 根据其二维坐标映射到缩略图对应的 patch 索引上（公式 (2)）。
    - 实现方法：`ithumb = (floor(xtile * Wtile / Worig) + wb_tile, floor(ytile * Htile / Hthumb) + hb_tile)`。
    - 效果：压缩位置编码长度（减轻远程衰减），同时保留二维几何关系。
  - **记忆混合策略（Memory Mixin Strategy）**：交叉注意力层间置于标准 Transformer 块（比例 1:4），并引入门控机制（`tanh(attn_gate)` 和 `tanh(ffw_gate)`) 调节视觉影响的强度。
  - **三阶段训练策略**：
    - 阶段1：训练投影器（projector）和混合层参数。
    - 阶段2：冻结门控参数，继续训练其余参数，防止模型过度依赖记忆路径。
    - 阶段3：全参数微调（SFT），训练目标转向指令跟随。

#### 3. 实验设计：数据集、基准、对比方法
- **数据集与基准**（7类任务）：
  - **Caption**：COCO、Flickr30k、No-Caps（CIDEr 评分）。
  - **Long-Generation**：LLaVABench（单图）、MMDU（多图+长文本）。
  - **Multi-Image**：BLINK、Mantis、MMT。
  - **Long-Context**：MM-NIAH（文本/图像 needle）、MileBench。
  - **Math**：MathVista、MathVision。
  - **General VQA**：MMBench、MME、MMVP、AI2D。
  - **OCR-Related**：ChartQA、TextVQA。
- **对比方法**：
  - **LVLM-S**（全自回归）：InternVL-2、InternVL-2.5、Qwen2-VL、MiniCPM-V-2。
  - **LVLM-X**（交叉注意力）：mPlug-owl3、LLama3.2-V。
  - **CoMemo**（本文方法）：使用相同的 LLM 骨干（InternLM-1.8B / InternLM-7B）和图像编码器（InternViT-300M），保证公平对比。
  - 额外对比闭源模型：GPT-4o、GPT-4V（作为参考）。

#### 4. 资源与算力
- **训练资源**：论文在 Table 5 中报告了训练效率，使用 **64块 NVIDIA A100 GPU**，batch size = 1024。预训练阶段共 4000 步（Phase1 2000步 + Phase2 2000步），微调阶段 9000 步。**未明确说明总训练时长**，但给出了每步训练时间（0.096 秒/步，即约 12.26 samples/s），可估算总时间约为 (4000+9000) * 0.096 ≈ 1248 秒 ≈ 0.35 小时，但这是单步时间，实际多 GPU 并行下可能更快。需要指出论文未提供具体的 GPU 小时数。

#### 5. 实验数量与充分性
- **实验数量**：论文进行了多组实验：
  - **主表对比**（Table 1）：在 7 类任务、18 个具体基准上与 10 余个模型对比，涵盖不同架构和规模。
  - **分表详细对比**（Table 2-4）：在生成/数学、多图/长上下文、通用VQA/OCR 三类上分别对比三种架构（LVLM-X, LVLM-S, CoMemo）。
  - **效率对比**（Table 5-6）：训练和推理速度比较。
  - **消融实验**（Table 7）：9 个变体，包括组件消融（memory、RoPE-DHR）、压缩率、模型规模（2B vs 8B）、数据集切换。
  - **额外分析**：注意力热力图可视化（Figure 8）、平衡实验（Figure 5）等。
- **充分性与公平性**：实验覆盖全面，控制变量严格（相同数据、骨干、超参）。消融实验清晰分离了各个模块的贡献。在多种任务上均表现一致提升，结论可信。但未涉及更大规模模型（如 13B+）的验证。

#### 6. 论文的主要结论与发现
- **主要结论**：
  1. CoMemo 双路径架构有效缓解了 LVLMs 对中间视觉内容的忽视问题，在长上下文和多图像任务上显著优于传统 LVLM-S 和 LVLM-X 架构。
  2. RoPE-DHR 位置编码通过缩略图位置聚合，压缩了位置长度并保留了二维结构，减轻了远程衰减，在长上下文和生成任务（Caption、MMDU）上提升明显。
  3. 三阶段训练策略平衡了双路径依赖，防止模型过度偏向记忆路径。
  4. CoMemo 在大多数基准上达到或超越同规模开源模型，尤其在 Caption（+17.2%）、Long-Generation（+7.0%）、Long-Context（+5.6%）任务上表现出色。
- **关键发现**：
  - “Lost in the middle”源于因果自注意力机制；RoPE 远程衰减因 DHR 加剧。
  - 记忆路径若不加以平衡会导致模型过度依赖交叉注意力；冻结门控参数可有效抑制。

#### 7. 优点：方法或实验设计上的亮点
- **方法亮点**：
  - 双路径设计直观地解决了注意力偏差，无需修改 LLM 内部机制，兼容现有 LLaVA 变体。
  - RoPE-DHR 简单高效，仅通过位置映射实现二维感知且不增加计算量。
  - 三阶段训练策略针对性地解决了路径不平衡问题，设计精巧。
- **实验亮点**：
  - 采用相同骨干、数据集、超参进行公平对比，排除其他因素干扰。
  - 覆盖 7 大类任务、18 个基准，评估维度全面（生成、理解、数学、OCR、长上下文等）。
  - 包含详尽的消融（组件、压缩率、规模、数据集），验证了每个设计的必要性。
  - 公开训练效率和推理速度，便于实际部署评估。

#### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等
- **实验覆盖**：
  - 仅验证 2B 和 8B 两种规模，缺乏更大模型（如 13B/70B）上的表现，可能无法充分展示方法在更大参数量下的泛化性。
  - 未在视频理解、3D 等更复杂多模态任务上测试。
  - 仅在 InternLM+InternViT 框架上验证，未在 LLaMA+CLIP 等其他流行组合上复现。
- **偏差风险**：
  - 训练数据来源于 InternVL-2 的公开数据，可能存在数据泄露风险（部分基准可能已包含在训练集中）。
  - OCR 任务上 CoMemo 略低于 LVLM-S（Table 4：ChartQA 73.6 vs 75.6，TextVQA 72.6 vs 74.2），说明压缩位置编码可能损失细粒度绝对位置信息，不适用于强依赖 OCR 的场景。
- **应用限制**：
  - 双路径架构在训练时需要更多的显存和计算（对比 LVLM-S 训练速度下降约 8.5%），推理时也略慢（约 10-20%），在资源受限场景下可能需要权衡。
  - RoPE-DHR 的映射假设缩略图与子图具有严格的几何对应，对于不规则切割或非矩形图像布局可能不适用。
  - 三阶段训练需要手动调节冻结时机，引入额外超参数。

（完）
