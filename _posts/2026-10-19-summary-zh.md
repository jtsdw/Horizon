---
layout: default
title: "Horizon Summary: 2026-10-19 (ZH)"
date: 2026-10-19
lang: zh
---

> 从 19 条内容中筛选出 2 条重要资讯。

---

1. [vLLM v0.32.0 新增结构化决策端点并广泛支持低精度 KV 缓存](#item-1) ⭐️ 8.0/10
2. [Together AI 推出 HybridAgent：在潜在空间推理，通过文本行动](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.32.0 新增结构化决策端点并广泛支持低精度 KV 缓存](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) ⭐️ 8.0/10

vLLM v0.32.0 包含来自 363 位贡献者的 814 次提交，新增了用于结构化 choice、noul 和 score 问题的 POST /v1/systemone 端点，支持读取检查点 response_template 的通用 Hugging Face 工具和推理解析器，并扩展了低精度 KV 缓存支持，包括在 SM8x/SM12x/SM90 上的 NVFP4 以及 SM100 上 GLM-5.x 默认使用 FP8 KV 缓存。 此版本通过在更多硬件上启用低精度 KV 缓存，显著提升了 LLM 服务的内存效率和吞吐量，并通过通用解析器简化了模型集成，惠及依赖 vLLM 进行生产推理的广大社区。 此版本包含重大变更，如放弃 Python 3.10、限制默认 CORS 来源和移除级联注意力；还修复了多个安全漏洞，并增加了共享内存张量竞技场和最少负载 API 工作线程路由等性能优化。

github · khluu · 10月18日 06:50

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理和服务引擎。KV 缓存存储注意力机制中的键和值张量，将其量化为 FP8 或 NVFP4 等低精度可以减少内存占用，从而在内存中存储更多 token 并支持更长的上下文窗口。SM 版本指 NVIDIA GPU 的计算能力，例如 SM90 对应 Hopper（H100），SM100 对应 Blackwell。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/features/quantization/quantized_kvcache/">Quantized KV Cache - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/tool_calling/">Tool Calling - vLLM</a></li>
<li><a href="https://www.whaleflux.com/blog/demystifying-gpu-architecture-why-it-matters-for-ai-how-to-manage-it-efficiently/">whaleflux.com/blog/demystifying- gpu - architecture -why-it-matters-for...</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#kv-cache`, `#quantization`, `#release`

---

<a id="item-2"></a>
## [Together AI 推出 HybridAgent：在潜在空间推理，通过文本行动](https://arxiv.org/abs/2610.18861) ⭐️ 8.0/10

Together AI（联合斯坦福、UIUC 和 Meta）发布了 HybridAgent，这是一种能在单次生成过程中动态切换潜在空间推理与文本交互的 LLM 智能体，并公开了代码、Hugging Face 模型以及 arXiv 论文 2610.18861 中的评估结果。 这项工作将潜在推理从研究 curiosities 推向可部署的智能体架构，可能在提升效率与能力的同时，引发关于在人类可读 token 之外进行推理的严重可解释性与安全性问题。 该智能体通过“Hybrid Link”将潜在向量与文本 token 交错，发布内容包含一个 8B 智能体 GGUF 模型；早期测试者报告了在简单问题上陷入无限思考循环等失败模式，论文的评估结果位于第 5 节。

hackernews · allinonai · 10月18日 20:48 · [社区讨论](https://news.ycombinator.com/item?id=50145337)

**背景**: 目前大多数 LLM 推理采用思维链（CoT），即模型用自然语言写出中间步骤。潜在推理则在不输出 token 的情况下在模型隐藏状态中进行计算，可能更高效但更难监控；HybridAgent 旨在在一个智能体中结合这两种模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/togethercomputer/HybridAgent">GitHub - togethercomputer/ HybridAgent · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2412.06769">[2412.06769] Training Large Language Models to Reason in a ... Safety-Aware Latent Space Reasoning in Large Language Models Reasoning Beyond Language: A Comprehensive Survey on Latent ... Latent Reasoning in LLMs - emergentmind.com Santosh Sawant - Training Large Language Models to Reason in ... Coconut: A Framework for Latent Reasoning in LLMs</a></li>
<li><a href="https://forum.effectivealtruism.org/posts/sNkua636jSni6Jftt/worries-about-latent-reasoning-in-llms">Worries about latent reasoning in LLMs — EA Forum</a></li>

</ul>
</details>

**社区讨论**: 评论者就安全性与可解释性展开辩论，指出潜在推理可能增强欺骗能力，并将其与 OpenAI 的多轮次方法相比较；一位用户报告 8B GGUF 模型在回答“谁是教皇？”时陷入无限思考循环，其他人则建议加宽嵌入或同时运行潜在与文本模式等架构调整。

**标签**: `#LLM agents`, `#latent reasoning`, `#AI safety`, `#interpretability`, `#Together AI`

---