---
layout: default
title: "Horizon Summary: 2026-09-03 (ZH)"
date: 2026-09-03
lang: zh
---

> 从 37 条内容中筛选出 4 条重要资讯。

---

1. [谷歌 DeepMind 发布 Gemini 3.8 Flash 及网络安全版](#item-1) ⭐️ 9.0/10
2. [Meta 发布 Muse Spark 1.3，DeepSWE 得分领先](#item-2) ⭐️ 8.0/10
3. [法院裁决后谷歌避免广告技术业务拆分](#item-3) ⭐️ 8.0/10
4. [谷歌 DeepMind 推出主动网络防御计划](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌 DeepMind 发布 Gemini 3.8 Flash 及网络安全版](https://deepmind.google/blog/introducing-gemini-3-8-flash-and-38-flash-cyber/) ⭐️ 9.0/10

谷歌 DeepMind 发布了新的轻量级模型 Gemini 3.8 Flash，以及专为网络安全设计的 Gemini 3.8 Flash Cyber 版本。Cyber 模型通过新的 Fairwind 计划向受信任的防御者提供。 此次发布延续了谷歌在 Flash 模型上的快速迭代，提供了更好的速度、成本和编码能力，对构建智能体工作流的开发者意义重大。Cyber 版本则满足了网络安全领域对 AI 驱动的漏洞检测和自动修补日益增长的需求。 据报道，Gemini 3.8 Flash 在 Artificial Analysis 上的智能得分为 59，与 Opus 5 medium 持平，并在 BenchLM 的编码能力排名中位列 148 个模型中的第 36 位。Cyber 模型取代了 3.5 版本，在内部测试中表现出显著改进，但并非面向普通公众使用。

rss · Google DeepMind Blog · 9月2日 16:18

**背景**: Gemini Flash 模型旨在平衡速度、成本和能力，适用于高吞吐量和低延迟的应用场景。它们支持包括音频和视频在内的多模态输入，而一些竞争对手的旗舰模型仅支持图像。Cyber 版本是 AI 模型向网络安全等专业领域发展的趋势之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/">Introducing Gemini 3.8 Flash and 3.8 Flash Cyber</a></li>
<li><a href="https://arstechnica.com/ai/2026/09/google-releases-gemini-3-8-flash-its-third-flash-model-in-six-weeks/">Google releases Gemini 3.8 Flash, its third Flash model in six weeks - Ars Technica</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-8-flash/">Gemini 3 . 8 Flash - Model Card — Google DeepMind</a></li>

</ul>
</details>

**社区讨论**: 社区成员对该模型的速度和编码能力印象深刻，有用户以 1.8 美分的成本在 13 秒内生成了一个酷炫的 HTML 演示。其他人指出其在基准测试中的强劲表现，在某些排行榜上超过了 Opus 5，并强调其多模态支持是关键的差异化优势。然而，有用户认为低思考水平相比 3.7 版本可能是一种退步。

**标签**: `#AI`, `#Google DeepMind`, `#Gemini`, `#model release`

---

<a id="item-2"></a>
## [Meta 发布 Muse Spark 1.3，DeepSWE 得分领先](https://developer.meta.com/ai/models/muse-spark/) ⭐️ 8.0/10

Meta 发布了 Muse Spark 1.3，该 AI 模型在 DeepSWE 基准测试中取得了 75.4 的最高分。该模型旨在提升代理和编码任务的性能，并增强了实际可用性。 此次发布表明 Meta 在竞争激烈的 AI 模型市场中持续发力，提供了一种成本效益高的替代方案，在关键基准测试上可与前沿模型媲美。强劲的性能和低廉的价格可能推动成本下降，并促进开放权重模型生态系统的进一步创新。 Muse Spark 1.3 在 DeepSWE 上得分为 75.4，超过了之前的领先者如 Gemini 3.8 Flash。该模型可通过 Meta 的 API 使用，Meta 还宣布即将发布 Muse Spark 1.2 的权重以及开放权重的 Muse Glimmer 模型。

hackernews · bvaldivielso · 9月2日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=49541256)

**背景**: DeepSWE 是一个长期软件工程基准，旨在评估编码代理在原始复杂任务上的表现，解决了像 SWE-bench 这样依赖 GitHub 修复的基准的局限性。Muse Spark 是 Meta 的一系列 AI 模型，1.3 版本专注于改进推理和代理能力。该模型是 Meta 提供有竞争力且成本效益高的 AI 解决方案的更广泛战略的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.meta.com/ai/models/muse-spark/">Muse Spark 1.3 | Meta</a></li>
<li><a href="https://research.meta.ai/blog/introducing-muse-spark-1-3">Introducing Muse Spark 1.3 | Meta AI Research</a></li>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE</a></li>

</ul>
</details>

**社区讨论**: 社区成员表达了积极情绪，如 simonw 指出与之前版本相比输出质量有所提高。superfrank 赞赏该模型的成本效益和实用性，bertili 则强调了其有竞争力的价格和基准领先地位。一些评论还涉及 Meta 的数据使用政策和更广泛的企业问题。

**标签**: `#AI`, `#Meta`, `#Muse Spark`, `#model release`, `#benchmarks`

---

<a id="item-3"></a>
## [法院裁决后谷歌避免广告技术业务拆分](https://www.nytimes.com/2026/09/02/technology/google-ad-tech-remedies.html) ⭐️ 8.0/10

2026 年 9 月 2 日，美国法院裁定，尽管此前认定谷歌在广告技术市场存在非法垄断行为，但谷歌无需剥离其广告技术业务。这一决定使谷歌免于被迫拆分其广告技术业务。 这一裁决意义重大，因为它避免了可能重塑谷歌广告技术业务及整个数字广告行业的重大结构性补救措施。同时，它为反垄断补救措施在科技垄断企业中的应用树立了先例，可能影响针对其他大型科技公司的在审案件。 谷歌的广告技术业务去年收入达 300 亿美元，约占 Alphabet 总收入的 8%，但其利润贡献估计不到 1%，且收入已连续 16 个季度下滑。此前谷歌被认定在两个广告技术市场拥有垄断地位，这是其近年来第三次反垄断败诉。

hackernews · donohoe · 9月2日 14:46 · [社区讨论](https://news.ycombinator.com/item?id=49537131)

**背景**: 广告技术（Ad Tech）是指用于自动化数字广告买卖的技术和平台，包括广告投放、广告交易平台和需求方平台等工具。美国司法部曾试图迫使谷歌出售其部分广告技术业务，以解决被指控的反竞争行为。这一裁决是大型科技公司面临更广泛反垄断审查的一部分，此前已有关于谷歌搜索主导地位和应用商店行为的裁决。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/news/story/judge-google-has-adtech-monopoly-7276514/">Judge: Google has adtech monopoly | LinkedIn</a></li>
<li><a href="https://www.adexchanger.com/platforms/google-is-found-guilty-of-operating-an-ad-tech-monopoly/">Google Is Found Guilty Of Operating An Ad Tech Monopoly (!)</a></li>
<li><a href="https://business.linkedin.com/advertise/resources/marketing-terms/what-is-adtech">What is AdTech? The fundamental guide</a></li>

</ul>
</details>

**社区讨论**: 社区评论反应不一：有人质疑反垄断补救措施的有效性，建议对垄断企业征收累进税。另一些人则对谷歌声称其广告技术业务规模较小的说法表示怀疑，指出 Alphabet 整体收入的 75%来自广告。还有人批评法院接受谷歌承诺停止滥用行为，而未采取更强有力的结构性补救措施。

**标签**: `#Google`, `#antitrust`, `#ad tech`, `#regulation`, `#monopoly`

---

<a id="item-4"></a>
## [谷歌 DeepMind 推出主动网络防御计划](https://deepmind.google/blog/proactive-cyber-defense-for-governments-and-enterprises/) ⭐️ 8.0/10

谷歌 DeepMind 宣布了一项新计划，专注于为政府和企业的主动网络防御，利用 AI 在威胁发生前进行预测和缓解。 这标志着领先的 AI 研究实验室将先进 AI 应用于国家和企业安全的重要一步，可能将网络安全从被动应对转向主动防御。这可能影响政府和企业采用 AI 驱动的防御机制。 该公告未具体说明技术或合作伙伴，但表明 DeepMind 进入网络安全领域并专注于主动措施。关于实施、时间表和具体 AI 模型的细节尚未披露。

rss · Google DeepMind Blog · 9月2日 16:24

**背景**: 主动网络防御涉及在威胁造成损害之前进行预测和中和，使用威胁情报、预测分析和自动响应等技术。谷歌 DeepMind 以 AlphaGo 和 AlphaFold 等 AI 突破而闻名，现在将其专业知识应用于网络安全，这是一个传统上由防火墙和杀毒软件等被动方法主导的领域。

**标签**: `#AI`, `#cybersecurity`, `#DeepMind`, `#defense`, `#enterprise`

---