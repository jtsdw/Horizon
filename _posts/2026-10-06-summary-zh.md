---
layout: default
title: "Horizon Summary: 2026-10-06 (ZH)"
date: 2026-10-06
lang: zh
---

> 从 59 条内容中筛选出 5 条重要资讯。

---

1. [Reflection 发布 501B 开放权重稀疏 MoE 模型 Beam](#item-1) ⭐️ 9.0/10
2. [vLLM v0.31.0 提升 DeepSeek-V4.1-Flash 性能并新增快速重启](#item-2) ⭐️ 8.0/10
3. [字节级 Transformer 通过 Token 叠加训练超越子词模型](#item-3) ⭐️ 8.0/10
4. [AgentPrivArena：审计真实世界 LLM 智能体工作流的隐私风险](#item-4) ⭐️ 8.0/10
5. [MAGI 智能体在九个真实药物发现项目中接受测试](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Reflection 发布 501B 开放权重稀疏 MoE 模型 Beam](https://reflection.ai/blog/introducing-beam) ⭐️ 9.0/10

Reflection 发布了 Beam，这是一个开放权重的稀疏混合专家（MoE）语言模型，总参数量为 5010 亿，激活参数为 230 亿，面向编程、推理和智能体（agentic）工作负载。该模型在 23.8 万亿经过筛选的 token 上完成预训练，并通过强化学习进一步调优，还在一个近期才走红、不可能出现在训练数据中的谜题任务上展现出很强的泛化能力。 Beam 为这个日益被 DeepSeek 等中国开放模型主导的领域增添了一个来自西方的大型开放权重竞争者，其发布可能影响开发者在编程和智能体应用中在开放与闭源模型之间的选择。随附的泛化实验也为“基准表现究竟反映真实推理还是记忆”的争论提供了一个具体（尽管非正式）的数据点。 根据社区与 DeepSeek V4.1 Flash 的对比，Beam 在预填充（prefill）和解码（decode）阶段每个 token 均激活 230 亿参数，不使用 N-gram 或 PLE 参数，训练 token 量约为 28 万亿。在那个走红的“陆地或水域”网格谜题上，Beam 据称达到 95.5% 的覆盖率，介于 Opus 5（92.5%）与另一个未具名模型之间。

hackernews · Philpax · 10月5日 19:16 · [社区讨论](https://news.ycombinator.com/item?id=49969183)

**背景**: 稀疏混合专家（MoE）模型把参数拆分成许多专门的“专家”子网络，并将每个 token 只路由到其中少数几个，因此总参数量可以非常大，而每个 token 实际消耗的算力却相对有限。这就是为什么像 Beam 这样的模型会用两个数字来描述：总参数量（5010 亿）和激活参数量（230 亿）。开放权重模型会公开训练好的权重，供他人下载、运行和微调，这与只能通过 API 访问的闭源模型形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://akash.network/the-bid/total-vs-active-parameters-moe-gpu-sizing-2026/">Total vs Active Parameters : LLM GPU Memory Guide (2026)</a></li>
<li><a href="https://mixroute.ai/models/deepseek-v4-1-flash/">deepseek-v4.1-flash – MixRoute Models</a></li>
<li><a href="https://www.unite.ai/best-open-source-llms/">5 Best Open Source LLMs (September 2026) – Unite.AI</a></li>

</ul>
</details>

**社区讨论**: 评论者欢迎又一个开放权重模型的发布，但对宣传说法持怀疑态度：有人指出 Beam 更大却仍落后于更小的免费中国模型，还有人给出了与 DeepSeek V4.1 Flash 的详细参数和 token 对比。那个泛化实验既引发了兴趣，也因其表述方式让人多看两眼，反映出关于这类演示究竟能证明多少的更大争论。

**标签**: `#open-weight models`, `#mixture-of-experts`, `#large language models`, `#AI research`, `#model release`

---

<a id="item-2"></a>
## [vLLM v0.31.0 提升 DeepSeek-V4.1-Flash 性能并新增快速重启](https://github.com/vllm-project/vllm/releases/tag/v0.31.0) ⭐️ 8.0/10

vLLM 发布 v0.31.0，包含来自 307 位贡献者的 717 次提交，为 DeepSeek-V4.1-Flash 带来重大性能优化，并通过新的 `vllm preload` 命令行工具引入快速重启的权重缓存守护进程。该版本还新增了 Model Runner V2 的投机解码、MoonEP 等大规模服务后端、新的调度控制选项，以及若干破坏性变更。 作为使用最广泛的开源大模型推理引擎之一，vLLM 的优化直接影响 DeepSeek-V4.1-Flash 等前沿模型的服务成本和延迟。快速重启功能减少了引擎重启期间的停机时间，这对需要高可用性的生产部署尤为重要。 该版本包含多项破坏性变更，例如将按请求的多模态参数限制在 `--trust-request-mm-kwargs` 之后、移除 `tokenizer_mode="slow"`、重命名 `--enable-mamba-fine-grained-prefix-cache`，以及用 `fp8_per_tensor` 简写替代通过 `quantization="fp8"` 进行的在线量化。此外还修复了前缀缓存键冲突和多模态缓存陈旧条目等安全问题。

github · khluu · 10月5日 06:44

**背景**: vLLM 是一个用于大语言模型高效推理和服务的开源框架，最初由加州大学伯克利分校 Sky Computing Lab 开发，核心是基于 PagedAttention 的 KV 缓存内存管理方法。DeepSeek-V4.1-Flash 是 DeepSeek 推出的多模态模型，在 45T token 语料上训练，采用稀疏注意力并支持最长 100 万 token 的上下文。FlashMLA 是 DeepSeek 为其模型优化的注意力内核库，本次发布将搭载 V4.1 NVFP4 压缩 KV 缓存的 FlashMLA mega attention 设为 SM100 GPU 上的默认实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/VLLM">VLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek-V4.1-Flash">DeepSeek-V4.1-Flash</a></li>
<li><a href="https://github.com/deepseek-ai/FlashMLA/blob/main/README.md">FlashMLA /README.md at main · deepseek-ai/ FlashMLA · GitHub</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#performance optimization`, `#DeepSeek`, `#release`

---

<a id="item-3"></a>
## [字节级 Transformer 通过 Token 叠加训练超越子词模型](https://arxiv.org/abs/2610.05978v1) ⭐️ 8.0/10

一篇新的 arXiv 论文（2610.05978）表明，采用 Token 叠加训练和哈希嵌入的字节级 Transformer，随着模型规模扩大，持续超越子词 Transformer，且无需专门的免分词器架构。研究还发现，字节 Transformer 能学习到类似分词的涌现抽象，将不确定性集中在局部结构边界附近，并在推测解码中实现 3.4 倍的接受 Token 数。 这项工作表明，免分词器的语言模型在规模上可以匹配或超越基于分词器的模型，可能通过消除手工设计分词器的需求来简化多语言和多模态流程。字节模型能学习自身分段的发现也为高效生成和可解释性开辟了新途径。 字节 Transformer 在没有专门的分词相关架构下训练，使用了 Token 叠加训练和哈希嵌入；将最多 25%的中间层限制为局部表示可保持下游性能，并且利用学习到的非均匀生成难度进行推测解码，比子词 Transformer 多接受 3.4 倍的 Token。

rss · arXiv Speculative Decoding · 10月5日 08:29

**背景**: 传统语言模型依赖分词器将文本切分为子词单元，这引入了归纳偏置，可能损害多语言或噪声文本的性能。免分词器模型直接处理原始字节，但更长的序列增加了计算量且缺乏显式的文本抽象。Token 叠加训练最近由 Nous Research 推广，通过在训练早期对 Token 包进行训练来加速预训练，而哈希嵌入则高效地将离散输入映射为连续向量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2610.05978">[2610.05978] Byte Language Models: Scaling, Emergent Abstractions...</a></li>
<li><a href="https://nousresearch.com/token-superposition">Efficient pretraining with token superposition - NOUS RESEARCH</a></li>
<li><a href="https://www.emergentmind.com/topics/tokenizer-free-architectures">Tokenizer - Free Architectures</a></li>

</ul>
</details>

**标签**: `#tokenizer-free`, `#byte-level models`, `#transformers`, `#scaling laws`, `#emergent abstractions`

---

<a id="item-4"></a>
## [AgentPrivArena：审计真实世界 LLM 智能体工作流的隐私风险](https://arxiv.org/abs/2610.06454v1) ⭐️ 8.0/10

研究者提出了 AgentPrivArena，一个在可复现执行环境中集成真实 MCP 工具与自托管服务、用于评估真实 LLM 智能体工作流隐私风险的框架，并配套提出轨迹级隐私指标以及 AgentPrivAudit 这一在智能体执行过程中监控隐私违规的运行时审计方法。针对当前最先进 LLM 智能体的实验揭示了现有基于结果的评测范式所忽视的大量隐私风险。 现有隐私基准依赖模拟轨迹和基于结果的指标，因而无法捕捉多步智能体执行过程中出现的风险；AgentPrivArena 的轨迹级审计填补了这一空白，对任何部署接触个人数据的工具调用型智能体的人都至关重要。它标志着面向可信智能体部署的评估正转向运行时、过程级的安全评测。 该框架在可复现执行环境中集成了真实 MCP 工具与自托管服务，其轨迹级指标量化了最终回复泄露之外的不必要信息访问。AgentPrivAudit 在执行过程中对隐私违规进行运行时监控，实验表明最先进的智能体表现出被既有范式忽视的大量风险。

rss · arXiv Agent Infra · 10月5日 14:55

**背景**: LLM 智能体是通过调用外部工具自主完成复杂任务的 AI 系统，而模型上下文协议（MCP）是一种新兴标准，让智能体能够连接日历、数据库和设计工具等服务。随着这些智能体获得个人数据访问权限，隐私风险随之上升，但此前的基准大多只根据最终答案是否泄露信息来评判隐私，忽视了智能体在过程中访问了什么。轨迹级指标则考察智能体所采取的完整步骤序列，而运行时审计在智能体仍在执行时即检查违规行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )? - Model Context Protocol</a></li>
<li><a href="https://arxiv.org/html/2608.14668">BRA- Audit : Budgeted Runtime Auditing for LLM Multi- Agent ...</a></li>
<li><a href="https://arxiv.org/pdf/2607.08395">Token-Flow Firewall: Semantic Runtime Auditing for Persistent AI...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#privacy`, `#benchmark`, `#AI safety`, `#runtime auditing`

---

<a id="item-5"></a>
## [MAGI 智能体在九个真实药物发现项目中接受测试](https://arxiv.org/abs/2610.06411v1) ⭐️ 8.0/10

研究人员开发了 MAGI，一个开放的模块化智能体，能够制定目标、启动并监控分子优化、解读构效关系并相应调整策略，并在来自三家制药公司的九个回顾性先导化合物优化项目中，在固定时间截点下进行了测试。MAGI 既可直接通过大语言模型生成分子，也可委托给 REINVENT 4 生成，两种路径均产生了有效结构，而项目成功与否取决于预测模型的准确性，而非生成路径。 这项工作提供了来自真实制药项目的罕见实证证据，表明智能体药物发现的瓶颈在于评分模型的适用域，而非工具编排，这可能引导研究者将精力转向改进预测模型而非生成方法。它还提供了一个新颖的基准和一个可插入现有计算化学工作流的开放协调层，对 AI/ML 和化学信息学从业者具有影响。 大语言模型提出的分子更接近局部化学空间，并在更少操作中达到相当或更高的主要活性，而 REINVENT 探索了更广阔的化学空间；一旦提出的化学结构超出预测模型的适用域，项目达成率就会下降。在一项盲评中，化学家无法区分智能体提出的分子与留出化合物，并认为构效关系推理大体合理但不完整。

rss · arXiv Agent Infra · 10月5日 14:28

**背景**: 智能体系统越来越多地协调分子设计工具，但在真实药物发现项目中，究竟是技术栈的哪一层限制了结果，此前并不清楚。先导化合物优化是提升有前景化合物活性、选择性等性质的阶段，通常依赖预测模型对候选分子打分。REINVENT 4 是广泛使用的强化学习从头分子生成框架，而 MAGI 被定位为一个可委托此类工具的协调层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2610.06411">[2610.06411] From Benchmark to Bench: Can Agents Survive...</a></li>
<li><a href="https://scirouter.ai/blog/reinvent4-vs-molmim-vs-drugex-molecule-generation/">REINVENT 4 vs MolMIM vs DrugEx: De Novo Molecule Generation ...</a></li>

</ul>
</details>

**标签**: `#drug-discovery`, `#agentic-systems`, `#benchmarking`, `#molecular-design`, `#AI-for-science`

---