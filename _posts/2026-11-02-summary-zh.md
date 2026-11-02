---
layout: default
title: "Horizon Summary: 2026-11-02 (ZH)"
date: 2026-11-02
lang: zh
---

> 从 15 条内容中筛选出 1 条重要资讯。

---

1. [Heretic 2.0 发布：面向所有人的模型修改工具](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Heretic 2.0 发布：面向所有人的模型修改工具](https://www.reddit.com/r/LocalLLaMA/comments/1xl2tcm/heretic_20_released_model_modification_for/) ⭐️ 8.0/10

经过近五个月的开发，开源审查移除工具 Heretic 发布了其最大版本 Heretic 2.0。该版本引入了全新的默认引导方法——任意秩消融（ARA），并采用基于插件的架构，支持非交互式运行和更广泛的模型，同时还能实现抑制垃圾内容、减少谄媚等通用修改。 Heretic 在本地 LLM 社区中被广泛采用，拥有 37k GitHub 星标、超过 8,500 个 Hugging Face 模型和 8,800 万次下载，因此此次发布大幅降低了定制模型行为的门槛。它从单一的审查移除工具转变为通用修改平台，可能重塑实践者在不进行昂贵再训练的情况下对齐或去对齐模型的方式。 ARA 放弃了方向消融的秩-1 假设，转而使用由 L-BFGS 优化的目标函数逐个修改矩阵，从而在没有秩限制的情况下引导表示。Heretic 2.0 与 1.x 配置不向后兼容，用户需查阅迁移指南；经典消融方法仍作为选项保留。

reddit · r/LocalLLaMA · /u/-p-e-w- · 11月1日 13:16

**背景**: Heretic 是一个无需训练的工具，通过修改权重来移除基于 Transformer 的语言模型中的审查（常称为安全对齐），从而避免昂贵的后训练。其原始方法“方向消融”（abliteration）假设拒绝行为由模型残差空间中的单一方向表示，并抑制该方向。该工具因能创建无审查的模型变体而在本地 LLM 社区中流行起来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/p-e-w/heretic">GitHub - p-e-w/heretic: Training-free language model ...</a></li>
<li><a href="https://heretic-project.org/">Heretic</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#model-modification`, `#open-source`, `#ai-safety`, `#tooling`

---