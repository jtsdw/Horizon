---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 25 条内容中筛选出 1 条重要资讯。

---

1. [Lean 形式化黎曼假设引发 AI 与证明可信度热议](#item-1) ⭐️ 10.0/10

---

<a id="item-1"></a>
## [Lean 形式化黎曼假设引发 AI 与证明可信度热议](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

据报道，黎曼假设（以及针对狄利克雷 L 函数的广义黎曼假设）已在 Lean 中完成形式化，验证文件显示形式陈述根据多个内核可从三条标准公理推出。该结果据称在 AI（Claude）大量辅助和人类专家参与下取得，在 Hacker News 上引发了激烈讨论（939 分，802 条评论）。 如果得到确认，这将是形式验证和 AI 辅助数学的里程碑式突破，可能重塑人们对证明助手的信任，并为攻克其他重大未解问题打开大门。这也凸显了 AI 在形式化大量现代数学方面日益增长的作用。 验证依赖于多个独立内核（如 con-leche 和 con-ron）及其一致性证明，因此同时影响一致性证明和 RH 证明的 bug 极不可能存在。该证明还通过在同一 Lean 和 Mathlib 版本上对 Robin 和 Lagarias 判据的独立形式化进行了交叉验证。

hackernews · g-b-r · 11月21日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=50589618)

**背景**: 黎曼假设是关于黎曼 zeta 函数零点的著名猜想，断言所有非平凡零点都位于实部为 1/2 的临界线上。Lean 是一个用于数学证明形式验证的交互式定理证明器，Mathlib 是其庞大的形式化数学库。形式验证涉及使用数学方法证明相对于形式规范的正确性，而内核独立性对于结果的可信度至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Riemann_hypothesis">Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://leanprover.github.io/theorem_proving_in_lean/introduction.html">1. Introduction — Theorem Proving in Lean 3 (outdated)...</a></li>
<li><a href="https://math.mit.edu/~drew/grh/">RH Lean proof: verification files - MIT Mathematics</a></li>

</ul>
</details>

**社区讨论**: 评论者争论了结果的可信度，指出多个带一致性证明的独立内核使得利用 bug 的证明几乎不可能，但过去如虚假 Collatz 反证通过某个检查器的事件仍提醒人们保持谨慎。一些人强调对现代数学的大规模形式化是一项基础性成就，另一些人则归功于人类专家 Levent 对 AI 的引导，并思考此类结果是否会开启更大的问题。

**标签**: `#Lean`, `#Riemann Hypothesis`, `#formal verification`, `#AI for math`, `#proof assistants`

---