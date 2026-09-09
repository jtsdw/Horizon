---
layout: default
title: "Horizon Summary: 2026-09-09 (ZH)"
date: 2026-09-09
lang: zh
---

> 从 56 条内容中筛选出 8 条重要资讯。

---

1. [数学家声称流体动力学突破，指控 OpenAI 窃取成果](#item-1) ⭐️ 9.0/10
2. [AlphaGenome Atlas 绘制 90 亿个 DNA 变异图谱](#item-2) ⭐️ 9.0/10
3. [OpenAI 推出 ChatGPT Images 2.5，实现个性化图像生成](#item-3) ⭐️ 8.0/10
4. [细粒度 AI 安全：拒绝有害子集而非整个话题](#item-4) ⭐️ 8.0/10
5. [样本引导的精确 Top-K 选择加速稀疏注意力](#item-5) ⭐️ 8.0/10
6. [Miles v0.1：面向生产的强化学习后训练系统](#item-6) ⭐️ 8.0/10
7. [HoneyRoute：基于蜜罐的路由防御 LLM 服务](#item-7) ⭐️ 8.0/10
8. [程序图：面向 LLM 智能体的自演化执行结构](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [数学家声称流体动力学突破，指控 OpenAI 窃取成果](https://cims.nyu.edu/~tristanb/statement.pdf) ⭐️ 9.0/10

纽约大学库朗研究所的数学家 Tristan Buckmaster 声称在 Navier-Stokes 相关问题（不可压缩多孔介质、Boussinesq 和三维不可压缩 Euler 方程的有限时间爆破）上取得了进展。他还指控 OpenAI 试图窃取其成果，未经同意使用其产品使用中获得的见解。 这一争议凸显了学术研究人员与 AI 公司之间在知识产权和数据使用方面日益紧张的关系。如果 Buckmaster 的指控得到证实，可能会为如何处理源自用户交互的 AI 训练数据开创先例，可能影响全球的研究人员。 Buckmaster 及其合作者、在 Anthropic 工作的 Levent Alpöge 并未证明 100 万美元的千禧年大奖问题，但声称证明了类似的非千禧年 Navier-Stokes 问题。OpenAI 表示无法排除用户交互的去标识化数据帮助改进了其模型，这为争议增添了不确定性。

hackernews · procedurecall · 9月8日 05:42 · [社区讨论](https://news.ycombinator.com/item?id=49605915)

**背景**: Navier-Stokes 方程描述粘性流体的运动，是流体动力学的基础。Navier-Stokes 存在性与光滑性问题（询问三维空间中是否总是存在光滑解）是七个千禧年大奖问题之一。Buckmaster 是一位受人尊敬的数学家，此前因在这些方程上的相关工作获得了 Clay 研究奖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier-Stokes_equations">Navier-Stokes equations</a></li>
<li><a href="https://cims.nyu.edu/~tristanb/">Tristan Buckmaster - NYU Courant</a></li>
<li><a href="https://officechai.com/ai/mathematician-tristan-buckmaster-says-he-cracked-a-fluid-dynamics-problem-with-ai-accuses-openai-of-trying-to-take-credit/">Mathematician Tristan Buckmaster Says He Cracked a Fluid Dynamics Problem With AI, Accuses OpenAI of Trying to Take Credit</a></li>

</ul>
</details>

**社区讨论**: 社区评论对 Buckmaster 表示强烈支持，许多人指责 OpenAI 的不道德行为，包括威胁研究人员并试图从其工作中获利。一些评论者指出 OpenAI 数据使用政策的模糊性，而其他人则将其与历史上的学术优先权争议相提并论。

**标签**: `#mathematics`, `#Navier-Stokes`, `#research`, `#OpenAI`, `#controversy`

---

<a id="item-2"></a>
## [AlphaGenome Atlas 绘制 90 亿个 DNA 变异图谱](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/alphagenome-atlas/) ⭐️ 9.0/10

谷歌 DeepMind 发布了 AlphaGenome Atlas，这是一个预测性图谱，对人类基因组中 90 亿个单核苷酸变异的分子效应和 AVI 评分进行了编目。该工具现已向研究人员公开。 这一资源可能显著加速遗传学研究，帮助科学家无需昂贵的湿实验即可识别潜在致病突变。它可能改善遗传病的诊断，并加深对非编码 DNA 在疾病中作用的理解。 该图谱覆盖所有可能的单字母变化，包括非编码区域，并提供 AVI（AlphaGenome 变异影响）评分。在一项验证研究中，将 Atlas 应用于英国生物银行数据，发现了 22%更多的非编码遗传关联。

hackernews · utiiiD · 9月8日 14:55 · [社区讨论](https://news.ycombinator.com/item?id=49611251)

**背景**: 单核苷酸变异（SNV）是指 DNA 中一个字母的变化，例如 A 被 G 替换。这些变化可能改变基因功能并导致疾病。AlphaGenome 建立在 DeepMind 的 AlphaFold 工作基础上，AlphaFold 曾从氨基酸序列预测蛋白质结构，将 AI 在生物学中的作用扩展到人类基因组。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/alphagenome-atlas-a-predictive-map-of-every-possible-dna-letter-change-in-the-human-genome/">AlphaGenome Atlas: A predictive map of every possible DNA ...</a></li>
<li><a href="https://spectrum.ieee.org/alphagenome-atlas">AlphaGenome Atlas Maps 9 Billion Possible DNA ... - IEEE Spectrum</a></li>
<li><a href="https://www.firstpost.com/tech/google-deepmind-maps-effects-of-all-9-billion-possible-dna-mutations-to-aid-genetic-research-14044229.html">Google DeepMind maps effects of all 9 billion possible DNA mutations...</a></li>

</ul>
</details>

**社区讨论**: 社区评论表现出热情，但也提出了问题。一些用户询问实际应用，例如使用 Atlas 与 23andMe 数据查找致病突变。其他人指出缺乏对启动子序列的讨论，并质疑非编码 DNA 效应是否被完全捕获。还有用户提到一项相关研究，该研究通过实验突变了一种病毒，与 Atlas 的预测性质形成对比。

**标签**: `#genomics`, `#AI`, `#DeepMind`, `#bioinformatics`, `#health`

---

<a id="item-3"></a>
## [OpenAI 推出 ChatGPT Images 2.5，实现个性化图像生成](https://openai.com/index/introducing-chatgpt-images-2-5) ⭐️ 8.0/10

OpenAI 宣布推出 ChatGPT Images 2.5，这是一款新的图像生成模型，能将用户的想法、草图和参考照片转化为更个性化和精美的图像。此次发布标志着 ChatGPT 图像生成能力的升级。 此次发布意义重大，因为它提升了 AI 生成图像的质量和个性化程度，可能影响依赖 AI 制作视觉内容的创意专业人士和普通用户。这也表明 OpenAI 持续投资多模态 AI，可能塑造创意工作流程和人机协作的未来。 该模型旨在更好地反映用户意图，处理草图、参考照片等输入，生成精美的输出。公告中未披露模型架构或基准测试等具体技术细节。

rss · OpenAI Blog · 9月8日 11:30

**背景**: ChatGPT Images 2.5 是 OpenAI 生成式 AI 工具套件的一部分，该套件包括文本和图像生成模型。像 DALL-E 这样的图像生成模型已经发展到能够理解复杂提示并生成高质量视觉内容，而这款新模型似乎延续了这一趋势，专注于个性化和精美度。

**标签**: `#OpenAI`, `#image generation`, `#AI`, `#ChatGPT`, `#multimodal`

---

<a id="item-4"></a>
## [细粒度 AI 安全：拒绝有害子集而非整个话题](https://huggingface.co/blog/MultiverseComputingCAI/safety-for-whom) ⭐️ 8.0/10

该博客提出了一种 AI 安全方法，使模型能够只拒绝话题中有害的子集，而不是整个话题，从而实现更精确的内容审核。这种方法旨在平衡安全性与保留良性内容。 这很重要，因为当前的审核常常过度限制内容，限制了合法讨论。细粒度的拒绝机制可以通过减少不必要的审查同时保持安全性，改善 AI 对齐，惠及语言模型的用户和开发者。 该方法可能涉及识别并针对更广泛话题中的特定有害子类别，使用细粒度分类或安全分类法等技术。它可能需要额外的训练数据或模型调整，以有效区分有害和良性方面。

rss · Hugging Face Blog · 9月8日 14:23

**背景**: 大型语言模型中的 AI 安全和内容审核通常依赖拒绝机制来防止生成有害内容。然而，这些机制可能过于宽泛，拒绝包含有害和良性元素的整个话题。最近的研究，如 SORRY-Bench 和关于审核实践的研究，强调了需要更细致的方法来区分话题的不同方面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/sorry-bench">SORRY-Bench: LLM Safety Refusal Evaluation</a></li>
<li><a href="https://link.springer.com/chapter/10.1007/978-3-032-05962-8_16">What Large Language Models Do Not Talk About: An Empirical Study of Moderation and Censorship Practices | Springer Nature Link</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#content moderation`, `#alignment`, `#language models`, `#ethics`

---

<a id="item-5"></a>
## [样本引导的精确 Top-K 选择加速稀疏注意力](https://arxiv.org/abs/2609.08450v1) ⭐️ 8.0/10

该论文提出了 HPC-Ops Top-K，一种用于不规则稀疏注意力分数行的样本引导精确选择器，通过使用固定步长的部分视图在完整行遍历之前提出边界，从而减少遍历开销。在 20 种算子配置中，相比最快的已验证外部精确基线实现了 1.29–1.75 倍的加速，几何平均加速比为 1.55 倍。 这项工作解决了长上下文模型中稀疏注意力的关键性能瓶颈，这对于大型语言模型的高效推理至关重要。所提出的方法可以显著降低推理延迟和成本，惠及长文档处理和实时 AI 助手等应用。 GPU 实现融合了完整行验证和候选集形成，并在可捕获图形的非规则行调度背后结合了持久化、KV 拆分和直接精确执行。该方法在 Hy4-Preview 的索引器分数上进行了验证，并在两个框架派生的稀疏注意力轨迹上实现了 1.36 倍和 1.48 倍的加速。

rss · arXiv LLM Inference · 9月8日 08:51

**背景**: 稀疏注意力机制仅保留固定大小的 token 子集以降低计算成本，但随着上下文长度的增长，精确的 Top-K 选择阶段可能成为瓶颈。传统的基数选择器需要完整遍历行才能找到第一个可操作的边界，导致冗余遍历。HPC-Ops 是腾讯开源的用于 LLM 推理的高性能算子库，这项工作是其持续优化工作的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.08450">[2609.08450] Sample-Guided Exact Top-K Selection for Long ...</a></li>
<li><a href="https://tokention.com/tencent-hunyuan-releases-hpc-ops-a-high-performance-llm-inference-operator-library/">Tencent Hunyuan Releases HPC - Ops : A High ... - Tokention</a></li>
<li><a href="https://github.com/Zhuofeng-Li/frontier-cs/tree/main/research/problems/ragged_attention">frontier-cs/research/problems/ragged_attention at main ...</a></li>

</ul>
</details>

**标签**: `#sparse attention`, `#top-k selection`, `#long-context`, `#efficient inference`, `#HPC`

---

<a id="item-6"></a>
## [Miles v0.1：面向生产的强化学习后训练系统](https://arxiv.org/abs/2609.08368v1) ⭐️ 8.0/10

Miles v0.1 是一个基于 slime 简洁设计、面向前沿后训练的全栈生产级系统。它支持多种后端（NVIDIA Megatron-LM 和 PyTorch FSDP）以及三种权重同步传输方式，并已在 GitHub 上开源。 该系统通过强调经过验证、简洁且可定制的组件，旨在让研究人员和企业都能使用前沿规模的强化学习。其生产就绪性和可扩展性可能显著降低高级后训练的门槛，影响更广泛的 AI/ML 生态系统。 Miles 支持全参数 RL、LoRA RL、同策略蒸馏、监督微调和真正的同策略 rollout-训练对齐，并扩展到扩散模型。在 GLM-5.2 744B-A40B 模型上针对终端使用编码任务的端到端案例研究中，在 64 个 NVIDIA GB300 GPU 上实现了 263 秒的中位步长时间。

rss · arXiv LLM Inference · 9月8日 07:35

**背景**: 后训练是使用强化学习或监督微调对已训练模型进行进一步优化的阶段，以对齐行为或提升推理能力。Miles 基于 slime，这是一个将 Megatron-LM 与 SGLang 连接起来以实现高性能训练和灵活数据生成的 LLM 后训练框架。SGLang 是一个高性能推理引擎，在许多后训练框架中用作 rollout 后端。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/THUDM/slime">GitHub - THUDM/slime: slime is an LLM post-training framework ...</a></li>
<li><a href="https://thudm.github.io/slime/">slime Documentation — slime</a></li>
<li><a href="https://github.com/sgl-project/sglang">GitHub - sgl-project/sglang: SGLang is a high-performance ...</a></li>

</ul>
</details>

**标签**: `#reinforcement-learning`, `#post-training`, `#systems`, `#AI/ML`, `#scalability`

---

<a id="item-7"></a>
## [HoneyRoute：基于蜜罐的路由防御 LLM 服务](https://arxiv.org/abs/2609.08306v1) ⭐️ 8.0/10

HoneyRoute 提出了一种新颖的推理服务层，能够检测恶意请求并将其路由到专用的蜜罐模型，从而保护生产模型并收集攻击者情报。该系统在 13 种对抗性变换下实现了 F1=0.911、中位额外延迟 38 毫秒和零逃逸。 该防御机制填补了 LLM 服务安全中的关键空白，保护了现有防御常常忽视的服务层。它提供了一种实用、低延迟的解决方案，能够显著降低对抗性攻击对生产 LLM 系统的影响，惠及 AI 服务提供商和用户。 路由器使用冻结的 0.8B 嵌入骨干网络和每领域 MLP 头，蜜罐可以是基于规则/提示工程的代码蜜罐或专用的同族副本。在 GCG 后缀负载的并发洪泛下，转移恶意流量使生产模型令牌消耗减少 97.8%，循环训练修正头将合法安全研究的误路由降低 9 倍，同时将检测 F1 提升至 0.933。

rss · arXiv LLM Inference · 9月8日 06:26

**背景**: LLM 服务系统面临越狱和提示注入等对抗性攻击。现有防御通常将陷阱嵌入模型内存或在协议层重建欺骗，导致服务层缺乏保护。HoneyRoute 结合了流式路由器、双实现蜜罐和分析循环，以检测和转移恶意请求，同时持续改进检测能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2510.22628">Sentra-Guard: A Real-Time Multilingual Defense Against Adversarial ...</a></li>
<li><a href="https://arxiv.org/html/2603.20895">LLM Router: Rethinking Routing with Prefill Activations</a></li>
<li><a href="https://arxiv.org/abs/2605.00356">[2605.00356] MemRouter: Memory-as-Embedding Routing for Long-Term Conversational Agents</a></li>

</ul>
</details>

**标签**: `#LLM security`, `#adversarial attacks`, `#honeypot`, `#inference serving`, `#AI safety`

---

<a id="item-8"></a>
## [程序图：面向 LLM 智能体的自演化执行结构](https://arxiv.org/abs/2609.09153v1) ⭐️ 8.0/10

本文提出了程序图（Procedural Graphs），一种将程序性知识组织为（程序，关系，程序）三元组的新框架，并利用带有 LLM 优化器的自演化图来指导 LLM 智能体在长时程任务中的行动。该框架在多个数据集和 LLM 上持续优于基于记忆的基线，并能修复有缺陷的专家先验。 这项工作解决了 LLM 智能体面临的一个关键挑战：在长时程任务中维持程序性知识，这对于可靠的任务执行至关重要。通过外部化程序性知识并实现自演化，它为提升智能体可靠性、减少人工工程提供了一条有前景的路径，可能广泛影响 AI 规划和智能体系统。 程序图是自演化的：LLM 优化器对比失败轨迹与成功轨迹，编辑图的拓扑和属性，仅提交那些保持或提升验证集性能的编辑。从最小骨架开始，该循环构建的图能达到或超越手工设计的图，并且还能修复有缺陷的专家先验。

rss · arXiv Agent Infra · 9月8日 17:59

**背景**: 大型语言模型（LLM）越来越多地被用作智能体，在长时程内进行规划并通过外部工具行动。传统智能体通常依赖于对累积历史的无约束生成，这可能导致目标丢失、工具调用顺序错误或重复无效操作。程序图类比知识图谱，后者将事实知识组织为（实体，关系，实体）三元组，而程序图则将程序性知识组织为（程序，关系，程序）三元组，以回答“该做什么”的问题。该框架在每一步决策时定位智能体的活动节点，并使用指导模型将周围的子图转化为步骤级指导，从而影响求解器的下一步行动，但不强制其执行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/YuxingLu613/Procedural-Graph">GitHub - YuxingLu613/Procedural-Graph</a></li>
<li><a href="https://arxiv.org/pdf/2609.09153">Procedural Graphs: Self-Evolving Execution Structures for LLM ...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#procedural knowledge`, `#graph-based reasoning`, `#AI planning`, `#self-evolving systems`

---