---
layout: default
title: "Horizon Summary: 2026-07-18 (ZH)"
date: 2026-07-18
lang: zh
---

> 从 22 条内容中筛选出 2 条重要资讯。

---

1. [首次在宜居带岩石系外行星发现大气层](#item-1) ⭐️ 8.0/10
2. [Kimi K3 通过鹈鹕基准测试揭示隐藏提示](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [首次在宜居带岩石系外行星发现大气层](https://www.bbc.com/news/articles/cy4kdd1e0ejo) ⭐️ 8.0/10

詹姆斯·韦伯空间望远镜在距离地球 48 光年的红矮星宜居带内，探测到岩石系外行星 LHS 1140b 的大气层。这是首次在宜居带岩石行星上确认存在大气层。 这一发现是系外行星科学的重大里程碑，为研究潜在宜居岩石世界的大气层打开了大门。然而，宿主星是红矮星，因潮汐锁定和恒星活动，其真正的地球相似性受到质疑。 LHS 1140b 的质量为地球的 6.38 倍，每 24.7 天绕恒星公转一周，距离恒星 0.0957 天文单位。JWST 的发射光谱排除了迷你海王星的可能性，确认了岩石成分和大气层的存在。

hackernews · neversaydie · 7月17日 14:06 · [社区讨论](https://news.ycombinator.com/item?id=48947560)

**背景**: 红矮星比太阳更冷、更暗，因此其宜居带非常靠近恒星，导致行星被潮汐锁定，一面永远朝向恒星。红矮星还容易发生强烈耀斑，可能剥离行星大气。LHS 1140b 属于超级地球，即比地球大但比海王星小的行星，这类行星在银河系中很常见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://science.nasa.gov/exoplanet-catalog/lhs-1140-b/">LHS 1140 b - NASA Science</a></li>
<li><a href="https://www.bbc.com/news/articles/cy4kdd1e0ejo">First atmosphere found around Earth-like planet LHS 1140 b</a></li>
<li><a href="https://www.sciencenews.org/article/rocky-exoplanet-helium-atmosphere">This “exotic weirdo” exoplanet has a rocky surface and an atmosphere</a></li>

</ul>
</details>

**社区讨论**: 社区既兴奋又怀疑。用户 tulio_ribeiro 最初因红矮星宜居性问题质疑其地球相似性，但后来承认 JWST 数据排除了迷你海王星的可能性。其他人则讨论了星际探测器的推进系统和费米悖论。

**标签**: `#exoplanets`, `#JWST`, `#astronomy`, `#habitable zone`, `#atmosphere`

---

<a id="item-2"></a>
## [Kimi K3 通过鹈鹕基准测试揭示隐藏提示](https://simonwillison.net/2026/Jul/16/kimi-k3/) ⭐️ 8.0/10

Simon Willison 使用“骑自行车的鹈鹕”SVG 基准测试分析了 Moonshot AI 的 Kimi K3 模型，发现了一个 85 个 token 的隐藏系统提示，并引发了关于基准测试有效性的社区讨论。 这项分析强调了创造性、对抗性基准测试在评估 LLM 方面的重要性，超越了标准指标，并揭示了隐藏的系统提示如何影响分词和模型行为。 Kimi K3 是一个 2.8 万亿参数的开源模型，具有 100 万 token 的上下文窗口，采用 Kimi Delta Attention (KDA)。鹈鹕基准测试显示，Kimi K3 的分词器对提示计数为 95 个 token，而 OpenAI 和 Anthropic 计数为 10 个，暗示存在 85 个 token 的隐藏系统提示。

hackernews · droidjj · 7月17日 14:21 · [社区讨论](https://news.ycombinator.com/item?id=48947717)

**背景**: “骑自行车的鹈鹕”基准测试是 Simon Willison 在 2024 年底创建的非正式测试，要求 LLM 生成一只骑自行车的鹈鹕的 SVG 图像。它评估模型生成正确、结构良好的 SVG 代码的能力。Kimi K3 是中国 AI 初创公司 Moonshot AI 的最新旗舰模型，以开源形式发布，拥有 2.8 万亿参数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2024/Oct/25/pelicans-on-a-bicycle/">Pelicans on a bicycle</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://venturebeat.com/technology/chinas-moonshot-ai-releases-kimi-k3-the-largest-open-source-model-ever-rivaling-top-u-s-systems">China’s Moonshot AI releases Kimi K3, the largest open-source model ever, rivaling top U.S. systems | VentureBeat</a></li>

</ul>
</details>

**社区讨论**: 评论者就鹈鹕提示是否可能出现在训练数据中展开辩论，有人指出 Simon 自己的博客内容会出现在 LLM 中。其他人提出了对抗性扩展，如 SWE-bench-adversarial-pelican-gen，以测试代理工具调用，并建议每个模型多次运行基准测试以确保统计有效性。

**标签**: `#LLM`, `#benchmark`, `#Kimi K3`, `#tokenization`, `#model evaluation`

---