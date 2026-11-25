---
layout: default
title: "Horizon Summary: 2026-11-25 (ZH)"
date: 2026-11-25
lang: zh
---

> 从 29 条内容中筛选出 3 条重要资讯。

---

1. [OpenAI 预印本声称矩阵乘法指数恰为 9/4](#item-1) ⭐️ 9.0/10
2. [GPT-6 模型展示内在蛋白质设计能力](#item-2) ⭐️ 9.0/10
3. [Ternary Bonsai 2.5 27B：在消费级 Mac 上实现接近前沿的 SWE-bench 性能](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 预印本声称矩阵乘法指数恰为 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 9.0/10

2026 年 11 月 24 日，OpenAI 在 GitHub 上发布预印本，声称证明了矩阵乘法指数ω在所有域上恰好为 9/4（即 2.25），解决了一个长期悬而未决的开放问题。该成果是四篇论文的一部分，这些论文据称解决了“数学前 500 开放问题”列表中的 8 个问题，包括强多项式线性规划（Smale 第九问题）、平均收益博弈和奇偶博弈等。 矩阵乘法是计算中的基础操作，确定其精确的渐近复杂度将解决理论计算机科学中一个数十年的难题，并对算法设计产生潜在的长期影响。该成果据称来自 OpenAI 未发布的模型，这也引发了关于企业 AI 研究激励以及 AI 与数学发现之间复合循环的讨论。 该证明据称通过张量退化而非优化改进建立了Ω(n^2.25)的下界，而上界 2.25 此前已知。该结果是渐近性的，并未确定实际可用的有竞争力的有限矩阵大小，且模型配方未公开。

hackernews · E-Reverance · 11月25日 01:19 · [社区讨论](https://news.ycombinator.com/item?id=50637220)

**背景**: 矩阵乘法指数（记为ω）描述了相乘两个 n×n 矩阵所需的算术运算次数随 n 增长的方式。朴素乘法需要 O(n^3)次运算，但快速算法已逐步降低该指数：从 1968 年的 3 降至 1986 年的 2.376，最近又降至约 2.371。确定ω的精确值几十年来一直是理论计算机科学中的重大开放问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://interestingengineering.com/culture/openai-exact-2-25-matrix-multiplication-exponent">OpenAI establishes exact 2.25 exponent for matrix multiplication</a></li>
<li><a href="https://www.unite.ai/openai-preprint-reports-9-4-bound-for-matrix-multiplication/">OpenAI Preprint Reports 9/4 Bound for Matrix Multiplication</a></li>
<li><a href="https://cryptobriefing.com/openai-matrix-multiplication-exponent-9-4/">OpenAI preprint claims the matrix multiplication exponent is ...</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，该论文是 OpenAI 一系列成果的一部分，解决了多个开放问题；一些人争论 OpenAI 和 Anthropic 是在复兴贝尔实验室式的开拓精神，还是主要为了公关。其他人推测，OpenAI 可能隐藏其最佳模型以取得基础性突破，然后利用这些突破在复合循环中构建更强的模型；还有一位评论者将标题更正为Θ(n^2.25)，并澄清该结果证明的是下界。

**标签**: `#matrix multiplication`, `#algorithms`, `#theoretical computer science`, `#OpenAI`, `#research breakthrough`

---

<a id="item-2"></a>
## [GPT-6 模型展示内在蛋白质设计能力](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities) ⭐️ 9.0/10

OpenAI 宣布其 GPT-6 模型能够利用推理和代码设计蛋白质结构和序列，实验室测试确认了针对五个靶标的结合。 这标志着人工智能与生物学交叉领域的重大突破，通过使 AI 能够在极少人工干预下设计功能性蛋白质，可能加速药物发现和蛋白质工程。 实验室验证显示了对五个靶标的结合证据，但具体靶标、结合亲和力和成功率等细节未披露；该方法依赖于 GPT-6 的推理和编码能力，而非专门的蛋白质设计模型。

rss · OpenAI Blog · 11月24日 13:00

**背景**: 蛋白质设计涉及创建具有所需功能的新蛋白质，例如用于治疗目的与特定靶标结合。传统上，这需要专门的计算模型如 AlphaFold 或 Rosetta，但大型语言模型的最新进展表明它们可以通过推理和代码生成来执行此类任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT - 6 models demonstrate intrinsic protein - design ... | OpenAI</a></li>
<li><a href="https://preview-www.nature.com/articles/s41586-026-10328-7?error=cookies_not_supported&code=3074ba93-c706-43ec-beb9-48958938b795">The past, present and future of de novo protein design | Nature</a></li>

</ul>
</details>

**标签**: `#AI`, `#protein design`, `#GPT-6`, `#biotechnology`, `#drug discovery`

---

<a id="item-3"></a>
## [Ternary Bonsai 2.5 27B：在消费级 Mac 上实现接近前沿的 SWE-bench 性能](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 8.0/10

三元量化本地模型 Ternary Bonsai 2.5 27B 已发布，用户报告其在消费级 Mac 上以可用速度提供接近前沿的 SWE-bench 性能和可靠的智能体编程能力，有用户在配备 24GB 内存的 Mac Mini M5 Pro 上达到 22-25 tokens/s 并支持 128k 上下文。 这很重要，因为它表明一个 27B 的三元量化模型可以在消费级硬件上本地运行，同时匹配前沿的 SWE-bench 分数，可能实现无需云依赖的私有、低成本智能体编程。 该模型采用三元量化（权重映射到{-1, 0, +1}），大幅减少内存占用；用户报告在 Mac Mini M5 Pro 上生成速度 22-25 tokens/s 并支持 128k 上下文，但基准有效性和潜在的“刷榜”行为存在争议。

hackernews · b0m · 11月24日 20:08 · [社区讨论](https://news.ycombinator.com/item?id=50633922)

**背景**: 三元量化是一种极端量化技术，将模型权重量化为三个值，在缩小模型尺寸和内存占用的同时力求保持准确性。SWE-bench 是一个评估大语言模型通过生成补丁解决真实 GitHub 问题的基准，而智能体编程指大语言模型自主执行多步骤编程任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2303.01505">[2303.01505] Ternary Quantization: A Survey - arXiv.org Ternary Quantization: A Survey - arXiv.org A Survey on Binary and Ternary Neural Networks and Their ... Ternary Quantization in Neural Networks - emergentmind.com TRAINED TERNARY QUANTIZATION - OpenReview Ternary quantization of spiking neural networks Ternary Quantization in Neural Networks - emergentmind.com</a></li>
<li><a href="https://www.swebench.com/">SWE-bench Leaderboards</a></li>
<li><a href="https://atomic.chat/blog/guides/best-local-llms-for-coding">Best Local LLM for Coding in 2026: A Comprehensive... - Atomic Chat</a></li>

</ul>
</details>

**社区讨论**: 社区评论总体积极，用户报告了令人印象深刻的速度和可靠的智能体性能；一些人争论 SWE-bench 分数是真实进步还是基准游戏，另一些人指出虽然分数可能低于 Qwen，但优势在于内存效率和速度。

**标签**: `#local-llm`, `#quantization`, `#small-models`, `#agentic-coding`, `#benchmarks`

---