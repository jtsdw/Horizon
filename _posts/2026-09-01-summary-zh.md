---
layout: default
title: "Horizon Summary: 2026-09-01 (ZH)"
date: 2026-09-01
lang: zh
---

> 从 60 条内容中筛选出 6 条重要资讯。

---

1. [通用上下文复用层实现跨模型 KV 缓存共享](#item-1) ⭐️ 8.0/10
2. [分层 KV 保留策略平衡 LLM 代理的 GPU 容量与恢复延迟](#item-2) ⭐️ 8.0/10
3. [SingProbe：复用 LLM 隐藏状态的轻量级内在护栏](#item-3) ⭐️ 8.0/10
4. [CHIPSMORE：结合互连与内存计算的 LLM 推理加速器](#item-4) ⭐️ 8.0/10
5. [记忆增强草稿提升长上下文投机解码](#item-5) ⭐️ 8.0/10
6. [DeepSeek V4 Flash Vision Exp 在 Hugging Face 上发布](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [通用上下文复用层实现跨模型 KV 缓存共享](https://arxiv.org/abs/2608.30963v1) ⭐️ 8.0/10

本文提出了一种通用上下文复用层，使得不同 LLM 之间能够共享 KV 缓存，包括规模、架构、注意力配置、分词器和模型家族不同的模型。实验显示显著的准确率提升和延迟降低，例如在 Qwen2.5-7B 到 Qwen2.5-1.5B 的迁移中，LongBench2 准确率从 27.59%提升到 34.48%，在 Llama3.1-70B 到 Qwen2.5-7B 的迁移中，延迟从 899ms 降低到 138ms。 这项工作挑战了 KV 缓存严格局限于单个模型的假设，提出了“上下文移动性”的新抽象，可能减少异构 LLM 服务和多智能体工作流中的冗余预填充计算。它有望显著降低计算成本并提高多模型服务系统的效率。 该方法在族内和跨族设置中进行了评估，包括异构情况如 Llama3.1-70B 到 Qwen2.5-7B，跨族切换实现了 44.0%的准确率，而原生推理为 45.7%，同时延迟从 899ms 降低到 138ms。论文还指出，对于 Qwen2.5-1.5B 到 Gemma-2-2B，在 4K 上下文长度下，KV 切换将目标侧预填充成本降低了高达 67.05%，同时保持解码困惑度接近原生基线。

rss · arXiv LLM Inference · 8月31日 15:28

**背景**: 在 LLM 服务中，预填充是模型并行处理输入令牌以计算键和值向量的阶段，这些向量存储在 KV 缓存中。现有的 KV 缓存重用机制在单个模型内有效，但跨模型重用因学习参数不同而具有挑战性，常常导致显著的准确率损失。本文提出一个通用层来在模型之间转换 KV 状态，实现跨模型共享。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jaehun.me/en/posts/paper-review-droidspeak-kv-cache-sharing-for-cross-llm-communication-and-multi-llm-serving/">[Paper Review] DroidSpeak: KV Cache Sharing for Cross- LLM ...</a></li>
<li><a href="https://www.alphaxiv.org/abs/2411.02820v4">DroidSpeak: KV Cache Sharing for Cross -LLM... | alphaXiv</a></li>
<li><a href="https://huggingface.co/blog/tngtech/llm-performance-prefill-decode-concurrent-requests">Prefill and Decode for Concurrent Requests - Optimizing LLM Performance</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#KV cache`, `#cross-model`, `#efficiency`, `#prefill`

---

<a id="item-2"></a>
## [分层 KV 保留策略平衡 LLM 代理的 GPU 容量与恢复延迟](https://arxiv.org/abs/2608.30830v1) ⭐️ 8.0/10

本文提出了一种针对 LLM 代理的分层 KV 保留策略，在等待人工审批期间平衡 GPU 容量与恢复延迟，并展示了保留全部 KV 会导致 41%的 goodput 损失，而驱逐 KV 则会导致近 10 倍的恢复延迟。 这解决了 LLM 服务中具有人工介入延迟的代理工作负载的一个新颖且实际的问题，提供了定量分析和分层保留策略。结果（41%的 goodput 损失对比 10 倍的恢复延迟）对系统研究具有重要意义，并可能提高代理型 LLM 服务系统的效率。 该控制器使用校准等待样本在无限期保留和负载索引过期之间进行选择，无需逐请求的等待预测。在人工规模的审批工作负载上，与 vLLM 基线相比，主动请求的 goodput 提高了 23-51%，比 MORI 提高了 22-29%，比 Continuum 提高了 41-52%。

rss · arXiv LLM Inference · 8月31日 14:05

**背景**: KV 缓存存储推理过程中的中间键和值计算以供重用，从而加速文本生成，但会消耗大量 GPU 内存。在 LLM 服务中，goodput 是一个同时考虑吞吐量和延迟要求的指标，像 vLLM 这样的系统使用 PagedAttention 来高效管理 KV 缓存。代理工作负载通常涉及可能持续数分钟或数小时的人工审批等待，在此期间代理的 KV 状态可能被挂起，从而在保留 KV 以快速恢复和驱逐 KV 以释放 GPU 容量之间产生权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>
<li><a href="https://arxiv.org/html/2603.20397v1">KV Cache Optimization Strategies for Scalableand Efficient LLM Inference</a></li>
<li><a href="https://arxiv.org/html/2401.09670v1">DistServe: Disaggregating Prefill and Decoding for Goodput-optimized ...</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#KV cache`, `#agentic systems`, `#GPU resource management`, `#systems for AI`

---

<a id="item-3"></a>
## [SingProbe：复用 LLM 隐藏状态的轻量级内在护栏](https://arxiv.org/abs/2608.30703v1) ⭐️ 8.0/10

SingProbe 是一种轻量级的内在运行时护栏，它复用 LLM 的隐藏状态，在 token 级别预测查询意图、响应安全性和幻觉风险，开销可忽略不计，并引入了用于评估流式护栏的 SingStreamBench 基准。 与外部护栏相比，这种方法可以显著降低推理开销并提高安全信号的延迟，为 LLM 部署提供了一种“免费午餐”的解决方案。它还提供了一个用于流式护栏的新基准，这对实时安全监控至关重要。 SingProbe 与规模大得多的独立护栏和专门的幻觉检测器相比，实现了具有竞争力或更优的性能，仅需约 200 万参数和不到 0.5% 的额外开销。它还通过 SingProbe-Med 扩展到医疗生成领域，仅在出现临床相关风险时选择性激活风险导向的解码干预。

rss · arXiv LLM Inference · 8月31日 12:42

**背景**: 运行时护栏对于可靠的 LLM 部署至关重要，但现有方法通常依赖独立的外部模型，增加了推理成本并延迟了安全信号。SingProbe 利用内部隐藏状态（已被证明编码了与安全相关的信息）在生成过程中提供高效的监控和控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2406.05644">[2406.05644] How Alignment and Jailbreak Work: Explain LLM ... GitHub - ydyjya/LLM-IHS-Explanation kNNGuard: Turning LLM Hidden Activations into a Training-Free ... LLM Guardrails in Production: Why One Layer Is Never Enough Bleeding Pathways: Vanishing Discriminability in LLM Hidden ... Advanced Prompt Injection Techniques 2026: 7 Attack Chains</a></li>
<li><a href="https://aclanthology.org/2024.findings-emnlp.139/">How Alignment and Jailbreak Work: Explain LLM Safety through ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#safety`, `#guardrails`, `#streaming`, `#hallucination`

---

<a id="item-4"></a>
## [CHIPSMORE：结合互连与内存计算的 LLM 推理加速器](https://arxiv.org/abs/2608.30509v1) ⭐️ 8.0/10

CHIPSMORE 是一种新型多模式 LLM 推理加速器，结合了互连内计算和内存内计算，以支持基础和 LoRA 推理。它采用异构处理单元（RRAM-ACIM 和 SRAM-DCIM）和可组合的分层 KV 内存方案，在 Mistral-7B 上相比 Nvidia H100 实现了高达 2.38 倍的吞吐量和 27 倍的能效提升。 这项工作解决了 LLM 推理中计算内存加速器面临的关键挑战，如处理多样化工作负载和长上下文。通过显著提高吞吐量和能效，它可能推动高效 LLM 推理在边缘和数据中心环境中的部署。 该架构使用可编程的 PE 间计算网络（IPCN）互连 RRAM-ACIM 和 SRAM-DCIM。它还采用非复制多请求执行流水线和状态感知的资源重配置机制，可对非活动资源进行电源门控，并通过周期精确的协同仿真进行了验证。

rss · arXiv LLM Inference · 8月31日 09:43

**背景**: 计算内存（CIM）加速器直接在内存阵列中执行计算，减少数据移动并提高能效。RRAM 模拟 CIM 将权重存储在电阻式存储器中，而 SRAM 数字 CIM 使用静态 RAM 进行数字运算。互连架构实现处理单元之间的通信，可组合的内存方案动态分配资源以适应变化的工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sciencedirect.com/topics/computer-science/interconnection-architecture">Interconnection Architecture - an overview | ScienceDirect Topics</a></li>
<li><a href="https://www.nature.com/articles/s41586-022-04992-8">A compute-in-memory chip based on resistive random-access memory | Nature</a></li>
<li><a href="https://www.mdpi.com/2079-9292/10/9/1063">In-Memory Computing with Resistive Memory Circuits: Status and Outlook</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#compute-in-memory`, `#hardware accelerator`, `#chiplet architecture`, `#LoRA`

---

<a id="item-5"></a>
## [记忆增强草稿提升长上下文投机解码](https://arxiv.org/abs/2608.30252v1) ⭐️ 8.0/10

本文提出了一种用于长上下文投机解码的记忆增强草稿方法，为强大的独立草稿模型配备压缩的草稿侧 KV 缓存，以保留远距离信息和精确的近期上下文。在 Llama 3.1-8B 和 70B 上，前缀长度高达 32K 的实验显示，草稿侧内存减少超过 70%，相对于自回归解码加速比分别高达 2.08 倍和 3.33 倍。 这项工作通过提高投机解码效率，解决了长上下文 LLM 推理中的关键瓶颈，这对文档摘要和多轮代理等应用至关重要。所提出的方法提供了一种实用的解决方案，在保持无损保证的同时减少内存开销，可能影响未来的推理优化研究。 该方法使用轻量级适配器构建并增量更新压缩的草稿侧 KV 内存，而目标验证器保留其完整的 KV 缓存并应用标准的接受/拒绝规则，从而保持投机解码的无损保证。实验在大型模型上展示了显著的内存节省和加速，突出了草稿容量与 KV 访问成本之间的权衡。

rss · arXiv Speculative Decoding · 8月31日 05:03

**背景**: 投机解码是一种推理时优化技术，使用较小的草稿模型提出候选令牌，然后由较大的目标模型在单次前向传播中验证，保持原始输出分布的同时降低延迟。然而，在长上下文长度下，KV 缓存变得很大，增加了内存和访问成本，可能抵消投机解码的优势。本文通过压缩草稿侧 KV 缓存来解决这个问题，使得即使在长前缀下也能高效使用强大的草稿模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding</a></li>
<li><a href="https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/">Mastering LLM Techniques: Inference Optimization | NVIDIA Technical...</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#KV cache`, `#long-context LLM`, `#inference optimization`

---

<a id="item-6"></a>
## [DeepSeek V4 Flash Vision Exp 在 Hugging Face 上发布](https://www.reddit.com/r/LocalLLaMA/comments/1w3vhv9/deepseek_v4_flash_vision_is_out/) ⭐️ 8.0/10

DeepSeek 已在 Hugging Face 和 DeepSeek API 平台上发布了实验性多模态模型 DeepSeek-V4-Flash-Vision-Exp。这是 DeepSeek-V4 系列中首个具备视觉能力的模型，基于 V4-Flash 架构并添加了视觉模块。 此次发布标志着 DeepSeek 进入多模态 AI 领域，可能扩大其模型在视觉-语言任务中的应用。它可能影响依赖开源权重模型进行多模态应用的开发者和研究人员，在竞争激烈的 AI 领域中提供新的选择。 该模型为实验性模型，可通过 DeepSeek API 设置 model='deepseek-v4-flash-vision-exp' 进行访问。它基于 DeepSeek-V4-Flash 架构，并经过持续训练以解锁视觉理解能力。

reddit · r/LocalLLaMA · /u/Key_Solid_1696 · 8月31日 23:55

**背景**: DeepSeek 是一家以开源权重大型语言模型闻名的中国 AI 研究公司。DeepSeek-V4-Flash 是近期发布的模型，具有增强的智能体能力。多模态模型结合了文本和视觉理解，可实现图像描述和视觉问答等任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp">deepseek -ai/ DeepSeek - V 4 - Flash - Vision -Exp · Hugging Face</a></li>
<li><a href="https://api-docs.deepseek.com/updates/">DeepSeek API Docs</a></li>
<li><a href="https://lmstudio.ai/models/deepseek-v4-flash">DeepSeek V 4 Flash</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI`, `#Machine Learning`, `#Vision`, `#Model Release`

---