---
layout: default
title: "Horizon Summary: 2026-08-30 (ZH)"
date: 2026-08-30
lang: zh
---

> 从 15 条内容中筛选出 2 条重要资讯。

---

1. [腾讯将 Hy4-preview 压缩至 200GB GGUF，性能保持 98%](#item-1) ⭐️ 8.0/10
2. [Qwen 3.8 27B 在 16GB GPU 上实现 50 tok/s 和 100k 上下文](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [腾讯将 Hy4-preview 压缩至 200GB GGUF，性能保持 98%](https://www.reddit.com/r/LocalLLaMA/comments/1w1o324/tencent_compressed_hy4preview_from_15tb_to_about/) ⭐️ 8.0/10

腾讯使用 GGUF 格式将其 Hy4-preview 模型从 1.5TB 压缩至约 200GB，同时保留了约 98%的原始性能。这显著减小了模型体积，使其更便于本地部署。 这一模型压缩方面的突破可能使大型语言模型能够在消费级硬件上更广泛地部署，降低基础设施成本，并为边缘计算和隐私保护 AI 应用开辟新的可能性。同时，这也为行业中的高效模型优化树立了先例。 该压缩利用了 GGUF 格式，该格式通过量化降低模型权重的精度，从而减少内存占用并加快推理速度。据报道，性能保持 98%表明量化过程经过精心校准，以最小化精度损失。

reddit · r/LocalLLaMA · /u/RedditUsr2 · 8月29日 14:31

**背景**: GGUF 是一种专为机器学习模型的高效存储和执行而设计的文件格式，尤其适用于本地硬件。它侧重于量化，即降低模型权重的精度以节省内存并提高速度，但会损失一些准确性。像量化这样的模型压缩技术对于使大型语言模型在实际应用中变得实用至关重要，尤其是在资源有限的设备上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GGUF">GGUF - Wikipedia</a></li>
<li><a href="https://medium.com/@vimalkansal/understanding-the-gguf-format-a-comprehensive-guide-67de48848256">Understanding the GGUF Format: A Comprehensive Guide</a></li>
<li><a href="https://ai-tldr.dev/learn/local-open-models/quantization-and-formats/what-is-gguf/">What Is GGUF? The Local Model File Format Explained | AI/TLDR</a></li>

</ul>
</details>

**标签**: `#model compression`, `#LLM`, `#GGUF`, `#Tencent`, `#efficiency`

---

<a id="item-2"></a>
## [Qwen 3.8 27B 在 16GB GPU 上实现 50 tok/s 和 100k 上下文](https://www.reddit.com/r/LocalLLaMA/comments/1w1lq7u/qwen_38_27b_at_50_toks_with_100k_context_on_a/) ⭐️ 8.0/10

一位用户分享了一套配置，在 16GB 的 RTX 4070 Ti SUPER 上以 47-50 tokens/秒的速度运行 Qwen 3.8 27B，上下文长度达 100k，使用了混合量化 GGUF 模型和 beellama.cpp 的 kvarn KV 缓存类型。该配置利用非对称的 kvarn5/kvarn4 缓存量化和 1024 token 的精度尾部，将大上下文装入显存。 这展示了一种在消费级 GPU 上运行大模型并支持长上下文的实用方法，解决了本地 LLM 推理中的常见痛点。混合量化、kvarn 缓存和 MTP 投机解码的结合，可能让更多用户无需昂贵硬件即可运行高质量模型。 该配置使用了 jrell 的 Qwen3.8-27B-i1-IQ4_XS-GGUF-Smaller 模型，这是一种自定义混合量化。关键优化包括 K 缓存使用 kvarn5、V 缓存使用 kvarn4，--kv-tail-tokens 1024 参数保持最近 token 的高精度，以及 --spec-type draft-mtp 配合 2 个草稿 token 进行投机解码。显存占用约 15.93 GB，仅剩 70 MB 空闲。

reddit · r/LocalLLaMA · /u/qaf23 · 8月29日 12:50

**背景**: KV 缓存量化减少了 Transformer 模型中键值缓存的内存占用，从而支持更长的上下文。KVarN 是一种免校准的 KV 缓存量化器，利用 Hadamard 旋转和方差归一化来减轻误差累积，beellama.cpp 实现了这些 kvarn 类型。多 token 预测（MTP）是一种投机解码技术，模型一次预测多个未来 token，无需单独的草稿模型即可加速推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/huawei-csl/KVarN">GitHub - huawei-csl/KVarN: KVarN is a native vLLM KV-cache quantization backend for your agents: 3-5x more context, throughput above FP16, and FP16-level accuracy. Calibration-free, one flag. · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2606.03458">[2606.03458] KVarN: Variance-Normalized KV-Cache Quantization Mitigates Error Accumulation in Reasoning Tasks</a></li>
<li><a href="https://www.datacamp.com/tutorial/multi-token-prediction-llama-cpp">Multi-Token Prediction Tutorial: How To Speed Up LLMs</a></li>

</ul>
</details>

**标签**: `#Local LLM`, `#Inference Optimization`, `#Quantization`, `#GPU`, `#Qwen`

---