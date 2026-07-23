---
layout: default
title: "Horizon Summary: 2026-07-23 (ZH)"
date: 2026-07-23
lang: zh
---

> 从 32 条内容中筛选出 3 条重要资讯。

---

1. [陶哲轩用 ChatGPT 探索雅可比猜想反例](#item-1) ⭐️ 9.0/10
2. [GigaToken：LLM 分词速度提升 1000 倍](#item-2) ⭐️ 8.0/10
3. [谷歌向创世纪计划承诺 4000 万美元 AI 代币](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [陶哲轩用 ChatGPT 探索雅可比猜想反例](https://chatgpt.com/share/6a5fdc7a-d6f8-83e8-bbea-8deb42cfed56) ⭐️ 9.0/10

菲尔兹奖得主陶哲轩分享了一段 ChatGPT 对话，他利用 AI 分析雅可比猜想的一个反例，展示了高级的 AI 辅助数学研究。 这表明顶尖数学家可以利用大语言模型加速研究，可能改变数学发现和验证的方式。 该反例由 Levent Alpöge 于 2026 年 7 月使用 Claude Fable 5 发现，否定了维度大于 2 时的雅可比猜想，而二维情形仍未解决。

hackernews · gmays · 7月22日 17:30 · [社区讨论](https://news.ycombinator.com/item?id=49010345)

**背景**: 雅可比猜想是代数几何中一个长期未解的问题，断言若多项式映射的雅可比行列式为非零常数，则该映射具有多项式逆。该猜想已悬置一个多世纪，且以众多错误证明而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jacobian_conjecture">Jacobian conjecture</a></li>
<li><a href="https://en.wikipedia.org/wiki/Terence_Tao">Terence Tao</a></li>

</ul>
</details>

**社区讨论**: 社区对陶哲轩熟练使用 ChatGPT 表示惊叹，指出他精准的提问和深刻理解使他能提取有价值的见解。一些人强调了新手与专家使用 AI 的差异，以及 AI 加速数学发现的潜力。

**标签**: `#AI`, `#mathematics`, `#research`, `#LLM`, `#conjecture`

---

<a id="item-2"></a>
## [GigaToken：LLM 分词速度提升 1000 倍](https://github.com/marcelroed/gigatoken/) ⭐️ 8.0/10

GigaToken 是一个开源 Rust 库，通过使用 SIMD 指令、缓存和无分支技术大幅优化预分词，实现了约 1000 倍的分词速度提升。 分词是 LLM 流程中的关键瓶颈，尤其在离线数据预处理和代理工作流中；这一加速在处理数 TB 文本进行训练或推理时能显著节省时间和成本。 主要改进在于用 SIMD 优化例程替代基于正则表达式的预分词，并缓存预分词映射，在主流 x86 和 ARM CPU 以及多种分词器上实现一致的加速效果。

hackernews · syrusakbary · 7月22日 17:20 · [社区讨论](https://news.ycombinator.com/item?id=49010167)

**背景**: 分词将原始文本转换为 LLM 处理的 token。预分词通常使用正则表达式，速度较慢。SIMD（单指令多数据）允许 CPU 并行处理多个数据点，从而提升文本处理等任务的性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Single_instruction,_multiple_data">Single instruction, multiple data - Wikipedia</a></li>
<li><a href="https://gist.github.com/MangaD/1fad63756ad8c946ce01dd1d52eff173">Comprehensive Guide to SIMD in C++ · GitHub</a></li>
<li><a href="https://www.nitin-rachabathuni.com/blog/gigatoken-llm-tokenization-performance-rust">Scaling LLM Infrastructure: Why GigaToken is Solving the ...</a></li>

</ul>
</details>

**社区讨论**: 社区反响非常积极，称赞其技术创新和实用价值，尤其适用于离线数据准备。有人指出分词通常只占推理时间的不到 0.1%，但其他人强调它在代理栈和训练数据处理中的重要性。

**标签**: `#tokenization`, `#LLM`, `#performance optimization`, `#SIMD`, `#open source`

---

<a id="item-3"></a>
## [谷歌向创世纪计划承诺 4000 万美元 AI 代币](https://deepmind.google/blog/accelerating-the-frontiers-of-scientific-discovery-googles-40m-commitment-to-the-genesis-mission/) ⭐️ 8.0/10

谷歌承诺向美国政府的“创世纪计划”提供 4000 万美元的 AI 代币和信用额度，以加速科学发现。这笔资金将为研究人员提供先进的 AI 计算资源。 这一承诺标志着重要的公私合作，可能显著加速聚变能源和材料科学等领域的 AI 驱动研究。它可能为大型科技公司如何支持国家科学计划树立先例。 创世纪计划于 2025 年 11 月启动，旨在创建一个连接超级计算机、实验设施和数据集的集中式 AI 平台。谷歌的贡献以 AI 代币形式提供，而非直接现金；AI 代币是 AI 模型处理的数据单元。

rss · Google DeepMind Blog · 7月22日 13:38

**背景**: 创世纪计划是美国能源部的倡议，不同于 NASA 早期的创世纪号航天器。该计划涉及阿贡和橡树岭等国家实验室托管新的 AI 超级计算机。AI 代币是 AI 模型用于处理和生成的基本文本或数据单元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Genesis_Mission">Genesis Mission</a></li>
<li><a href="https://www.energy.gov/undersecretaryforscience/genesis-mission/genesis-mission">The Genesis Mission | Department of Energy</a></li>
<li><a href="https://blogs.nvidia.com/blog/ai-tokens-explained/">What Are AI Tokens? The Language and Currency Powering Modern AI | NVIDIA Blog</a></li>

</ul>
</details>

**标签**: `#AI`, `#scientific discovery`, `#Google DeepMind`, `#funding`, `#research`

---