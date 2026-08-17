---
layout: default
title: "Horizon Summary: 2026-08-17 (ZH)"
date: 2026-08-17
lang: zh
---

> 从 12 条内容中筛选出 2 条重要资讯。

---

1. [Anthropic 公开 Claude 系统提示词以提升透明度](#item-1) ⭐️ 8.0/10
2. [AI 模型在权重上故意变笨](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 公开 Claude 系统提示词以提升透明度](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 已公开发布 Claude 模型在 claude.ai 和移动应用上使用的系统提示词，使用户和研究人员能够查看给模型的确切指令。此次发布包括多个模型的提示词，如 Opus 4.8 以及新提到的 Claude Fable 5 和 Claude Mythos 5。 这一透明化举措意义重大，因为它让社区能够分析和理解 Claude 的行为，增进信任，并促进关于 AI 安全和治理的更知情讨论。同时，它为开发者和研究人员研究提示工程和模型行为提供了宝贵的见解。 系统提示词包含防止幻觉的指令，例如告诉 Claude 在假设图像存在之前先验证图像是否确实存在。提示词还引导 Claude 将产品相关问题引导至官方支持页面。社区成员 Simon Willison 创建了这些提示词变更的 git 历史，突出显示了诸如引用 Claude Fable 5 和 Claude Mythos 5 等值得注意的新增内容。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是在对话开始时给 AI 模型的初始指令，用于设置上下文和引导行为。它们通常包括当前日期、使用指南和具体的行为规则。通过发布这些提示词，Anthropic 旨在提高透明度，并允许外部审查其模型如何被引导。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/release-notes/system-prompts">System Prompts - Claude Platform Docs</a></li>
<li><a href="https://simonwillison.net/2025/May/25/claude-4-system-prompt/">Highlights from the Claude 4 system prompt</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，用户赞赏这种透明度以及追踪随时间变化的能力。然而，一些用户对提示词的长度和具体性表示担忧，认为更短的提示词可能更有效。此外，还有人担心论坛上可能审查或删除负面 AI 故事。

**标签**: `#AI`, `#Claude`, `#system prompts`, `#transparency`, `#Anthropic`

---

<a id="item-2"></a>
## [AI 模型在权重上故意变笨](https://w4g1.dev/blog/models-are-getting-dumber-on-purpose) ⭐️ 8.0/10

文章认为，AI 模型正有意地减少在权重中存储知识，转而更多地依赖外部工具和检索机制。这一趋势可能改变模型的评估和使用方式。 这种转变可能导致更小、更高效的模型，更易于更新且更不易产生幻觉，可能重塑 AI 行业从扩大参数规模转向整合外部知识源的焦点。同时，它也对基准测试和模型卡的设计提出了疑问。 文章引用了 SimpleQA（一个事实回忆基准），当前领先的 Gemini 2.5 Pro 得分仅为 53%，凸显了基于权重知识的局限性。文章还提到，随着权重知识在数年内过时，模型卡最终可能不再列出知识截止日期。

hackernews · hruvhwe · 8月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=49322695)

**背景**: AI 模型将训练数据中学习到的模式存储为称为权重的数值，这些数值决定了模型的行为。检索增强生成（RAG）是一种技术，允许 LLM 在生成响应前从外部数据源获取信息，从而减少对存储知识的依赖。这种方法可以在不重新训练模型的情况下提高准确性和时效性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/07/28/technology/open-weight-ai.html">What Is Open-Weights A.I.? - The New York Times</a></li>
<li><a href="https://en.wikipedia.org/wiki/Retrieval-augmented_generation">Retrieval - augmented generation - Wikipedia</a></li>
<li><a href="https://aws.amazon.com/what-is/retrieval-augmented-generation/">What is RAG ? - Retrieval - Augmented Generation AI Explained - AWS</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了各种观点：有人设想可插拔的知识库以实现模块化专业知识，也有人批评文章引用的基准过时，并指出这一趋势可能并不那么明确。还有人怀疑完全将知识与推理分离，因为推理往往依赖于世界知识。

**标签**: `#AI`, `#LLM`, `#model architecture`, `#knowledge retrieval`, `#future of AI`

---