---
layout: default
title: "Horizon Summary: 2026-09-28 (ZH)"
date: 2026-09-28
lang: zh
---

> 从 25 条内容中筛选出 1 条重要资讯。

---

1. [Fireworks AI 发布开源推理模型 Ember-1](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Fireworks AI 发布开源推理模型 Ember-1](https://fireworks.ai/blog/ember-1) ⭐️ 8.0/10

Fireworks AI 发布了 Ember-1，这是一款由 Fireworks Research 基于 Kimi K3 构建的新型开源专用推理模型，可通过 Fireworks 的无服务器 API 以及 OpenRouter 调用。此次发布让许多用户首次得知，主要作为开源模型 API 提供商而闻名的 Fireworks 也拥有自己的模型研究团队。 此次发布表明，API 提供商正从单纯部署开源模型向上游延伸，开始主动研究并发布自己的模型，这可能会以专有实验室难以企及的方式加速开源模型的进步。同时，这也让开发者开始思考：是否应该信任一个与其所托管模型存在竞争关系的 API 提供商。 Ember-1 被定位为一款专用推理模型，旨在解决思考型模型“过度思考”的问题，据称在 Bedside Bench 专用智能指数上达到了帕累托前沿。它基于 Kimi K3 构建，通过 Fireworks 的无服务器 API 按 token 计费提供，可使用 Fireworks 的 Python 客户端、REST API 或 OpenAI 的 Python 客户端调用。

hackernews · gmays · 9月27日 17:31 · [社区讨论](https://news.ycombinator.com/item?id=49868830)

**背景**: Fireworks AI 是一个通过 API 托管和提供开源大语言模型的平台，同时也提供针对高达 1T+ 参数模型的训练和微调服务。推理模型是指在回答前生成较长思维链的大语言模型，这能提升难题的准确率，但在简单任务上可能浪费 token。Kimi K3 是月之暗面（Moonshot AI）推出的大型开放权重模型，也是 Ember-1 的基础模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fireworks.ai/blog/ember-1">Introducing Ember - 1 | Fireworks AI</a></li>
<li><a href="https://openrouter.ai/fireworks/ember-1">Ember - 1 - API Pricing & Providers | OpenRouter</a></li>
<li><a href="https://fireworks.ai/models/fireworks/ember-1">Ember - 1 API & Playground | Fireworks AI</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对开源模型的进步持积极态度，一位用户分享了自己使用 Qwen 3 0.6B 和 Astra 进行为期两天、仅用本地 CPU 训练英译 Bash 模型并取得成功的经历。也有人对 API 提供商从事模型研究表达了复杂情绪，担心依赖 Fireworks 作为服务商的风险，还有人比较了 Kimi K3 与更便宜的 Sol 等替代方案，对定价提出疑虑。

**标签**: `#AI`, `#machine-learning`, `#open-source`, `#model-training`, `#Fireworks-AI`

---