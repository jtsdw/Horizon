---
layout: default
title: "Horizon Summary: 2026-11-14 (ZH)"
date: 2026-11-14
lang: zh
---

> 从 30 条内容中筛选出 3 条重要资讯。

---

1. [llama.cpp 发布 v1.0.0，稳定 API 并新增多项功能](#item-1) ⭐️ 9.0/10
2. [美国联邦航空管理局因电信故障下令全国停飞，4.5 小时后解除](#item-2) ⭐️ 8.0/10
3. [OpenAI 推出 ChatGPT 钱包，支持 AI 代理购物](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [llama.cpp 发布 v1.0.0，稳定 API 并新增多项功能](https://github.com/ggml-org/llama.cpp/releases/tag/v1.0.0) ⭐️ 9.0/10

llama.cpp 发布了 v1.0.0 版本，从公共 API 中移除了 35 个已弃用的函数和 defrag_thold 参数，并将 NextN/推测解码 API 提升至 llama.h。此版本还新增了 OCP FP8 KV 缓存、带可配置 CPU 份额的主机内存 MoE 专家缓存、新模型架构（Kimi-K3.1-Pro、Ripple、xing4_0）、drama-3 TTS、视觉支持，并加固了 llama-server 的安全性。 达到 v1.0.0 稳定了众多下游项目所依赖的公共 API，减少了未来更新带来的破坏，并标志着这个最广泛使用的本地 LLM 推理引擎走向成熟。FP8 KV 缓存和 MoE 专家缓存等新功能提高了内存效率和性能，使本地推理在消费级硬件上更加可行。 FP8 KV 缓存支持使用图级缩放，并可选择静态的每张量缩放；MoE 缓存允许为未命中配置 CPU 份额，并采用 LRFU/ClassLRU 替换策略。llama-server 现在包含针对 SSRF、CORS、DNS 重绑定和 MCP 工具取消的安全修复，并新增了兼容 OpenAI 的 /v1/audio/speech 端点。

github · github-actions[bot] · 11月13日 10:20

**背景**: llama.cpp 是一个基于 ggml 张量库的开源 C/C++ 大语言模型推理引擎，支持在 CPU 和 GPU 上本地运行模型。它支持量化和其他优化，以降低内存占用并加速推理。公共 API（llama.h）被许多下游项目使用，因此对其更改可能产生广泛影响。1.0.0 版本是经过多年快速发展后的首个稳定 API 版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiweekly.co/alerts/llamacpp-merges-fp8-kv-cache-support-for-ocp-fp8-models">llama.cpp merges FP8 KV-cache support for OCP-FP8 models</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp/blob/master/docs/moe-cache.md">llama.cpp/docs/moe-cache.md at master · ggml-org/llama.cpp</a></li>
<li><a href="https://deepwiki.com/ggml-org/llama.cpp/8.3-speculative-decoding">Speculative Decoding | ggml-org/llama.cpp | DeepWiki</a></li>

</ul>
</details>

**标签**: `#llm-inference`, `#llama.cpp`, `#ggml`, `#api-stability`, `#release`

---

<a id="item-2"></a>
## [美国联邦航空管理局因电信故障下令全国停飞，4.5 小时后解除](https://www.nbcnews.com/news/us-news/faa-orders-nationwide-ground-stop-departing-flights-reasons-safety-rcna609247) ⭐️ 8.0/10

2026 年 11 月 13 日，美国联邦航空管理局（FAA）因影响空中交通管制的通信中断，对全美所有离港航班发布了全国范围的停飞令。该停飞令在大约 4.5 小时后解除，但此前已导致全国范围内大量航班延误和取消。 全国范围的停飞是极其罕见的事件，会中止美国所有离港空中交通，凸显了关键基础设施的脆弱性以及电信故障对国家空域系统的连锁影响。该事件影响了数千名乘客，并引发了对 FAA 老化系统韧性的担忧。 早期报告显示，中断影响了由 L3Harris Technologies 管理的一个电信网络，该网络负责处理空中交通管制员与飞行员通信所用的无线电频率；目前尚不清楚雷达信号是否也受到影响。官员表示该问题与近期微软服务中断无关，白宫官员将原因描述为新设备压垮了旧系统，并强调需要进行完整的系统 overhaul。

hackernews · zulln · 11月13日 21:05 · [社区讨论](https://news.ycombinator.com/item?id=50489641)

**背景**: FAA 的国家空域系统（NAS）依赖一个由通信、导航和监视设备组成的复杂网络来管理空中交通。停飞是一种交通管理措施，当空中交通管制无法在特定空域安全处理飞机时使用，通常由于恶劣天气、安全威胁或设备故障。FAA 电信基础设施（FTI）是支持空中交通管制运行的关键网络，过去的故障（如 2009 年的一次）已凸显了这些系统的脆弱性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/us-news/live/2026/nov/13/us-politics-latest-news-updates-democrats-republicans-donald-trump-van-hollen-chuck-schumer?page=with:block-6af789c78f080d8d1c27a4b6">US flight outage live updates: FAA grounds thousands... | The Guardian</a></li>
<li><a href="https://www.usatoday.com/story/news/nation/2026/11/13/faa-orders-nationwide-groundstop-at-us-airports-citing-safety/92765499007/">FAA orders ground stop at US airports over safety concerns: Live...</a></li>
<li><a href="https://abcnews.com/US/nationwide-ground-stop-ordered-airports-faa/story?id=138121848">FAA issues rare nationwide ground stop ; no indication of... - ABC News</a></li>

</ul>
</details>

**社区讨论**: 评论者指出官方信息稀少并进行了猜测，一些人将其与 2009 年 FAA 电信基础设施故障相提并论，另一些人引用《华尔街日报》的报道称中断影响了 L3Harris 管理的、负责空中交通管制员无线电频率的网络。白宫简报将原因归咎于新设备压垮旧系统，强化了更换整个系统的呼声。

**标签**: `#FAA`, `#aviation`, `#infrastructure`, `#outage`, `#telecommunications`

---

<a id="item-3"></a>
## [OpenAI 推出 ChatGPT 钱包，支持 AI 代理购物](https://openai.com/index/introducing-chatgpt-wallet) ⭐️ 8.0/10

OpenAI 推出了 ChatGPT 钱包，这是一种安全的支付方式，允许 ChatGPT Work、Codex 和 dots 中的 AI 代理在用户批准并享有现有信用卡保护的情况下完成购买。 这标志着向代理式商务迈出了重要一步，AI 代理可以自主处理购物任务，可能改变用户与金融系统和电子商务平台的互动方式。 该钱包要求每笔购买都需用户批准，并将现有信用卡保护扩展到代理发起的交易，但技术实现细节和支持地区尚未披露。

rss · OpenAI Blog · 11月13日 15:00

**背景**: 代理式商务是指 AI 代理代表用户独立执行购买流程，这与需要在关键决策点进行人工交互的传统电子商务不同。ChatGPT Work 是 OpenAI 的企业生产力平台，Codex 是其编码代理，dots 是一款用于持续后台工作的新产品。此次发布将支付能力直接集成到这些 AI 工具中，既带来了机遇，也引发了对安全和欺诈的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agentic_commerce">Agentic commerce</a></li>
<li><a href="https://openai.com/chatgpt-work/">ChatGPT Work for every team | OpenAI</a></li>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI agents`, `#payments`, `#agentic commerce`, `#security`

---