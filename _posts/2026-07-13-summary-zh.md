---
layout: default
title: "Horizon Summary: 2026-07-13 (ZH)"
date: 2026-07-13
lang: zh
---

> 从 23 条内容中筛选出 2 条重要资讯。

---

1. [llama.cpp b9970 为 DeepSeek V3.2/V4 添加闪电索引器](#item-1) ⭐️ 8.0/10
2. [Chromium 148 的 Math.tanh 可识别操作系统](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [llama.cpp b9970 为 DeepSeek V3.2/V4 添加闪电索引器](https://github.com/ggml-org/llama.cpp/releases/tag/b9970) ⭐️ 8.0/10

llama.cpp 版本 b9970 引入了一个新的 GGML 操作 GGML_OP_LIGHTNING_INDEXER，实现了 DeepSeek V3.2 和 V4 模型使用的闪电索引器，并提供了 CPU 支持、f16 掩码处理以及掩码广播修复。 这一优化显著提升了 DeepSeek V3.2/V4 模型的推理效率，将长上下文推理成本降低高达 6-7 倍，使先进的稀疏注意力在本地部署中变得实用。 闪电索引器是一个轻量级组件，在 top-k 集合上实现了 99.7% 的召回率和 2 倍加速，该版本还包含针对掩码广播和浮点运算计数的全面测试。

github · github-actions[bot] · 7月12日 12:03

**背景**: DeepSeek V3.2 引入了 DeepSeek 稀疏注意力（DSA），它使用闪电索引器高效选择注意力相关 token，大幅减少 KV 缓存内存和计算量。闪电索引器效率极高，可在 BF16 下运行并带有量化 FP32 路径，从而在消费级硬件上实现长上下文推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ggml-org/llama.cpp/releases">Releases · ggml -org/llama.cpp · GitHub</a></li>
<li><a href="https://aidownload.com/updates/3e4520e8-d8dc-453b-91fd-d8d5c70f4776">ggml -org/llama.cpp b9970 | AI Download</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp/discussions/21183">Testing DeepSeek V3.2 Lightning Indexer and Sparse Attention implementation · ggml-org/llama.cpp · Discussion #21183</a></li>

</ul>
</details>

**社区讨论**: 社区讨论（issue #21183）强调需要对闪电索引器和 DSA 实现进行充分测试，开发者确认 DSA 注意力在 2048 token 之前与 MLA 工作方式相同，之后才开始分化。总体情绪积极，重点在于验证和优化。

**标签**: `#llama.cpp`, `#DeepSeek`, `#GGML`, `#LLM inference`, `#machine learning`

---

<a id="item-2"></a>
## [Chromium 148 的 Math.tanh 可识别操作系统](https://scrapfly.dev/posts/browser-math-os-fingerprint/) ⭐️ 8.0/10

自 Chromium 148 起，Math.tanh 的实现因操作系统而异，攻击者可通过一次 tanh 调用的输出来识别底层操作系统。 这一新的指纹识别向量削弱了依赖伪造 User-Agent 头部的隐私保护措施，因为 Math.tanh 的操作系统签名可能与伪造的 User-Agent 相矛盾。这也凸显了浏览器指纹识别与反追踪措施之间持续的军备竞赛。 该指纹识别之所以可行，是因为不同操作系统的数学库对相同的 tanh 输入会产生略微不同的结果，而 Chromium 148 将 Math.tanh 委托给底层的 C 运行时。这意味着输出可用作操作系统级别的签名，甚至可能推断出浏览器版本范围。

hackernews · joahnn_s · 7月12日 21:12 · [社区讨论](https://news.ycombinator.com/item?id=48884853)

**背景**: 浏览器指纹识别是一种无需 Cookie 即可通过收集设备和浏览器的独特特征来识别用户的追踪技术。常见的指纹向量包括屏幕分辨率、已安装字体和 WebGL 渲染器。Math.tanh 是一个计算双曲正切的 JavaScript 函数，由于底层数学库实现的差异，其行为在不同平台上可能不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Browser_fingerprinting">Browser fingerprinting</a></li>
<li><a href="https://learn.microsoft.com/en-us/dotnet/api/system.math.tanh?view=net-10.0">Math.Tanh (Double) Method (System) | Microsoft Learn</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（365 分，171 条评论）反应不一：一些用户指出该指纹仅限于操作系统检测，且可能被伪造的 User-Agent 所矛盾；另一些人则认为它还能识别浏览器版本范围。有人对文章由 AI 生成表示怀疑，还有人建议推动正确舍入的超越函数以消除此类差异。

**标签**: `#browser fingerprinting`, `#privacy`, `#Chromium`, `#JavaScript`, `#security`

---