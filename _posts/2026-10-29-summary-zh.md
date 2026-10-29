---
layout: default
title: "Horizon Summary: 2026-10-29 (ZH)"
date: 2026-10-29
lang: zh
---

> 从 34 条内容中筛选出 3 条重要资讯。

---

1. [Google DeepMind 发布 Gemini 4 Carbon 前沿模型](#item-1) ⭐️ 9.0/10
2. [llama.cpp v0.8.0 新增 LFM3 多模态模型和流式音频 API](#item-2) ⭐️ 8.0/10
3. [Qwenputer：在 Qwen3.5 模型内实现确定性 RISC-V CPU](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google DeepMind 发布 Gemini 4 Carbon 前沿模型](https://deepmind.google/blog/gemini-4-carbon-our-next-frontier-model/) ⭐️ 9.0/10

Google DeepMind 发布了 Gemini 4 Carbon，这是继 Gemini 4 Argon 之后的下一代前沿 AI 模型，其基准测试涵盖软件工程、科学、长上下文检索、计算机使用和网络安全。 作为 Google DeepMind 的新前沿模型，Gemini 4 Carbon 可能显著提升 AI 能力，并加剧领先 AI 实验室之间的竞争，影响依赖前沿 AI 的开发者和企业。 发布基准测试覆盖多个领域，但模型的公开可用性和定价在推广期间可能有所不同，社区成员指出，如果没有立即发布，基准分数可能很快过时。

rss · Google DeepMind Blog · 10月28日 17:00

**背景**: 前沿 AI 模型是能力最先进的通用模型，支持推理、多模态生成和代理工作流。Google DeepMind 的 Gemini 系列是其旗舰产品线，每一代新模型都在推动性能边界。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work - NVIDIA</a></li>
<li><a href="https://kingy.ai/blog/gemini-4-carbon/">Gemini 4 Carbon: Specs, Benchmarks, Pricing and Availability</a></li>
<li><a href="https://deepmind.google/models/gemini/">Gemini — Google DeepMind</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Google 混乱的模型命名和分层表示不满，有人建议采用行业标准标签如 Ultra、Pro、Flash 和 Lite。其他人批评只公布基准测试而不立即发布模型，指出在快速发展的领域中，延迟会使分数变得不那么有意义。

**标签**: `#AI`, `#LLM`, `#Google DeepMind`, `#frontier models`, `#machine learning`

---

<a id="item-2"></a>
## [llama.cpp v0.8.0 新增 LFM3 多模态模型和流式音频 API](https://github.com/ggml-org/llama.cpp/releases/tag/v0.8.0) ⭐️ 8.0/10

llama.cpp 发布了 v0.8.0 版本，引入了 LiquidAI LFM3 系列（文本、视觉、音频和全模态模型）、mtmd 中的实验性流式音频 API，以及用于实时音频输入输出的新服务器端点 /v1/realtime 和 /tts。该版本还新增了对 DeepSeek V4.1 Flash、SenseNova U1、Beam、Kolibri-1、Flint 和 Muse Spark 等多种新架构的支持，并将 ggml 升级到 v0.28.0，带来后端性能改进。 这是广泛使用的本地 LLM 推理引擎的一次重大发布，显著扩展了其多模态和实时音频能力，可能催生新的语音应用，并提升稀疏注意力和 MoE 模型的性能。众多新模型架构的加入使 llama.cpp 保持在本地推理支持的前沿。 流式音频 API（mtmd_audio_stream）可将 PCM 音频实时转换为解码器可用的嵌入，新的 /v1/realtime 端点实现了 OpenAI 实时协议，用于对话和转录。核心优化包括针对稀疏注意力（QSA/DSA）的融合掩码操作、用于主机驻留 MoE 专家的 50/50 SLRU 缓存，以及更清晰的 no_alloc 内存处理；CLI 现在要求使用 --model 或 -hf。

github · github-actions[bot] · 10月28日 12:47

**背景**: llama.cpp 是一个开源 C/C++ 推理引擎，用于在各种硬件（从 CPU 到 GPU）上本地运行大型语言模型。它使用 ggml 张量库作为计算后端，并通过转换和量化支持多种模型架构。mtmd 库为 llama.cpp 扩展了多模态能力，允许在文本之外输入图像和音频。QSA（Qwen 稀疏注意力）和 DSA（DeepSeek 稀疏注意力）等稀疏注意力技术通过关注输入的相关部分来降低计算成本，而 MoE（混合专家）模型每个 token 只激活一部分参数，需要高效的专家缓存。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ggml-org/llama.cpp/discussions/13759">Audio input support in llama.cpp - GitHub</a></li>
<li><a href="https://deepwiki.com/ggml-org/llama.cpp/6.5-multimodal-support-(libmtmd)">Multimodal Support (libmtmd) | ggml-org/llama.cpp | DeepWiki</a></li>
<li><a href="https://sebastianraschka.com/llm-architecture-gallery/qwen-sparse-attention/">Qwen Sparse Attention | Sebastian Raschka, PhD</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#ggml`, `#LLM inference`, `#multimodal`, `#release`

---

<a id="item-3"></a>
## [Qwenputer：在 Qwen3.5 模型内实现确定性 RISC-V CPU](https://divagr.com/blog/qwenputer) ⭐️ 8.0/10

一位开发者创建了 Qwenputer，在 Qwen3.5 语言模型内部完整模拟了一个功能完整且确定性的 RISC-V CPU，并配备了文件系统。该项目已在 Hugging Face 上发布为 Qwen3.5-4B-Qwenputer，并在 ModelScope 上提供在线演示。 该项目展示了大型语言模型中令人惊讶的涌现计算能力，表明 LLM 能够模拟像 CPU 这样的复杂确定性系统。它引发了关于参数效率、工具调用以及 LLM 更原生地处理计算机使用任务的潜力的讨论。 该实现是确定性的，意味着 CPU 产生一致的输出，并且包含文件系统，这增加了复杂性。使用的模型是 Qwen3.5-4B，一个 40 亿参数的模型，表明在此任务中参数使用效率较高。

hackernews · csmantle · 10月29日 00:25 · [社区讨论](https://news.ycombinator.com/item?id=50282838)

**背景**: RISC-V 是一种开源指令集架构（ISA），任何人都可以免费使用，与 x86 和 ARM 等专有 ISA 形成对比。像 Qwen3.5 这样的大型语言模型（LLM）是在大量文本数据上训练的神经网络，用于预测和生成文本，它们有时会表现出涌现能力——即随着规模扩大而出现的意外能力。Qwen 是阿里巴巴开发的一系列开放基础模型，Qwen3.5 是近期版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://riscv.org/">Home - RISC - V International</a></li>
<li><a href="https://arxiv.org/pdf/2206.07682">Emergent Abilities of Large Language Models</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了娱乐和着迷，一些人开玩笑说这对 AI 代理和回形针最大化目标的影响。其他人讨论了在 AdderBoard（一个最小化 Transformer 的竞赛）背景下的参数效率，并猜测在 CPU 上运行 LLM，导致“LLM 一路到底”的说法。

**标签**: `#LLM`, `#RISC-V`, `#emergent-computation`, `#Qwen`, `#Hacker News`

---