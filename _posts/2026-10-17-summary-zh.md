---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 31 条内容中筛选出 2 条重要资讯。

---

1. [Claude 破解 NIST ECDSA 曲线种子之谜](#item-1) ⭐️ 9.0/10
2. [中国拟对 23 项 AI 技术实施出口管制，开源技术豁免](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude 破解 NIST ECDSA 曲线种子之谜](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic 的 Claude 发现，NIST 椭圆曲线（P-192、P-224、P-256、P-384 和 P-521）的种子是使用 C 库的 lrand48 随机数生成器并以 Unix 时间戳作为种子生成的，从而解开了一个长期存在的密码学谜团。这一发现由 Filippo Valsorda 发布，他曾悬赏征集种子解决方案。 这解决了关于 NIST 曲线如何生成的 25 年之谜，可能影响对这些曲线及密码学标准制定过程的信任。同时，它也展示了 AI 解决复杂密码学难题的能力，可能影响未来此类研究的方式。 第五个二进制种子 B-163 仍无法解释，不符合该模式，可能是公布的种子中存在笔误。这一发现并不意味着曲线本身存在弱点，因为种子是随机生成的，这些曲线仍被认为是安全的。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**背景**: ECDSA 是最广泛使用的椭圆曲线密码学标准，由 NIST 于 2000 年作为 FIPS 186-2 的一部分采纳。该标准规定了素域和二进制域上的曲线，每条曲线都有一个种子，据称是随机生成并用 SHA-1 哈希以推导曲线参数。然而，这些种子的来源从未被解释，引发了关于潜在后门的猜测和阴谋论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://words.filippo.io/seeds-solved/">The NIST Elliptic Curves Seeds Bounty Has Been Claimed</a></li>
<li><a href="https://www.unite.ai/anthropic-says-claude-traced-nist-ecdsa-curve-seeds-to-a-1990s-rng/">Anthropic Says Claude Traced NIST ECDSA Curve Seeds to a ...</a></li>

</ul>
</details>

**社区讨论**: 社区讨论（746 分，289 条评论）显示出一种混合了娱乐和宽慰的情绪，评论开玩笑说方法很简单（例如使用 srand48(time(NULL))），并指出这打破了许多关于 NIST 的阴谋论。一些评论者指出，生成方法并不能排除故意选择具有特定属性的曲线的可能性，但其他人指出，如果曲线本来就不被信任，这种选择就没有必要。

**标签**: `#cryptography`, `#ECDSA`, `#NIST`, `#AI`, `#security`

---

<a id="item-2"></a>
## [中国拟对 23 项 AI 技术实施出口管制，开源技术豁免](https://www.reddit.com/r/LocalLLaMA/comments/1x7g3zq/china_proposes_export_controls_on_23_ai/) ⭐️ 8.0/10

2026 年 10 月 16 日，中国商务部和科技部发布了《中国禁止出口限制出口技术目录》修订草案，拟新增 40 项技术，其中 23 项与人工智能相关，涵盖基础/大模型、智能体和计算集群。公众意见征询截止至 11 月 15 日，临时出口前登记要求立即生效。 这是一项重要的地缘政治和技术政策发展，可能影响全球 AI 供应链和开放权重模型生态，尤其是对 DeepSeek 和 Qwen 等中国实验室。尽管开源发布获得豁免，但管制措施为未发布模型和海外部署引入了新的合规步骤，可能影响 AI 技术在全球的共享方式。 已通过开源发布或学术出版物公开的技术明确豁免，开源 AI 技术有资格获得简化的自动许可。然而，尚未发布的新模型在向海外转移权重或源代码前可能面临登记或审批，基于性能、参数和数据敏感性的阈值仍在制定中。

reddit · r/LocalLLaMA · /u/Stannis_Loyalist · 10月16日 13:22

**背景**: 中国的《禁止出口限制出口技术目录》是政府发布的清单，用于规范技术出口以维护国家经济和技术利益。它是列出中国出口管制物项的三大文件之一，另外两个是两用物项出口管制清单。此次修订草案反映了对 AI 作为战略技术的日益关注，类似于美国对先进 AI 模型权重的出口管制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cset.georgetown.edu/publication/china-export-control-catalog-2023/">Chinese Catalogue of Technologies Prohibited or Restricted ...</a></li>
<li><a href="https://www.china-briefing.com/news/technologies-subject-to-export-control-in-china-prohibited-restricted-export-catalogue">China’s Catalogue for Prohibited and Restricted Export ...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#export controls`, `#open-source AI`, `#China`, `#large language models`

---