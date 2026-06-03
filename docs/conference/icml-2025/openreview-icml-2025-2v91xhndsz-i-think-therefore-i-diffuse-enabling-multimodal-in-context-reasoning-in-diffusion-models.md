---
title: "I Think, Therefore I Diffuse: Enabling Multimodal In-Context Reasoning in Diffusion Models"
title_zh: 我思故我扩散：在扩散模型中实现多模态上下文推理
authors: "Zhenxing Mi, Kuan-Chieh Wang, Guocheng Qian, Hanrong Ye, Runtao Liu, Sergey Tulyakov, Kfir Aberman, Dan Xu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=2v91xhNdsz"
tags: ["query:mm-reasoning"]
score: 9.0
evidence: 利用VLM增强扩散模型的多模态上下文推理
tldr: 现有扩散模型微调方法聚焦像素级重建而缺乏推理能力，且受限于推理数据集。ThinkDiff提出一种新对齐范式，通过将视觉语言模型与编码器-解码器大语言模型的解码器对齐（而非扩散解码器）作为代理任务，赋予扩散模型多模态上下文理解和推理能力。实验表明该方法有效提升了多模态推理性能，为扩散模型的应用开辟了新方向。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1743, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 854, \"height\": 801, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1761, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1767, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1759, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 691, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 854, \"height\": 626, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1436, \"height\": 2290, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1744, \"height\": 1825, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1757, \"height\": 2146, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1410, \"height\": 2165, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1617, \"height\": 1862, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2v91xhndsz/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1713, \"height\": 2156, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-2v91xhndsz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1773, \"height\": 230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2v91xhndsz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1771, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2v91xhndsz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1767, \"height\": 203, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2v91xhndsz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 695, \"height\": 246, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2v91xhndsz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 864, \"height\": 155, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2v91xhndsz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1775, \"height\": 386, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2v91xhndsz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 863, \"height\": 260, \"label\": \"Table\"}]"
motivation: 现有扩散模型缺乏多模态上下文推理能力，且受限于推理数据集的复杂性。
method: 提出ThinkDiff，将视觉语言模型与大语言模型解码器对齐作为代理任务，而非直接对齐扩散解码器。
result: 在多个多模态推理任务上取得显著提升，验证了代理任务对齐的有效性。
conclusion: 代理任务对齐是一种高效赋予扩散模型多模态推理能力的方法。
---

## Abstract
This paper presents ThinkDiff, a novel alignment paradigm that empowers text-to-image diffusion models with multimodal in-context understanding and reasoning capabilities by integrating the strengths of vision-language models (VLMs). Existing multimodal diffusion finetuning methods largely focus on pixel-level reconstruction rather than in-context reasoning, and are constrained by the complexity and limited availability of reasoning-based datasets. ThinkDiff addresses these challenges by leveraging vision-language training as a proxy task, aligning VLMs with the decoder of an encoder-decoder large language model (LLM) instead of a diffusion decoder. This proxy task builds on the observation that the **LLM decoder** shares the same input feature space with **diffusion decoders** that use the corresponding **LLM encoder** for prompt embedding. As a result, aligning VLMs with diffusion decoders can be simplified through alignment with the LLM decoder. Without complex training and datasets, ThinkDiff effectively unleashes understanding, reasoning, and composing capabilities in diffusion models. Experiments demonstrate that ThinkDiff significantly improves accuracy from 19.2% to 46.3% on the challenging CoBSAT benchmark for multimodal in-context reasoning generation, with only 5 hours of training on 4 A100 GPUs. Additionally, ThinkDiff demonstrates exceptional performance in composing multiple images and texts into logically coherent images. Project page: https://mizhenxing.github.io/ThinkDiff.

---

## 论文详细总结（自动生成）

# 论文总结：I Think, Therefore I Diffuse: Enabling Multimodal In-Context Reasoning in Diffusion Models

## 1. 核心问题与整体含义（研究动机和背景）

现有文本到图像扩散模型虽然能根据显式提示生成高质量图像，但**缺乏多模态上下文推理能力**——例如理解隐含的逻辑关系（如“飞行猴子”和“飞行猫”后应生成“飞行斑马”）。当前的多模态扩散微调方法（如IP-Adapter、ControlNet）主要聚焦于**像素级重建**，而非语义推理；同时，构建推理专用的数据集复杂度高、规模有限，限制了模型在多样化推理任务上的泛化能力。因此，论文提出一种新范式，将**视觉语言模型（VLM）的推理能力迁移到扩散模型中**，同时避免从头训练和复杂数据集。

## 2. 方法论

### 核心思想
- **代理任务对齐**：不直接对齐VLM与扩散解码器，而是先对齐VLM与**编码器-解码器大语言模型（LLM）的解码器**。这是因为扩散模型（如FLUX）使用的提示编码器往往是LLM的编码器，因此**LLM解码器与扩散解码器共享同一输入特征空间**。通过对齐到LLM解码器，间接实现对扩散解码器的对齐。
- 对齐方式：使用**视觉-语言训练**（即根据图像生成文本描述），以文本交叉熵损失为监督。训练仅更新一个轻量级**对齐器网络（aligner）**，而VLM、LLM解码器、扩散解码器均保持冻结。

### 关键技术细节
1. **对齐器网络**：两层线性层 + GELU + RMSNorm。RMSNorm的初始化参数取自LLM编码器的最终RMSNorm层，以保证尺度匹配，解决收敛问题。
2. **两种变体**：
   - **ThinkDiff-LVLM**：使用大型视觉语言模型（LVLM，如Qwen2-VL）作为VLM。提取LVLM**生成令牌**的深层特征（而非输入令牌），因为生成过程中蕴含了上下文推理。训练时采用**随机掩码**策略：将生成令牌和特征分为两部分，只用第一部分预测第二部分，避免“捷径映射”，促进鲁棒对齐。
   - **ThinkDiff-CLIP**：使用CLIP视觉编码器（EVA-CLIP ViT-G/14）提取图像令牌，经对齐器映射后与LLM编码器对部分标题的编码特征拼接，输入LLM解码器预测剩余标题。在推理时替换LLM解码器为扩散解码器。
3. **训练与推理流程**：训练时VLM输出→对齐器→LLM解码器（文本预测）；推理时VLM输出→对齐器→扩散解码器（图像生成）。支持多个图像和文本的交错输入。

## 3. 实验设计

### 数据集与基准
- **CoBSAT基准**：包含10种多模态上下文推理生成任务（如颜色、风格、动作、纹理等），分别有2-shot和4-shot设置（输入2或4张图片及对应文本，要求生成下一个正确对象与属性的图像）。
- **其他测试**：COCO数据集（图像条件生成质量）、GenEval/DPG-Bench（文本条件生成质量）、单图像+文本/多图像+文本的组合生成（定性）、视频生成（结合CogVideoX）。

### 对比方法
- **ThinkDiff-LVLM** 对比：SEED-LLaMA、Emu、GILL（均为可基于图像和文本生成图像的方法）。报告CoBSAT准确率。
- **ThinkDiff-CLIP** 对比：FLUX1.1-pro-Ultra API（可能的重建微调方法）。在单图像+文本、多图像+文本等场景定性比较。

### 消融实验
- 对齐器中的RMSNorm设计（有无、初始化方式）。
- 随机掩码训练（有无）。
- 使用LVLM输入令牌 vs 生成令牌。
- 对比学习（ImageBind风格）替代文本预测损失。
- 不同LVLM（InternVL2.5-8B、Qwen2-VL-72B）。
- 数据规模（1.7M vs 3.4M）。
- 与Janus Pro、Flux Redux的对比。

## 4. 资源与算力

- **ThinkDiff-LVLM**：在**4块A100 GPU**上训练**5小时**，总batch size 96，训练25,000步。
- **ThinkDiff-CLIP**：在**4块A100 GPU**上训练**约1天**，总batch size 168，训练100,000步。
- 对比方法：SEED-LLaMA需要64 A100训练216小时；Emu需要128 A100训练48小时；GILL需要2 A6000训练48小时。ThinkDiff显著降低了资源需求。

## 5. 实验数量与充分性

- **量化评估**：CoBSAT上的2-shot和4-shot准确率（共10个任务），两组实验（表1、表2）。
- **生成质量评估**：COCO图像条件（FID、CLIP-I、CLIP-T）、GenEval和DPG-Bench文本条件（表4、表5）。
- **定性展示**：多个示意图（图5、6、8、9-14），涵盖不同推理与组合场景。
- **消融实验**至少6组（表3、6、7），涵盖架构、训练策略、数据量、VLM选择、对比方法等。
- **鲁棒性分析**：训练损失曲线（图7）。
- **总体充分性**：实验覆盖了主要基准、多种场景、以及与SOTA的全面比较，消融实验充分验证了设计选择。但缺少在大规模多模态对话数据集上的下游任务评估；CoBSAT基准虽具挑战性，但评价维度均为分类准确率，缺乏对图像质量与推理一致性的联合人类评估。

## 6. 主要结论与发现

- **ThinkDiff-LVLM在CoBSAT上取得SOTA**：2-shot平均准确率从19.2%（SEED-LLaMA）提升至46.3%（4-shot）；在9/10任务上超越所有对比方法，尤其在Action-I、Color-II、Action-II等困难任务上提升超20%。
- **4-shot更优**：ThinkDiff-LVLM 4-shot比2-shot准确率提升4.7%，而对比方法下降，表明其能更好利用复杂多模态上下文。
- **代理对齐任务高效**：仅需文本损失，无需推理数据集，即可转移VLM的推理能力。
- **ThinkDiff-CLIP在组合能力上优于重建微调方法**：能同时理解图像语义和文本指令，生成逻辑一致的多模态组合结果。
- **消融验证核心设计**：随机掩码、生成令牌特征、RMSNorm初始化等均至关重要。

## 7. 优点

- **思路新颖**：利用LLM解码器作为桥梁的代理对齐，避免直接对齐扩散解码器的困难，且无需推理专用数据集。
- **高效轻量**：仅需少量GPU和数小时训练，远低于对比方法。
- **通用性强**：支持多种VLM（LVLM和CLIP），且可扩展至视频生成（结合CogVideoX）。
- **消融完整**：从训练稳定性、对齐策略、数据量等多个角度验证了设计合理性。
- **开源友好**：提供了项目页面和明确的实现细节。

## 8. 不足与局限

- **仍存在困难案例**：在复杂推理任务上准确率虽高但非完美，部分场景仍可能失败（论文附录A提及）。
- **图像保真度非主要目标**：论文主要关注逻辑推理，未专门优化图像忠实度（如身份保持），限制了在图像编辑等任务的应用。
- **评估基准单一**：CoBSAT虽然是权威推理基准，但仅包含分类准确率，缺乏对生成图像质量与推理一致性的联合人工评价。
- **未与最新统一生成模型（如Janus Pro）全面对比**：虽然与Janus Pro和Flux Redux进行了部分对比，但更多是作为补充实验，而非系统benchmark。
- **VLM依赖性强**：ThinkDiff-LVLM的性能受LVLM本身推理能力的限制（例如使用更强LVLM可进一步提升），但论文未探讨对弱VLM的迁移效果。
- **数据与任务扩展性**：当前训练数据仅为图像-描述对，未探索视频、音频等模态；部分组合生成任务仍显简单（如图8、13），缺乏更复杂组合的定量评估。

（完）
