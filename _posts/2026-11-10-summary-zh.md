---
layout: default
title: "Horizon Summary: 2026-11-10 (ZH)"
date: 2026-11-10
lang: zh
---

> 从 61 条内容中筛选出 5 条重要资讯。

---

1. [Anthropic 发布 Claude Fable 5.2 和 Mythos 5.2](#item-1) ⭐️ 8.0/10
2. [Evolving Infra：面向智能体工作负载的自适应 LLM 服务框架](#item-2) ⭐️ 8.0/10
3. [RecoGEM：面向生产环境的生成式推荐服务系统](#item-3) ⭐️ 8.0/10
4. [预测 LLM 智能体信息级联需考虑局部网络环境](#item-4) ⭐️ 8.0/10
5. [MIRIX-2.0：面向 LLM 智能体的多智能体记忆系统](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 发布 Claude Fable 5.2 和 Mythos 5.2](https://www.anthropic.com/claude-fable-and-mythos-5-2) ⭐️ 8.0/10

Anthropic 发布了 Claude Fable 5.2 和 Claude Mythos 5.2，这是其面向高难度技术工作的最新模型。Fable 5.2 在 Anthropic 的开源基准 data-eng-bench 上表现最强，而 Mythos 5.2 是同一模型，仅通过验证的组织可用于网络安全和生命科学研究。 此次发布标志着 Anthropic 在平衡其模型阵容方面的努力，Fable 5.2 在编码、推理和视觉方面较 Fable 5.1 有所提升。社区的高度参与和实际使用中显著生产力提升的报告表明，这些模型可能对软件开发和科学计算工作流程产生重大影响。 Fable 5.2 要求 30 天的数据保留期，除非得到 Anthropic 明确授权，否则不适用于零数据保留。Mythos 5.2 仅限通过 Anthropic 验证计划验证的组织使用，社区成员对基准测试方法提出了质疑，例如与 Carbon 和 Argon 等特定模型的比较。

hackernews · lairv · 11月9日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=50429068)

**背景**: Anthropic 是一家 AI 安全与研究公司，开发了 Claude 系列大型语言模型。模型发布通常伴随基准测试结果以展示能力，但这些基准的方法和公平性在社区中经常受到争议。Fable 和 Mythos 似乎是新的模型系列，其中 Mythos 是面向专业领域的受限版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude-fable-and-mythos-5-2">Introducing Claude Fable 5.2 and Claude Mythos 5.2 \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/models/fable-5-2/overview">Claude Fable 5 . 2 - Claude Platform Docs</a></li>
<li><a href="https://platform.claude.com/docs/en/models/mythos-5-2/overview">Claude Mythos 5.2 - Claude Platform Docs</a></li>

</ul>
</details>

**社区讨论**: 评论者报告了强大的编码和代码审查能力，包括在 60 万行 Fortran 代码库上实现 36 倍加速，以及在机器视觉项目中发现严重错误。然而，一些人对基准比较提出质疑，例如将 Fable xHigh 与 Carbon Med 对比以及 Carbon 不寻常的努力-智能曲线，其他人则推测发布时机与竞争对手有关。

**标签**: `#llm`, `#anthropic`, `#model-release`, `#benchmarks`, `#ai-coding`

---

<a id="item-2"></a>
## [Evolving Infra：面向智能体工作负载的自适应 LLM 服务框架](https://arxiv.org/abs/2611.12304v1) ⭐️ 8.0/10

Evolving Infra 提出了一种智能体自适应的 LLM 服务框架，利用智能体上下文信号动态重新分配预填充/解码计算并管理 KV 缓存。在编码、数学和计算机使用任务上，使用 GLM-5.2 和 Kimi K2.6 在多达 256 块 GB300 GPU 上，相比 NVIDIA 的 Dynamo，它将平均端到端请求延迟和 P95 首令牌时间分别降低了最多 4.1 倍和 14 倍。 这项工作解决了面向智能体工作负载的预填充-解码分离服务中的实际低效问题，其中负载不均衡和过早的 KV 缓存驱逐会损害性能。它可以显著提高为长时间运行、有状态的智能体应用提供服务的 AI 基础设施的可扩展性和成本效率。 该框架将计算分配与 KV 缓存管理解耦，使节点能够在预填充和解码之间高效切换，并采用在线规划器根据工作负载组成匹配 PD 拆分，以及一个智能体感知的分布式 KV 管理器来指导缓存驱逐和传输。目前它是一篇未经同行评审或社区讨论的 arXiv 预印本。

rss · arXiv LLM Inference · 11月9日 12:26

**背景**: 大语言模型推理通常将每个请求分为两个阶段：预填充，处理输入提示且计算密集；解码，生成输出令牌且内存密集。分离式服务将这些阶段运行在独立的 GPU 池上，以避免干扰并提高资源利用率。智能体工作负载，如编码助手或计算机使用智能体，是长时间运行、有状态的会话，会反复调用模型并增长上下文，因此缓存重用和动态资源分配至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://qubittool.com/blog/disaggregated-llm-serving-prefill-decode">Disaggregated LLM Serving : Prefill and Decode | QubitTool</a></li>
<li><a href="https://arxiv.org/pdf/2603.20397">KV Cache Optimization Strategies for Scalable and Efficient ...</a></li>
<li><a href="https://arxiv.org/abs/2608.15127">[2608.15127] From LLM Inference to Agentic Workloads ...</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#inference systems`, `#KV cache management`, `#agentic workloads`, `#distributed systems`

---

<a id="item-3"></a>
## [RecoGEM：面向生产环境的生成式推荐服务系统](https://arxiv.org/abs/2611.12296v1) ⭐️ 8.0/10

RecoGEM 是一个面向生成式推荐（GR）的生产级服务系统，它引入了运行时与引擎解耦的架构，以处理候选状态转换和实时工件更新等 GR 特有的职责。该系统已在生产线上部署超过九个月，服务数亿用户和十余个 GR 模型家族，单实例实现超过 1,000 QPS 的吞吐量，P99 延迟低于 35 毫秒，相比基线吞吐量提升 2.88 倍。 这项工作解决了将生成式推荐从研究推向生产的关键系统挑战，即在大候选空间上执行短的依赖解码步骤并满足严格的延迟约束。它表明 LLM 服务栈可以针对工业规模的推荐系统工作负载进行适配，可能加速生成式推荐在整个行业的采用。 执行引擎利用 GR 的短 token 序列、大候选群体和可预测的步骤形状来优化自注意力、候选选择和执行规划。评估基于 OneModel 生产工作负载，系统支持十余个 GR 模型家族，但摘要中未详细说明具体的模型架构和硬件配置。

rss · arXiv LLM Inference · 11月9日 12:20

**背景**: 生成式推荐（GR）是从传统推荐系统（对候选物品打分）到自回归生成物品标识符的范式转变，有望提高质量，但由于在大物品空间上执行短的依赖解码步骤，使得服务更加困难。像 vLLM 这样的 LLM 服务系统是为长序列和批处理吞吐量设计的，与 GR 的延迟关键、短步骤工作负载存在结构性不匹配。RecoGEM 通过将 GR 特有的运行时职责与执行引擎解耦来弥合这一差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/transformer-index-for-generative-recommenders-tiger">TIGER: Transformer Index for Generative Recommenders</a></li>
<li><a href="https://mortalapps.com/infrastructure/ai-serving-infrastructure/vllm-architecture/">vLLM Runtime Architecture | AI Infrastructure | MortalApps</a></li>
<li><a href="https://vinija.ai/recsys/candidate-gen/">Vinija's Notes • Recommendation Systems • Candidate Generation</a></li>

</ul>
</details>

**标签**: `#generative-recommendation`, `#serving-systems`, `#LLM-inference`, `#recommender-systems`, `#systems-architecture`

---

<a id="item-4"></a>
## [预测 LLM 智能体信息级联需考虑局部网络环境](https://arxiv.org/abs/2611.12256v1) ⭐️ 8.0/10

一篇新的 arXiv 论文表明，预测 LLM 智能体网络中的信息级联需要在智能体的局部网络环境中测量其响应，因为忽略联系人数量的响应会错误预测级联，其误差可通过解析推导得出，且仅凭网络拓扑无法揭示。当在上下文中测量时，该响应通过平均场理论能够预测完整的模拟结果，包括临界点。 这项工作对 AI 安全和大规模多智能体系统的部署具有重要意义，因为它表明预测 LLM 智能体的集体行为需要在局部网络环境中评估它们，而不是孤立地评估。这些发现可以为设计更安全的 AI 系统提供信息，并提高用于社会科学和政策研究的多智能体模拟的保真度。 该研究关注智能体根据有多少联系人分享了帖子来决定是否分享的网络，并发现即使在相同的分享联系人比例下，智能体的响应也取决于其联系人总数和帖子内容。解析误差推导表明，在异质网络上错误预测会增加，而当响应在上下文中测量时，平均场理论成功预测了包括临界点在内的级联。

rss · arXiv Agent Infra · 11月9日 11:47

**背景**: 信息级联是指人们基于他人的行为决定采取某种行为，这在社交网络中很常见。平均场理论是一种数学工具，通过对相互作用进行平均来近似复杂系统的行为，常用于研究网络上的动力学。LLM 智能体是由大语言模型驱动的 AI 系统，可以在多智能体环境中模拟类人决策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Information_cascade">Information cascade - Wikipedia</a></li>
<li><a href="https://ctp.itp.ac.cn/EN/abstract/article/0253-6102/17593">An Improved Heterogeneous Mean - Field Theory for the Ising Model...</a></li>
<li><a href="https://arxiv.org/abs/2605.30144">[2605.30144] AgentSchool: An LLM-Powered Multi-Agent ...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#multi-agent systems`, `#complex networks`, `#information cascades`, `#AI safety`

---

<a id="item-5"></a>
## [MIRIX-2.0：面向 LLM 智能体的多智能体记忆系统](https://arxiv.org/abs/2611.12068v1) ⭐️ 8.0/10

MIRIX-2.0 提出了一种多智能体长期记忆系统，采用六个类型化记忆智能体和一个溯源超图，在多个问答和程序性基准上达到最先进准确率，包括 LoCoMo 上的 91.4% 和 LongMemEval-S 上的 72.6%，后者领先最强基线 14.3 个百分点。 这项工作解决了 LLM 智能体长期记忆的挑战，这对于个性化、一致性和技能复用至关重要，并证明了无需微调且使用闭源和开源模型即可构建实用、准确且高效的记忆系统。 该系统将完整记录作为记录系统，使用带有 n 元帧的溯源超图进行索引，并在显式预算下运行检索，因此证据不会随历史增长；AutoDream 在不重写记录的情况下合并重复锚点并将任务会话提炼为技能，在禁用 AutoDream 时，它在所有五个计时基准上比 HyperMem 回答更快。

rss · arXiv Agent Infra · 11月9日 08:43

**背景**: LLM 智能体的长期记忆旨在让它们记住过去的交互并复用成功的策略，但现有方法如参数化记忆（需要训练）、整合（可能丢失细节）和存储每条记录（无限增长）都存在权衡。LoCoMo 和 LongMemEval-S 等基准评估长期对话记忆，而 ALFWorld 和 WebShop 测试交互环境中的程序性记忆。基于超图的记忆（如 HyperMem）使用超边捕获记忆项之间的多路关系，MIRIX-2.0 在此基础上构建了引用源记录的溯源超图。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2604.08256">HyperMem: Hypergraph Memory for Long-Term Conversations</a></li>
<li><a href="https://arxiv.org/abs/2402.17753">Evaluating Very Long - Term Conversational Memory of LLM Agents</a></li>
<li><a href="https://arxiv.org/html/2512.18950">Learning Hierarchical Procedural Memory for LLM Agents through...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#memory systems`, `#multi-agent`, `#long-term memory`, `#benchmarks`

---