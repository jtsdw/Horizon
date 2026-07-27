---
layout: default
title: "Horizon Summary: 2026-07-27 (ZH)"
date: 2026-07-27
lang: zh
---

> 从 14 条内容中筛选出 2 条重要资讯。

---

1. [vLLM v0.26.0：支持 Inkling 模型、DeepSeek-V4 优化、灵活注意力后端](#item-1) ⭐️ 8.0/10
2. [美国公民因 GrapheneOS 手机在边境被擦除而遭起诉](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0：支持 Inkling 模型、DeepSeek-V4 优化、灵活注意力后端](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 引入了对 Inkling 模型系列的全面支持，包括分段 CUDA 图、Hopper FA4 相对注意力和 NVFP4 量化。同时为 DeepSeek-V4 带来了显著的性能优化，支持 fp32 lm_head，并允许按 KV 缓存组灵活选择注意力后端。 此版本增强了 vLLM 的通用性和性能，使其成为在生产环境中部署 Inkling 和 DeepSeek-V4 等前沿模型的更优选择。注意力后端灵活性和 KV 卸载改进有利于混合模型和大规模推理部署。 此版本包含来自 212 位贡献者的 411 次提交，新增功能包括 Rust 前端对多模态视频/音频的支持、KV 卸载指标以及 Transformers 5.13 迁移。值得注意的限制：NVFP4 量化目前仅适用于 Hopper GPU，部分功能（如 DSpark 推测解码）为特定供应商支持。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎，支持多种模型架构和量化方法。Inkling 模型系列是 Thinking Machines Lab 推出的通用多模态模型，而 DeepSeek-V4 是一个大型 MoE 模型，需要高效的路由和注意力优化。Hopper FA4 指针对 NVIDIA Hopper GPU 的 FlashAttention-4 优化，NVFP4 是 NVIDIA ModelOpt 提供的 4 位浮点量化格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/thinkingmachines/Inkling">thinkingmachines/ Inkling · Hugging Face</a></li>
<li><a href="https://docs.vllm.ai/en/latest/api/vllm/models/inkling/nvidia/model/">model - vLLM</a></li>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling : Our Open-Weights Model - Thinking Machines Lab</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#performance optimization`, `#open source`, `#AI infrastructure`

---

<a id="item-2"></a>
## [美国公民因 GrapheneOS 手机在边境被擦除而遭起诉](https://www.techspot.com/news/113236-us-prosecutors-charge-atlanta-man-after-grapheneos-phone.html) ⭐️ 8.0/10

一名美国公民因其使用 GrapheneOS 手机的胁迫 PIN 在边境搜查中自动擦除设备而被起诉。该指控将擦除行为视为旨在阻止政府扣押的财产破坏。 此案为边境检查中使用胁迫 PIN 和擦除设备的行为树立了法律先例，可能抑制注重隐私用户的安全实践。它凸显了数字隐私权与美国边境政府搜查权之间的紧张关系。 GrapheneOS 的胁迫 PIN 在输入后会不可逆地擦除设备和已安装的 eSIM。被告据称提供了胁迫 PIN 而非真实 PIN，导致设备被擦除并随后被起诉。

hackernews · eecc · 7月26日 22:21 · [社区讨论](https://news.ycombinator.com/item?id=49063022)

**背景**: GrapheneOS 是一个注重隐私的基于 Android 的操作系统，包含胁迫 PIN 功能：输入特定 PIN 会擦除设备而非解锁。美国边境官员拥有广泛的电子设备搜查权，故意销毁证据可能导致刑事指控。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidauthority.com/grapheneos-duress-pin-us-prosecution-3691271/">GrapheneOS duress PIN could land a man in prison - Android Authority</a></li>
<li><a href="https://discuss.grapheneos.org/d/14722-using-duress-password-example">Using duress password example - GrapheneOS Discussion Forum</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论了胁迫 PIN 的法律风险，有人认为用户必须接受后果，而另一些人则建议使用携带已擦除手机或诱饵卷等替代方法。讨论强调了需要针对边境场景制定威胁模型。

**标签**: `#privacy`, `#legal`, `#grapheneos`, `#security`, `#border search`

---