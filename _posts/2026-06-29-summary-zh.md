---
layout: default
title: "Horizon Summary: 2026-06-29 (ZH)"
date: 2026-06-29
lang: zh
---

> 从 23 条内容中筛选出 2 条重要资讯。

---

1. [llama.cpp b9840 新增 DeepSeek V4 支持](#item-1) ⭐️ 8.0/10
2. [HackerRank 开源 ATS，揭示 LLM 评分缺陷](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [llama.cpp b9840 新增 DeepSeek V4 支持](https://github.com/ggml-org/llama.cpp/releases/tag/b9840) ⭐️ 8.0/10

llama.cpp 版本 b9840 新增了对 DeepSeek V4 的支持，包括模型转换、推理和聊天模板更新。该版本还包含了多位社区成员的贡献，如 sinkhorn epsilon 修正和 pro 模型支持。 该版本使得通过 llama.cpp 在消费级硬件上本地推理 DeepSeek V4（一个前沿的 1 万亿参数模型）成为可能，极大地扩展了大规模 AI 模型对开发者和研究人员的可访问性。 该实现包括新的架构特定图输入、对 flash attention 的支持以及内联聊天模板的机制。该版本还预留了最坏情况的 KV 缓存，并启用了部分检查点以提高效率。

github · github-actions[bot] · 6月29日 10:25

**背景**: llama.cpp 是一个开源的 C/C++ 库，用于在 CPU 和 GPU 上高效推理大型语言模型。DeepSeek V4 是由 DeepSeek 开发的 1 万亿参数模型，采用 Engram 记忆架构，性能可与 GPT-4.5 和 Claude 4.5 等模型竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepseek.ai/deepseek-v4">DeepSeek V 4 (2026) — 1T Params, Benchmarks & Pricing</a></li>
<li><a href="https://en.wikipedia.org/wiki/Llama.cpp">llama.cpp - Wikipedia</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#DeepSeek V4`, `#AI inference`, `#open-source`, `#machine learning`

---

<a id="item-2"></a>
## [HackerRank 开源 ATS，揭示 LLM 评分缺陷](https://danunparsed.com/p/hackerrank-open-source-ats) ⭐️ 8.0/10

HackerRank 已在 GitHub 上开源其申请人跟踪系统（ATS），任何人都可以测试 LLM 如何对简历进行评分。详细分析显示，由于 LLM 的非确定性，同一份简历在多次运行中可能获得截然不同的分数（例如 90、74、88、83）。 这很重要，因为许多公司使用基于 AI 的 ATS 来筛选候选人，而非确定性的评分意味着合格的申请人可能因随机性而被不公平地拒绝或通过。这凸显了在没有适当确定性保障的情况下依赖 LLM 进行招聘决策的关键缺陷。 该 ATS 使用温度为 0.1 的 LLM 来提取和评分简历部分，但即使在温度 0 下，分数也会显著变化（例如六次运行中分别为 27、34、32、34、34、30）。非确定性是一个根本性的设计缺陷，而不是可以通过调整消除的 bug。

hackernews · sambellll · 6月29日 01:44 · [社区讨论](https://news.ycombinator.com/item?id=48713832)

**背景**: 申请人跟踪系统（ATS）是雇主用来管理和筛选求职申请的软件工具。许多现代 ATS 集成了大型语言模型（LLM）来解析简历并根据职位描述对候选人进行评分。然而，LLM 本质上是随机的，这意味着即使输入相同，其输出也可能不同，这给招聘的可重复性带来了挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://danunparsed.com/p/hackerrank-open-source-ats">HackerRank open sourced its ATS. My resume scored 90/100. Oh wait 74/100. No — 88/100. Actually 83/100.</a></li>
<li><a href="https://www.reddit.com/r/leetcode/comments/1tynum1/hacker_rank_open_sourced_their_ats_system_so_you/">r/leetcode on Reddit: Hacker Rank open sourced their ATS system so you can know exactly why AI rejected your resume</a></li>

</ul>
</details>

**社区讨论**: 评论者就 LLM 非确定性在招聘中的影响展开辩论，一些人认为确定性输出对于简历评分来说并不一定是可取的。其他人分享了构建类似系统的经验，指出虽然不完美，但 AI 评分仍然节省时间，并能可靠地过滤掉非常低或高质量候选人。

**标签**: `#LLM`, `#ATS`, `#resume scoring`, `#HackerRank`, `#job search`

---