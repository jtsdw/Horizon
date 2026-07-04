---
layout: default
title: "Horizon Summary: 2026-07-04 (ZH)"
date: 2026-07-04
lang: zh
---

> 从 18 条内容中筛选出 2 条重要资讯。

---

1. [Mistral 发布 Leanstral-1.5：用于形式验证的 6B 活跃参数模型](#item-1) ⭐️ 9.0/10
2. [Hugging Face Transformers v5.13.0 新增 KimiK 2.5-2.7](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Mistral 发布 Leanstral-1.5：用于形式验证的 6B 活跃参数模型](https://www.reddit.com/r/LocalLLaMA/comments/1umgdhx/mistral_released_leanstral15119ba6b/) ⭐️ 9.0/10

Mistral 发布了 Leanstral-1.5，一个拥有 6B 活跃参数的模型，在形式验证方面取得了最先进的结果，包括在 miniF2F 基准上达到饱和，解决了 672 个 PutnamBench 问题中的 587 个，并在 FATE-H 和 FATE-X 上分别达到 87% 和 34%。它还在 57 个开源仓库中发现了 5 个以前未知的错误。 此次发布意义重大，因为它表明相对较小且高效的模型可以在形式验证这一确保软件正确性的关键领域取得突破性性能。开源的 Apache-2.0 许可证使这些能力广泛可用，可能加速自动化定理证明在软件开发中的采用。 Leanstral-1.5 采用混合专家架构，总参数为 119B，但每个 token 仅激活 6B 参数，因此推理效率高。它通过中期训练、监督微调和基于 CISPO 算法的强化学习进行训练，该算法通过裁剪重要性采样权重来实现稳定的策略优化。

reddit · r/LocalLLaMA · /u/Tall-Ad-7742 · 7月3日 14:44

**背景**: 形式验证使用数学证明来验证软件或硬件是否符合其规范，提供比测试更强的保证。像 miniF2F 和 PutnamBench 这样的基准包含来自竞赛的形式化数学问题，用于评估自动化定理证明器。CISPO 是一种强化学习算法，通过裁剪重要性采样权重来提高训练稳定性和样本效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openai/miniF2F">GitHub - openai/miniF2F: Formal to Formal Mathematics Benchmark · GitHub</a></li>
<li><a href="https://www.emergentmind.com/topics/cispo-algorithm">CISPO: Clipped Importance Sampling RL - emergentmind.com</a></li>
<li><a href="https://trishullab.github.io/PutnamBench/">PutnamBench : A Multilingual Mathematics Benchmark for Formal...</a></li>

</ul>
</details>

**标签**: `#AI`, `#formal verification`, `#open-source`, `#LLM`, `#theorem proving`

---

<a id="item-2"></a>
## [Hugging Face Transformers v5.13.0 新增 KimiK 2.5-2.7](https://github.com/huggingface/transformers/releases/tag/v5.13.0) ⭐️ 8.0/10

Hugging Face Transformers v5.13.0 新增了对 KimiK 2.5、2.6 和 2.7 的支持，这是一个用于编码和自主任务的开源多模态智能体模型，同时还加入了 MiMo-V2-Flash 和 Nemotron 3.5 ASR。 此版本将前沿的多模态智能体能力引入广泛使用的 Transformers 库，使开发者能够轻松地将长周期编码和基于群体的任务编排集成到他们的项目中。 KimiK 2.5 是一个原生多模态模型，联合优化文本和视觉，支持跨 Rust、Go 和 Python 等语言的长期编码、主动自主执行和基于群体的任务编排。

github · vasqu · 7月3日 16:06

**背景**: Hugging Face Transformers 是一个流行的开源库，提供数千个用于自然语言处理、计算机视觉等领域的预训练模型。多模态智能体模型结合文本和视觉输入，在较长时间内执行复杂的自主任务，这是人工智能领域的一个增长趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2602.02276">[2602.02276] Kimi K2.5: Visual Agentic Intelligence</a></li>
<li><a href="https://www.kimi.com/ai-models/kimi-k2-5">Kimi K2.5 | Open Visual Agentic Model for Real Work</a></li>
<li><a href="https://oracore.dev/en/news/kimi-k2-6-turns-agents-into-a-swarm-en">Kimi K2.6 turns agents into a swarm | OraCore.dev</a></li>

</ul>
</details>

**标签**: `#transformers`, `#huggingface`, `#multimodal`, `#AI`, `#open-source`

---