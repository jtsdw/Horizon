---
layout: default
title: "Horizon Summary: 2026-11-21 (ZH)"
date: 2026-11-21
lang: zh
---

> 从 34 条内容中筛选出 2 条重要资讯。

---

1. [Levent Alpöge 宣称证明广义黎曼猜想，并附大规模 Lean 形式化验证](#item-1) ⭐️ 10.0/10
2. [陶哲轩将无外力流体奇点与广义黎曼假设联系起来](#item-2) ⭐️ 9.0/10

---

<a id="item-1"></a>
## [Levent Alpöge 宣称证明广义黎曼猜想，并附大规模 Lean 形式化验证](https://alpo.ge/remark.pdf) ⭐️ 10.0/10

数学家 Levent Alpöge 发布论文，宣称证明了广义黎曼猜想（GRH），并附带了约 1.3 GB、约 1500 万行的 Lean 形式化验证。该证明据称由 AI 辅助完成，于 2026 年 11 月 20 日公布，同日 Ravi Vakil 也发布了 Alessandro Masullo 的另一份证明草稿。 如果得到验证，GRH 的证明将成为数论领域具有范式转变意义的突破，对素数分布和密码学产生深远影响。庞大的 Lean 形式化验证也凸显了 AI 和机器可检验证明在数学中日益增长的作用，有望加速该领域的信任建立与合作。 Lean 证明被分成 14 个部分，总计 1.3 GB、约 1500 万行，用户需下载并合并各部分后再解压。该声明仍有待数学界的正式审查，同时 Alessandro Masullo 的另一份未使用 AI 辅助的证明也正在由 Brian Conrad 审查。

hackernews · iamronaldo · 11月20日 14:16 · [社区讨论](https://news.ycombinator.com/item?id=50574968)

**背景**: 黎曼猜想是数学中最著名的未解决问题之一，它猜想黎曼 ζ 函数的所有非平凡零点都位于一条临界线上。广义黎曼猜想将此猜想推广到更广泛的 L-函数类，包括狄利克雷 L-函数，并被广泛认为成立。Lean 是一个交互式定理证明器，允许数学家将证明形式化，并通过机器检验其正确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis</a></li>
<li><a href="https://lean-lang.org/">Lean Programming Language</a></li>
<li><a href="https://arxiv.org/pdf/2501.18639">A Comprehensive Survey of the Lean 4 Theorem Prover ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（2521 分，1738 条评论）显示出强烈的兴趣，既有兴奋也有怀疑。一些评论者惊叹于理论突破的速度，并担忧更广泛的社会影响；另一些人则指出需要弥合理论与现实影响之间的差距。还有人分享了 2014 年对 Alpöge 的采访链接，他在采访中表示解决黎曼猜想是他的人生目标。

**标签**: `#mathematics`, `#Riemann Hypothesis`, `#formal verification`, `#Lean`, `#research breakthrough`

---

<a id="item-2"></a>
## [陶哲轩将无外力流体奇点与广义黎曼假设联系起来](https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/) ⭐️ 9.0/10

陶哲轩发表文章，讨论了一个将无外力欧拉/纳维-斯托克斯奇点与广义黎曼假设（GRH）联系起来的证明；同一天，Levent Alpöge 提出了一个 AI 辅助的 GRH 证明，Ravi Vakil 也发布了 Alessandro Masullo 的证明草稿。该文章引发了关于形式验证和 AI 驱动数学的广泛社区讨论。 这代表了一项重大数学突破，因为它可能解决两个长期未决的问题——纳维-斯托克斯存在性与光滑性问题以及广义黎曼假设——并凸显了 AI 和形式验证在高等数学中日益重要的作用。社区的高度参与（402 分，169 条评论）强调了其重要性。 据报道，该证明充分利用了朗兰兹纲领和算术几何的现代发展，并且两个独立的 Lean 内核已接受该结果，表明没有内核漏洞被利用。然而，关于形式验证是否真正捕捉到了预期的数学陈述，仍存在疑问。

hackernews · archon1410 · 11月20日 17:21 · [社区讨论](https://news.ycombinator.com/item?id=50578358)

**背景**: 纳维-斯托克斯存在性与光滑性问题询问描述流体流动的方程在三维空间中是否总是具有光滑解，它是千禧年大奖难题之一。广义黎曼假设将关于黎曼 ζ 函数零点的经典黎曼假设推广到更广泛的 L-函数类，是数论中的核心猜想。使用 Lean 等证明助手进行形式验证，使数学家能够以计算机精度检查证明，而 AI 系统正越来越多地被用于生成此类形式证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier–Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis</a></li>
<li><a href="https://cacm.acm.org/research/formal-reasoning-meets-llms-toward-ai-for-mathematics-and-verification/">Formal Reasoning Meets LLMs: Toward AI for Mathematics and ...</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了兴奋与担忧：一些人质疑新的数学抽象是如何创造的，另一些人指出两个独立内核接受证明降低了内核漏洞的风险，还有一位评论者询问如何确保大型 Lean 证明真正验证了预期陈述而非平凡内容。此外，还有关于对职业生涯和数学发现本质的更广泛影响的讨论。

**标签**: `#mathematics`, `#Navier-Stokes`, `#Riemann Hypothesis`, `#formal verification`, `#AI for math`

---