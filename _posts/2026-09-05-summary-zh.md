---
layout: default
title: "Horizon Summary: 2026-09-05 (ZH)"
date: 2026-09-05
lang: zh
---

> 从 22 条内容中筛选出 2 条重要资讯。

---

1. [正在被利用的 Chromium 沙箱远程代码执行漏洞 CVE-2026-85046](#item-1) ⭐️ 9.0/10
2. [Anthropic 在 Lean 中形式化费马大定理](#item-2) ⭐️ 9.0/10

---

<a id="item-1"></a>
## [正在被利用的 Chromium 沙箱远程代码执行漏洞 CVE-2026-85046](https://nvd.nist.gov/vuln/detail/cve-2026-85046) ⭐️ 9.0/10

Google 已针对 CVE-2026-85046 发布了紧急补丁，该漏洞是 Chrome 的 V8 JavaScript 和 WebAssembly 引擎中的类型混淆漏洞，目前已被积极利用。攻击者可通过特制的 HTML 页面在沙箱内执行任意代码。 该漏洞影响所有基于 Chromium 的浏览器，波及全球数十亿用户，其积极利用构成了重大安全风险。这是 Google 在 2026 年修补的第六个零日漏洞，凸显了浏览器引擎安全面临的持续挑战，因此紧迫性尤为突出。 该漏洞的 CVSS 评分为 8.8，是 V8 引擎中的类型混淆问题。虽然它允许在沙箱内执行代码，但本身并不能逃逸沙箱，因此通常需要与单独的沙箱逃逸漏洞链式利用才能完全控制系统。

hackernews · negura · 9月4日 21:52 · [社区讨论](https://news.ycombinator.com/item?id=49570669)

**背景**: Chromium 浏览器使用沙箱将网页内容与底层操作系统隔离，以限制渲染器被攻破后造成的损害。然而，V8 引擎中的类型混淆等漏洞可能允许攻击者在沙箱内执行代码，如果与沙箱逃逸漏洞结合，则可能导致完整的远程代码执行。Google 一直在积极修补此类零日漏洞，CVE-2026-85046 是 2026 年第六个被利用的漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://socprime.com/blog/cve-2026-85046-analysis/">CVE-2026-85046: Chrome V8 Zero-Day Exploited</a></li>
<li><a href="https://www.helpnetsecurity.com/2026/09/04/google-chrome-zero-day-cve-2026-85046/">Google patches actively exploited Chrome zero-day (CVE-2026-85046) - Help Net Security</a></li>
<li><a href="https://www.esecurityplanet.com/threats/news-google-chrome-cve-2026-85046-zero-day/">Google’s Chrome Update Patches Sixth Zero-Day Exploited in 2026</a></li>

</ul>
</details>

**社区讨论**: 社区评论反映了担忧和怀疑的混合情绪。一些用户质疑该漏洞的金钱价值，指出 Google 仅为报告支付了 1000 美元，而另一些用户则讨论沙箱的有效性以及运行来自网络的任意代码的固有风险。还有关于各浏览器更新及时性的讨论，比较了 Brave 和 GrapheneOS。

**标签**: `#security`, `#chromium`, `#CVE`, `#RCE`, `#browser`

---

<a id="item-2"></a>
## [Anthropic 在 Lean 中形式化费马大定理](https://www.anthropic.com/research/formalizing-fermats-last-theorem) ⭐️ 9.0/10

Anthropic 宣布在 Lean 证明助手中形式化了费马大定理，生成了 1300 万行 Lean 代码和 29,500 个中间定理的证明。这标志着首次使用 AI 辅助完成这一著名定理的完整形式化。 这一成就表明 AI 现在能够处理极其复杂的数学证明，可能改变数学验证和形式化的方式。它可能导致发现现有证明中的错误，减轻人类审稿人的负担，并加速数学大领域的形式化。 该证明遵循 Darmon–Diamond–Taylor 在 1995 年对 Wiles–Taylor–Wiles 论证的阐述，而非现代证明。Anthropic 的代码库发展了 Fontaine 理论和 Mazur 关于 Eisenstein 理想的工作，以得出没有 Frey 曲线可以具有 p 阶点的结论。

hackernews · jlebar · 9月4日 18:42 · [社区讨论](https://news.ycombinator.com/item?id=49568506)

**背景**: 费马大定理由皮埃尔·德·费马在 1637 年著名地提出，直到 1994 年安德鲁·怀尔斯证明之前，它悬而未决了超过 350 年。Lean 是一个开源的证明助手，允许数学家编写机器检查的形式化证明，确保正确性。在 Lean 中形式化证明涉及将数学推理转化为计算机可以验证的语言，这是一个劳动密集型过程，现在 AI 可以协助完成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Wiles's_proof_of_Fermat's_Last_Theorem">Wiles's proof of Fermat's Last Theorem - Wikipedia</a></li>
<li><a href="https://www.explainx.ai/blog/anthropic-claude-fermats-last-theorem-lean-proof-2026">Claude Formalizes Fermat's Last Theorem in Lean (2026 ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论提到 Kevin Buzzard 的博客文章提供了背景，并对 1300 万行 Lean 代码的可靠性提出疑问，怀疑如此庞大的证明是否真的没有错误。一些评论者指出这一成就对于形式化大范围数学和发现错误的重要性，而另一些人则指出该证明基于较旧的阐述而非现代方法。

**标签**: `#formal verification`, `#AI research`, `#mathematics`, `#Lean`, `#proof assistants`

---