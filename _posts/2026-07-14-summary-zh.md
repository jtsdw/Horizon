---
layout: default
title: "Horizon Summary: 2026-07-14 (ZH)"
date: 2026-07-14
lang: zh
---

> 从 43 条内容中筛选出 7 条重要资讯。

---

1. [llama.cpp b9993 新增 Hy3 支持与 MTP 推测解码](#item-1) ⭐️ 8.0/10
2. [苹果 SpeechAnalyzer API 与 Whisper 的基准测试](#item-2) ⭐️ 8.0/10
3. [JobHop v2：从简历中提取的大规模职业轨迹数据集](#item-3) ⭐️ 8.0/10
4. [GPU-Tile-Sim：面向 LLM 协同设计的以 Tile 为中心的 GPU 仿真框架](#item-4) ⭐️ 8.0/10
5. [TreeThink：用于 LLM 数学推理的模块化树搜索库](#item-5) ⭐️ 8.0/10
6. [振幅门控：用于 LLM 结构化输出的非破坏性 FFN 干预方法](#item-6) ⭐️ 8.0/10
7. [TIGER：面向多模态推测解码的文本条件视觉门控路由](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [llama.cpp b9993 新增 Hy3 支持与 MTP 推测解码](https://github.com/ggml-org/llama.cpp/releases/tag/b9993) ⭐️ 8.0/10

llama.cpp 版本 b9993 新增了对腾讯混元 3（Hy3）架构的支持，这是一个 295B 参数的混合专家模型，并引入了多令牌预测（MTP）推测解码以加速推理。 此版本使 llama.cpp 用户能够在本地运行腾讯强大的开源权重 Hy3 模型，并通过 MTP 推测解码提高吞吐量，扩展了消费级硬件上支持的大型语言模型生态系统。 Hy3 架构具有每头 Q/K RMSNorm、带专家选择偏置的 sigmoid 路由器、始终激活的无门控共享专家以及前导密集块。MTP 推测解码使用多个预测头在每次前向传播中草拟多个令牌，从而在不改变输出质量的情况下提升速度。

github · github-actions[bot] · 7月13日 23:09

**背景**: llama.cpp 是一个流行的开源项目，能够在 CPU 和 GPU 上高效运行大型语言模型。像 Hy3 这样的混合专家（MoE）模型使用多个专门的子网络（专家）在每个令牌上激活，以平衡性能和计算成本。推测解码是一种技术，使用草稿模型预测多个令牌，然后由目标模型验证，从而减少延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.spheron.network/blog/deploy-hunyuan-3-gpu-cloud/">Deploy Hunyuan 3 on GPU Cloud: Self-Host Tencent 's 295B MoE...</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency in AI Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#model support`, `#speculative decoding`, `#MoE`, `#open source`

---

<a id="item-2"></a>
## [苹果 SpeechAnalyzer API 与 Whisper 的基准测试](https://get-inscribe.com/blog/apple-speech-api-benchmark.html) ⭐️ 8.0/10

苹果在其 iOS 26 的 Speech 框架中发布了新的设备端语音识别 API SpeechAnalyzer，基准测试显示它在 LibriSpeech 上的速度和准确性均优于 Whisper Small。 该 API 为开发者提供了一种保护隐私、无需付费的云端服务替代方案，可能颠覆依赖 Whisper 等模型的付费语音转文字应用市场。 SpeechAnalyzer 完全在设备端运行，确保用户隐私并消除按次收费，同时支持流式转录，适用于实时场景。

hackernews · get-inscribe · 7月13日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=48894752)

**背景**: Whisper 是 OpenAI 的开源语音识别模型，广泛用于转录，但通常需要云端处理或大型本地模型。苹果之前的 API SFSpeechRecognizer 在准确性上落后。SpeechAnalyzer 旨在提供更快的设备端替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.apple.com/documentation/speech/speechanalyzer">SpeechAnalyzer | Apple Developer Documentation</a></li>
<li><a href="https://www.siliconreport.com/apple-launches-on-device-speechanalyzer-api-beating-whisper-small-on-speed-and-accuracy-4cf2a0b7">Apple Launches On-Device SpeechAnalyzer API, Beating Whisper ...</a></li>
<li><a href="https://get-inscribe.com/blog/apple-speech-api-benchmark.html">Apple's New Speech API vs Whisper: The First Real Benchmark</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，Nvidia 的 Nemotron 和 Parakeet 或 Mistral 的 Voxtral 等新模型可能是更好的基准。一些人称赞 SpeechAnalyzer 的流式支持是重大的用户体验改进，而另一些人则质疑付费语音转文字应用的长期可行性。

**标签**: `#speech recognition`, `#Apple`, `#benchmark`, `#Whisper`, `#ASR`

---

<a id="item-3"></a>
## [JobHop v2：从简历中提取的大规模职业轨迹数据集](https://arxiv.org/abs/2607.11715v1) ⭐️ 8.0/10

JobHop v2 是一个公开可用的数据集，包含从 44 万份假名化多语言简历中提取的 355,315 条职业轨迹，采用基于 LLM 的提取流水线并带有重试机制，实现了 100% 的 JSON 解析率，并标注了 ESCO 职业代码、季度时间戳和五级教育水平。 该数据集填补了公开职业轨迹数据的关键空白，为劳动力市场分析、职位推荐和劳动力规划的可重复研究提供了更丰富的标注和更大的规模。 JobHop v2 中最佳提取器与标注者间一致性上限仅差 1.1–2.7 个百分点，数据集包含重新设计的提取流水线（采用推理控制的 LLM 推理）以及针对三个基线的修订评估协议。

rss · arXiv LLM Inference · 7月13日 15:42

**背景**: ESCO（欧洲技能、能力、资格和职业）是一个描述欧盟劳动力市场相关职业和技能的欧洲分类系统，在 ISCO 分类法基础上扩展了五位职业代码。VDAB 是弗拉芒公共就业服务机构，为本数据集提供了假名化简历。JobHop v1 是该数据集的早期版本，v2 在规模和标注丰富度上均有提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/datasets/aida-ugent/JobHop">aida-ugent/ JobHop · Datasets at Hugging Face</a></li>
<li><a href="https://engineerseurope.com/sites/default/files/Background+note_ESCO.pdf">ESCO (European Skills, Competences, Qualifications and...)</a></li>
<li><a href="https://europeanjobdays.eu/en/company/vdab">VDAB | EURES - European Job Days</a></li>

</ul>
</details>

**标签**: `#dataset`, `#career trajectory`, `#LLM`, `#labor market`, `#NLP`

---

<a id="item-4"></a>
## [GPU-Tile-Sim：面向 LLM 协同设计的以 Tile 为中心的 GPU 仿真框架](https://arxiv.org/abs/2607.11262v1) ⭐️ 8.0/10

研究人员提出了 GPU-Tile-Sim，这是一个以 tile 为中心的 GPU 仿真框架，通过 warp 级 tile 图对 LLM 内核性能进行建模，在 A100 和 H100 GPU 上实现了高精度（MAPE 1.22%–8.71%）。 该框架弥合了缓慢的指令级模拟器与粗糙的分析模型之间的差距，为 LLM 工作负载实现了高效的硬件-软件协同设计，这对优化 GPU 内核性能和部署效率至关重要。 GPU-Tile-Sim 将内核执行表示为 warp 级 tile 图，其中节点是 tile 操作，边编码数据和顺序约束。它包含自动 tile 图前端和图驱动仿真后端，并已扩展到 Blackwell 架构并进行了初步验证。

rss · arXiv LLM Inference · 7月13日 08:45

**背景**: 现代 LLM 内核依赖细粒度依赖调度和计算-内存重叠来实现高性能。现有的 GPU 性能模型要么太慢（指令级模拟器），要么太粗糙（分析模型），无法捕捉这些特性。基于 tile 的编程模型（如 NVIDIA 的 cuTile 和 Triton）将计算分解为 tile，以利用并行性和局部性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.marktechpost.com/2026/07/11/a-coding-guide-to-nvidias-tile-based-gpu-programming-from-cutile-and-triton-kernels-to-flash-attention/">A Coding Guide to NVIDIA’s Tile-Based GPU Programming: From cuTile and Triton Kernels to Flash Attention - MarkTechPost</a></li>
<li><a href="https://arxiv.org/html/2605.19652">Characterizing Real-World Bugs in Tile Programs for Automated Bug...</a></li>

</ul>
</details>

**标签**: `#GPU simulation`, `#LLM`, `#hardware-software co-design`, `#kernel optimization`, `#performance modeling`

---

<a id="item-5"></a>
## [TreeThink：用于 LLM 数学推理的模块化树搜索库](https://arxiv.org/abs/2607.11258v1) ⭐️ 8.0/10

TreeThink 是一个新的开源 Python 库，为神经定理证明提供模块化、完全异步的树搜索，集成了基于 vLLM 的推理管道和 Lean 4、Rocq、Isabelle/HOL 的形式化验证器。 它填补了 LLM 树搜索库（缺乏形式化验证器集成）与定理证明系统（使用特定任务搜索）之间的空白，实现了高达 6.3 倍的挂钟加速和跨语言形式化证明搜索。 TreeThink 支持从轻量级启发式到神经评估器的多种节点评估技术，并直接连接到每种语言的 REPL 服务器进行实时验证。它在 miniF2F 和 MATH500 上进行了评估，展示了跨语言形式化证明搜索和自然语言推理能力。

rss · arXiv LLM Inference · 7月13日 08:40

**背景**: 树搜索算法系统地探索神经定理证明中的证明空间。现有的 LLM 树搜索库专注于自然语言推理，缺乏与形式化验证器的原生集成，而定理证明系统通常采用特设的搜索实现。TreeThink 通过提供一个模块化、异步的库，将树搜索与形式化验证相结合，解决了这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pypi.org/project/treethink/">treethink · PyPI</a></li>
<li><a href="https://github.com/GGLAB-KU/treethink/tree/main/">GitHub - GGLAB-KU/treethink: TreeThink: Mathematical ...</a></li>
<li><a href="https://github.com/leanprover-community/repl">GitHub - leanprover-community/repl: A simple REPL for Lean 4 ... Kimina Lean Server: Technical Report - arXiv.org Kimina Lean Server: A High-Performance Lean Server for Large ... Lean 4 Web Home - Lean Runner Lean Server - LeanInteract</a></li>

</ul>
</details>

**标签**: `#neural theorem proving`, `#tree search`, `#LLM`, `#formal verification`, `#open-source`

---

<a id="item-6"></a>
## [振幅门控：用于 LLM 结构化输出的非破坏性 FFN 干预方法](https://arxiv.org/abs/2607.11183v1) ⭐️ 8.0/10

研究人员提出振幅门控（AG），一种非破坏性的前馈网络（FFN）干预方法，在 LLM 推理过程中调节激活幅度以改善结构化输出，无需重新训练。在 Qwen3.5-9B 上，AG 将工具/结构化/智能体性能从 38.66%提升至 42.92%（+4.27 个百分点），Hermes 函数调用任务提升约 7.6 个百分点。 这项工作将工具结构化推理确定为安全 FFN 级推理优化的最可信首要目标，提供了一种无需修改模型权重即可增强 LLM 在工具使用场景中可靠性的实用方法。它还引入了一个严格的评估协议，将 oracle 上限与学习门控分开，为未来研究树立了标准。 该研究定义了一个细粒度的干预系统，涵盖 P1/P2/P3 以及分支特定的 P1s/P2a/P2b 位点，并比较了基于熵的 AG 与 Newton-Schulz 窗口 AG，发现两者均非普遍占优。Qwen2.5-7B 保留了 oracle 上限，但当前学习门控未能捕捉到它，表明需要模型和类别特定的路由。

rss · arXiv LLM Inference · 7月13日 07:28

**背景**: 大型语言模型（LLM）越来越多地充当工具使用智能体，格式或函数调用中的小错误可能导致响应无效。前馈网络（FFN）干预旨在推理时改善结构化输出而无需重新训练。作者最初探索了正交残差投影（ORP），这是一种改变方向的修复方法，但常常造成损害，因此他们开发了振幅门控（AG），该方法保留预训练权重方向，仅调节激活幅度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/mshojaei77/swiglu-the-ffn-upgrade-i-use-to-get-free-performance-33jc">SwiGLU: The FFN Upgrade I Use to Get Free Performance</a></li>
<li><a href="https://arxiv.org/abs/2605.26092">[2605.26092] OrpQuant: Geometric Orthogonal Residual ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#FFN intervention`, `#structured outputs`, `#tool use`, `#inference-time optimization`

---

<a id="item-7"></a>
## [TIGER：面向多模态推测解码的文本条件视觉门控路由](https://arxiv.org/abs/2607.11131v1) ⭐️ 8.0/10

TIGER 提出了一种文本条件视觉门控路由框架，能够动态选择相关的视觉 token 用于多模态推测解码，并通过基于验证器奖励的接受对齐策略训练来优化草稿模型。 这项工作通过提高推测解码效率，解决了加速视觉语言模型（VLM）的关键瓶颈，能够在不牺牲准确性的情况下显著降低多模态任务的推理延迟。 TIGER 使用门控机制根据草稿模型的当前文本状态选择稀疏的上下文相关视觉 token，并采用基于 KL 锚定的接受对齐分组策略训练来最大化接受前缀长度。

rss · arXiv Speculative Decoding · 7月13日 06:06

**背景**: 推测解码通过让轻量级草稿模型提出多个 token，再由大型目标模型验证，从而加速自回归生成。虽然对纯文本 LLM 有效，但在 VLM 中收益有限，因为草稿模型常在视觉关键内容上出现偏差。TIGER 通过动态选择相关视觉 token 并将草稿模型训练与验证结果对齐来解决这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding</a></li>
<li><a href="https://arxiv.org/html/2505.14260">Speculative Decoding Reimagined for Multimodal Large Language...</a></li>
<li><a href="https://arxiv.org/pdf/2606.12412">Reroute, Don't Remove: Recoverable Visual Token Routing for ...</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#multimodal`, `#VLM`, `#efficient inference`, `#visual gating`

---