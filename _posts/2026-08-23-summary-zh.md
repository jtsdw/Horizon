---
layout: default
title: "Horizon Summary: 2026-08-23 (ZH)"
date: 2026-08-23
lang: zh
---

> 从 21 条内容中筛选出 1 条重要资讯。

---

1. [llama.cpp 中的 DFlash 2：编码提示加速 2.26 倍，配合 n-gram 草稿器最高可达 4.68 倍](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [llama.cpp 中的 DFlash 2：编码提示加速 2.26 倍，配合 n-gram 草稿器最高可达 4.68 倍](https://www.reddit.com/r/LocalLLaMA/comments/1vvncyh/i_benchmark_dflash_2_pr_build_in_llamacpp_on_qwen/) ⭐️ 8.0/10

一位 Reddit 用户在 llama.cpp 中对 Qwen 3.8 27B 上的 DFlash 2 进行了基准测试，报告在 100 个真实编码提示上实现了 2.26 倍加速（从 67.97 到 153.91 tok/s），并且与单个 n-gram 查找草稿器结合时最高可达 4.68 倍。基准测试还显示，添加第二个 n-gram 表会降低性能，这与 DFlash 1 的结果相反。 该基准测试提供了真实世界的证据，表明 DFlash 2 可以显著加速编码任务上的 LLM 推理，这对使用本地模型的开发者和研究人员至关重要。关于 n-gram 草稿器组合的发现为优化投机解码配置提供了实用指导，可能改善整个生态系统的推理速度和用户体验。 基准测试使用 RTX PRO 6000 GPU，并发数为 1，仅 DFlash 2 就增加了 +2.7 GB 显存。发现推荐的 --spec-draft-n-max 7 已超过峰值；将其设置为 5 在 8K 编码提示上大约多出 11% 的性能，而高于 7 的值会被静默截断。此外，--spec-draft-p-min 对 DFlash 2 没有效果，因为代码路径从不读取它。

reddit · r/LocalLLaMA · /u/FantasticNature7590 · 8月22日 20:41

**背景**: 投机解码是一种使用小型草稿模型并行预测多个 token 的技术，然后主模型在单次前向传播中验证这些 token，从而加速推理。DFlash 2 是一种用于投机解码的块扩散模型，而 llama.cpp 是一个流行的本地运行 LLM 的 C++ 库。该基准测试将 DFlash 2 与普通解码、MTP 和 n-gram 草稿器进行比较，为最佳配置提供了见解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lmsys.org/blog/2026-06-15-next-generation-speculative-decoding-dflash-v2/">The next generation of speculative decoding: DFlash and Spec V2 - LMSYS Org</a></li>
<li><a href="https://github.com/z-lab/dflash">GitHub - z-lab/dflash: DFlash: Block Diffusion for Flash Speculative Decoding · GitHub</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp/blob/master/docs/speculative.md">llama . cpp /docs/speculative.md at master · ggml-org/ llama . cpp · GitHub</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#llama.cpp`, `#benchmark`, `#LLM inference`, `#DFlash`

---