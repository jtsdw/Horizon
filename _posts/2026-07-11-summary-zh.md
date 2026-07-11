---
layout: default
title: "Horizon Summary: 2026-07-11 (ZH)"
date: 2026-07-11
lang: zh
---

> 从 23 条内容中筛选出 2 条重要资讯。

---

1. [GPT-5.6 Sol Ultra 证明循环双覆盖猜想](#item-1) ⭐️ 9.0/10
2. [SGLang v0.5.15 在 Blackwell GPU 上大幅提升 GLM-5.2 性能](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Sol Ultra 证明循环双覆盖猜想](https://cdn.openai.com/pdf/04d1d1e4-bc75-476a-97cf-49055cd98d31/cdc_proof.pdf) ⭐️ 9.0/10

OpenAI 发布了一篇预印本，声称 GPT-5.6 Sol Ultra 生成了图论中一个重大开放问题——循环双覆盖猜想的证明。该证明及所用提示词已以 PDF 形式公开。 这标志着人工智能首次生成了一个长期数学猜想的所谓证明，可能彻底改变数学和理论计算机科学的研究方式。它也展示了 OpenAI 最新前沿模型 GPT-5.6 Sol Ultra 的高级推理能力。 该证明极为简洁，暗示其利用了一个专家可能忽略的巧妙技巧。提示词中包含了拒绝模糊乐观情绪并要求实际解决问题的明确指令，突显了即使对于先进模型，当前仍需精心设计提示词。

hackernews · scrlk · 7月10日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=48863490)

**背景**: 循环双覆盖猜想询问：是否每个无桥无向图都存在一组环，使得每条边恰好出现在两个环中？该猜想由 Tutte、Itai、Rodeh、Szekeres 和 Seymour 提出，是图论中著名的开放问题。GPT-5.6 Sol Ultra 是 OpenAI 的最新模型，具有新的“ultra”模式，可协调多个智能体完成复杂任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover_conjecture">Cycle double cover conjecture</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>

</ul>
</details>

**社区讨论**: 社区对这一成就印象深刻，但指出该证明极为简洁，引发了对它是否正确或是否利用了某种技巧的疑问。一些评论者强调，提示词仍需大量人工引导，其他人则讨论了自动化数学研究的标准。

**标签**: `#AI`, `#mathematics`, `#graph theory`, `#OpenAI`, `#research`

---

<a id="item-2"></a>
## [SGLang v0.5.15 在 Blackwell GPU 上大幅提升 GLM-5.2 性能](https://github.com/sgl-project/sglang/releases/tag/v0.5.15) ⭐️ 8.0/10

SGLang v0.5.15 引入了 Spec V2 和 IndexShare MTP 优化，在 8 块 B300 GPU 上为 GLM-5.2 NVFP4 实现了每用户每秒超过 500 token 的性能，其中 Spec V2 带来 11% 的端到端 TPS 提升，IndexShare MTP 将 draft 步骤成本降低最多 1.9 倍。 此版本显著提升了大型语言模型在 NVIDIA Blackwell GPU 上的服务效率，使高吞吐推理更易于投入生产部署。特别是针对 GLM-5.2 的优化，展示了 SGLang 在推动 LLM 服务性能前沿方面的承诺。 Spec V2 通过可 CUDA 图化的 DSA draft-extend 和融合元数据操作实现了零开销调度，而 IndexShare MTP 跨 draft 步骤复用索引器 top-k 以降低成本。其他改进包括 TopK V2 融合、索引器 prologue 融合（从 12 个内核减少到 4 个），以及针对 Blackwell 的形状专用 JIT 路由 GEMM。

github · Fridge003 · 7月10日 22:58

**背景**: SGLang 是一个用于大型语言模型和多模态模型的高性能服务框架。推测解码是一种技术，它使用 draft 模型并行预测多个 token，然后由目标模型验证以加速推理。NVFP4 是 NVIDIA 为 Blackwell GPU 引入的 4 位浮点格式，旨在提高效率的同时保持精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.sglang.io/docs/advanced_features/speculative_decoding">Speculative Decoding - SGLang Documentation</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#GPU optimization`, `#speculative decoding`, `#Blackwell`, `#SGLang`

---