---
layout: default
title: "Horizon Summary: 2026-07-30 (ZH)"
date: 2026-07-30
lang: zh
---

> 从 64 条内容中筛选出 8 条重要资讯。

---

1. [开源引擎在 M 系列 Mac 上仅用 2GB 内存运行 Gemma 4 26B](#item-1) ⭐️ 9.0/10
2. [llama.cpp b10174 为 GLM-5.2 添加 NextN/MTP 推测解码支持](#item-2) ⭐️ 8.0/10
3. [两个 API 设置使 GPT-5.6 在 ARC-AGI-3 上的得分提高三倍](#item-3) ⭐️ 8.0/10
4. [OpenAI 向 10 万研究人员免费提供 ChatGPT](#item-4) ⭐️ 8.0/10
5. [面向 LLM KV 缓存的光子-CXL 内存设备](#item-5) ⭐️ 8.0/10
6. [OmegaUse-OfficeVal：基于经济成本的办公任务 LLM 智能体基准测试](#item-6) ⭐️ 8.0/10
7. [InferScale：面向个性化 LLM 服务的 GPU 原生 KV 注入](#item-7) ⭐️ 8.0/10
8. [NELSSA：面向混合长度 LLM 服务的 GPU-PNM 异构系统](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [开源引擎在 M 系列 Mac 上仅用 2GB 内存运行 Gemma 4 26B](https://github.com/drumih/turbo-fieldfare) ⭐️ 9.0/10

TurboFieldfare 是一个开源的 Swift/Metal 推理引擎，通过从 SSD 流式传输路由专家，在任何 M 系列 Mac 上仅用约 2GB 内存即可运行 4 位量化的 Gemma 4 26B-A4B-IT 模型。 这一突破使得在内存受限的设备（如 8GB MacBook Air）上运行大型 MoE 模型成为可能，无需昂贵的硬件升级即可普及设备端 AI。 该引擎在 8GB M2 MacBook Air 上达到 5–6 tok/s，在 M5 MacBook Pro 上达到 31–35 tok/s，通过小型专家缓存和有界并行 pread 将 SSD 读取与 GPU 计算重叠。

hackernews · gitpusher42 · 7月29日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=49098510)

**背景**: Gemma 4 26B-A4B 是一个混合专家（MoE）模型，总参数量 260 亿，但每个 token 仅激活 40 亿参数。传统推理需要将所有 260 亿参数加载到 RAM 中，超出大多数消费级 Mac 的内存。TurboFieldfare 仅将共享层和 KV 缓存保留在 RAM 中，按需从 SSD 流式传输专家权重。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/google/gemma-4-26B-A4B">google/gemma-4-26B-A4B · Hugging Face</a></li>
<li><a href="https://ai.google.dev/gemma/docs/core">Gemma 4 model overview | Google AI for Developers</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了这一创新，有人指出 llama.cpp 通过 mmap 也能在低内存下运行大模型，但缺乏同步 SSD 读取。其他人询问了与其他模型（如 Qwen3）和树莓派的兼容性，并提供了针对旧版 macOS 的编译技巧。

**标签**: `#on-device AI`, `#inference engine`, `#model quantization`, `#Mac`, `#open-source`

---

<a id="item-2"></a>
## [llama.cpp b10174 为 GLM-5.2 添加 NextN/MTP 推测解码支持](https://github.com/ggml-org/llama.cpp/releases/tag/b10174) ⭐️ 8.0/10

llama.cpp 发布版本 b10174，为 GLM-5.2 模型添加了 NextN/MTP 推测解码支持，通过轻量级草稿头每步预测多个 token，实现更快的推理。 这一优化显著降低了大型 MoE 模型 GLM-5.2 的推理延迟，使其更适用于实时应用，并降低了 AI 从业者的计算成本。 该实现包括一个 graph_mtp 构建器，包含密集 MLA、sigmoid 门控 MoE 和共享专家/头，以及一个单独的 MTP KV 缓存，仅保存 nextn 层，而主上下文使用过滤后的 DSA 缓存。

github · github-actions[bot] · 7月29日 07:14

**背景**: 推测解码通过使用小型草稿模型生成候选 token，再由大模型并行验证，从而加速 LLM 推理。GLM-5.2 采用密集-稀疏交替（DSA）架构和 IndexShare 稀疏注意力机制，高效处理长上下文。NextN/MTP（多 token 预测）是一种轻量级草稿头，可一次性预测多个未来 token，进一步提升吞吐量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rocm.blogs.amd.com/software-tools-optimization/mtp/README.html">Efficient LLM Serving with MTP : DeepSeek V3 and... — ROCm Blogs</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.2">GLM-5.2 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#speculative decoding`, `#GLM-5.2`, `#inference optimization`, `#machine learning`

---

<a id="item-3"></a>
## [两个 API 设置使 GPT-5.6 在 ARC-AGI-3 上的得分提高三倍](https://openai.com/index/how-two-settings-tripled-our-arc-agi-3-scores) ⭐️ 8.0/10

OpenAI 发现，启用两个 API 设置——保留推理（retained reasoning）和压缩（compaction）——使 GPT-5.6 Sol 在 ARC-AGI-3 基准测试中的得分从 7.8%提高到 13.3%，同时输出 token 减少了 6 倍。 这一发现表明，简单的配置更改可以显著提升 AI 在复杂推理基准上的表现，为在智能体任务中部署大型语言模型提供了实用见解。 保留推理（retained reasoning）跨轮次保留模型的思维链，而压缩（compaction）则总结长对话历史以适配上下文限制。官方测试工具得分为 13.3%，虽仍远低于人类水平，但代表了显著的相对提升。

rss · OpenAI Blog · 7月29日 15:00

**背景**: ARC-AGI-3 是一个交互式基准测试，通过新颖的 2D 解谜游戏测试 AI 智能体的探索、目标推断和规划能力。之前的模型如 GPT-5.5 在此基准上仅得 0.4%，凸显了此类智能体推理任务的难度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">[2603.24621] ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence</a></li>

</ul>
</details>

**标签**: `#AI`, `#benchmark`, `#GPT`, `#reasoning`, `#ARC-AGI`

---

<a id="item-4"></a>
## [OpenAI 向 10 万研究人员免费提供 ChatGPT](https://openai.com/index/chatgpt-for-academic-researchers) ⭐️ 8.0/10

OpenAI 正在向 10 万名学术研究人员免费提供其最先进的 AI 模型（通过 ChatGPT），以加速科学发现。 这一举措可能通过向学者提供以前昂贵或难以获得的强大 AI 工具，大幅加速各学科的研究，从而在医学、物理学等领域带来突破。 该优惠包括通过 ChatGPT 访问 OpenAI 最先进的模型（如 GPT-4 及更高版本），面向全球学术研究人员。

rss · OpenAI Blog · 7月29日 10:00

**背景**: ChatGPT 是一个对话式 AI 系统，可协助数据分析、文献综述和假设生成等任务。学术研究通常需要处理大量信息并生成见解，而 AI 可以加速这一过程。

**标签**: `#AI`, `#OpenAI`, `#academic research`, `#scientific discovery`, `#ChatGPT`

---

<a id="item-5"></a>
## [面向 LLM KV 缓存的光子-CXL 内存设备](https://arxiv.org/abs/2607.27187v1) ⭐️ 8.0/10

研究人员提出了 Marvell 光子织物内存设备，这是一种光子-CXL 混合架构，用无源光纤混洗替代电开关，为 LLM 推理提供跨 16 台主机的 32 TB 共享内存。仿真结果显示，与电 CXL 池相比，延迟降低超过 50%。 这解决了 LLM 推理中关键的 KV 缓存内存墙问题，支持长上下文模型的可扩展部署。该架构消除了缓存驱逐悬崖，并将多轮对话的首令牌时间提升 6.6 倍，有望变革 AI 基础设施。 该设计采用无开关的全交叉拓扑结构，使用无源光纤混洗，在 16 台主机间实现 32 TB 共享内存。仿真显示与电 CXL 池相比延迟降低超过 50%，并在多轮工作负载中消除了缓存驱逐悬崖。

rss · arXiv LLM Inference · 7月29日 17:55

**背景**: LLM 推理需要大型 KV 缓存来存储中间注意力状态，但当前内存层级无法同时满足容量和带宽需求。CXL 内存池化提供了一种潜在解决方案，但存在交换机延迟、线缆距离限制和功耗扩展问题。光子互连提供高带宽和低延迟，适合扩展内存池。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>
<li><a href="https://computeexpresslink.org/blog/overcoming-the-ai-memory-wall-how-cxl-memory-pooling-powers-the-next-leap-in-scalable-ai-computing-4267/">Overcoming the AI Memory Wall: How CXL Memory Pooling Powers...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#KV cache`, `#photonics`, `#CXL`, `#memory architecture`

---

<a id="item-6"></a>
## [OmegaUse-OfficeVal：基于经济成本的办公任务 LLM 智能体基准测试](https://arxiv.org/abs/2607.27155v1) ⭐️ 8.0/10

研究人员推出了 OmegaUse-OfficeVal 基准测试，包含 100 个具有经济基础的长期办公套件任务，并提供了人类劳动时间和任务价格代理用于成本比较。该基准测试评估 LLM 智能体在文字处理、电子表格和演示文稿等任务上的表现，并使用基于代码的验证器进行稳定评估。 该基准测试能够直接比较人类工作者与 LLM 智能体之间的成本效益，填补了智能体评估中的一个关键空白。它提供了一种标准化方法来衡量 LLM 智能体能否以合理成本完成办公工作流程，这对于实际部署至关重要。 这 100 个任务平均需要 2.32 小时的人类劳动，每个任务都配有经济信号：人类劳动时间和任务价格代理。评估的前沿 LLM 虽然比人类更便宜、更快，但尚未达到人类水平的交付质量。

rss · arXiv LLM Inference · 7月29日 17:33

**背景**: LLM 智能体是能够自主执行任务的 AI 系统，例如编辑文档或创建电子表格。现有的基准测试通常缺乏经济考量，难以将智能体成本与人类劳动进行比较。OmegaUse-OfficeVal 引入了任务级经济基础，使得这种比较成为可能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.27155v1">OmegaUse-OfficeVal: Benchmarking LLM Agents on Long-Horizon ...</a></li>
<li><a href="https://github.com/baidu-frontier-research/OmegaUse-OfficeVal">baidu-frontier-research/OmegaUse-OfficeVal - GitHub</a></li>
<li><a href="https://huggingface.co/papers/2607.27155">OmegaUse-OfficeVal: Benchmarking LLM Agents on Long-Horizon ...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#benchmark`, `#office automation`, `#economic grounding`

---

<a id="item-7"></a>
## [InferScale：面向个性化 LLM 服务的 GPU 原生 KV 注入](https://arxiv.org/abs/2607.27090v1) ⭐️ 8.0/10

InferScale 提出了一种 GPU 原生内存系统，它预先计算记忆事实的 KV 表示，并直接注入到 vLLM 的分页缓存中，从而消除了个性化 LLM 服务中重复的提示预填充。它还提出了 Chunked RoPE 来处理旋转位置嵌入下动态组装的内存。 该方法显著降低了个性化 LLM 服务的首令牌时间（TTFT），使其在检索预算增加时几乎保持不变，这对对话式 AI 等实时应用至关重要。它在不牺牲准确性的情况下实现了 72-79%的 TTFT 降低和 3.7-4.5 倍的吞吐量提升，使个性化 LLM 服务更加实用和经济高效。 InferScale 通过 vLLM 的 KV 连接器接口实现，无需修改引擎或微调模型。它使用上下文窗口编码（Context-Window Encoding）来缓解跨事实上下文的丢失，通过将每个记忆事实与前面的一小段对话上下文一起编码，同时只缓存目标事实的 KV。

rss · arXiv LLM Inference · 7月29日 16:18

**背景**: 大型语言模型（LLM）通常使用持久的个性化上下文，如记忆档案或对话历史，这些内容在每次请求时被检索并注入到提示中。传统的服务系统会重复预填充相同的内容，导致 TTFT 随检索预算增加而增加。KV 缓存存储注意力层中的键值对以避免重复计算，vLLM 的分页缓存高效地管理这些缓存。旋转位置嵌入（RoPE）通过旋转查询和键向量来编码令牌位置，这给位置变化时的直接 KV 注入带来了复杂性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/paged_attention/">Paged Attention - vLLM</a></li>
<li><a href="https://adalkiran.github.io/llama-nuts-and-bolts/10-ROPE-ROTARY-POSITIONAL-EMBEDDINGS/">RoPE ( ROTARY POSITIONAL EMBEDDINGS ) - Llama Nuts and Bolts</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#KV cache`, `#personalization`, `#GPU memory`, `#inference optimization`

---

<a id="item-8"></a>
## [NELSSA：面向混合长度 LLM 服务的 GPU-PNM 异构系统](https://arxiv.org/abs/2607.26633v1) ⭐️ 8.0/10

NELSSA 是一个 GPU-PNM 异构 LLM 服务系统，采用基于长度的请求放置策略，将短上下文请求路由到 GPU，长上下文请求路由到近内存处理（PNM）加速器，并支持运行时迁移以应对动态上下文增长。相比纯 GPU 基线，吞吐量提升最高达 5.5 倍，P99 延迟降低最高达 15 倍。 该工作解决了由混合长度工作负载引起的 LLM 服务关键性能瓶颈，这类负载在智能体应用中日益常见。通过基于 CXL 分解的 GPU 与 PNM 加速器集成，NELSSA 展示了一种可扩展且灵活的 LLM 基础设施的有前景范式。 NELSSA 在 PNM 上实现了设备级稀疏注意力、GPU 解码内核，以及一个主机端运行时，通过支持 RPC 和 RDMA 的 CXL 协调调度和跨层级内存移动。该原型是端到端的，并使用硬件感知的交叉阈值进行基于长度的放置。

rss · arXiv LLM Inference · 7月29日 08:58

**背景**: 现代 LLM 服务系统面临上下文长度从几百到几十万 token 的异构工作负载。以 GPU 为中心的架构在处理混合长度工作负载时效率低下，因为其吞吐量依赖于受内存限制的大批量。近内存处理（PNM）将计算靠近内存以减少数据移动，而 CXL 支持跨层级的内存分解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.26633v1">NELSSA: A GPU–PNM Heterogeneous System for Mixed-Length LLM ...</a></li>
<li><a href="https://people.inf.ethz.ch/omutlu/pub/ModernPrimerOnPIM_springer-emerging-computing-bookchapter21.pdf">Modern Primer on Processing in Memory</a></li>
<li><a href="https://www.emergentmind.com/topics/processing-near-memory">Processing - Near - Memory Architectures</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#GPU`, `#Processing-near-Memory`, `#heterogeneous computing`, `#systems`

---