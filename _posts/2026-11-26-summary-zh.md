---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 58 条内容中筛选出 7 条重要资讯。

---

1. [斯科特·阿伦森回应 AI 在矩阵乘法上的突破](#item-1) ⭐️ 9.0/10
2. [1Password 披露安全事件：攻击者通过员工笔记本推送恶意代码](#item-2) ⭐️ 8.0/10
3. [PARK：面向多轮 LLM 推理的最优路由与 KV 缓存保留策略](#item-3) ⭐️ 8.0/10
4. [Libtt 通过 PJRT 将 PyTorch 和 JAX 引入 Tenstorrent](#item-4) ⭐️ 8.0/10
5. [IRTIQA 基准测试 LLM 智能体自我进化能否从英语迁移至乌尔都语](#item-5) ⭐️ 8.0/10
6. [Chasm 框架揭示跨模型潜在通信的安全风险](#item-6) ⭐️ 8.0/10
7. [Crucible Bench：新基准测试评估 LLM 智能体在可执行化学研究中的能力](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [斯科特·阿伦森回应 AI 在矩阵乘法上的突破](https://scottaaronson.blog/?p=10379) ⭐️ 9.0/10

斯科特·阿伦森发表博客文章，回应 AI 在数学领域的一项重大突破，具体是指矩阵乘法指数为九分之四（2.25）的声称结果，该结果将建立匹配的上界和下界。这篇文章在 Hacker News 上引发了超过 1200 条评论的激烈讨论。 如果这一突破得到验证，将解决计算复杂性领域一个长期悬而未决的问题，并可能对算法设计、密码学和科学计算产生广泛影响。同时，它也加剧了关于 AI 在数学领域能力不断增强及其相关风险的广泛讨论。 这一声称的结果详细发表在 11 月 24 日的一篇预印本论文中，题为《矩阵乘法指数为九分之四》，该论文为任意域上的方阵乘法建立了匹配的上界和下界。讨论还涉及 AI 实验室是否可能拥有秘密的密码学突破，评论者们在争论此类秘密被保守的可能性。

hackernews · Kotlopou · 11月25日 19:11 · [社区讨论](https://news.ycombinator.com/item?id=50646108)

**背景**: 矩阵乘法指数通常用 omega 表示，它代表两个 n×n 矩阵可以在 O(n^omega)时间内相乘的最小数值。几十年来，研究人员一直试图降低 omega 的上界，目前已知的最佳上界约为 2.371。证明 omega 等于 2.25 将是一个重大的理论进展，而 AI 参与发现这一结果将标志着 AI 在数学领域的一个重要里程碑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://aiweekly.co/alerts/aaronson-warns-ai-math-gains-threaten-human-relevance">Aaronson warns AI math gains threaten human relevance | AI Weekly</a></li>

</ul>
</details>

**社区讨论**: 评论者们表达了各种观点：一些人认为 AI 在公理化数学上的成功并不意味着它能解决所有领域或构成生存威胁，而另一些人则担心人类在生物学上无法理解变化的规模。还有人怀疑 AI 实验室是否拥有秘密的密码学突破，一些人认为鉴于实验室的规模，这样的秘密很难保守。

**标签**: `#AI`, `#mathematics`, `#matrix multiplication`, `#existential risk`, `#research breakthrough`

---

<a id="item-2"></a>
## [1Password 披露安全事件：攻击者通过员工笔记本推送恶意代码](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password 披露了一起安全事件，攻击者通过攻破一名员工的笔记本电脑，访问了源代码并向其后端服务推送了恶意代码，导致部分客户的管理数据被下载。公司表示客户密码库未被访问，仍然安全。 该事件凸显了 SaaS 公司面临的关键供应链攻击向量：单个员工设备被攻破就可能导致代码被注入生产系统。作为广泛使用的密码管理器，1Password 的此次事件引发了对分支保护、代码审查和部署安全措施的担忧，进而影响人们对 SaaS 安全的整体信任。 攻击者利用被攻破的账户访问源代码，并向其后端服务推送恶意代码，进而下载了客户的管理数据。1Password 未说明是否设置了分支保护规则或这些规则是否被绕过，少数受影响用户已收到专门通知。

hackernews · lxhrstn · 11月25日 17:18 · [社区讨论](https://news.ycombinator.com/item?id=50644817)

**背景**: 1Password 是一款流行的密码管理器，将用户凭据存储在加密密码库中。在 SaaS 供应链攻击中，攻击者攻破可信赖供应商的系统或代码管道以注入恶意代码，进而可能影响下游客户。此次事件之前，1Password 曾发生过多起安全事件，包括 2023 年与 Okta 支持系统相关的泄露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving 1Password’s backend systems.</a></li>
<li><a href="https://thehackernews.com/2026/11/1password-hacked-customer-data-and.html">1Password Hacked, Customer Data and Source Code Stolen in GitHub...</a></li>
<li><a href="https://1password.com/blog/okta-incident">Okta Support System incident and 1Password</a></li>

</ul>
</details>

**社区讨论**: 包括安全专家 tptacek 在内的评论者强调，员工笔记本电脑被攻破是 SaaS 公司最重要的攻击向量，分支保护和代码部署安全措施至关重要。其他人质疑 1Password 为何未明确说明是否禁用了直接推送主分支或分支保护是否被绕过，一些长期用户对在线密码库和供应链风险表示担忧。

**标签**: `#security`, `#supply-chain`, `#saas`, `#password-manager`, `#incident-response`

---

<a id="item-3"></a>
## [PARK：面向多轮 LLM 推理的最优路由与 KV 缓存保留策略](https://arxiv.org/abs/2611.34584v1) ⭐️ 8.0/10

该论文为多轮 LLM 推理建立了一个流体模型，并提出了 PARK，一种基于影子价格和局部保留指数的渐近最优路由与 KV 缓存保留控制器。在 16 块 H200 GPU 上服务 1970 亿参数 MoE 模型的实验中，PARK 相比最强基线将输出吞吐量提升了 24.2%至 40.0%，并在 128 GPU 规模下达到 91.3%至 97.4%的前缀缓存命中率。 多轮 AI 智能体正成为 LLM 的主要工作负载，联合优化请求路由和 KV 缓存保留对于降低生产集群的延迟和成本至关重要。PARK 将理论最优性与异步到达、延迟负载报告等实际约束相结合，为 LLM 服务系统提供了一种可部署的解决方案。 PARK 采用在线投影次梯度价格更新和单轮迁移前瞻，并使用按每字节-纪元预期重用价值排序的局部 KV 保留指数。消融实验表明，仅保留指数就将先前前缀 token 丢失率从 13.26%降至 2.17%，相比 LRU 驱逐将吞吐量提升了 36.7%。

rss · arXiv LLM Inference · 11月25日 15:45

**背景**: 多轮 AI 智能体迭代地调用 LLM 和外部工具，产生轮次间的延迟，在此期间如果会话被路由到同一服务器，KV 缓存（中间注意力状态）就可以被重用。在集群中高效管理这种缓存具有挑战性，因为路由决策影响缓存局部性，而缓存驱逐策略影响未来的重用。现有的 vLLM 和 llm-d 等系统提供了 KV 缓存管理，但缺乏一个统一的理论框架来联合优化路由和保留。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.34584">Routing and Cache Retention for Multi-Turn LLM Inference ...</a></li>
<li><a href="https://llm-d.ai/docs/architecture/kv-management">KV Cache Management - llm-d</a></li>
<li><a href="https://vllm.ai/">vLLM</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#KV cache`, `#routing`, `#resource allocation`, `#systems`

---

<a id="item-4"></a>
## [Libtt 通过 PJRT 将 PyTorch 和 JAX 引入 Tenstorrent](https://arxiv.org/abs/2611.34273v1) ⭐️ 8.0/10

Libtt 是一个新的编译器和运行时栈，它实现了 PJRT 接口，使得 JAX 可以直接在 Tenstorrent 处理器上运行，而 PyTorch 则通过 TorchTPU 以最小改动运行。它以单个共享库的形式发布，并包含对 Tenstorrent 开源软件的大量修复和优化。 这大大降低了 PyTorch 和 JAX 用户采用 Tenstorrent 硬件的门槛，因为针对 TPU 的软件只需替换自定义内核即可运行。它通过提供成熟的、框架兼容的软件栈，增强了 Tenstorrent 在 AI 加速器市场中的地位。 Libtt 通过了大多数 JAX 和 TorchTPU 测试套件，并成功运行 SGLang、TorchTitan 和 Miles，覆盖了服务、微调和强化学习工作负载。然而，它是一篇未经同行评审且尚无社区讨论的 arXiv 预印本。

rss · arXiv LLM Inference · 11月25日 12:34

**背景**: Tenstorrent 设计 AI 处理器，与 GPU 和 TPU 竞争，但其软件生态系统一直不太成熟。PJRT 是一个硬件和框架无关的接口，被 JAX 和 PyTorch/XLA 等基于 XLA 的框架用于面向不同加速器。TorchTPU 是由 Google 和 Meta 共同开发的 TPU 原生 PyTorch 后端，取代了 PyTorch/XLA。Libtt 利用这些接口为 Tenstorrent 带来框架兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensource.googleblog.com/2023/05/pjrt-simplifying-ml-hardware-and-framework-integration.html">PJRT : Simplifying ML Hardware and Framework Integration</a></li>
<li><a href="https://openxla.org/">OpenXLA Project</a></li>
<li><a href="https://github.com/openxla/community/blob/main/rfcs/20230123-pjrt-plugin.md">community/rfcs/20230123- pjrt -plugin.md at main · openxla/community</a></li>

</ul>
</details>

**标签**: `#Tenstorrent`, `#PJRT`, `#JAX`, `#PyTorch`, `#compiler`, `#runtime`, `#ML hardware`

---

<a id="item-5"></a>
## [IRTIQA 基准测试 LLM 智能体自我进化能否从英语迁移至乌尔都语](https://arxiv.org/abs/2611.34303v1) ⭐️ 8.0/10

研究人员发布了 IRTIQA 基准，包含 DROP、SNIPS、AppWorld 和 SkillsBench 的英语、乌尔都语翻译及乌尔都语代码混合对齐变体，并用它评估了三个自我进化框架——Tool-R0、AgentEvolver 和 Autogenesis——与其未进化基线的对比。他们发现自我进化通常能提升任务表现，但很少能缩小语言差距，进化后的系统在英语上仍强出最多 0.26 DROP F1。 这项工作表明，语言平等不会从智能体自我改进中自动产生，因此面向多语言部署的开发者必须将其作为明确的设计目标。它影响到所有为非英语或代码混合用户构建 LLM 智能体的人，揭示了性能差距可能扩大的隐藏风险。 该基准通过矩阵语言代码混合流程构建并经过人工验证，评估使用共享的 Gemma-4 31B 骨干模型。值得注意的是，语言差距在进化前就存在，在多步任务上最大，且代码混合表现为一种独立条件而非退化的翻译；基于 RL 的进化甚至可能对乌尔都语推理的伤害大于英语。

rss · arXiv Agent Infra · 11月25日 12:56

**背景**: LLM 智能体越来越多地被训练从自身经验中学习——这一过程称为自我进化——但用于这种学习和评估的任务几乎总是英语。代码混合，即在一个对话中混合两种语言，在多语言社区中很常见，但在基准中很少体现。IRTIQA 通过创建现有智能体任务的对齐多语言变体来填补这一空白，以测试收益是否能跨语言迁移。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2602.21320">Tool - R 0 : Self -Evolving LLM Agents for Tool- Learning from Zero Data</a></li>
<li><a href="https://aclanthology.org/2023.findings-acl.185/">The Decades Progress on Code-Switching Research in NLP: A ...</a></li>
<li><a href="https://arxiv.org/html/2004.12376">GLUECoS : An Evaluation Benchmark for Code-Switched NLP</a></li>

</ul>
</details>

**标签**: `#multilingual NLP`, `#LLM agents`, `#self-evolution`, `#benchmark`, `#code-switching`

---

<a id="item-6"></a>
## [Chasm 框架揭示跨模型潜在通信的安全风险](https://arxiv.org/abs/2611.34278v1) ⭐️ 8.0/10

一篇新论文提出了 Chasm 框架，该框架刻画了多智能体 LLM 系统中跨模型交接攻击的三个新攻击面：源模型、映射器和交接机制本身。实验表明，通过 KV 缓存传输的潜在交接会严重削弱安全对齐，一个原生仅遵循 0.4%基准提示注入的目标模型，在通过映射器传输后遵循率高达 44.2%。 这项工作揭示，潜在通信作为多智能体系统的一种新兴效率技术，会创建新的攻击面，能够绕过安全对齐和提示注入防御。随着异构多智能体系统日益普遍，这些发现强调需要在潜在交接层面而非仅在文本接口层面采取安全措施。 对于越狱攻击，仅传输就能使同一模型家族内的攻击成功率提高最多 24.6 个百分点，零样本攻击提高最多 69.2 个百分点，而通过映射器进行白盒优化可将成功率提升至 92.5%，而普通 GCG 仅为 37.5%。作者提出了一种轻量级目标端缓存防护机制，通过校正传输的缓存来恢复目标模型的拒绝行为，从而显著缓解这些攻击。

rss · arXiv Agent Infra · 11月25日 12:35

**背景**: 跨模型 KV 缓存传输是一种实验性技术，它将一个大语言模型生成的键值缓存转换为另一个模型可用的表示，使智能体能够共享上下文而无需重新编码。这减少了多智能体系统中的通信开销和预填充计算，但也意味着目标模型消费了并非由自身编码的上下文，从而引发对其安全对齐是否仍然有效的疑问。Chasm 框架系统地研究了这些安全影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiwiki.ai/wiki/cross_model_kv_cache_transfer">Cross-Model KV Cache Transfer - AI Wiki</a></li>
<li><a href="https://arxiv.org/pdf/2609.00891">CacheBridge: Efficient Cross-Model KV Cache Transfer</a></li>
<li><a href="https://onetriangle.ai/blog/32b-prefill-8b-decode/">32B Prefill, 8B Decode | OneTriangle Research</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#multi-agent systems`, `#latent communication`, `#KV cache transfer`, `#security`

---

<a id="item-7"></a>
## [Crucible Bench：新基准测试评估 LLM 智能体在可执行化学研究中的能力](https://arxiv.org/abs/2611.34254v1) ⭐️ 8.0/10

研究人员推出了 Crucible Bench，这是一个包含 1,078 个任务的基准测试，涵盖 12 个任务家族，这些任务从 18 个已发表的数据集中精选而来，覆盖了设计-制造-测试-分析（DMTA）循环的全部四个阶段。智能体通过模型上下文协议在七个隔离环境中使用 75 种领域特定工具，沙箱评分器验证合成路线和实验方案等输出。 该基准测试填补了评估 LLM 智能体在知识问答之外能力的关键空白，转向需要工具使用和解释的可执行研究任务。它通过提供标准化方法来衡量和比较智能体执行真实化学工作流程的能力，有望推动 AI for science 的进展。 在评估的 14 个 LLM 中，最佳模型总体得分为 0.545，合成规划和闭环优化是最难的领域；值得注意的是，总体性能不能很好地预测优化性能，总体排名第十二的模型在闭环优化中获得了最高分。错误分析显示，智能体尽管成功运行了工具，但经常提交化学上无效的结果，而更强的模型从工具访问中获益更多。

rss · arXiv Agent Infra · 11月25日 12:18

**背景**: 设计-制造-测试-分析（DMTA）循环是药物发现中的核心迭代工作流程，其中分子被设计、合成、测试和分析，以指导下一轮优化。模型上下文协议（MCP）是一种标准化接口，使 LLM 智能体能够连接外部工具和数据源，简化集成。Crucible Bench 利用 MCP 在沙箱环境中为智能体提供领域特定的化学工具，实现安全且可重复的评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/article/pii/S2472630325000202">Digitalizing the design-make-test-analyze workflow in drug ...</a></li>
<li><a href="https://inferensys.com/glossary/molecular-informatics-and-bio-artificial-intelligence/de-novo-drug-design/design-make-test-analyze-cycle">Design-Make-Test-Analyze Cycle Definition | Inference Systems</a></li>
<li><a href="https://www.linkedin.com/posts/andreashendyw_ai-artificialintelligence-agenticai-activity-7488413643206930432-uTr0">Model Context Protocol Simplifies LLM Tool Integration | LinkedIn</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#benchmark`, `#chemistry`, `#AI for science`, `#tool use`

---