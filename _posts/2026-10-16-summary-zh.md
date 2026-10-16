---
layout: default
title: "Horizon Summary: 2026-10-16 (ZH)"
date: 2026-10-16
lang: zh
---

> 从 73 条内容中筛选出 8 条重要资讯。

---

1. [四个 Gemini 4 Argon 智能体自主通关《我的世界》末影龙](#item-1) ⭐️ 9.0/10
2. [Meta 发布 Muse Spark Open：816B 开放权重多模态模型](#item-2) ⭐️ 9.0/10
3. [Hugging Face Transformers v5.20.0 新增 Meta 816B Muse Spark Open 与 Ling 3.0](#item-3) ⭐️ 8.0/10
4. [Google DeepMind 利用 Antigravity 加速抗菌肽发现](#item-4) ⭐️ 8.0/10
5. [NVIDIA 与 Hugging Face 发布 2.8 万亿 Token 的印度语言预训练数据集](#item-5) ⭐️ 8.0/10
6. [远程 KV 缓存可能拖累分离式 LLM 服务的尾延迟](#item-6) ⭐️ 8.0/10
7. [Range：将 KV 缓存复用粒度与存储开销解耦](#item-7) ⭐️ 8.0/10
8. [基于市场的后训练让智能体集群实现自组织协调](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [四个 Gemini 4 Argon 智能体自主通关《我的世界》末影龙](https://arxiv.org/abs/2610.22319v1) ⭐️ 9.0/10

由四个 Gemini 4 Argon AI 智能体组成的团队在沙盒《我的世界》生存世界中自主击败了末影龙，全程编写了 2783 个程序，协调运行超过 27 小时 14 分钟，期间没有任何人工干预。它们从随机生成的简单难度世界出发，在死亡 605 次后完成通关，仅使用开源库 Mineflayer，没有依赖人类编写的游戏逻辑或预先勘探的种子。 这被认为是 AI 智能体首次仅使用标准工具端到端自主通关《我的世界》，是长时程规划、自主编写代码和多智能体协作方面的一个里程碑。这些能力与需要数千个相互依赖步骤的复杂现实软件工程和企业任务直接相关。 每个智能体通过 Mineflayer 控制一个玩家角色，并借助游戏内聊天和共享记忆与队友协调，没有预先分配角色；研究人员可以通过实时仪表盘监控并随时暂停或终止运行，但全程无需干预。团队采用的策略包括分工、共享已学知识和互相拾回掉落物品，不过论文也讨论了该结果的局限性。

rss · arXiv Agent Infra · 10月15日 17:51

**背景**: Mineflayer 是一个开源的 JavaScript（也可通过 Python 使用）库，它将《我的世界》的底层协议抽象为事件驱动的 API，用于处理世界状态、物理、物品栏和实体追踪，让开发者能够创建可编程的游戏机器人。Gemini 4 Argon 是 Google DeepMind 于 2026 年 9 月发布的前沿推理模型，定位于现实世界的编程、企业知识工作和网络防御。末影龙是《我的世界》的最终 Boss，玩家需要采集资源、制作装备、穿越不同维度，并按顺序完成数千个步骤才能将其击败。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/PrismarineJS/mineflayer">GitHub - PrismarineJS/mineflayer: Create Minecraft bots with ... mineflayer/examples/python/README.md at master - GitHub PrismarineJS/mineflayer | DeepWiki mineflayer - npm Mineflayer – Create Advanced Minecraft Bots Easily What is Mineflayer used for?</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-4-argon/">Gemini 4 Argon - Model Card — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/">Introducing Gemini 4 Argon - The Keyword</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#Minecraft`, `#multi-agent systems`, `#autonomous planning`, `#reinforcement learning`

---

<a id="item-2"></a>
## [Meta 发布 Muse Spark Open：816B 开放权重多模态模型](https://www.reddit.com/r/LocalLLaMA/comments/1x6r9pz/introducing_muse_spark_open_the_most_capable_us/) ⭐️ 9.0/10

Meta 发布了 Muse Spark Open，这是一个拥有 816B 总参数（42B 激活参数）的开放权重多模态模型，具备 100 万 token 的上下文窗口，专为编程和智能体任务打造。该模型在 SGLang 中内置了可自动调优的 Helion 内核，在 NVIDIA 和 AMD GPU 上实现了 1.03–3.95 倍的内核加速，并已在 Hugging Face、Amazon SageMaker AI、Google Cloud Model Garden 和 Microsoft Foundry Models 上提供下载。 该模型被称为迄今为止能力最强的美国开放权重模型，其对多种推理引擎的广泛支持（SGLang、vLLM、TensorRT-LLM、Hugging Face Transformers、Apple MLX、llama.cpp、Unsloth）以及对 AMD、Apple、Intel 和 NVIDIA 芯片的优化，可能大幅降低在本地运行前沿级模型的门槛。同时，这也加剧了与中国开放权重模型（如 Qwen 和 GLM）的竞争，社区成员指出后者在某些基准测试上仍表现更优。 该模型总参数为 816B，但仅激活 42B，表明其采用了混合专家（MoE）架构，并支持文本、图像、视频和音频模态。它依据 Muse Model License 发布，附带有限的商业条款，其中特别包含一项限制条款：对于总营收超过 2000 万美元的“模型即服务”（Model as a Service）提供商，其免费使用将受到限制。

reddit · r/LocalLLaMA · /u/AIatMeta · 10月15日 17:03

**背景**: 开放权重模型是指其训练后的参数（权重和偏置）被公开发布的 AI 模型，任何人都可以下载并在自己的硬件上运行，但许可证可能限制修改或再分发。这与完全开源的 AI 不同，后者还会发布源代码、训练数据和技术文档。历史上，DeepSeek、阿里云和 Moonshot AI 等中国实验室在以 Apache 或 MIT 等宽松许可证发布开放权重模型方面处于领先地位，而 OpenAI、Anthropic 和 Google DeepMind 等美国实验室则倾向于专有方案。Helion 是 PyTorch 推出的一个 Python 嵌入式领域特定语言，用于编写可移植的高性能机器学习内核，并可编译为 Triton；SGLang 则是一个开源的高吞吐量推理引擎，用于服务大型语言和多模态模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://pytorch.org/blog/helion/">Helion: A High-Level DSL for Performant and Portable ML Kernels</a></li>
<li><a href="https://en.wikipedia.org/wiki/SGLang">SGLang - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一：一些人指出，Artificial Analysis 的基准测试显示 Muse Spark Open 的表现不及 Qwen3.8 Flash Next 和 GLM 5.3 Flash，而后者可在单台 B300 上运行，说明 Meta 在开放权重领域仍需追赶。另一些人则赞赏该模型几乎支持所有主流模型运行器，也有人讨论许可证的商业限制，并认为 Meta 的战略是构建具有粘性的生态护城河，而非直接通过模型访问变现。

**标签**: `#open-weight models`, `#LLM`, `#Meta`, `#multimodal`, `#inference optimization`

---

<a id="item-3"></a>
## [Hugging Face Transformers v5.20.0 新增 Meta 816B Muse Spark Open 与 Ling 3.0](https://github.com/huggingface/transformers/releases/tag/v5.20.0) ⭐️ 8.0/10

Hugging Face 发布了 Transformers v5.20.0，原生支持多个新模型，其中最引人注目的是 Meta 的 Muse Spark Open——一个拥有 8160 亿总参数、每 token 激活 420 亿参数、上下文窗口最高达 1,048,576 token 的多模态混合专家模型，以及 InclusionAI 的 Ling 3.0 Flash 混合 MoE 语言模型。该版本还新增了 Kolibri1、MiniCPM-V 4.7、UnlimitedOcr 和 UltraBERT。 由于 Transformers 是加载和运行开源模型的事实标准库，原生支持意味着开发者无需编写自定义代码或使用 trust_remote_code 即可使用这些大型多模态和 MoE 模型。Meta 的 8160 亿参数模型和 InclusionAI 的混合架构被纳入，表明开源生态正持续向稀疏化、多模态、长上下文模型方向发展。 Muse Spark Open 接受文本、图像、音频和视频输入并生成文本，针对智能体编码任务训练，提供 BF16 和 NVFP4 两种格式；Ling 3.0 Flash 将五个 Kimi Delta Attention 层与一个 Multi-head Latent Attention 层组合，并以 BailingHybridForCausalLM 原生加载。其他新增模型包括 Kolibri1（50 层，每 token 路由到 384 个专家中的 6 个）、采用 canvas M-RoPE 的 MiniCPM-V 4.7、百度的 30 亿参数 UnlimitedOcr（使用 Reference Sliding Window Attention）以及 UltraBERT。

github · vasqu · 10月15日 18:05

**背景**: 混合专家（MoE）模型将计算分散到许多专门的子网络中，每个 token 只激活其中少数几个，因此能以远低于稠密模型的计算量扩展到极大的参数量。多模态模型可处理文本、图像、音频、视频等多种输入类型，而上下文窗口指模型一次能考虑的最大 token 数量。NVFP4 是 NVIDIA 的 4 位浮点量化格式，可在精度损失极小的情况下降低内存和计算开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Context_window">Context window - Wikipedia</a></li>

</ul>
</details>

**标签**: `#huggingface`, `#transformers`, `#llm`, `#mixture-of-experts`, `#multimodal`

---

<a id="item-4"></a>
## [Google DeepMind 利用 Antigravity 加速抗菌肽发现](https://deepmind.google/blog/accelerating-antimicrobial-discovery/) ⭐️ 8.0/10

Google DeepMind 宣布使用 Google Antigravity for Science 这一由 AI 智能体驱动的软件开发平台，来加速新型抗菌肽的搜索。该工作利用能够编写、运行和测试代码的 AI 智能体，简化这一生物医学研究领域的发现流程。 抗菌素耐药性日益成为全球健康威胁，因此迫切需要抗菌肽等新型治疗药物。将智能体式 AI 应用于科学工作流，有望大幅缩短发现周期，并为更广泛的 AI 驱动药物发现树立范例。 Google Antigravity 是一个让 AI 智能体以不同程度自主性编写、运行和测试代码的平台，其专门的 Science 插件提供并行化、定制化和知识管理工具。抗菌肽通常由 10 到 50 个氨基酸组成，通过破坏微生物膜而非传统抗生素机制发挥作用。

rss · Google DeepMind Blog · 10月15日 16:08

**背景**: 抗菌肽（AMP），又称宿主防御肽，是核糖体合成的小型多肽，构成所有生命类别先天免疫反应的一部分。它们能够杀死革兰氏阴性菌和革兰氏阳性菌、包膜病毒、真菌甚至转化细胞，因此有望成为传统抗生素的替代品。Google Antigravity 是 Google 的软件开发平台，其中 AI 智能体可自主编写、运行和测试代码，其科学用例旨在消除重复性任务并简化科学工作流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Google_Antigravity">Google Antigravity - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Antimicrobial_peptides">Antimicrobial peptides</a></li>
<li><a href="https://antigravity.google/use-cases/science">Why choose Google Antigravity for science</a></li>

</ul>
</details>

**标签**: `#AI for Science`, `#Antimicrobial Peptides`, `#Drug Discovery`, `#Google DeepMind`, `#Biotechnology`

---

<a id="item-5"></a>
## [NVIDIA 与 Hugging Face 发布 2.8 万亿 Token 的印度语言预训练数据集](https://huggingface.co/blog/nvidia/scaling-indic-pretraining) ⭐️ 8.0/10

Hugging Face 与 NVIDIA 联合发布了 Nemotron-pretraining-Indic-v1 语料库，该数据集包含约 2.8 万亿个 Token，覆盖 22 种印度语言，并附带一个开放的数据生成流水线。该语料库由 NVIDIA 与 IIT Madras 的 AI4Bharat 合作开发，包含 2,601.0 亿原生文字 Token 和 2,246 亿罗马化 Token（使用 Gemma-4 分词器统计）。 印度语言在大语言模型训练数据中历来代表性不足，这阻碍了这些语言社区的 AI 发展。这一大规模开放数据集和可复现的流水线有望加速低资源语言建模的进展，并推动多语言 AI 更加包容。 该语料库区分了原生文字和罗马化 Token，反映了印度语言的语言多样性，而开放的数据生成流水线则支持可复现性和进一步研究。该数据集属于 Nemotron 模型系列，专为大规模预训练设计。

rss · Hugging Face Blog · 10月16日 01:44

**背景**: 印度语言有超过十亿的使用者，但用于训练 AI 模型的高质量数字文本却十分有限。此前 AI4Bharat 的 IndicLLMSuite 等努力生成了 2510 亿个 Token，因此这个 2.8 万亿 Token 的语料库代表了显著的规模提升。预训练是语言模型在针对特定任务微调之前，从大规模文本语料中学习通用语言模式的初始阶段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/nvidia/scaling-indic-pretraining">Scaling Indic Pretraining: 2.8 Trillion Tokens and an Open ...</a></li>
<li><a href="https://www.printingpressai.com/article/generative-ai/scaling-indic-pretraining-2-8-trillion-tokens-and-an-open-data-generation-pipeli">Scaling Indic Pretraining: 2.8 Trillion Tokens and an Open ...</a></li>
<li><a href="https://github.com/AI4Bharat/IndicLLMSuite">GitHub - AI4Bharat/IndicLLMSuite: A blueprint for creating ...</a></li>

</ul>
</details>

**标签**: `#multilingual NLP`, `#Indic languages`, `#pretraining`, `#open data`, `#large language models`

---

<a id="item-6"></a>
## [远程 KV 缓存可能拖累分离式 LLM 服务的尾延迟](https://arxiv.org/abs/2610.21500v1) ⭐️ 8.0/10

一篇新论文研究了在 8xB300 节点上以预填充上下文并行（PCP8）方式部署 GLM-5.3（一种带 MLA 的 FP8 混合专家模型）的分离式推理场景，发现启用远程 KV 缓存层（由 Valkey 存储支持的 LMCache）后，首 token 中位延迟不变，但 16k token 的 p99 从 3.96 秒升至 17.3 秒。作者提出一个两项成本模型，并通过按 rank 分片的 MLA KV 存储、按 rank 划分远程层（GET 带宽提升 6.3 倍至 10.76 GB/s）、异步加载以及修复三个客户端 bug，将高命中流的 p99 从 83.32 秒降至 0.67 秒。 这是一个反直觉且贴近生产的重要发现：能改善中位延迟的远程 KV 缓存层可能严重恶化尾延迟，甚至让一次命中比重新计算提示词还慢，这直接影响系统工程师为长上下文 LLM 服务设计和规划共享缓存层的方式。论文提出的成本模型与分片协议为从业者判断远程缓存何时真正划算提供了具体标准。 该成本模型表明，只有当远程层带宽超过 B* = sR（对该模型和 GPU 为 2.53 GB/s）时，远程命中才划算；而固定的每次命中引擎开销（T0 ≈ 0.33 秒）意味着对短于约 17k token 的提示词，无论带宽多高，命中都无法胜过重新计算；实测中一次远程命中耗时 0.88 秒，而重新计算仅需 0.31 秒。同步加载会把高命中流变成不稳定的队列（p99 达 83.32 秒，而 GPU 利用率仅 7%）；分片存储将预填充吞吐提升 14%，配合上游内核修复后提升 34%，所有改动均已提交至 LMCache 上游。

rss · arXiv LLM Inference · 10月15日 08:37

**背景**: 在长上下文 LLM 服务中，注意力 KV 缓存保存中间键值张量，使重复的提示词前缀无需在预填充阶段重新计算，而预填充正是逐 token 解码之前处理输入提示词的阶段。分离式推理将预填充与解码拆分为独立阶段或实例，生产系统越来越多地引入跨引擎共享的远程 KV 缓存层（此处为 LMCache 搭配 Valkey 键值存储），以便在单张 GPU 显存之外复用缓存前缀。多头潜在注意力（MLA）是 DeepSeek 等模型采用的注意力变体，可压缩 KV 缓存；预填充上下文并行（PCP）则将预填充计算分片到多个 rank 上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lmcache.ai/en/">Building the Foundation of AI Memory Tensor with KV Cache ...</a></li>
<li><a href="https://docs.lmcache.ai/kv_cache/storage_backends/valkey.html">Valkey | LMCache</a></li>
<li><a href="https://pytorch.org/blog/disaggregated-inference-at-scale-with-pytorch-vllm/">Disaggregated Inference at Scale with PyTorch & vLLM</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#KV cache`, `#remote caching`, `#tail latency`, `#disaggregated inference`

---

<a id="item-7"></a>
## [Range：将 KV 缓存复用粒度与存储开销解耦](https://arxiv.org/abs/2610.21241v1) ⭐️ 8.0/10

一篇新的 arXiv 论文提出了 Range，这是一个面向 vLLM 和 LMCache 的 KV 缓存存储引擎，使存储路径上的每一项开销都随字节数或物理批次扩展，而不是随逻辑对象数量扩展。在固定 6 GiB 恢复任务中，Range 在 32 倍对象数量范围内将 TTFT 中位数稳定保持在 1.79–1.80 秒，而经过调优的进程内 LMCache 则从 2.12 秒上升到 3.01 秒。 这项工作表明，主导 KV 缓存恢复延迟的是每个对象的开销，而不是 SSD 的原始带宽，这直接影响长上下文 LLM 服务的首 token 时间。由于 Range 保留了 cuFile 内核路径，并且只修改了 vLLM 的四行代码，这一思路有望被在生产环境中运行 vLLM 和 LMCache 的从业者快速采用。 恢复同样的 6 GiB KV 数据，作为 192 个对象时耗时 2.1 秒，而作为 6,144 个对象时耗时 3.0 秒，在逐层加载下耗时更长，因为查找、分配、I/O 提交、GPU 传输、存储和索引都按逻辑对象计费。Range 采用 ticket、字节条带和由完成事件驱动的 GPU 传输 bank，其结果与前缀已驻留 GPU 内存的情况相差不到 70 毫秒。

rss · arXiv LLM Inference · 10月15日 04:37

**背景**: LLM 服务通过复用缓存的键值（KV）状态来跳过预填充，而不断增长的上下文使这些状态超出 GPU HBM 和 CPU DRAM 的容量，被下沉到 NVMe SSD，从而使前缀恢复位于首 token 时间的关键路径上。vLLM 是一个广泛使用的开源推理引擎，以 PagedAttention 为核心；LMCache 则是一个模块化的 KV 缓存层，可在 GPU、CPU 内存和外部后端之间存储和复用 KV 缓存。此前的系统将按对象的工作从 CPU 转移到 GPU，但工作仍然按对象进行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lmcache.ai/en/">Building the Foundation of AI Memory Tensor with KV Cache ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/VLLM">vLLM - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2510.09665">LMCache : An Efficient KV Cache Layer for Enterprise-Scale LLM...</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#KV cache`, `#storage systems`, `#vLLM`, `#LMCache`

---

<a id="item-8"></a>
## [基于市场的后训练让智能体集群实现自组织协调](https://arxiv.org/abs/2610.22322v1) ⭐️ 8.0/10

一篇新的 arXiv 论文提出了基于市场的后训练（MPT）框架，通过让智能体以竞标方式表达参与意愿，联合学习去中心化智能体集群的动作策略与自组织协调机制，并在 GitHub 上开源了代码与训练好的模型。在具身制作、机器人导航和深度研究三类任务上，MPT 的表现优于单体式后训练，并证明学习得到的自组织协调优于其他协调策略。 这项工作针对现有多智能体系统的一个核心局限：它们通常在固定的编排结构内训练智能体，并将个体能力学习与集体组织方式割裂开来。通过让协调机制本身可学习，MPT 指向了能够复用、扩展并在智能体掉线时保持鲁棒性的集群，这对机器人、分布式 AI 系统以及任何依赖去中心化智能体协作的应用都具有重要意义。 在 MPT 中，智能体通过竞标决定谁参与行动，集体结果则提供局部训练信用，因此动作与竞标行为无需中央协调者即可共同适应。消融实验表明，动作与竞标都能从学习中获益，学习到的竞标能提供更有效的动作训练信号，而且推理时更大的集群规模在智能体掉线时性能损失更小。

rss · arXiv Agent Infra · 10月15日 17:51

**背景**: 多智能体强化学习（MARL）研究多个学习型智能体共存于共享环境、各自追求自身奖励的情形，面临非平稳性、可扩展性、协调与信用分配等众所周知的挑战。在去中心化编排中，智能体自组织以适应变化的环境，无需人工重新规划，这与由单一中央控制器或固定结构主导行为的单体式系统形成对比。后训练指在初始预训练之后对模型进一步训练以使其行为专门化，而 MPT 将这一思路同时应用于动作策略与协调机制本身。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Multi-agent_reinforcement_learning">Multi-agent reinforcement learning - Wikipedia</a></li>
<li><a href="https://anycap.ai/page/en-US/ai/agentic-ai-orchestration">Agentic AI Orchestration : Architecture Patterns & Best Practices (2026)</a></li>

</ul>
</details>

**标签**: `#multi-agent systems`, `#decentralized coordination`, `#reinforcement learning`, `#swarm intelligence`, `#post-training`

---