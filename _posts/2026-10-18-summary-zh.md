---
layout: default
title: "Horizon Summary: 2026-10-18 (ZH)"
date: 2026-10-18
lang: zh
---

> 从 22 条内容中筛选出 2 条重要资讯。

---

1. [DeepSeek 发布 V4.1-Flash-1017，一款在编码基准上领先的快速开放模型](#item-1) ⭐️ 8.0/10
2. [Xolotl 在单张 RTX 4090 上以 27 tok/s 运行 552B DeepSeek-V4.1-Flash](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek 发布 V4.1-Flash-1017，一款在编码基准上领先的快速开放模型](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4.1-Flash-1017，这是其 V4.1-Flash 模型在 2026 年 10 月 17 日的快照版本，在多项编码基准上得分高于前代版本，并在 11 项基准中的 10 项上击败了 Sol 5.6。该模型可通过 DeepSeek 网站、应用和 API 以 deepseek-flash 模型名使用，同时也在 OpenRouter 上提供服务。 此次发布表明，中国实验室的开放权重模型如今能在关键基准上匹配或超越领先的专有编码模型，同时提供更快的推理和更高的透明度，这可能促使开发者从闭源提供商转向此类模型。它在 Hacker News 上的热烈反响（754 分、610 条评论）表明，从业者越来越看重速度、开放性和生态多样性，而非单纯的基准领先地位。 V4.1-Flash 是一个稀疏混合专家模型，也是首个基于 DeepSeek 的因果编码器-解码器（CED）架构构建的模型，使用 CSA2 为每个注意力层分配三种静态模式（Full、Reindex 或 Reuse）之一，以跨层共享 KV 和索引器 K。DeepSeek 称此次更新在性能和成本上实现了帕累托改进，输出更短，并建议升级到 DeepSeek Harness v0.2.1-rc.1 或更高版本以获得最佳体验。

hackernews · theykk · 10月17日 08:21 · [社区讨论](https://news.ycombinator.com/item?id=50129045)

**背景**: DeepSeek 是一家以发布开放权重大语言模型闻名的中国 AI 实验室，其 V4.1-Flash 是面向编码和智能体任务的轻量快速变体。编码基准是用于比较大语言模型编程能力的标准化测试（如 HumanEval 或 SWE-bench 类任务），但研究者提醒结果在很大程度上取决于基准的严谨性和可复现性。OpenRouter 是一个统一的 API 平台，将请求路由到众多提供商的数百个模型，使开发者能轻松试用此类新发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash">deepseek-ai/DeepSeek-V4.1-Flash · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash-1017">DeepSeek V4.1 Flash 1017 - API Pricing & Benchmarks</a></li>
<li><a href="https://api-docs.deepseek.com/news/news261017/">DeepSeek-V4.1-Flash-1017: Wish-Driven Programming Made Real</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞该模型的速度（每秒 token 数和首 token 时间）和开放性，多人表示现在编码时默认使用 DeepSeek Flash 而非 Claude 或 Sol，因为它能快速且正确地完成任务，并允许查看思维链。其他人则将此次发布视为多样化 AI 生态价值的证据，反对有利于现有巨头的监管障碍，还有一位用户分享了四个智能体审查大型 C++代码库的“苹果对香蕉”式对比。

**标签**: `#llm`, `#deepseek`, `#ai-models`, `#benchmarks`, `#coding-assistants`

---

<a id="item-2"></a>
## [Xolotl 在单张 RTX 4090 上以 27 tok/s 运行 552B DeepSeek-V4.1-Flash](https://www.reddit.com/r/LocalLLaMA/comments/1x8m0jj/xolotl_strata_based_deepseekv41flash_552b_on_a/) ⭐️ 8.0/10

开发者发布了基于 Strata 的推理引擎 Xolotl，可在单张 RTX 4090（24GB 显存）、90GB DDR4 内存和 NVMe 硬盘的配置上运行完整的 552B DeepSeek-V4.1-Flash 模型，解码速度约 27 tok/s，预填充速度 180-320 tok/s，支持 512K 上下文。该引擎还支持 GLM-5.3-Flash、Qwen3.8-Flash-Next 和 Qwen3.8-27B，并计划在几天内发布 1017 版本的无审查量化模型。 这表明通过专家卸载技术，大规模混合专家模型可以在消费级硬件上本地运行，显著降低了实验最先进大模型的门槛。它可能让更多研究者和爱好者无需昂贵的多 GPU 配置就能运行和微调巨型模型。 该引擎将模型权重分布在显存、固定系统内存和 NVMe 上，动态加载每个 token 所需的专家。基准测试包括 HumanEval 21/21、工具调用 10/10 和代理式 bug 修复循环 3/3，均通过启用思考模式的真实服务器完成；即将推出的 1017 量化版本由于权重与 V4.1 不同，需要完全重新校准和量化。

reddit · r/LocalLLaMA · /u/indrasmirror · 10月17日 21:40

**背景**: 像 DeepSeek-V4.1-Flash 这样的混合专家（MoE）模型包含许多专门的子网络（专家），但每个 token 只激活少数几个，从而能以较低计算量实现巨大的总参数量。Strata 是一个开源推理引擎，通过将不活跃的专家卸载到系统内存或 NVMe，使这类大型 MoE 模型能在消费级 GPU 上运行，以速度换取内存容量。量化（如 GSQ）通过降低权重精度来缩小模型体积，而“无审查”或“消融”模型则移除了安全过滤器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stratallm.org/">Strata LLM – Run 125B+ MoE Models on 12GB VRAM Consumer GPUs ...</a></li>
<li><a href="https://apxml.com/courses/mixture-of-experts-advanced-implementation/chapter-4-efficient-moe-inference/expert-offloading">MoE Expert Offloading to CPU/NVMe - apxml.com</a></li>
<li><a href="https://github.com/IST-DASLab/GSQ">IST-DASLab/ GSQ : Gumbel-Softmax post-training quantization for...</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#inference-engine`, `#model-quantization`, `#moe`, `#deepseek`

---