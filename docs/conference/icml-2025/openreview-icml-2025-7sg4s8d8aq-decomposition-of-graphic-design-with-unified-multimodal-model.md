---
title: Decomposition of Graphic Design with Unified Multimodal Model
title_zh: 基于统一多模态模型的图形设计分解
authors: "Hui Nie, Zhao Zhang, Yutao Cheng, Maoke Yang, Gonglei Shi, Qingsong Xie, Jie Shao, Xinglong Wu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=7SG4s8d8AQ"
tags: ["query:unified-mm"]
score: 8.0
evidence: 提出统一多模态模型DeaM用于图形设计分解
tldr: 该论文提出图形设计层级分解新任务LDGD，将复合图形设计转换为有序RGB-A层和元数据。为此设计DeaM模型，一个大型统一多模态模型，集成联合视觉编码器和语言模型。模型能够预测每层属性并恢复重叠区域的遮挡部分。实验证明该方法能高保真重建图像，为数字内容编辑和管理提供新工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-7sg4s8d8aq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1770, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7sg4s8d8aq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1767, \"height\": 953, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7sg4s8d8aq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1381, \"height\": 566, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7sg4s8d8aq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1415, \"height\": 774, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7sg4s8d8aq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 863, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7sg4s8d8aq/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 857, \"height\": 671, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7sg4s8d8aq/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 796, \"height\": 842, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-7sg4s8d8aq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 860, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7sg4s8d8aq/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 835, \"height\": 159, \"label\": \"Table\"}]"
motivation: 将视觉内容转换为结构化数据以支持精确编辑，但现有方法无法处理重叠层恢复。
method: 提出统一多模态模型DeaM，结合视觉编码器和语言模型进行层级分解。
result: 模型能预测图层属性并高保真恢复遮挡区域，实现结构化图像分解。
conclusion: 统一多模态模型在图形设计结构化解构中具有巨大潜力。
---

## Abstract
We propose Layer Decomposition of Graphic Designs (LDGD), a novel vision task that converts composite graphic design (e.g., posters) into structured representations comprising ordered RGB-A layers and metadata. By transforming visual content into structured data, LDGD facilitates precise image editing and offers significant advantages for digital content creation, management, and reuse. This task presents two core challenges: (1) predicting the attribute information (metadata) of each layer, and (2) recovering the occluded regions within overlapping layers to enable high-fidelity image reconstruction. To address this, we present the Decompose Layer Model (DeaM), a large unified multimodal model that integrates a conjoined visual encoder, a language model, and a condition-aware RGB-A decoder. DeaM adopts a two-stage processing pipeline: first generates layer-specific metadata containing information such as spatial coordinates and quantized encodings, and then reconstructs pixel-accurate layer images using a condition-aware RGB-A decoder. Beyond full decomposition, the model supports interactive decomposition via textual or point-based prompts.  Extensive experiments  demonstrate the effectiveness of the proposed method. The code is accessed at https://github.com/witnessai/DeaM.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：数字媒体中广泛使用多层复合图像（如海报）来传达信息，但高效编辑、管理和复用这些图像需要理解其底层层次结构。现有图像分割、修复等方法难以同时处理多层的重叠遮挡、文本层识别和结构化解构。
- **核心问题**：首次提出 **Layer Decomposition of Graphic Designs (LDGD)** 新任务，目标是将复合图像分解为有序的 **RGB-A 层**（带透明度）及其**结构化元数据**（位置、颜色、字体等），实现高保真重建和精确编辑。
- **意义**：将视觉内容转换为结构化数据，为数字内容创建、管理和编辑提供基础工具，填补了自动层分解的空白。

## 2. 方法论
- **核心思想**：采用 **统一多模态模型（DeaM）** 架构，将层分解建模为“元数据生成 + 图像重建”的端到端生成任务，支持全分解和交互式按需分解。
- **关键技术细节**：
  - **RGB-A VQ-GAN**：将传统 RGB VQ-GAN 扩展为4通道（RGB + Alpha），并改进重建损失权重（RGB 权重更高），消除编码歧义。下采样率 f=16，对语义丰富图像输入分辨率 192×192（产生144个token），装饰性元素 128×128（64个token）。
  - **联合视觉编码器（Conjoined Visual Encoder）**：同时使用 CLIP Vision Encoder 和 DINO v2 编码视觉特征，通道拼接后得到 N×(1024×2) 维度，兼顾高层语义和低层细节。
  - **语言模型主干**：基于 InternLM2-7B，扩展词汇表加入 VQ-GAN codebook 索引对应特殊 token `<vt-{number}>`。为解决精确序列预测难题，在训练时对 token 矩阵每行末尾添加换行符 `\n` 增加规律性。
  - **条件感知 RGB-A 解码器（Condition-Aware RGB-A Decoder）**：在 VQ 解码基础上引入输入图像裁剪区域作为条件，并通过预测遮挡 mask 聚焦于被遮挡区域生成，提升图像清晰度。
  - **训练三阶段**：
    1. 训练 RGB-A VQ-GAN（含 ImageNet + LAION 百万级子集）；
    2. 指令微调 DeaM，学习生成 JSON 格式元数据（位置、顺序、VQ-GAN 索引等），同时融入文本引导、点引导和 GPT-4 生成的对话数据；
    3. 训练条件感知解码器（保持 VQ 编码器冻结，只训练解码器和条件编码器 ResNet），与第二阶段解耦。

## 3. 实验设计
- **数据集**：
  - 训练：自建 **CreatiLD** 数据集，包含 224,054 张带有完整层注释的图形设计（海报为主），平均每图 10.30 层，图像层与文本层比例约 6.3:3.7。额外使用 ImageNet 训练集和 LAION 子集训练 VQ-GAN。
  - 评估：公开学术数据集 **Crello**（现 VistaCreate），测试集 >2000 张。
- **Benchmark**：无现成基准，作者自建 **Baseline** 方法（结合 OCR、图像修补、抠图，只能分解为背景+主图+文本三层）。
- **对比方法**：
  - Baseline（上述）
  - 图像矢量化方法 **LIVE**（Ma et al., 2022）——生成 SVG 表示。
  - 指令编辑方法 **MGIE**（Fu et al., 2024）——仅定性对比。
- **评价指标**：
  - 图像重建质量：**FID**（Fr´echet Inception Distance）。
  - 位置预测准确率：通过匈牙利匹配计算匹配框的 **mean IoU**（称为 Loc α）。
- **实验场景**：
  - 全自动层分解（定量 FID 和 IoU）
  - 文本引导/点引导交互分解（定性展示）
  - 与矢量化和指令编辑方法的定性比较

## 4. 资源与算力
- **文中明确说明**：使用 **16 块 NVIDIA A800 GPU** 进行训练。
- **未明确说明**：具体训练时长（每个阶段耗时）、环境软件版本等。元数据中也未提及。

## 5. 实验数量与充分性
- **主要定量实验**：
  - **消融实验**（Table 1）：逐步添加联合视觉编码器、增强预测规律性、条件感知解码器，FID 从 105.524 降至 70.629，验证各组件有效。
  - **与 Baseline 对比**（Table 2）：DeaM 的 FID 70.629 显著优于 Baseline 的 99.603；Loc α 略高（0.7128 vs 0.7069）。
- **定性实验**：
  - 层分解可视化（图4）：显示多层层分解结果。
  - 与 Baseline 重建对比（图5）：DeaM 更少伪影。
  - 与 LIVE（图7）：DeaM 在复杂自然图上更好。
  - 点引导/文本引导交互（图6）：与 MGIE 对比。
- **充分性评价**：
  - **优点**：设计了消融、基准对比、多场景定性展示，覆盖了核心功能。
  - **不足**：仅与自建 baseline 和简洁的 LIVE 对比，未与近期的其他统一多模态模型（如 Emu、Show-o等）或专业分割模型（如 SAM）定量比较；Crello 测试集仅2000张，规模偏小；未报告更细致的指标（如文字识别准确率、层顺序正确率）。

## 6. 主要结论与发现
- DeaM 成功解决了 LDGD 这一新任务，能自动分解海报类图像为多层 RGB-A 图像并附带元数据。
- 三项关键设计（联合视觉编码、规律化预测、条件解码）均显著提升性能，其中条件解码改善最大。
- 与基线相比，DeaM 不仅支持更多层数（>3层），且重建质量大幅提升（FID 降低 29）。
- 支持文本和点交互，具有实用灵活性。
- 当前局限：解码质量仍有提升空间（需更强大的图像分词器），字体预测精度不理想，对装饰元素层次判断偶有误差。

## 7. 优点
- **任务创新**：首次定义并求解 LDGD，具有明确的实用价值。
- **模型设计**：巧妙结合 LLM 与 VQ-GAN，通过元数据+token 序列实现多图层端到端生成，支持交互式分解。
- **训练策略**：三阶段解耦（VQ-GAN → 指令微调 → 解码器）降低训练难度，并利用 GPT-4 生成多样化指令数据增强泛化能力。
- **透明度支持**：RGB-A 四通道设计确保层叠合成的正确性。
- **消融设计**：清晰验证了每个核心组件的贡献。

## 8. 不足与局限
- **实验广度不足**：仅与自建 baseline 和一个矢量化方法对比，缺乏与当前主流分割模型（SAM等）、其他统一多模态生成模型（如 Emu3、Janus）的定量比较，说服力减弱。
- **数据集问题**：CreatiLD 是内部数据集，未公开；Crello 测试集规模小，且领域偏向海报，泛化性受限。
- **评价指标单一**：FID 和 IoU 无法全面衡量文字识别、字体匹配、层顺序正确性等。
- **计算资源未充分说明**：无训练时长、显存需求、推理速度，可复现性打折扣。
- **质量局限性**：作者指出“字体的预测不够好”，“图像解码质量有待提升”，说明重建高保真目标尚未完全达到。
- **应用限制**：主要针对海报类图形设计，对自然照片的适用性未经测试；层分解的“逻辑顺序”在人眼中可能存在歧义，影响评估公平性。

（完）
