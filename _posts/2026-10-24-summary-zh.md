---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 22 条内容中筛选出 3 条重要资讯。

---

1. [月之暗面发布 Kimi K3.1 Pro 及高速版本](#item-1) ⭐️ 8.0/10
2. [Block 发布 Dessa，号称最真实的全双工语音模型](#item-2) ⭐️ 8.0/10
3. [OpenAI 将 Habitat 存储扩展至 10 亿用户，读取速度提升 12 倍](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [月之暗面发布 Kimi K3.1 Pro 及高速版本](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

2026 年 10 月 24 日，月之暗面（Moonshot AI）发布了 Kimi K3.1 Pro，这是其全新 K3.1 系列的首个模型，同时推出了速度更快的 Kimi K3.1 Pro Highspeed 版本。该公司称 K3.1 Pro 是其迄今最强大的 3T 级开放权重模型，拥有 100 万 token 的上下文窗口，并在编程、3D 创作、金融研究和智能体能力方面有显著提升。 此次发布使月之暗面成为开放权重前沿模型领域的有力竞争者，Pac-Man 基准等独立评测显示其性能与 Claude Sonnet 5.5 大致相当，而成本不到后者的一半。这表明中国的开放权重模型在能力和价格上的竞争力日益增强，可能对定价形成压力并加速开发者的采用。 Kimi K3.1 Pro 是一款 3T 级开放权重模型，上下文窗口达 100 万 token；社区在 Pac-Man 基准上的测试显示，它以 93 分与 Claude Sonnet 5.5 持平，成本为 0.68 美元、耗时 11 分钟，而 Sonnet 为 1.61 美元、14 分钟。不过，用户对使用限额以及移除网络安全相关训练数据提出了担忧，这可能影响某些安全研究用例。

hackernews · Jowsey · 10月23日 16:59 · [社区讨论](https://news.ycombinator.com/item?id=50212065)

**背景**: Kimi 是中国 AI 初创公司月之暗面（Moonshot AI）开发的一系列大语言模型。开放权重模型会公开其训练后的参数，使研究者和开发者能够在本地运行和微调，这与 OpenAI 或 Anthropic 等仅提供 API 的闭源模型不同。Artificial Analysis 是一个独立的基准评测平台，从质量、价格、输出速度和延迟等方面对模型进行比较，帮助开发者做出明智选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-1-pro-quickstart">Kimi K3.1 Pro - Kimi API Platform</a></li>
<li><a href="https://www.unite.ai/moonshot-ai-releases-kimi-k3-1-pro-first-model-in-new-k3-1-series/">Moonshot AI Releases Kimi K3.1 Pro, First Model in New K3.1 ...</a></li>
<li><a href="https://artificialanalysis.ai/">AI Model & API Providers Analysis | Artificial Analysis</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一：一位测试者指出，该模型有时自称 Kimi，有时又假定自己是 ChatGPT，并提及“评估者”或幻影指令行，引发了对身份和对齐行为的疑问。另一位用户称赞其在 Pac-Man 基准上的性价比，但也有人批评 5 小时使用限额使订阅变得不可用，并质疑从训练数据中移除网络安全数据的做法。

**标签**: `#llm`, `#ai-models`, `#moonshot-ai`, `#benchmarks`, `#model-release`

---

<a id="item-2"></a>
## [Block 发布 Dessa，号称最真实的全双工语音模型](https://block.xyz/dessa) ⭐️ 8.0/10

Block 发布了 Dessa，这是一款新的全双工语音模型，号称是迄今为止最真实的。该模型据称可在 MacBook Pro M4 Max 或更高配置上本地运行，并且仅使用一台 NVIDIA GB200 NVL72 系统完成训练。 如果 Dessa 兑现其承诺，它可能在消费设备上实现高度自然、低延迟的语音交互，而无需依赖云端，从而显著推进本地 AI 能力。这也表明训练先进的语音模型可能不需要庞大的计算集群，降低了小型团队的门槛。 该模型专为全双工对话设计，意味着它可以同时听和说，从而实现更自然的打断和反馈。在单台 GB200 NVL72（一台配备 72 块 Blackwell GPU 的机架级系统）上训练，在效率方面值得注意，但关于数据集大小和模型架构的细节仍然很少。

hackernews · dsr12 · 10月23日 19:09 · [社区讨论](https://news.ycombinator.com/item?id=50213925)

**背景**: 全双工语音模型是对话 AI 的最新进展，允许系统连续处理音频并实时响应，而无需等待用户说完。这与传统的轮次对话模型形成对比。NVIDIA GB200 NVL72 是一种液冷机架级系统，集成了 36 个 Grace CPU 和 72 个 Blackwell GPU，专为大规模 AI 训练和推理设计。在 MacBook Pro 等设备上本地运行此类模型是端侧 AI 大趋势的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/gb200-nvl72/">GB200 NVL72 | NVIDIA</a></li>
<li><a href="https://arxiv.org/abs/2405.19487">[2405.19487] A Full-duplex Speech Dialogue Scheme Based On ... DyaPlex: Full-Duplex Speech-Motion Model for Dyadic Interaction GitHub - Ruiqi-Yan/Awesome-Full-Duplex-SDM: A curated list of ... GitHub - cyrta/awesome-full-duplex-speech-to-speech: A ... Fullduplex — an observatory for speech-to-speech, full-duplex ...</a></li>
<li><a href="https://llmpicker.blog/posts/mac-for-local-llms/">Mac for Local LLMs: The Complete Apple Silicon Guide (2026)</a></li>

</ul>
</details>

**社区讨论**: 评论者对低延迟和表现力印象深刻，有人称其为“独立 AI 的一项了不起的成就”。然而，其他人批评“最真实”的说法是营销炒作，并认为双工演示过于人工化，存在强行打断和不自然的笑声。一些人还推测了训练数据，指出听起来像播客。

**标签**: `#speech-model`, `#full-duplex`, `#AI`, `#local-inference`, `#machine-learning`

---

<a id="item-3"></a>
## [OpenAI 将 Habitat 存储扩展至 10 亿用户，读取速度提升 12 倍](https://openai.com/index/scaling-storage-one-billion-users-part-two) ⭐️ 8.0/10

OpenAI 发布了关于扩展其在线存储平台 Habitat 的工程博客第二部分，详细介绍了如何通过可靠的多租户架构、全局缓存和 Azure Cosmos DB 集成，为 ChatGPT 实现 12 倍的读取速度提升。该系统目前每秒处理超过 7000 万次请求，覆盖近 40 个地理区域，每周服务超过 10 亿用户。 这一深度剖析展示了大型 AI 公司如何应对极端规模的存储挑战，为分布式系统和基础设施工程师提供了宝贵经验。多租户、全局缓存和 Cosmos DB 等技术可能影响云原生应用中构建低延迟、高吞吐存储层的最佳实践。 Habitat 经历了从单一多租户 Azure Cosmos DB 容器到单租户后端容器，再回归多租户模型的演变，凸显了隔离性与效率之间的权衡。在保持每秒 7000 万次请求和近 40 个区域可靠性的同时，实现了 12 倍的读取速度提升。

rss · OpenAI Blog · 10月23日 17:00

**背景**: Habitat 是 OpenAI 的内部在线存储平台，为 ChatGPT 等产品提供快速可靠的数据访问。Azure Cosmos DB 是微软的全球分布式 NoSQL 数据库服务，专为高可用性和低延迟设计。多租户是一种架构模式，其中单个软件实例为多个客户服务，需要精心设计以确保性能和隔离性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/scaling-storage-one-billion-users-part-one/">Rapidly scaling online storage to serve over 1 ... - OpenAI</a></li>
<li><a href="https://openai.com/index/scaling-storage-one-billion-users-part-two/">Rapidly scaling online storage to serve over 1 ... - OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Azure_Cosmos_DB">Azure Cosmos DB</a></li>

</ul>
</details>

**标签**: `#distributed-systems`, `#storage`, `#scalability`, `#caching`, `#cloud-infrastructure`

---