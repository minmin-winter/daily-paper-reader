---
title: Unifying Specialized Visual Encoders for Video Language Models
title_zh: 统一专用视觉编码器的视频语言模型
authors: "Jihoon Chung, Tyler Zhu, Max Gonzalez Saez-Diez, Juan Carlos Niebles, Honglu Zhou, Olga Russakovsky"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=oYzDcCZdR9"
tags: ["query:unified-mm"]
score: 8.0
evidence: 统一多个专用视觉编码器生成全面的视频表示
tldr: "本文针对当前视频大语言模型仅使用单一视觉编码器导致信息受限的问题，提出MERV多编码器视频表示。首先对齐编码器特征的时空信息，然后投影到统一结构，最后通过交叉注意力融合。在公平比较下，准确率提升高达4.62%，且训练速度更快。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 849, \"height\": 414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1686, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 772, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 846, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 798, \"height\": 822, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 856, \"height\": 266, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 850, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1681, \"height\": 1586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1752, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1706, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1591, \"height\": 2048, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1687, \"height\": 1377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oyzdcczdr9/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1702, \"height\": 887, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1782, \"height\": 570, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 497, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 500, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 510, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1431, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1613, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1260, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 943, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 942, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1603, \"height\": 357, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1686, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 587, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1690, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1693, \"height\": 200, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oyzdcczdr9/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1605, \"height\": 360, \"label\": \"Table\"}]"
motivation: 单一视觉编码器限制了视频大模型的信息量。
method: MERV对齐多编码器特征后投影融合，通过交叉注意力整合。
result: "准确率提升4.62%，同时训练速度更快。"
conclusion: 多编码器融合可为视频语言模型提供更全面的视觉信息。
---

## Abstract
Recent advances in vision backbones have yielded powerful and diverse visual and video encoders. Yet, current Video Large Language Models encode visual inputs using an encoder from a single backbone family, limiting the amount and type of visual information they can process. We propose MERV, a Multi-Encoder Video Representation, which utilizes multiple encoders for a comprehensive video representation. To optimize heterogeneous features from a broad spectrum of encoders and ensure efficient and coherent feature integration, MERV first aligns encoder features spatio-temporally, then projects them into a unified structure, and finally fuses them through cross-attention. Under fair comparison, MERV achieves up to 4.62% higher accuracy than its base model, while introducing minimal extra parameters and training faster than equivalent single-encoder methods after parallelizing visual processing. Qualitative analysis shows MERV successfully captures and integrates domain knowledge from each encoder, opening new possibilities for scaling enhanced video understanding.

---

## 论文详细总结（自动生成）

# 论文总结：Unifying Specialized Visual Encoders for Video Language Models (MERV)

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：当前视频大语言模型（VideoLLM）仅依赖单一视觉编码器（如 CLIP、LanguageBind）提取视频特征，导致模型只能获取该编码器擅长类型的视觉信息，而其他编码器擅长的信息（如细粒度时空理解、运动感知等）被忽略，限制了模型的整体理解能力。
- **背景**：视觉编码器种类繁多（对比学习型、自监督型、纯视频型等），各有专长。例如 CLIP 擅长语言-视觉语义对齐，DINOv2 擅长细粒度对象识别，ViViT 擅长时间动态建模。但现有 VideoLLM 均未同时利用多种编码器的互补优势。
- **含义**：提出 MERV（Multi-Encoder Video Representation），首次在 VideoLLM 中系统性地融合多个专用视觉编码器，以获取更全面的视频表示，从而提升视频理解性能。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：使用多个异构视觉编码器并行提取特征，通过时空对齐、维度投影和交叉注意力融合，将不同编码器的专业知识整合为一个统一的视频表示，供 LLM 使用。
- **技术流程**：
  1. **多编码器特征提取**：选用四种互补编码器：
     - **空间专家**：DINOv2（ViT-L/14，自监督，擅长对象部件理解）。
     - **时间专家**：ViViT（ViViT-B/16×2，监督视频分类，擅长运动建模）。
     - **图像-语言专家**：SigLIP（ViT-B/16，对比学习，擅长视觉-语言关联）。
     - **视频-语言专家**：LanguageBind（ViT-L/14，多模态对比学习，擅长视频-语言语义对齐）。
  2. **时空对齐**：对不同编码器的输出特征进行时间维度对齐（通过调整输入帧数使所有编码器输出相同时间步数），空间维度使用 2D 自适应平均池化统一到相同空间分辨率（h×w）。
  3. **预融合投影**：对每个编码器的特征通过线性层投影到 LLM 的统一隐空间维度 d，得到序列长度为 ℓ = t×h×w 的特征张量 xₑ。
  4. **特征融合**：使用交叉注意力（Cross-Attention）进行加法融合：一个可学习查询向量 Q 对各编码器特征（经序列平均后的 key 和原始 value）计算注意力权重，得到统一视觉特征 O ∈ R^{ℓ×d}。公式为：
     O = Softmax(Q Xᵀ / √d) X，其中 X 为所有编码器特征拼接。
  5. **LLM 解码**：将融合后的视觉特征与文本指令拼接，输入 LLaMA-2 7B 进行生成。

- **训练策略**：
  - **MERV (frozen)**：仅执行 Stage 2 指令微调（1 轮，学习率 2e-5），冻结 LLM 和所有编码器，只训练投影层和交叉注意力融合模块。训练时间仅为 Video-LLaVA 全流程的 43%。
  - **MERV (full)**：执行 Stage 1 预训练（冻结编码器，训练投影和融合，学习率 1e-4，LLM 也参与训练） + Stage 2 指令微调，在部分基准上表现更好（如 Perception Test）。

## 3. 实验设计

- **数据集与 benchmark**：
  - 开放式问答：MSVD-QA、MSRVTT-QA、TGIF-QA、ActivityNet-QA
  - 多项选择问答：Perception Test、NExT-QA、VLEP、TVQA（其中后三个为 held-out 测试集，开发期间未使用）
  - 额外专项分析：Something-Something v2（SSv2）改编为 5-way 多项选择（SSv2-MCQ）以及 12 类时间敏感子集（SSv2-Temporal）
- **对比方法**：
  - 同数据混合：Video-LLaVA（Lin et al., 2024），使用相同训练数据（LAION 558k+Valley 702k 预训练，LLaVA 665k+Video-ChatGPT 100k 指令微调）
  - 不同数据混合：Video-Chat、LLaMA-Adapter、Video-LLaMA、Video-ChatGPT、SeViLA、LLaMA-VID-7B/13B 等
- **评估方式**：零样本评估，遵循 Video-ChatGPT 协议，使用 GPT-3.5-turbo 进行评分（score）和准确率（acc）。

## 4. 资源与算力

- 训练环境：使用 **8 块 NVIDIA L40-48GB GPU**，MERV (frozen) 完成训练< 24 小时；使用 **8 块 H100 GPU** 可缩短至 < 8 小时。
- 对比：Video-LLaVA 代码库在相同 L40 配置下 Stage 2 训练约需 38 小时。
- 论文未提及单次训练的具体 FLOPs 或 GPU 小时数，但通过并行化视觉编码（FSDP），多编码器引入的额外时间开销很小（图 3 显示平均 step 时间仅从 13.60s 增加到 16.31s，主要受最慢单编码器主导）。

## 5. 实验数量与充分性

- **实验数量**：设计了大量消融实验，包括：
  - 预融合投影器类型（2D Avg Pool、2D Attn、2D Conv、3D Avg、3D Conv 等）
  - 投影输出 token 长度（1~256 个 token）
  - 特征融合策略（交叉注意力、序列拼接、通道拼接、可学习权重、固定权重）
  - 训练配方（Stage 2 only、Stage 1+2、混合数据、冻结/全微调）
  - 编码器组合（移除单个编码器、替换 ViViT 为 Hiera）
  - 在 Something-Something v2 上对时间敏感性和整体理解进行专项分析
- **充分性**：实验覆盖了主要设计维度，并在多个多样化 benchmark 上验证，且考虑了公平对比（与 Video-LLaVA 同数据混合）。但缺乏对更大规模 LLM（如 13B）或更多编码器组合的探索。此外，所有实验均基于 LLaMA-2 7B，未测试其他 LLM 架构。
- **客观性**：held-out 测试集（NExT-QA、VLEP、TVQA）在最终阶段才使用，避免了开发过程中的过拟合；消融实验采用相同指标和数据，结果可信。

## 6. 主要结论与发现

- MERV 在几乎所有 benchmark 上优于 Video-LLaVA（同数据混合），准确率提升最高达 **4.62%**（TVQA），平均提升约 2-3%。
- MERV (full) 在 Perception Test 上达到 **48.4%**，超过 SeViLA（46.2%）。
- 使用多个编码器始终优于任何单编码器模型，且这种优势不是简单累加——移除任一编码器均导致性能下降，证明每个编码器贡献了独特信息。
- 交叉注意力权重分析表明，不同编码器的激活与视频类型相关（例如 ViViT 在高运动视频中权重更高，SigLIP 在包含文字的视频中权重更高）。
- 在 Something-Something v2 上，ViViT 在时间敏感子集上表现突出（39.8%），而在整体理解上较弱（26.8%），MERV 综合了双方优点，达到 42.0%。
- 效率：MERV 的训练速度与单编码器方法相当，因为视觉编码可并行处理，且 LLM 计算占主导地位。

## 7. 优点

- **方法创新**：首次在 VideoLLM 中系统性地融合多个 RGB 视觉编码器（而非不同模态），设计了完整的时空对齐、投影和交叉注意力融合流程。
- **实验充分性**：消融实验覆盖了几乎所有设计选择，并包含 held-out 测试集和额外 analytical 数据集（SSv2-MCQ），验证了方法的泛化能力和对编码器专长的捕捉。
- **公平对比**：确保与 Video-LLaVA 使用完全相同的数据混合和训练设置，隔离了多编码器带来的增益。
- **效率设计**：利用并行化（FSDP）和轻量投影器，使多编码器带来的额外计算开销极小，训练时间可接受。
- **分析深入**：通过交叉注意力权重可视化、WH-word 分类分析、SSv2 时间子集分析等多种方式，定量/定性证明了模型确实学习了各编码器的专长。

## 8. 不足与局限

- **计算资源依赖**：尽管效率优化良好，但多编码器仍需要更多 GPU 内存，可能限制在单卡或低资源环境下的部署。
- **编码器质量上限**：若选择的编码器本身在某种任务上能力有限，MERV 无法完全弥补，只能进行组合。
- **训练数据局限**：仅使用 Video-LLaVA 的数据混合（约 1.3M 图文 + 100K 视频指令），可能限制了模型的泛化能力和鲁棒性。未来应探索更大规模、更高质量的数据集。
- **LLM 限制**：所有实验基于 LLaMA-2 7B，未测试更大 LLM（如 13B、70B）或其他架构（如 FlanT5），结论可能受限于 LLM 规模。
- **编码器选择未穷尽**：只测试了四种 RGB 编码器，未探索更大集合（如 CLIP 变体、VideoPrism、V-JEPA 等），也未考虑融入音频、深度等非 RGB 模态。
- **SSv2 评估方式**：将分类任务转化为 5-way 多项选择，可能与实际应用场景有差距，且随机选择干扰项导致难度不确定。
- **可解释性**：交叉注意力权重虽能反映一部分偏好，但缺乏对融合后特征语义的深入分析。

（完）
