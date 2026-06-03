---
title: "Imagine While Reasoning in Space: Multimodal Visualization-of-Thought"
title_zh: 在空间中边想象边推理：多模态可视化思维
authors: "Chengzu Li, Wenshan Wu, Huanyu Zhang, Yan Xia, Shaoguang Mao, Li Dong, Ivan Vulić, Furu Wei"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=6vk6Xg24ZC"
tags: ["query:mm-reasoning"]
score: 8.0
evidence: 多模态可视化思维生成推理轨迹图像以辅助空间推理
tldr: 本文针对Chain-of-Thought在复杂空间推理中的不足，提出多模态可视化思维（MVoT）新范式。通过自回归生成推理轨迹的可视化图像，并引入令牌差异损失提升视觉质量。实验验证了MVoT在空间推理任务上的有效性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 776, \"height\": 471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1759, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 642, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1642, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 483, \"height\": 486, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1768, \"height\": 1376, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1760, \"height\": 1576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1749, \"height\": 413, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 275, \"height\": 288, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-6vk6xg24zc/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 793, \"height\": 598, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1754, \"height\": 480, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 777, \"height\": 200, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1327, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 894, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 945, \"height\": 365, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 632, \"height\": 576, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 723, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 988, \"height\": 406, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1329, \"height\": 112, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1713, \"height\": 960, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1071, \"height\": 1287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-6vk6xg24zc/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1772, \"height\": 752, \"label\": \"Table\"}]"
motivation: CoT在空间推理任务中表现不佳，需要结合图像思考。
method: 提出MVoT生成推理图像，并引入令牌差异损失提高视觉保真度。
result: 在空间推理任务上优于传统CoT方法。
conclusion: 可视化推理轨迹是提升空间推理的有效途径。
---

## Abstract
Chain-of-Thought (CoT) prompting has proven highly effective for enhancing complex reasoning in Large Language Models (LLMs) and Multimodal Large Language Models (MLLMs). Yet, it struggles in complex spatial reasoning tasks. Nonetheless, human cognition extends beyond language alone, enabling the remarkable capability to think in both words and images. Inspired by this mechanism, we propose a new reasoning paradigm, Multimodal Visualization-of-Thought (MVoT). It enables visual thinking in MLLMs by generating image visualizations of their reasoning traces. To ensure high-quality visualization, we introduce token discrepancy loss into autoregressive MLLMs. This innovation significantly improves both visual coherence and fidelity. We validate this approach through several dynamic spatial reasoning tasks. Experimental results reveal that MVoT demonstrates competitive performance across tasks. Moreover, it exhibits robust and reliable improvements in the most challenging scenarios where CoT fails. Ultimately, MVoT establishes new possibilities for complex reasoning tasks where visual thinking can effectively complement verbal reasoning.

---

## 论文详细总结（自动生成）

1. 核心问题与整体含义  
- 核心问题：Chain-of-Thought（CoT）在复杂空间推理任务（如迷宫导航、物体交互、动态环境规划）中表现不佳，原因在于它仅依赖文本描述，无法有效捕捉视觉和空间布局信息。  
- 整体含义：受人类通过语言和视觉图像协同思考（双编码理论）的启发，作者提出**多模态可视化思维（MVoT）**，让多模态大语言模型在推理过程中同时生成文本和图像推理轨迹，实现“边想象边推理”，从而提升空间推理的准确性和可解释性。

2. 方法论：核心思想、关键技术细节  
- **核心思想**：MVoT 让模型在生成中间推理步骤时，同步生成对应的图像可视化（visual thought），形成**交错文本-图像序列**，通过图像直接展示每一步的状态变化，避免纯文本描述可能引入的误差。  
- **关键技术细节**：  
  - 基于自回归多模态架构（Chameleon-7B + Anole-7B），使用统一的 Transformer 处理文本和图像令牌。  
  - 定义推理过程：  
    - 视觉思维（图像）生成：\(\hat{v}_i \sim P_\theta(v_i | \hat{z}_1, \hat{v}_1, \dots, \hat{v}_{i-1}, \hat{z}_i)\)  
    - 下步文本思维：\(\hat{z}_{i+1} \sim P_\theta(z_{i+1} | x, \hat{z}_1, \hat{v}_1, \dots, \hat{z}_i, \hat{v}_i)\)  
  - **令牌差异损失（Token Discrepancy Loss, \(L_D\)）**：解决单独训练的视觉码本与语言嵌入之间的对齐差异。  
    - 计算预测令牌与真实令牌在视觉嵌入空间中的相似度（MSE），惩罚分配给偏离真实嵌入令牌的概率。  
    - 公式：\(L_D = \sum_{i=1}^{n} S_{t_{\text{vis},i}} \cdot P(\hat{t}_i)\)，其中 \(S\) 为相似度矩阵。  
  - 总损失：\(L = L_C + L_D\)，其中 \(L_C\) 为交叉熵损失（覆盖文本和图像令牌）。  
- 训练时冻结两个 tokenizer，仅通过 LoRA 优化部分参数。

3. 实验设计  
- **数据集**：针对三个动态空间推理任务自行构建，覆盖不同复杂度：  
  - **MAZE**（抽象迷宫导航）：给定初始迷宫和动作序列，预测最终目的地（A/B/C/D）。  
  - **MINI BEHAVIOR**（安装打印机）：预测动作序列是否成功（成功/丢下失败/拿起失败/缺失关键物体）。  
  - **FROZEN LAKE**（冰湖导航）：预测是否安全到达礼物（成功/掉入洞中/未到达且安全）。  
- **对比方法**：  
  - 直接提示（Direct）  
  - 标准 CoT（带环境布局与坐标）  
  - CoT 无环境布局  
  - 交错文本-图像训练（Interleaved，仅计算文本损失）  
  - MVoT（本文方法，计算全部令牌损失）  
  - GPT-4o（零样本 / 零样本 CoT / 利用 MVoT 生成的视觉思维作为插件）  
- **指标**：任务准确率；可视化质量（V-Acc.、V-Red.、V-Steps、V-Ratio）。

4. 资源与算力  
- GPU 型号：MI300X。  
- 训练配置：MVoT 使用 32 GPU，Direct/CoT/Interleaved 使用 8 GPU（具体见表 8）。  
- 训练轮次：40 epochs，学习率 0.0002，batch size 4。  
- 文中未明确给出总训练时间或 GPU 小时数，但给出了超参数细节。

5. 实验数量与充分性  
- 实验覆盖三个任务，每个任务包含多种网格尺寸（3×3 到 10×10），并报告了细粒度性能（表 15）。  
- 进行了多组对比：Direct、CoT（有/无布局）、Interleaved、MVoT（有/无 \(L_D\)），以及与 GPT-4o 的联合试验。  
- 消融实验：分析了令牌差异损失对可视化质量和任务性能的影响（表 3、图 4、图 10）。  
- 还计算了 CoT 与 MVoT 的联合上限（表 2），证明二者互补。  
- 整体实验设计较全面，对比公平（均在同一骨干模型上微调或使用相同 API 设置），但仅基于 7B 参数模型，未在更大规模模型上验证。

6. 主要结论与发现  
- MVoT 在三个任务上均优于传统 CoT 和 Direct 基线，尤其在复杂场景（FROZEN LAKE）中表现稳健，比 CoT 高 20% 以上。  
- MVoT 比 CoT 对环境复杂度更鲁棒（网格增大时 CoT 显著下降，MVoT 保持稳定）。  
- 可视化质量直接影响任务性能：加入 \(L_D\) 后可视化准确率提高、冗余减少，任务准确率提升明显。  
- MVoT 与 CoT 互补：联合上限接近 100%，表明它们从不同角度贡献推理信息。  
- 作为插件，MVoT 生成的视觉思维可显著提升 GPT-4o 等闭源模型的空间推理能力（提升超 15%）。

7. 优点  
- **创新性**：首次在自回归 MLLM 中实现通过生成图像进行推理，与人类“边想象边推理”机制一致。  
- **损失设计**：令牌差异损失有效桥接视觉码本与语言嵌入之间的间隙，提升图像生成质量。  
- **鲁棒性**：MVoT 在环境复杂度增加时表现稳定，克服了 CoT 依赖于准确文本描述的局限。  
- **可解释性**：直观展示推理状态变化，用户更容易理解模型决策过程。  
- **灵活扩展**：可作为插件增强闭源模型；框架可推广到其他模态。

8. 不足与局限  
- **实验规模**：仅使用 7B 参数模型（Chameleon-7B / Anole-7B），未在更大模型上验证泛化性。  
- **图像生成质量**：在复杂背景（如 FROZEN LAKE 的漫画风格）下仍可能出现细节模糊、冗余图案等问题（图 4、图 6、图 7）。  
- **计算开销**：显式生成多张中间图像增加了推理时的计算成本，文中未给出具体效率对比。  
- **任务覆盖**：仅评估了网格世界类抽象任务，未涉及真实场景（如 3D 导航、物理交互）。  
- **依赖图像 detokenizer**：可视化质量受限于预训练的图像 tokenizer 重建能力，可能引入噪声。  

（完）
