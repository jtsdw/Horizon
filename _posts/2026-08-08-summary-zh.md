---
layout: default
title: "Horizon Summary: 2026-08-08 (ZH)"
date: 2026-08-08
lang: zh
---

> 从 32 条内容中筛选出 2 条重要资讯。

---

1. [SGLang v0.5.17 发布，首日支持 2.8T 参数的 MoE 模型 Kimi K3](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Flash 0731：更快、更便宜、能力更强](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.17 发布，首日支持 2.8T 参数的 MoE 模型 Kimi K3](https://github.com/sgl-project/sglang/releases/tag/v0.5.17) ⭐️ 9.0/10

SGLang v0.5.17 发布，新增对 Kimi K3 的首日支持，这是一个 2.8T 参数的多模态 LatentMoE 模型，拥有 896 个专家和 1M token 的上下文。该版本还新增了对视频生成模型 MiniMax-H3 的首日支持，并引入了 Rust 前端、用于 MoE 预填充的 DWDP 以及会话引用感知缓存。 该版本标志着在服务超大规模 MoE 模型方面的重要里程碑，SGLang 为 Kimi K3（迄今最大的开源模型之一）提供了即时支持。在 GB300 和 MI35x 上的优化和硬件验证展示了 SGLang 在高性能 LLM 推理领域的领先地位，使开发者和企业能够部署前沿模型。 Kimi K3 采用 LatentMoE 架构，拥有 896 个专家，在 3584 维潜在空间中进行 top-16 路由，并将 69 个 KDA 线性注意力层与 24 个 MLA 层交错。它原生提供 MXFP4 检查点，SGLang 通过 DCP、DSpark 投机解码、带 TP 解码的 chunked-prefill PP 以及量化权重上的 LoRA 支持它。该版本还包含来自 194 位贡献者的 582 个 PR。

github · Fridge003 · 8月8日 00:19

**背景**: LatentMoE 是一种改进的混合专家（MoE）架构，通过降低路由专家路径的成本（通常减少专家计算的有效维度）来提高每参数和每 FLOP 的准确性。MXFP4 是 OCP 标准化的 4 位量化格式，可在保持精度的同时压缩模型权重，并得到 NVIDIA Blackwell GPU 的支持。DCP（上下文并行）是一种跨设备分片 KV 缓存以处理长上下文的并行策略，SGLang 的实现支持多种通信后端。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jianyuh.github.io/fp8/2026/01/31/LatentMoE.html">Reading Note on LatentMoE | Jianyu Huang’s Blog</a></li>
<li><a href="https://research.nvidia.com/labs/nemotron/LatentMoE/">Think Smart About Sparse Compute: LatentMoE ... - NVIDIA Nemotron</a></li>
<li><a href="https://www.kapilsharma.dev/posts/mxfp4-visualizer/">Understanding MXFP 4 Quantization | Kapil Sharma</a></li>
<li><a href="https://docs.vllm.ai/en/latest/serving/context_parallel_deployment/">Context Parallel Deployment - vLLM</a></li>

</ul>
</details>

**标签**: `#SGLang`, `#Kimi K3`, `#LLM serving`, `#MoE`, `#AI infrastructure`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 0731：更快、更便宜、能力更强](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek V4 Flash 0731，这是其稀疏混合专家模型的一个重新训练版本，总参数 284B，激活参数 13B。尽管激活参数更少，它在基准测试上超越了 DeepSeek V4 Pro (Preview)，并引入了原生 DSpark，解码速度最高可提升 2 倍。 该版本在性能和成本之间取得了引人注目的平衡，使高质量的 AI 更易于用于编码、推理和智能体工作流。其速度和性价比可能会使用户从更昂贵的专有模型转移，加剧 LLM 市场的竞争。 该模型支持 1M 上下文窗口，并已在 Hugging Face、ModelScope 和 OpenRouter 等平台上线。用户报告了出色的本地性能，例如在 2x RTX Pro 6000 Blackwell 上预填充约 8k tok/s，单流约 250 tok/s，部分用户看到 1000 tok/s。

hackernews · tosh · 8月7日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49214008)

**背景**: DeepSeek V4 Flash 是一个稀疏混合专家（MoE）模型，意味着每个 token 只激活部分参数，从而实现高效。DSpark 是 DeepSeek 提出的新解码算法，优于朴素的多 token 预测（MTP），从而加快生成速度。0731 版本是早期 Flash 预览版的更新版本，质量有显著提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek -ai/ DeepSeek - V 4 - Flash - 0731 · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V 4 Flash 0731 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://unsloth.ai/docs/models/deepseek-v4">DeepSeek-V4: How to Run Locally | Unsloth Documentation</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，用户称赞其性价比和速度，称其“几乎适用于所有场景”，且成本低到可以忽略。然而，一些用户报告在智能体平台上出现无限循环和浪费 token 的问题，还有一位用户提到其 Claude 账户被封，可能与这个模型无关。

**标签**: `#AI`, `#DeepSeek`, `#LLM`, `#model release`, `#performance`

---