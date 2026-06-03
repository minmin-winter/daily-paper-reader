---
title: Learning Vision and Language Concepts for Controllable Image Generation
title_zh: 面向可控图像生成的视觉与语言概念学习
authors: "Shaoan Xie, Lingjing Kong, Yujia Zheng, Zeyu Tang, Eric P. Xing, Guangyi Chen, Kun Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=hUHRTaTfvZ"
tags: ["query:native-multi"]
score: 4.0
evidence: 学习可识别的多模态概念对齐
tldr: 本文建立了从多模态分布中学习原子概念及其交互的理论条件，通过将概念学习建模为隐变量识别问题，并利用图模型指定模态间交互，提供了可识别性保证。该工作为多模态表征对齐奠定了理论基础。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 369, \"height\": 360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1759, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1772, \"height\": 1170, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 819, \"height\": 563, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 756, \"height\": 485, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1477, \"height\": 1869, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1666, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1653, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1823, \"height\": 1947, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1791, \"height\": 1202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-huhrtatfvz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1699, \"height\": 2026, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-huhrtatfvz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 856, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-huhrtatfvz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 827, \"height\": 508, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-huhrtatfvz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 906, \"height\": 202, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-huhrtatfvz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 981, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-huhrtatfvz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 991, \"height\": 201, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-huhrtatfvz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 836, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-huhrtatfvz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1587, \"height\": 464, \"label\": \"Table\"}]"
motivation: 从多模态数据中学习原子概念及其交互的理论基础尚不明确。
method: 将概念学习建模为隐变量识别问题，用图模型表示模态间交互，并证明可识别性条件。
result: 理论分析确认了可识别性条件，实验验证了所学概念的可解释性和下游任务有效性。
conclusion: 该工作为多模态概念学习提供了坚实的理论基础和算法保障。
---

## Abstract
Concept learning seeks to extract semantic and interpretable representations of atomic concepts from high-dimensional data such as images and text, which can be instrumental to a variety of downstream tasks (e.g., image generation/editing). Despite its importance, the theoretical foundations for learning atomic concepts and their interactions, especially from multimodal distributions, remain underexplored.
In this work, we establish fundamental conditions for learning atomic multimodal concepts and their underlying interactions With identfiability guarantees. We formulate concept learning as a latent variable identification problem, representing atomic concepts in each modality as latent variables, with a graphical model to specify their interactions across modalities. Our theoretical contribution is to provide component-wise identifiability of atomic concepts under flexible, nonparametric conditions that accommodate both continuous and discrete modalities.  Building on these theoretical insights, we demonstrate the practical utility of our theory in a downstream task text-to-image (T2I) generation. We develop a principled T2I model that explicitly learns atomic textual and visual concepts with sparse connections between them, allowing us to achieve image generation and editing at the atomic concept level. Empirical evaluations show that our model outperforms existing methods in T2I generation tasks, offering superior controllability and interpretability.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：从多模态数据（文本-图像对）中学习“原子概念”（atomic concepts）及其交互作用，是可控图像生成（如局部编辑）的关键。然而，现有方法缺乏理论保证，导致概念纠缠和模态错位，使得文本修改常引发图像中非预期的全局变化。
- **动机**：尽管因果表征学习在单模态场景下已有进展，但针对多模态分布中原子概念的**组件级可识别性**（component-wise identifiability）的理论尚不完善。现有工作要么仅实现块级可识别性（只能区分共享表示块），要么依赖半参数假设（如指数族、加性因果），或无法处理离散变量。
- **目标**：建立**非参数、支持连续与离散变量**的可识别性条件，并据此设计一个原理驱动的可控文本到图像生成模型。

## 2. 方法论

### 核心思想
将概念学习建模为隐变量识别问题。假设：
- 文本 `t` 由离散原子文本概念 `zT ∈ N^(d(zT))` 经可逆映射 `gT` 生成；
- 图像 `i` 由连续原子视觉概念 `zI ∈ R^(d(zI))` 经可逆光滑映射 `gI` 生成；
- `zI` 以稀疏方式条件依赖于 `zT`（由二分图 `Gt→i` 描述），即 `zI ~ p(zI|zT)` 且 `zI` 各分量在给定 `zT` 下条件独立。

### 两步可识别性理论
1. **视觉概念识别（Condition 4.2）**：
   - 利用 `zT` 通过 `t` 的变化充分改变 `p(zI|zT)`（足够变异性条件），可证明 `zI` 各分量可被组件级识别。
   - 所需条件包括：`gT,gI` 可逆光滑、条件密度光滑正定、`zI` 给定 `zT` 下条件独立、存在 `2d(zI)+1` 个不同 `zT` 值使某向量组线性无关。
2. **文本概念识别（Condition 4.3）**：
   - 在 `zI` 已识别的基础上，利用文本概念 `zT` 到视觉概念 `zI` 的**稀疏连接**（非子集观测子节点条件），可识别 `zT` 各分量及二分图 `Gt→i`。
   - 辅助条件包括非退化、无双胞胎变量、极大性等，源自离散隐变量识别文献。

**Theorem 4.4**：在上述条件下，`zT` 和 `zI` 均可组件级识别（即每个原子概念可被唯一恢复，仅允许置换和可逆变换），且图 `Gt→i` 可恢复。

### 模型设计：ConceptAligner
- **文本网络 `RT`**：用预训练文本嵌入 + perceive-resampler 提取 `zT`（预设64个维度）。
- **图像网络 `RI`**：用SigLIP图像嵌入 + transformer 输出高斯参数 `μ,σ`，采样外生变量 `ϵ`（重参数化）。
- **概念网络 `RC`**：将 `zT` 与可学习稀疏掩码 `m` 相乘后，与 `ϵ` 结合生成 `zI`（`zI = RC(zT ⊙ m, ϵ)`）。
- **条件生成 `vθ`**：扩散transformer以 `zI` 为条件进行去噪。
- **损失函数**：
  - 扩散损失 `L_diff`：匹配噪声预测。
  - KL散度 `L_kl`：正则化 `ϵ` 接近标准正态。
  - 稀疏正则化 `L_spa = ||m||_1`：促进 `zT→zI` 稀疏连接。
  - 总损失：`L = L_diff + λ_spa L_spa + λ_kl L_kl`。

## 3. 实验设计

### 数据集
- **训练数据**：使用 FLUX-S 基于 LAION 提示生成200万张图像，再通过 QWEN2-VL 生成准确文本描述。
- **评估数据集**：
  - **Emu-Edit**：3589对提示词，覆盖7种图像编辑类型，用于可控生成对比。
  - **PIE-Bench**：标准图像编辑基准，含源/目标提示对。
  - **自定义解缠分析集**：用ChatGPT生成10个动物名×10个动作，共100组提示对，重复10种子，得1000对。

### 对比方法
- **T2I生成**：SD3.5-M/L、FLUX-S/D、SANA、SANA-Finetune（在训练数据上微调）。
- **真实图像编辑**：BlendedDiffusion、Pix2pix-zero、Plug-and-Play、PnpInv、LEDITS-SDXL、RF-Inversion、Fireflow-FLUX、Instruct-Pix2pix等。

### 评价指标
- **图像对相似度**：CLIP图像相似度（CLIP-I）、LPIPS（越低越好）、DINO相似度。
- **文本-图像对齐**：CLIP文本-图像相似度（CLIP-T）。
- **解缠能力**：用Qwen2.5-VL评估主题一致性（subject consistency）和提示一致性（prompt consistency）。

## 4. 资源与算力

- **文中未明确说明具体的GPU型号、数量及训练耗时。** 仅提及：
  - 使用LoRA调整扩散transformer，rank=256。
  - batch size=768，学习率5e-5。
  - 其他轻量网络（RT、RI、RC）各包含6个注意力块。
- **推理效率**：在H100 GPU上，ConceptAligner单张图像生成0.48秒，快于SANA（0.58秒）等基线。

## 5. 实验数量与充分性

### 实验组数
| 实验类型 | 数量/组 | 示例 |
|----------|---------|------|
| T2I可控生成对比（Emu-Edit） | 1组（Table 2） | 7个基线 + 4个消融 |
| T2I可控生成对比（PIE-Bench） | 2组（Table 4,5） | 常规提示 & 长提示扩展 |
| 消融实验 | 3组（Table 2, Figure 5,6） | 移除稀疏、扩散损失、KL损失 |
| 多概念编辑 | 定性（Figure 8） | 2/3/4个概念同时编辑 |
| 真实图像编辑 | 1组（Table 7） | 9个基线对比，含配对/非配对方法 |
| 解缠分析 | 1组（Table 3, Figure 9） | 1000对生成，自动化评估 |
| 概念可视化 | 定性（Figure 4） | 插值概念生成图像 |

### 充分性与客观性
- **优点**：对比了当前主流开源/闭源T2I模型，包含多种规模（SD3.5-M/L、FLUX-S/D、SANA）及精调版本。消融覆盖理论关键组件（稀疏性、扩散、KL）。解缠分析用自动化LLM评估减少主观偏差。使用多种客观指标（CLIP-I/DINO/LPIPS/CLIP-T）。
- **可改进**：训练数据为合成（FLUX-S生成、QWEN2-VL描述），可能引入分布偏差；缺乏对真实拍摄图像的可控生成评估（仅在真实图像编辑任务中评估，但面向的是图像编辑而非从头生成）。指标未涉及人工评估（user study）。长提示实验仅有SANA系列对比，范围较窄。

## 6. 主要结论与发现

1. **理论贡献**：首次在非参数设定下，为多模态（连续+离散）原子概念学习提供了**组件级可识别性**保证，且不依赖特定参数形式。
2. **模型有效性**：ConceptAligner在所有可控生成指标上**显著超越现有基线**（如CLIP-I达0.903，DINO达0.835），同时生成速度最快。
3. **稀疏连接是关键**：消融表明，移除稀疏正则化会导致编辑时产生不必要的图像变化，验证了理论中稀疏图对于识别文本概念的必要性。
4. **可解释性**：通过概念网络可分解出独立的视觉元素（如“蝙蝠侠披风”、“孔雀形状”），支持定向替换而不影响其他属性。
5. **多概念编辑**：模型可同时处理至多4个概念编辑，且保持目标一致性。

## 7. 优点

- **理论严谨性**：首次将多模态概念学习的可识别性推进到组件级，且条件在实际中大致可满足（数据集多样、稀疏性自然）。
- **原理驱动的设计**：模型组件（稀疏掩码、条件独立、外生变量）直接对应理论条件，而非启发式。
- **全面的公平对比**：涵盖主流T2I模型（SD3.5、FLUX、SANA）并增加微调基线，结果可靠。
- **高效推理**：通过压缩条件表示（64 tokens vs SANA的300 tokens）实现最快生成速度。
- **丰富消融**：验证稀疏性、扩散损失、KL损失各自作用，支撑理论假设。

## 8. 不足与局限

- **理论条件验证不充分**：Condition 4.2-iv的“足够变化性”虽理论上合理，但实验中未量化验证数据集是否满足；若caption质量低（如过短或缺失），可识别性可能失效。
- **训练数据依赖合成**：200万张图像由FLUX-S生成，描述由QWEN2-VL生成，未使用真实拍摄图像-描述对。这可能导致模型偏向FLUX-S的生成分布，影响对真实世界分布的泛化。
- **计算资源未透明**：未报告GPU型号、数量及训练时长，不利于复现和成本评估。
- **评估指标局限**：主要依赖Embedding相似度（CLIP/DINO/LPIPS），缺乏人工感知评估（如用户对编辑质量的投票）；CLIP-T在部分实验中变化微小（如0.314 vs 0.318），区分度不足。
- **离散文本概念表示**：文本概念zT被设计为可微的连续向量（通过perceive-resampler输出），但理论上为离散；实验中未强制离散化，与理论假设存在差距。
- **应用范围有限**：方法聚焦文本到图像生成与编辑，未推广到其他多模态任务（如视觉问答、跨模态检索）。同时，模型未支持任意长度或复杂关系的多个概念编辑（例如涉及数量变化或空间关系）。

---

（完）
