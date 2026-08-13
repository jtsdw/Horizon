---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 44 条内容中筛选出 8 条重要资讯。

---

1. [Qwen 发布 2.4T 参数 MoE 模型](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Pro 0813 发布，性能强劲且性价比高](#item-2) ⭐️ 8.0/10
3. [谷歌 DeepMind 的 SL2T 模型将手语转化为文本](#item-3) ⭐️ 8.0/10
4. [Blackwell Ultra 的 INT8 支持在 NVIDIA 全栈中被撤回](#item-4) ⭐️ 8.0/10
5. [高带宽闪存反而拖慢 KV 为中心的 LLM 服务](#item-5) ⭐️ 8.0/10
6. [语义 Lenia：大语言模型语义空间中稳态孤子的涌现](#item-6) ⭐️ 8.0/10
7. [通过监督架构和证据驱动调优实现 LLM 辅导员的答案保留](#item-7) ⭐️ 8.0/10
8. [VAKRA 基准测试揭示 AI 智能体在多跳推理上的困难](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 发布 2.4T 参数 MoE 模型](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) ⭐️ 9.0/10

Qwen 发布了 Qwen3.8-2.4T-A95B，这是一个拥有 2.4 万亿参数的混合专家（MoE）模型，激活参数为 950 亿，提供 BF16 和 FP8 两种格式。模型卡声称其性能介于 Opus 4.8 和 Fable 5 之间，并被定位为 Kimi k3 的竞争对手。 此次发布推动了开源大语言模型的前沿，提供了与顶级专有模型相当的性能，同时保持开源。它也凸显了超大规模 MoE 模型的增长趋势，以及随之而来的量化和服务挑战，这将影响 AI 基础设施生态系统。 该模型是一个 2.4T 参数的 MoE，激活参数为 950 亿，需要大量内存：BF16 约 4.9TB，FP8 约 2.4TB，1 位量化版本约 397GB。开源版本缺少视觉输入和 1M 上下文长度，这些功能保留给官方 Qwen3.8-Max。

hackernews · Philpax · 8月12日 15:01 · [社区讨论](https://news.ycombinator.com/item?id=49273478)

**背景**: 混合专家（MoE）模型每个 token 只激活部分参数，从而在计算成本不按比例增加的情况下实现更大的总参数量。FP8 等量化技术可以减少内存占用并加速推理，但可能需要校准数据并影响质量。像 Qwen3.8 这样的开源权重模型使社区能够进行实验和部署，但大规模服务它们需要高端硬件和优化的基础设施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/serve-qwen3-8-2-4t-a95b-a-2-4t-parameter-model-with-configurable-reasoning-on-nvidia-gb300-nvl72/">Serve Qwen 3 . 8 - 2 . 4 T -A95B, a 2 . 4 T -Parameter Model , with...</a></li>
<li><a href="https://www.remio.ai/post/qwen-3-8-open-weight-model-announcement-promises-2-4t-parameters-but-proof-comes">Qwen 3 . 8 Open-Weight Model Announcement Promises...</a></li>
<li><a href="https://witho2.com/news/qwen-3-8-alibaba-2-4t-open-weight-model">Qwen 3 . 8 Open Weight Model : 2 . 4 T Params, Not Shipped Yet</a></li>

</ul>
</details>

**社区讨论**: 社区评论关注模型的大小和服务挑战，指出只发布了 BF16 和 FP8，使其比 Kimi k3 更难服务。讨论还涉及需要 QAT 量化以将大小降至约 1.3TB，以及与 DeepSeek V4-Pro 基准的比较。一些用户对 1 位量化版本在消费级硬件上的性能印象深刻，而另一些用户则指出开源版本缺乏视觉和 1M 上下文功能。

**标签**: `#AI/ML`, `#Large Language Models`, `#MoE`, `#Qwen`, `#Open Source`

---

<a id="item-2"></a>
## [DeepSeek V4 Pro 0813 发布，性能强劲且性价比高](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek V4 Pro 0813 已发布，并已在 OpenRouter 上列出。用户反馈其在开发任务中性能强劲且性价比高，一位用户提到在交通模拟器中取得了显著改进且未引入新问题。 此次发布对 AI/ML 社区意义重大，因为它以低成本提供了高性能模型，可能颠覆昂贵的专有模型市场。它使开发者能够以可负担的价格处理繁重的开发任务，提高了先进 AI 能力的可及性。 该模型已在 OpenRouter 上提供，但官方 API 文档和基准测试链接提供了更多细节。用户指出了使用成本，一位用户报告约 12.50 美元用于 20 亿个 token，缓存命中率为 50%，表明 token 使用效率高。

hackernews · explosion-s · 8月12日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=49274600)

**背景**: DeepSeek 是一家以发布开源大语言模型而闻名的中国 AI 研究公司。V4 Pro 0813 是最新版本，继 DeepSeek Flash 更新之后推出，旨在以比 Claude Sonnet 或 Opus 等模型更低的成本处理复杂任务（如开发）。

**社区讨论**: 社区情绪积极，用户称赞模型的性能和性价比。一些用户将其与 Kimi-K3、GLM-5.2 和 Minimax 等其他模型进行有利比较，指出它能以极低的成本处理繁重的开发任务。一位用户建议链接到官方 API 文档和基准测试，而不是 OpenRouter，以获取更有用的信息。

**标签**: `#AI`, `#DeepSeek`, `#LLM`, `#release`, `#machine learning`

---

<a id="item-3"></a>
## [谷歌 DeepMind 的 SL2T 模型将手语转化为文本](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 8.0/10

谷歌 DeepMind 推出了手语转文本（SL2T）模型，这是一个突破性模型，为聋人和听力障碍用户提供新的手语功能。该模型已集成到 Gboard 和 Live Transcribe 中，可在 Pixel 11 设备上实时将手语转录为文本。 这一进展显著提升了无障碍性，使聋人和听力障碍用户在通常需要打字的日常场景中能够更自然地交流。它代表了 AI 在弥合沟通鸿沟方面的重要一步，可能影响整个科技行业未来的无障碍功能。 SL2T 模型嵌入在 Gboard 和 Live Transcribe 中，并在 Pixel 11 设备上提供。它能够实时将手语转换为文本，为偏好手语而非打字的用户提供了实用工具。

rss · Google DeepMind Blog · 8月12日 14:01

**背景**: 手语识别（SLR）技术已发展多年，利用 AI 解读手势和面部表情。传统的 SLR 系统通常需要专用硬件或仅限于特定词汇。谷歌 DeepMind 的 SL2T 模型旨在通过将其集成到广泛使用的移动应用中，使这项技术更易获取，可能促进聋人和听力障碍社区的更广泛采用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands — Google DeepMind</a></li>
<li><a href="https://www.engadget.com/2234618/deepmind-newest-model-allows-pixel-11-devices-to-transcribe-sign-language-into-text/">DeepMind's newest model allows Pixel 11 devices to transcribe sign language into text - Engadget</a></li>
<li><a href="https://cryptobriefing.com/google-deepmind-sl2t-sign-language-text-model/">Google DeepMind's SL2T model brings sign language recognition to deaf and hard of hearing users</a></li>

</ul>
</details>

**标签**: `#AI`, `#accessibility`, `#sign language`, `#DeepMind`, `#NLP`

---

<a id="item-4"></a>
## [Blackwell Ultra 的 INT8 支持在 NVIDIA 全栈中被撤回](https://arxiv.org/abs/2608.11693v1) ⭐️ 8.0/10

一项审计显示，NVIDIA 的 Blackwell Ultra GPU（B300）在 PTX 和 CUTLASS 中缺乏 INT8 张量核心支持，尽管规格表暗示 FP8:INT8 比率为 30:1。PTX ISA 从未在 sm_103a 上暴露带有 .kind::i8 的 tcgen05.mma，并且 CUTLASS 跳过为 103a 目标生成 INT8 UMMA。 这一差异影响了 vLLM 和 SGLang 等 LLM 推理引擎，它们默认无法在 Blackwell Ultra 上运行 INT8 量化模型。这凸显了量化格式的可用性是整个软件栈的属性，而不仅仅是硬件规格表。 审计追踪了 INT8 W8A8 支持在四个层面：规格、PTX、CUTLASS 和推理引擎。它记录了通过 Triton 后端为 vLLM 提供的逃生通道、分析器方法中的假阴性陷阱，以及使简单测试成本高昂的失败语义。

rss · arXiv LLM Inference · 8月12日 06:04

**背景**: NVIDIA 的 Blackwell 架构引入了 tcgen05.mma 指令用于张量核心操作，取代了 Hopper 的 wgmma。虽然 PTX ISA 9.3 文档将 INT8 列为 tcgen05.mma 支持的类型，但审计发现 .kind::i8 变体未在 sm_103a 上暴露，仅留下传统的 warp 级 IMMA。这造成了宣传能力与实际软件支持之间的差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.nvidia.com/cuda/parallel-thread-execution/">1. Introduction — PTX ISA 9.3 documentation</a></li>
<li><a href="https://docs.nvidia.com/cutlass/latest/media/docs/cpp/blackwell_functionality.html">Blackwell SM100 GEMMs — NVIDIA CUTLASS Documentation</a></li>
<li><a href="https://research.colfax-intl.com/cutlass-tutorial-writing-gemm-kernels-using-tensor-memory-for-nvidia-blackwell-gpus/">CUTLASS Tutorial: Writing GEMM Kernels Using Tensor Memory For NVIDIA® Blackwell GPUs - Colfax Research</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#GPU`, `#INT8`, `#LLM serving`, `#PTX`

---

<a id="item-5"></a>
## [高带宽闪存反而拖慢 KV 为中心的 LLM 服务](https://arxiv.org/abs/2608.11668v1) ⭐️ 8.0/10

一篇新论文表明，在 Mooncake 风格的 KV 卸载栈中用高带宽闪存（HBF）替代 SSD 会降低 LLM 服务性能，在 H100 和 B200 配置下，平均端到端延迟增加 2-5.5 倍，最大 SLO 有效吞吐量降低 1.1-2.7 倍。 这挑战了“更快的存储直接提升 LLM 服务性能”的常见假设，揭示了 GPU 近层容量和带宽的权衡可能超过 HBF 的读取优势。它为 AI 基础设施中的存储层次设计提供了关键见解，指导架构师将 HBF 用作选择性存储而非直接替代 SSD。 该研究使用了扩展的 TokenSim 模拟器，包含四个两小时的 Qwen-Bailian 生产轨迹、五个密集和混合专家模型，以及 H100/B200 配置。成本效益模型表明，HBF 仅在读取 I/O 成为瓶颈、读取多于写入且带宽可持续时才有帮助；而瞬时 KV 不满足这三个条件。此外，3D-ICE 模型显示写密集型流将栈推向热极限，且 TLC HBF 比容量匹配的 SSD 池磨损更快。

rss · arXiv LLM Inference · 8月12日 05:25

**背景**: 高带宽闪存（HBF）将 NAND 堆叠在宽封装本地接口后面，提供闪存级容量，且读取延迟和带宽优于 SSD。Mooncake 是一个服务平台，采用混合 KV 缓存管理，并卸载到 SSD 以平衡成本和性能。TokenSim 是一个 LLM 服务模拟器，模拟硬件和软件优化，包括分离的预填充/解码架构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/kvcache-ai/Mooncake">GitHub - kvcache-ai/Mooncake: Mooncake is the serving platform for Kimi, a leading LLM service provided by Moonshot AI. · GitHub</a></li>
<li><a href="https://kvcache-ai.github.io/Mooncake/design/mooncake-store.html">Mooncake Store — Mooncake</a></li>
<li><a href="https://arxiv.org/pdf/2503.08415v1">TokenSim : Enabling Hardware and Software Exploration for</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#storage systems`, `#KV cache`, `#high-bandwidth flash`, `#performance characterization`

---

<a id="item-6"></a>
## [语义 Lenia：大语言模型语义空间中稳态孤子的涌现](https://arxiv.org/abs/2608.11657v1) ⭐️ 8.0/10

语义 Lenia 将大语言模型推理转化为 logit 空间中的连续动力系统，引入稳态反馈回路以平衡语义吸引与句法排斥。这导致“自主语义孤子”的涌现，避免了重复结晶，并使生成轨迹保持在混沌边缘。 该框架利用动力系统理论为生成模型控制提供了新方法，可能实现更具创造性和连贯性的输出。它连接了人工生命与 LLM 研究，为理解机器认知和提升生成模型稳定性开辟了新途径。 论文识别出一条关键的“宜居脊”，在此处引导力与句法惯性平衡，实现溯因跳跃而不致结构崩溃。它还建立了机器认知的物理标度律，但该工作为预印本，实际影响尚不明确。

rss · arXiv LLM Inference · 8月12日 04:56

**背景**: Lenia 是一种连续元胞自动机，能生成复杂、类似生命的图案，与康威生命游戏等离散自动机形成对比。大语言模型（LLM）通常将推理视为静态优化，但语义 Lenia 将其重新解释为动力系统，借鉴了认知架构中的稳态反馈回路等概念。该方法与近期将 LLM 嵌入闭环控制系统以实现更自适应行为的努力一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lenia">Lenia - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2205.10463">[2205.10463] Glaberish: Generalizing the continuously-valued Lenia framework to arbitrary Life-like cellular automata</a></li>
<li><a href="https://www.techrxiv.org/doi/pdf/10.36227/techrxiv.176779758.84227760">Enactive Cognitive Architectures for LLMs: A Homeostatic ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#artificial life`, `#dynamical systems`, `#generative models`, `#semantic solitons`

---

<a id="item-7"></a>
## [通过监督架构和证据驱动调优实现 LLM 辅导员的答案保留](https://arxiv.org/abs/2608.12292v1) ⭐️ 8.0/10

该论文介绍了一个已部署的 LLM 辅导系统，通过监督架构和证据驱动的调优方法强制实现答案保留，并在随机研究中达到了所有四项验收标准的完全合规。 这项工作解决了 AI 辅导中的一个关键挑战——苏格拉底式教学中可靠的答案保留，这直接影响学习效果和 AI 安全。所提出的架构和调优循环为任何必须拒绝其拥有能力的 LLM 代理提供了可复用的方法，可能影响未来的教育 AI 系统。 该系统使用一个非 LLM 策略核心，读取可信的学习者状态，在八级帮助阶梯上设置每轮上限，一个确定性检测器去除解决方案代码，以及一个单独的 LLM 法官检查有风险的回复。调优过程使用脚本化的学生角色和更强的模型进行重新评分，揭示了一个可解释的“过度帮助阶梯”，从解决方案泄露到过度引用事实。

rss · arXiv Agent Infra · 8月12日 17:35

**背景**: 大型语言模型（LLM）越来越多地用于教育辅导，但它们常常直接给出答案，这可能阻碍学习。苏格拉底式辅导通过保留答案并引导学生思考问题，已被证明能提高长期记忆。然而，可靠地强制答案保留很困难，因为模型在压力下可能会泄露解决方案。本文提出了一种监督架构和证据驱动的调优方法以确保合规。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.evelynlearning.com/blog/the-socratic-method-meets-machine-learning-how-ai-tutoring-tools-are-teaching-students-to-think-not-just-answer">AI Tutoring & the Socratic Method in Higher... | Evelyn Learning</a></li>
<li><a href="https://arxiv.org/html/2607.22996">Beyond Direct Answering : Aligning Educational LLMs as Socratic ...</a></li>
<li><a href="https://www.medhavy.com/blog/socratic-prompting-the-midwifery">Socratic Prompting: The Midwifery of Thought - Medhavy</a></li>

</ul>
</details>

**标签**: `#LLM`, `#AI in Education`, `#Socratic Tutoring`, `#AI Safety`, `#Tutoring Systems`

---

<a id="item-8"></a>
## [VAKRA 基准测试揭示 AI 智能体在多跳推理上的困难](https://arxiv.org/abs/2608.12282v1) ⭐️ 8.0/10

IBM 研究人员推出了 VAKRA 基准测试，包含 62 个领域的 8000 多个可执行 API，用于评估 AI 智能体的多跳推理能力。该基准测试显示，即使最好的模型在单跳任务上也仅达到 70.4%的准确率，在组合 API 上降至 50-51%，且随着推理深度增加，性能下降超过 50%。 该基准测试通过将 API 和检索任务与工具使用策略相结合，填补了关键空白，反映了真实的企业智能体场景。研究结果强调，语言中介推理（而非工具调用机制）是主要瓶颈，为未来研究指明了改进实体消歧和跨源基础的方向。 该基准测试包含三个难度递增的设置：多样化的 API 交互风格、结构化 API 上的多跳推理、以及带有自然语言工具使用策略约束的多源推理。正确性通过重新执行预测的工具调用与实时 API 进行验证，并允许多种有效路径。策略约束问题暴露出严重失败，在不可回答查询上的准确率低至 2.4%。

rss · arXiv Agent Infra · 8月12日 17:27

**背景**: 企业 AI 智能体通常需要跨结构化 API 和文档集合进行推理，但现有基准测试孤立地评估这些能力。VAKRA 使用固定的 ReAct 框架来隔离模型能力与智能体架构，从而公平比较前沿和开放权重模型。该基准测试已在 GitHub 和 Hugging Face 上公开，其设计包括实时 API 验证以确保实际相关性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/new/announcements/introducing-vakra-benchmark">Introducing VAKRA : Benchmark for evaluating multi - hop ... | IBM</a></li>
<li><a href="https://github.com/IBM/vakra/blob/main/README.md">vakra /README.md at main · IBM/ vakra · GitHub</a></li>
<li><a href="https://ibm-research-vakra.hf.space/">VAKRA — Multi - Hop , Multi-Source, Multi-Tool Agent Benchmark</a></li>

</ul>
</details>

**标签**: `#benchmark`, `#multi-hop reasoning`, `#tool-use`, `#agents`, `#retrieval`

---