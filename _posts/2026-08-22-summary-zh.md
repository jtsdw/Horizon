---
layout: default
title: "Horizon Summary: 2026-08-22 (ZH)"
date: 2026-08-22
lang: zh
---

> 从 27 条内容中筛选出 3 条重要资讯。

---

1. [NVIDIA AVO 在 ARC-AGI-3 上取得满分](#item-1) ⭐️ 9.0/10
2. [SGLang v0.5.18：710 个 PR、新模型支持与性能提升](#item-2) ⭐️ 8.0/10
3. [DeepMind 与游戏工作室合作，原型化 AI 游戏玩法](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [NVIDIA AVO 在 ARC-AGI-3 上取得满分](https://www.reddit.com/r/LocalLLaMA/comments/1vuh7to/nvidia_avo_got_100_on_arcagi3_it_completed_all/) ⭐️ 9.0/10

NVIDIA 的 AVO 模型在 ARC-AGI-3 基准测试中取得了 100% 的分数，在 25 个公开环境中完成了全部 183 个关卡，且无需任何指令、明确规则或既定目标。这标志着 AI 智能体智能的一个重要里程碑。 这一成就展示了自主目标发现和长时程规划方面的前沿能力，可能加速迈向通用人工智能（AGI）的进程。它也凸显了智能体架构在跨新任务泛化方面的潜力，对 AI 研究和应用产生影响。 AVO 是围绕 Anthropic 的 Claude Opus 5 模型的包装器，后者在相同的公开测试集上仅获得 30% 的分数，而 AVO 达到了 100%。NVIDIA 还将 AVO 与 GPT-5.6 Sol 配对用于具有挑战性的子集，展示了其与模型无关的设计。

reddit · r/LocalLLaMA · /u/theologi · 8月21日 14:01

**背景**: ARC-AGI-3 是一个交互式推理基准测试，挑战 AI 智能体探索新环境、即时获取目标并构建环境动态的内部模型。它旨在衡量 AI 智能体的人类智能，要求在没有明确指令的情况下对未见过的任务进行泛化。此前最先进的模型如 GPT-5.6 Sol 在该基准上仅获得 7.8% 的分数，凸显了任务的难度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">[2603.24621] ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence</a></li>
<li><a href="https://developer.nvidia.com/blog/nvidia-avo-reaches-100-on-arc-agi-3-demonstrating-a-frontier-level-general-purpose-architecture-for-long-horizon-autonomous-agents/">NVIDIA AVO Reaches 100% on ARC-AGI-3, Demonstrating...</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论可能包含对这一突破的兴奋，一些用户质疑基准测试的有效性以及 AVO 的成功是否真正表明 AGI 的进展。其他人可能讨论对 AI 安全的影响以及智能体架构在未来 AI 系统中的作用。

**标签**: `#AI`, `#AGI`, `#NVIDIA`, `#ARC-AGI`, `#Generalization`

---

<a id="item-2"></a>
## [SGLang v0.5.18：710 个 PR、新模型支持与性能提升](https://github.com/sgl-project/sglang/releases/tag/v0.5.18) ⭐️ 8.0/10

SGLang v0.5.18 已发布，包含来自 212 位贡献者的 710 个拉取请求。此版本新增了对多个模型的支持，包括 Muse Glimmer、SANA-Video 和 LTX-2.5，并引入了重叠检查点暂存和 TP LMHead 全对全通信等性能优化。 此版本显著扩展了 SGLang 的模型覆盖范围，新增了对多模态和扩散模型的支持，使其成为更通用的推理框架。性能改进，如更快的启动速度和更低的 LMHead 延迟，直接惠及在高端硬件上运行大型模型（如 DeepSeek-V4）的用户。 关键技术细节包括重叠检查点暂存，使 Qwen3-32B 启动速度提升高达 2.38 倍；TP LMHead 全对全通信将 DeepSeek-V4-Pro 的 LMHead 时间从 320 微秒降至 169 微秒。此版本还将编译内核缓存统一到 SGLANG_CACHE_DIR，并将依赖更新为 torch 2.13.0、flashinfer 0.6.17 和 sgl-kernel 0.4.6.post1。

github · Fridge003 · 8月22日 00:09

**背景**: SGLang 是一个用于大型语言模型和多模态模型的高性能服务框架，以其加速推理的 RadixAttention 技术而闻名。它与 vLLM 和 LMDeploy 等其他框架竞争。新支持的模型包括 Muse Glimmer（一个用于智能体任务的 300 亿参数模型）和 SANA-Video（一个用于视频生成的高效扩散模型）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sglang.io/">SGLang – Fast, Open-Source LLM & Multimodal Serving Framework</a></li>
<li><a href="https://github.com/sgl-project/sglang">sgl-project/ sglang : SGLang is a high-performance serving framework ...</a></li>
<li><a href="https://huggingface.co/unsloth/Muse-Glimmer-30B">unsloth/ Muse - Glimmer -30B · Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2509.24695">[2509.24695] SANA-Video: Efficient Video Generation with Block Linear Diffusion Transformer</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#SGLang`, `#release`, `#AI/ML`, `#open source`

---

<a id="item-3"></a>
## [DeepMind 与游戏工作室合作，原型化 AI 游戏玩法](https://deepmind.google/blog/from-atari-to-eve-online-building-on-15-years-of-ai-research-in-games/) ⭐️ 8.0/10

谷歌 DeepMind 宣布与游戏工作室合作，基于 15 年的游戏 AI 研究，原型化突破性的 AI 游戏玩法。该计划包括开发像 SIMA 2 这样的通用智能体，以在持久世界中解锁新的游戏体验。 这标志着将先进 AI 智能体整合到商业游戏中的重要一步，可能改变玩家体验和游戏设计。它还可能加速游戏行业对 AI 的采用，影响开发者和玩家。 该公告强调了 DeepMind 对通用智能体的关注，这些智能体可以跨游戏泛化，正如早期 SIMA 研究所示。与游戏工作室的合作旨在在真实游戏环境中原型化这些智能体，但具体工作室和时间表未披露。

rss · Google DeepMind Blog · 8月21日 11:59

**背景**: 谷歌 DeepMind 在游戏 AI 研究方面有着悠久历史，从 Atari 游戏到 EVE Online，将游戏作为强化学习和智能体开发的试验场。SIMA（可扩展可指导多智能体）是最近的项目，专注于构建能够在各种游戏世界中遵循指令并执行任务的智能体。这一新合作旨在从研究转向商业游戏中的实际应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/from-atari-to-eve-online-building-on-15-years-of-ai-research-in-games/">Exploring new frontiers of AI and games research — Google DeepMind</a></li>
<li><a href="https://techcrunch.com/2024/03/13/google-deepmind-trains-a-video-game-playing-ai-to-be-your-co-op-companion/">Google DeepMind trains a video game-playing AI to be your co-op companion | TechCrunch</a></li>

</ul>
</details>

**标签**: `#AI`, `#gaming`, `#DeepMind`, `#research`, `#industry`

---