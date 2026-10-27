---
layout: default
title: "Horizon Summary: 2026-10-27 (ZH)"
date: 2026-10-27
lang: zh
---

> 从 36 条内容中筛选出 2 条重要资讯。

---

1. [OpenAI 预印本声称推翻指数时间假设](#item-1) ⭐️ 10.0/10
2. [Sebastian Raschka 发布从零构建推理模型的视频课程](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 预印本声称推翻指数时间假设](https://github.com/openai/math/blob/main/preprints/The-Exponential-Time-Hypothesis-is-False-October-25-2026/paper.pdf) ⭐️ 10.0/10

OpenAI 在 GitHub 上发布的一篇预印本声称推翻了指数时间假设（ETH），即 3-SAT 问题无法在亚指数时间内求解的长期假设。该结果据称已在 Lean 中验证，并与其他发现一同公布，在 Hacker News 上引发了专家的激烈讨论。 如果正确，这将是复杂性理论中具有范式转变意义的结果，推翻支撑细粒度复杂性和许多条件下界的 foundational 硬度假设。它可能重塑研究人员处理算法设计和复杂性分类的方式，尽管并不直接解决 P vs. NP 问题。 论文指出，形式为 2^o(n)的运行时间界在一般多项式时间归约下不传递，因此该结果并不意味着一般 NP 问题存在亚指数时间算法。该主张正由 MIT 和加州大学圣地亚哥分校的研究人员进行独立审查，其对 SAT 求解的实际影响尚不清楚。

hackernews · vok · 10月26日 21:59 · [社区讨论](https://news.ycombinator.com/item?id=50251661)

**背景**: 指数时间假设（ETH）由 Impagliazzo 和 Paturi 提出，指出 3-SAT 无法在亚指数时间内求解；如果成立，则意味着 P ≠ NP，但这是一个更强的陈述。ETH 是计算复杂性中一个关键且未经证明的假设，指导着算法设计和条件下界。该新闻还提到 OpenAI 宣布在数学、计算机科学和物理学领域的三个新发现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Exponential_time_hypothesis">Exponential time hypothesis - Wikipedia</a></li>
<li><a href="https://www.explainx.ai/blog/openai-exponential-time-hypothesis-false-kakeya-yang-mills-three-results-lean-collaborations-2026">OpenAI Exponential Time Hypothesis Disproved? 3 Claims ...</a></li>
<li><a href="https://www.aichatdaily.com/ai-models/openai-says-internal-model-disproved-exponential-time-hypothesis">OpenAI says its internal model disproved the Exponential Time ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对这一声称的结果表示惊讶，一些人澄清由于 2^o(n)界不可传递，这并不意味着 NP 是亚指数的。其他人质疑其对 SAT 求解的实际应用，指出复杂性类分离非常罕见，并讨论了关于算法发现直觉的历史转变。

**标签**: `#complexity-theory`, `#ETH`, `#SAT-solving`, `#theoretical-computer-science`, `#research-breakthrough`

---

<a id="item-2"></a>
## [Sebastian Raschka 发布从零构建推理模型的视频课程](https://magazine.sebastianraschka.com/p/building-reasoning-models) ⭐️ 8.0/10

知名机器学习教育者 Sebastian Raschka 发布了一套名为《Build Your Own Reasoning Model》的完整视频课程，教授如何从零构建推理模型。课程从预训练大语言模型出发，涵盖评估、推理时扩展、带可验证奖励的强化学习以及蒸馏等内容。 推理模型是当前大语言模型研究的前沿，该课程提供了关于其背后技术的实用、动手入门，使更广泛的受众能够理解这些高级概念。它还在机器学习社区引发了关于从零教程的教学价值和局限性的重要讨论。 课程强调，推理模型本质上是通过使用可验证奖励的强化学习进行后训练（并可选地使用推理扩展技术）对传统大语言模型的升级。课程设计力求通俗易懂，但与任何从零教程一样，由于计算和数据的限制，它并不旨在产出生产就绪的模型。

hackernews · sgiannopoulos · 10月26日 15:11 · [社区讨论](https://news.ycombinator.com/item?id=50245138)

**背景**: 推理模型（如 OpenAI 的 o1）是使用扩展思考在回答前探索多条推理路径来解决复杂问题的大语言模型。带可验证奖励的强化学习（RLVR）是一种关键技术，它利用可自动检查的结果（如正确的数学答案）来训练模型更好地推理。从零教程是教育性项目，指导学习者在小规模上实现核心算法，而非训练全尺寸模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/building-reasoning-models">Build Your Own Reasoning Model : A Full Video Course</a></li>
<li><a href="https://sebastianraschka.com/from-scratch/">Super Intelligence (SI) From Scratch | Sebastian Raschka , PhD</a></li>
<li><a href="https://news.ycombinator.com/item?id=50245138">Sebastian Raschka 's from - scratch video course on... | Hacker News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（87 条评论）围绕从零教程的目的展开，一些人澄清这些教程并非为了产出生产就绪的大语言模型，而是为了建立直觉和理解。其他人赞扬了 Raschka 的教学风格及其著作《Build Your Own LLM From Scratch》，还有一些人质疑推理模型的定义以及仅靠 RLVR 是否能体现其本质。

**标签**: `#LLM`, `#reasoning-models`, `#education`, `#reinforcement-learning`, `#from-scratch`

---