---
layout: default
title: "Horizon Summary: 2026-07-12 (ZH)"
date: 2026-07-12
lang: zh
---

> 从 17 条内容中筛选出 2 条重要资讯。

---

1. [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](#item-1) ⭐️ 8.0/10
2. [DeepSeek 正在开发自研 AI 芯片](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 将 Model Runner V2 设为所有稠密模型的默认执行路径，并移除了旧版 PagedAttention 实现。同时引入了 LLaVA-OneVision-2、GLM-5 等新模型，新增流式解析引擎，并支持异构词表的通用推测解码。 此版本标志着 vLLM 的重大架构转变，通过标准化 Model Runner V2 提升了性能和可维护性。移除 PagedAttention 以及新增通用推测解码等功能将惠及整个 LLM 推理生态，使 vLLM 更快、更灵活。 Model Runner V2 现在支持 EVS、实时嵌入、Mamba 混合模型的前缀缓存以及多模态前缀双向注意力。Transformers 建模后端现在与原生 vLLM 速度相当，此版本包含来自 232 位贡献者的 558 次提交。

github · khluu · 7月11日 20:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎，使用 PagedAttention 高效管理键值缓存内存。Model Runner V2 是重新设计的执行路径，旨在比原始 V1 更简洁、更模块化。移除旧版 PagedAttention 表明新后端（V1/MRv2）已成为标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/latest/design/paged_attention/">Paged Attention - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/v0.14.1/api/vllm/multimodal/evs/">evs - vLLM</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#open source`, `#AI infrastructure`, `#release`

---

<a id="item-2"></a>
## [DeepSeek 正在开发自研 AI 芯片](https://www.reddit.com/r/LocalLLaMA/comments/1uu15mz/chinas_deepseek_developing_its_own_ai_chip/) ⭐️ 8.0/10

据路透社报道，中国 AI 初创公司 DeepSeek 正在开发自研 AI 芯片，该芯片专为推理设计，旨在减少对英伟达和华为芯片的依赖。 此举可能在地缘政治紧张局势下重塑 AI 硬件格局，有望降低 DeepSeek 对出口管制的脆弱性，并增强中国 AI 产业的自主性。 该芯片专注于推理而非训练，项目仍处于早期阶段，量产时间表尚未确定。

reddit · r/LocalLLaMA · /u/TheRealMasonMac · 7月12日 01:04

**背景**: DeepSeek 在 2025 年初凭借其 R1 模型引起全球关注，该模型尽管因美国出口限制而使用性能较弱的芯片，但仍能与西方顶级 AI 模型竞争。开发自研芯片将使 DeepSeek 进一步优化性能并降低供应链风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/">EXCLUSIVE: China's DeepSeek developing its own AI chip ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-07-07/chinese-ai-startup-deepseek-developing-own-ai-chip-reuters-says">Chinese AI Startup DeepSeek Developing Own AI Chip, Reuters Says - Bloomberg</a></li>
<li><a href="https://www.usnews.com/news/top-news/articles/2026-07-07/exclusive-chinas-deepseek-developing-its-own-ai-chip-sources-say">Exclusive-China's DeepSeek Developing Its Own AI Chip ...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#DeepSeek`, `#hardware`, `#China`, `#AI industry`

---