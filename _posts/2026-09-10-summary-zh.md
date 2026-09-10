---
layout: default
title: "Horizon Summary: 2026-09-10 (ZH)"
date: 2026-09-10
lang: zh
---

> 从 58 条内容中筛选出 8 条重要资讯。

---

1. [OpenAI 发布 GPT-6 Astra，面向企业的最强模型](#item-1) ⭐️ 9.0/10
2. [vLLM v0.29.0 发布：Model Runner V2 成为所有模型的默认执行核心](#item-2) ⭐️ 8.0/10
3. [Hugging Face Transformers v5.17.0 新增 7800 亿参数 HYV4 MoE 模型](#item-3) ⭐️ 8.0/10
4. [Maverick 通过矩阵-向量乘法委托实现私密可验证的大模型推理](#item-4) ⭐️ 8.0/10
5. [HBFSim 在真实 GPU 上模拟高带宽闪存以加速 LLM 推理](#item-5) ⭐️ 8.0/10
6. [Epoch 将扩散块编译为稀疏 MoE 服务单元](#item-6) ⭐️ 8.0/10
7. [Avatar 利用 LLM 自主编排科学工作流](#item-7) ⭐️ 8.0/10
8. [内核管理的共享内存提升 AIOS 上的 AI 个性化能力](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6 Astra，面向企业的最强模型](https://openai.com/index/gpt-6-astra-next-generation-work) ⭐️ 9.0/10

OpenAI 发布了 GPT-6 Astra，称其为面向企业场景能力最强的模型，具备高级推理、计算机操作以及更强的写作与设计判断力。据维基百科介绍，该模型于 2026 年 9 月 3 日先向获批用户开放，次日全面可用。 这是 OpenAI 的一次重要前沿模型发布，其对企业工作流、计算机操作和设计判断的侧重，表明 AI 厂商的竞争正从聊天转向自动化知识工作。这将影响选择 AI 平台的企业，也会波及 Anthropic、Google 等直接竞争计算机操作与推理模型的实验室。 OpenAI 强调 Astra 仅凭演示模板中的几页幻灯片，就能制作出关于一个虚构模型的完整幻灯片，且语气与版式保持一致，说明其模板遵循与设计感更强。社区讨论还提到有报道称 Astra 采用了“循环深度”或循环 Transformer，该技术通过复用层间权重来节省 GPU 显存，而非某种全新的隐藏推理机制。

rss · OpenAI Blog · 9月9日 11:00

**背景**: GPT-6 Astra 是 OpenAI 的大语言模型，属于其 GPT 系列的最新一代，定位为面向职场与企业使用。“计算机操作”指 AI 模型通过返回鼠标键盘动作或编写代码来直接操控软件界面，而不依赖定制工具。“高级推理”模型会在作答前投入额外算力进行逐步思考，这一能力已成为各大 AI 实验室的关键竞争点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra - Wikipedia</a></li>
<li><a href="https://openai.com/index/gpt-6-astra/">GPT-6 Astra : A new generation of intelligence | OpenAI</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/tools-computer-use">Computer use | OpenAI API</a></li>

</ul>
</details>

**社区讨论**: 评论者对实时计算机操作演示印象深刻，有人称 MSPAINT 演示令人瞠目结舌。另一些人则讨论其技术原理，认为循环 Transformer 本质上等同于堆叠更多层，只是节省了 GPU 显存；还有用户抱怨 Astra 在周二的一次变动后质量似乎下降，感觉现在像是一个更弱的模型。

**标签**: `#OpenAI`, `#GPT-6`, `#AI model release`, `#business AI`, `#natural language processing`

---

<a id="item-2"></a>
## [vLLM v0.29.0 发布：Model Runner V2 成为所有模型的默认执行核心](https://github.com/vllm-project/vllm/releases/tag/v0.29.0) ⭐️ 8.0/10

vLLM 发布 v0.29.0，包含来自 277 位贡献者的 594 次提交，在完成从池化模型开始的推广后，正式将 Model Runner V2（MRV2）设为所有模型的默认执行核心。该版本还新增了对多款大模型的支持，包括腾讯 770B 总参数/49B 激活参数的 Hy4-preview MoE、Qwen3.8-Flash-Next、GraniteSWA/GraniteMoeSWA、NemotronH_Omni_Reasoning_V3 以及 Kimi K3 NVFP4 检查点，并带来大量推理性能优化。 将 MRV2 全面设为默认是 vLLM 这一最广泛使用的开源 LLM 推理引擎的重要架构里程碑，因为 MRV2 用 GPU 原生 Triton 内核和异步调度重构了执行核心以提升吞吐。新增大模型支持与性能优化将直接影响所有在生产环境中部署前沿 MoE 与推理模型的用户。 MRV2 新增了用于 KV 缓存自动定容的 CUDA graph 内存分析、可将每步 logits 内存降低 1/TP 的批分片采样、prompt embeds，以及为投机解码下统一 decode 提供的填充式 FULL cudagraph 调度；MRV1 仍在少数 ROCm 模型及 MRV2 尚未支持的功能中继续使用。破坏性变更包括移除十种已弃用的模型架构、将 FlexOlmo/Olmo3/Hunyuan V1/VL 迁移至 Transformers 建模后端、移除 PyAV 视频解码器，以及弃用 `python -m vllm.entrypoints.openai.api_server` 转而推荐 `vllm serve`。

github · khluu · 9月9日 08:54

**背景**: vLLM 是面向大语言模型的开源高吞吐推理服务引擎，其 Model Runner 是真正在 GPU 上执行模型前向计算的组件。Model Runner V2（MRV2）从第一性原理重新构建，用 GPU 原生 Triton 内核取代了早期基于 Python 的运行器，并通过异步调度将 CPU 调度与 GPU 执行分离，官方称其可显著提升吞吐。本次发布通过将 MRV2 设为所有模型的默认执行核心完成了这一迁移，同时为少数 ROCm 场景及 MRV2 尚未支持的功能保留了旧版 MRV1。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://www.spheron.network/blog/vllm-model-runner-v2-mrv2-deployment-guide/">vLLM Model Runner V2 on GPU Cloud: Deploy MRV2 for Faster LLM Inference (2026) | Spheron Blog</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#model-serving`, `#release`, `#gpu-optimization`

---

<a id="item-3"></a>
## [Hugging Face Transformers v5.17.0 新增 7800 亿参数 HYV4 MoE 模型](https://github.com/huggingface/transformers/releases/tag/v5.17.0) ⭐️ 8.0/10

Hugging Face 发布了 Transformers v5.17.0，新增了 HYV4（Hy4-Preview）——一个拥有 7800 亿参数、每个 token 激活 490 亿参数的混合专家语言模型，支持 100 万 token 的上下文窗口。该版本还引入了用于多说话人语音合成的 VibeVoice、NeoMME 多模态编码器以及 Fun-ASR-Nano 语音识别模型。 此次发布将一个具有新颖注意力机制的前沿规模 MoE 模型引入最广泛使用的开源模型库，使开发者无需编写自定义代码即可直接加载。这表明 MLA 和稀疏注意力等先进长上下文架构正逐渐成为主流生态中的标准组件。 HYV4 结合了多头潜在注意力（MLA）、带 IndexShare 的 DeepSeek 稀疏注意力（DSA）、带可学习注意力汇的门控 MLA 以及独立超连接（iHC）。每个 MoE 层包含 256 个路由专家和一个共享专家，每个 token 被路由到其中 8 个专家；该实现在加载时会忽略多 token 预测（MTP）层，但保留其权重以供其他运行时进行投机解码。

github · vasqu · 9月9日 15:42

**背景**: 混合专家（MoE）是一种将模型拆分为多个专门子网络（专家）的架构，每个输入 token 只被路由到其中少数几个专家，从而以更低的单 token 计算成本获得大模型容量。多头潜在注意力（MLA）将键和值压缩为低秩潜在表示以减少内存占用，而 DeepSeek 稀疏注意力（DSA）则使用轻量级索引器为每个查询只选择最相关的键，从而降低长上下文注意力的开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2512.02556">[2512.02556] DeepSeek-V3.2: Pushing the Frontier of Open Large Language Models</a></li>
<li><a href="https://www.emergentmind.com/topics/deepseek-sparse-attention-dsa">DeepSeek Sparse Attention Mechanism (DSA)</a></li>

</ul>
</details>

**标签**: `#huggingface`, `#transformers`, `#mixture-of-experts`, `#large-language-models`, `#attention-mechanisms`

---

<a id="item-4"></a>
## [Maverick 通过矩阵-向量乘法委托实现私密可验证的大模型推理](https://arxiv.org/abs/2609.10264v1) ⭐️ 8.0/10

Maverick 提出了首个信息论意义上可靠的矩阵-向量乘法委托验证协议，该运算是大语言模型中的主导操作，且具有透明预处理和几乎为零的服务器开销。结合基于 LPN 的伪随机掩码实现输入隐私，在 Qwen3-4B 上的端到端原型相比本地推理，在单客户端线程和最多 128 线程的 CPU 服务器下，在线掩码、预计算掩码和仅验证场景分别实现了最高 17 倍、45 倍和 44 倍的吞吐量提升。 这项工作解决了外包大模型推理中关键的隐私和正确性缺口，即用户必须信任第三方服务商处理其输入和输出。通过以极小的服务器开销使私密且可验证的推理变得实用，Maverick 有望推动更广泛地采用不可信的云或边缘服务器来运行开源大模型，而无需牺牲机密性或完整性。 该协议提供信息论意义上可靠的验证，具有透明预处理和高效的批量验证，并将此原语与基于 LPN 的伪随机掩码结合以实现输入隐私。评估显示，在四个客户端线程下，在线掩码、预计算掩码和仅验证场景的吞吐量提升分别为 13 倍、18 倍和 17 倍；当服务器计算不再是瓶颈时，带有模拟网络延迟的客户端微基准测试显示加速比分别为 12-20 倍、34-135 倍和 38-157 倍。

rss · arXiv LLM Inference · 9月9日 14:53

**背景**: 大语言模型在推理过程中会执行大量矩阵-向量乘法，而缺乏本地算力的用户通常将推理外包给第三方服务商，这引发了隐私和正确性问题。现有的隐私保护或可验证推理方案通常会给服务器带来沉重开销，或依赖硬件证明等额外信任假设。Maverick 转而通过密码学验证协议来委托矩阵-向量乘法本身，旨在不增加服务器端沉重成本的情况下提供强安全保证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Matrix_multiplication">Matrix multiplication - Wikipedia</a></li>
<li><a href="https://docs.opengradient.ai/learn/onchain_inference/private_inference.html">Private LLM Inference | OpenGradient Docs</a></li>
<li><a href="https://arxiv.org/pdf/2603.18046">NanoZK: Privacy -Preserving Verifiable Inference for Large Language...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#privacy`, `#verifiable computation`, `#matrix-vector multiplication`, `#cryptography`

---

<a id="item-5"></a>
## [HBFSim 在真实 GPU 上模拟高带宽闪存以加速 LLM 推理](https://arxiv.org/abs/2609.09800v1) ⭐️ 8.0/10

HBFSim 是首个在真实 GPU 上执行真实 LLM 推理工作负载的同时，施加高带宽闪存（HBF）时序、容量和热效应的评估平台。它通过重写 PTX 并门控内核启动，在全部六个校准断点上与实测设备完全吻合且零不安全启动，并能在未修改的 vLLM 0.15.1 上服务 Qwen3-30B-A3B，返回与未插桩基线相同的 token 标识符。 HBF 硬件预计要到 2027 年初才会提供样品，因此 LLM 服务中的容量与数据放置决策不能等到芯片就绪才做。HBFSim 让设计者在真实工作负载下测量这些决策，而不是凭空假设，可能影响未来 AI 推理内存系统的评估方式。 HBFSim 将发射与消费分离，使真实硬件提供可隐藏访问的计算，并且其时序来自对真实设备的测量而非参数表，结温同时决定 HBF 可持续速率和迫使刷新写入的保持期限。其设备快速路径处理 Qwen3-30B-A3B 用例仅需 2 秒，而详细参考路径需要 44 秒，加速达 20.8 倍。

rss · arXiv LLM Inference · 9月9日 06:51

**背景**: 高带宽闪存（HBF）将 NAND 闪存堆叠在加速器封装内，位于高带宽内存（HBM）之下一个层级，其规范于 2026 年 8 月 3 日发布，首批推理设备预计在 2027 年初提供样品。现有评估方法各有不足：存储模拟器只重放记录好的访问序列而不执行工作负载，GPU 模拟器不运行真实计算内核，周期精确模拟器则无法完成一次 LLM 推理运行。PTX 是 NVIDIA 编译器生成的中间代码，介于 CUDA C++ 与机器码之间，HBFSim 通过重写它来实现插桩执行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sandisk.com/company/newsroom/blogs/2025/scaling-beyond-the-wall-inside-sandisks-high-bandwidth-flash-for-ai">Scaling the Memory Wall: Behind Sandisk's High Bandwidth Flash for AI Inferencing</a></li>
<li><a href="https://semiengineering.com/flash-getting-stacked-high-bandwidth-version/">Flash Getting Stacked High-Bandwidth Version - Semiconductor Engineering</a></li>
<li><a href="https://developer.nvidia.com/blog/understanding-ptx-the-assembly-language-of-cuda-gpu-computing/">Understanding PTX, the Assembly Language of CUDA GPU Computing | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#High-Bandwidth Flash`, `#GPU simulation`, `#memory systems`, `#PTX`

---

<a id="item-6"></a>
## [Epoch 将扩散块编译为稀疏 MoE 服务单元](https://arxiv.org/abs/2609.09748v1) ⭐️ 8.0/10

一篇新的 arXiv 论文提出了 Epoch，这是一个将扩散块视为编译单元的服务系统，用于优化扩散语言模型的稀疏 MoE 执行。该系统在 8 块 NVIDIA H100 GPU 上实现，并在 LLaDA-MoE、LLaDA2.0-mini 和 LLaDA2.0-Flash（7B 到 100B 参数）上评估，相比最强基线端到端执行时间最高提升 2.7 倍，同时保持任务质量。 扩散语言模型通过迭代精炼循环生成文本，这与大多数 LLM 服务系统的单次前向执行单元不匹配，导致冗余计算和通信。Epoch 通过具体技术（Atlas、LSP、FreshLane）解决了这一不匹配问题，有望使稀疏 MoE 扩散模型服务更高效，并在基线内存不足的大批量场景下保持可行。 Epoch 为一个扩散块的块时钟结构编译一个小型块计划，并在迭代时钟上刷新所有可能影响活跃解码决策的值。Atlas 为每层编译覆盖驱动的活跃专家支持，同时每次迭代重新计算门控 logits；LSP 仅将活跃、新解码和需要刷新的位置通过新的路由专家计算；FreshLane 将这一新的 token-专家工作列表贯穿专家并行分发、内核和合并，然后在层边界恢复密集逻辑分片。

rss · arXiv LLM Inference · 9月9日 05:47

**背景**: 扩散语言模型是一类深度生成模型，通过迭代去噪损坏的文本来重建连贯序列，用并行 token 精炼替代顺序生成。稀疏混合专家（MoE）模型每个 token 只激活部分专家，减少计算量，但需要专家并行集合通信在设备间分发和合并工作。现有 LLM 服务系统通常针对自回归的单次前向执行进行优化，因此每次前向都会重建相似的路由结构，并为 logits 已经失效的位置重新计算专家输出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2508.10875">A Survey on Diffusion Language Models</a></li>
<li><a href="https://www.emergentmind.com/topics/diffusion-language-models-dlms">Diffusion Language Models : Iterative Denoising in NLP</a></li>

</ul>
</details>

**标签**: `#diffusion models`, `#MoE`, `#LLM serving`, `#compiler optimization`, `#systems`

---

<a id="item-7"></a>
## [Avatar 利用 LLM 自主编排科学工作流](https://arxiv.org/abs/2609.10509v1) ⭐️ 8.0/10

研究人员提出了 Avatar，一种基于 actor 的架构，通过单一适配器验证的动作目录，将可插拔的 LLM 决策策略集成到科学工作流编排中，并使用 Academy 框架实现。在三个工作负载上的评估显示，Avatar 的规则模式用同一个未改动的核心复现了原生执行，而其 LLM 模式将计算浪费减少了 55%，并将 GPU 忙碌时间削减了 40%。 这项工作解决了科学计算中的一个真实痛点：传统工作流管理系统依赖固定的手工调优规则，造成计算和 GPU 时间的浪费。通过证明 LLM 驱动的编排可以与传统的基于规则的执行运行在同一核心上，Avatar 为迈向能够自我推理的工作流系统提供了一条低风险路径；而由分布式计算领域的领军人物 Ian Foster 参与撰写，也意味着其潜在影响力很高。 Avatar 由三个 actor 组成——编排器、执行器和溯源监控器——它们的决策策略通过单一适配器验证的动作目录实现可插拔，因此基于规则和基于 LLM 的控制在不同工作流管理系统之间共享同一核心。评估覆盖三个工作负载，并表明规则模式无需修改即可复现原生执行，不过论文未具体说明所使用的 LLM 模型或提示设计。

rss · arXiv Agent Infra · 9月9日 17:45

**背景**: 科学工作流管理系统（WMS）负责自动化执行科学应用中的计算与数据处理步骤，但通常使用固定的、手工调优的规则进行编排。Actor 模型是一种分布式计算范式，其中独立的 actor 通过消息进行通信，因而非常适合可插拔的模块化控制。LLM 智能体近来在自主决策方面展现出潜力，但在工作流编排中何处引入智能体推理、如何约束其风险以及它何时真正有用，仍不明确。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Scientific_workflow_system">Scientific workflow system - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/computer-networks/architecture-styles-in-distributed-systems/">Architecture Styles in Distributed Systems - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#workflow orchestration`, `#scientific computing`, `#autonomous systems`, `#distributed systems`

---

<a id="item-8"></a>
## [内核管理的共享内存提升 AIOS 上的 AI 个性化能力](https://arxiv.org/abs/2609.10144v1) ⭐️ 8.0/10

一篇新论文为 AIOS 提出了内核管理的共享内存，这是一种系统级抽象，由智能体系统内核而非单个智能体来管理内存检索、隐私执行和提示注入。该方案在 GPT-4o、Llama-3.1:8B 和 Qwen-2.5:7B 三个助手模型上进行了 1800 次试验评估，相比未受管理的 Mem0 外部内存后端，个性化得分在 5 分制上提升了 2.4 至 4.0 分，所有对比的显著性均达到 p < 10^-18。 这项工作表明，将内存管理集中到智能体系统内核中，而不是让单个智能体自行处理检索和隐私执行，能够以极低的成本获得接近无约束上下文所带来的大部分个性化收益。这对多智能体 AI 操作系统的设计具有重要意义，因为在智能体之间共享有用上下文、同时控制隐私和 token 成本仍是一项关键挑战。 与完整、未过滤的上下文拼接相比，内核管理的注入在三个模型中的两个上统计性能相当，在第三个模型上仅表现出较小的、与模型相关的差距，同时使用的提示要短得多。三个模型的端到端延迟均降低了 15% 至 61%，每次调用的 token 用量和推理成本也相应减少。

rss · arXiv Agent Infra · 9月9日 13:20

**背景**: AIOS 是一个 LLM 智能体操作系统，其内核通过将智能体查询分解为执行单元并由调度器编排来管理这些查询。在多智能体系统中，一个智能体学到的上下文往往无法被其他智能体使用，从而限制了个性化能力。Mem0 是一种外部内存后端，用于存储和检索这类上下文，但当检索和隐私执行交由单个智能体负责时，结果可能不一致且成本高昂。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.aios.foundation/aios-docs/aios-kernel/overview">Overview | AIOS Docs</a></li>
<li><a href="https://www.emergentmind.com/papers/2403.16971">AIOS : LLM Agent Operating System</a></li>

</ul>
</details>

**标签**: `#multi-agent systems`, `#shared memory`, `#personalization`, `#AIOS`, `#kernel design`

---