---
layout: default
title: "Horizon Summary: 2026-10-23 (ZH)"
date: 2026-10-23
lang: zh
---

> 从 71 条内容中筛选出 7 条重要资讯。

---

1. [Quad9 因 DNS 封锁令将退出法国](#item-1) ⭐️ 8.0/10
2. [NVIDIA OpenShell：面向自主 AI 智能体集群的安全运行时](#item-2) ⭐️ 8.0/10
3. [研究发现 LLM 推理优化并非总能迁移至 Apple Silicon](#item-3) ⭐️ 8.0/10
4. [LLVMhammer：Rowhammer 位翻转攻击 Triton 编译器，拖慢 LLM 推理](#item-4) ⭐️ 8.0/10
5. [AfterDeleteBench：LLM 智能体在三分之二的情况下能恢复已删除的秘密](#item-5) ⭐️ 8.0/10
6. [DoorDash 利用多智能体 LLM 系统自动清理功能开关](#item-6) ⭐️ 8.0/10
7. [LLM 多智能体系统易出现羊群效应和失控级联](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Quad9 因 DNS 封锁令将退出法国](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

瑞士非营利公共 DNS 解析器 Quad9 宣布，在 2025 年 11 月 24 日之后将停止为法国用户提供服务，原因是法院命令要求其封锁特定域名，并对不遵守行为处以罚款。该命令由索尼音乐娱乐德国公司获得，该公司使用 VPN 证明 Quad9 的地理 IP 封锁可以被绕过。 此案开创了一个先例：即使 DNS 解析器尝试进行地理 IP 封锁，也可能因规避行为而被追究责任，这可能会迫使其他公共解析器退出市场或遵守广泛的封锁令。它引发了关于互联网基础设施提供商责任以及法国乃至全球互联网自由和隐私未来的重要问题。 Quad9 首席技术官 John Todd 表示，地理 IP 封锁不足以选择性地拒绝解析，该组织可能在 11 月 24 日之后使用地理 IP 过滤器来封锁法国用户。在索尼通过 VPN 绕过地理 IP 封锁后，法院以藐视法庭为由对 Quad9 处以罚款，凸显了即使采取技术措施也存在法律风险。

hackernews · farrokhi · 10月22日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=50195959)

**背景**: Quad9 是由瑞士非营利基金会运营的免费公共 DNS 解析器，它封锁恶意软件和钓鱼域名，同时强调隐私保护。DNS 解析器将域名转换为 IP 地址，而 DNS 级别的封锁是限制网站访问的常见方法。法国越来越多地使用法院命令强制 DNS 解析器和 ISP 封锁与盗版相关的域名，类似行动也曾针对谷歌、Cloudflare 和思科。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9 - Wikipedia</a></li>
<li><a href="https://quad9.net/">Quad9 | A public and free DNS service for a better security ...</a></li>
<li><a href="https://www.internetsociety.org/resources/doc/2025/mandated-dns-blocking/">Mandated DNS Blocking: A Guide for Legal Professionals</a></li>

</ul>
</details>

**社区讨论**: 评论者大多批评该裁决，认为惩罚 DNS 解析器类似于让电话簿为罪犯的号码负责。一些人建议解析器应停止解析起诉它们的公司的域名，而另一些人指出 Quad9 的退出跟随了思科的类似举措，并反映了版权所有者与互联网基础设施之间更广泛的紧张关系。

**标签**: `#DNS`, `#privacy`, `#legal`, `#internet governance`, `#France`

---

<a id="item-2"></a>
## [NVIDIA OpenShell：面向自主 AI 智能体集群的安全运行时](https://github.com/NVIDIA/OpenShell) ⭐️ 8.0/10

NVIDIA 发布了 OpenShell，这是一个开源运行时（版本 0.1.0），允许自主 AI 智能体集群读取文件、安装软件包、调用 API 并使用凭证，同时通过策略强制执行对数据、机密和网络资源的访问限制。该项目托管在 GitHub 上，并在 Hacker News 上引发了 335 分、175 条评论的热烈讨论。 随着 AI 智能体从只读助手转变为具有写权限和工具使用能力的自主系统，传统的 API 安全已不足够；OpenShell 满足了运行时隔离和策略执行的关键需求，以防止数据泄露和权限提升。这对于在生产环境中部署智能体集群的组织至关重要，尤其是那些需要可审计性和零信任控制的受监管行业。 OpenShell 结合了沙箱执行、受控服务访问、凭证管理和形式化策略分析，以限制 API 操作并在智能体工作负载之外保护凭证，且无需重写智能体。Cadence、Slack 和 Gecko 等组织被提及为使用者，但该项目仍处于 0.1.0 版本，安全与能力之间的权衡仍是争论的话题。

hackernews · niemandhier · 10月22日 17:44 · [社区讨论](https://news.ycombinator.com/item?id=50198675)

**背景**: 自主 AI 智能体是利用大型语言模型规划和执行任务的软件系统，通常需要访问文件、网络和凭证。沙箱和运行时隔离是限制智能体行为的技术，可降低恶意或意外有害行为的风险。基于策略的执行允许管理员声明关于智能体可以访问哪些资源的细粒度规则，类似于容器安全和零信任架构的工作方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/NVIDIA/OpenShell">GitHub - NVIDIA/OpenShell: OpenShell is the safe, private ...</a></li>
<li><a href="https://developer.nvidia.com/blog/add-runtime-controls-to-ai-agents-with-nvidia-openshell/">Add Runtime Controls to AI Agents with NVIDIA OpenShell</a></li>
<li><a href="https://www.nvidia.com/en-us/ai/openshell/">NVIDIA OpenShell | Open, Secure Runtime for AI Agents</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为在容器中运行智能体是必要的，一些人分享了使用 iron proxy 进行网络限制和 OpenShell 进行策略管理的积极经验。然而，对于 OpenShell 既能提供完整能力又能保证安全的营销宣传存在怀疑，一位评论者称其为矛盾修辞；其他人则强调了即使使用域名允许列表，防止数据泄露仍是未解决的挑战。

**标签**: `#AI agents`, `#security`, `#sandboxing`, `#NVIDIA`, `#runtime isolation`

---

<a id="item-3"></a>
## [研究发现 LLM 推理优化并非总能迁移至 Apple Silicon](https://arxiv.org/abs/2610.31479v1) ⭐️ 8.0/10

一篇新的 arXiv 论文在四台 Apple Silicon 设备上，以单请求解码负载评估了四类 LLM 推理优化——KV 缓存剪枝、推测解码、移植的 GPU 内核和训练后量化，并在可能的情况下与 RTX 4090 进行匹配对比。研究发现，KV 缓存剪枝在 Apple 上可实现最高 1.75 倍的端到端吞吐量提升，但在桌面级 NVIDIA GPU 上可能降低吞吐量；而所有评估的推测解码方法在 Apple 上均降低吞吐量，尽管在服务器 GPU 上报道有 2-6 倍的提升。 Apple Silicon 是本地 LLM 推理的主要平台，但大多数优化都是在服务器级 NVIDIA GPU 上针对批量服务负载设计和验证的。研究结果表明，加速并非技术本身的便携属性，而是技术、运行时、硬件契约和工作负载机制的联合函数，这对不断增长的本地 LLM 社区和选择优化的开发者具有重要意义。 CUDA 内核设计仅能部分迁移：公开的 Metal 缺少异步拷贝，且批大小为 1 的解码使若干面向服务的机制不适用，不过可迁移组件仍带来最高 1.20 倍解码吞吐量提升。量化收益因机器而异，研究覆盖四台 Apple 设备，采用统一的单请求解码负载。

rss · arXiv LLM Inference · 10月22日 16:04

**背景**: KV 缓存剪枝在长上下文推理中丢弃注意力分数较低的缓存键值 token，以减少内存和计算。推测解码使用较小的草稿模型生成候选 token，再由较大的目标模型验证，旨在不改变输出质量的情况下加速生成。训练后量化降低模型精度（如降至 4 位或 8 位），以减少内存占用并提高吞吐量。Metal 是 Apple 的 GPU API，类似于 NVIDIA 硬件上的 CUDA，其功能集与 CUDA 存在差异，影响内核的可移植性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2402.01528">[2402.01528] Decoding Speculative Decoding</a></li>
<li><a href="https://research.google/blog/looking-back-at-speculative-decoding/">Looking back at speculative decoding</a></li>
<li><a href="https://arxiv.org/abs/2510.07651">[2510.07651] OBCache: Optimal Brain KV Cache Pruning for ... Layer-Dependent KV Cache Pruning for Long-Context LLM Inference GitHub - samuelcrowther/kv-cache-pruner: KV cache pruning ... LevelKV: Hierarchical KV Cache Pruning for Efficient and ... DepthKV: Layer-Dependent KV Cache Pruning for Long-Context ... DepthKV: Layer-Dependent KV Cache Pruning for Long-Context ...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#Apple Silicon`, `#performance evaluation`, `#GPU optimization`, `#quantization`

---

<a id="item-4"></a>
## [LLVMhammer：Rowhammer 位翻转攻击 Triton 编译器，拖慢 LLM 推理](https://arxiv.org/abs/2610.30798v1) ⭐️ 8.0/10

研究人员提出 LLVMhammer，这是首个通过 Rowhammer 攻击在 Triton 基于 MLIR/LLVM 的编译流水线中翻转比特的攻击，使 Triton 生成功能正确但性能次优的 GPU 内核。由于 Triton 会将编译后的内核缓存到磁盘，一次成功的位翻转即可在 NVIDIA RTX 4090 和 AMD RX 7900 XTX 上持续将 LLM 推理延迟增加 4% 至 16%。 这种跨层攻击将 CPU DRAM 硬件故障与持续的 GPU 推理性能下降联系起来，表明 Rowhammer 不仅可破坏正确性，还可被武器化以降低性能。由于 Triton 的目标无关编译阶段在不同 GPU 厂商间共享，该攻击具有厂商无关性，在多 GPU 部署规模下可能转化为可观的年度运营成本。 作者构建了 Karnage 工具，用于自动定位 Triton 目标无关流水线中可利用的位翻转位置，并在 Qwen2.5-7B-Instruct、Llama-3.1-8B-Instruct、Mistral-7B-Instruct-v0.3 和 Deepseek-llm-7B-chat 上评估 LLVMhammer。除性能下降外，该攻击还能破坏 LLM 输出，在不同 GPU 厂商上将 BERTScore 降至最低 25%。

rss · arXiv LLM Inference · 10月22日 06:24

**背景**: Rowhammer 是一种 DRAM 漏洞，通过快速访问某一行内存，可能翻转相邻行的比特，从而篡改数据或代码。Triton 是一种基于 Python 的语言和编译器，用于编写高性能 GPU 内核；它通过 MLIR/LLVM 流水线降低内核并缓存生成的二进制文件。LLM 依赖这类即时编译内核实现高效推理，因此编译器优化阶段中的故障可能悄无声息地产生更慢或错误的代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Row_hammer">Row hammer - Wikipedia</a></li>
<li><a href="https://triton-lang.org/main/index.html">Welcome to Triton’s documentation! — Triton documentation</a></li>
<li><a href="https://pytorch.org/blog/triton-kernel-compilation-stages/">Triton Kernel Compilation Stages - PyTorch</a></li>

</ul>
</details>

**标签**: `#Rowhammer`, `#LLM inference`, `#GPU security`, `#Triton compiler`, `#hardware fault attacks`

---

<a id="item-5"></a>
## [AfterDeleteBench：LLM 智能体在三分之二的情况下能恢复已删除的秘密](https://arxiv.org/abs/2610.31366v1) ⭐️ 8.0/10

研究人员提出了 AfterDeleteBench，这是一种受控的行为审计方法，显示固定权重的 LLM 智能体（Qwen2.5-7B-Instruct）在约三分之二的情况下能恢复已删除的秘密，而匹配的从未接触过该秘密的对照组恢复率为零。即使没有逐字副本，在公开组合规则下从单独存储的组件中精确重建秘密，在 Qwen、Mistral 和 Phi-3 模型上的成功率也达到 62%至 99%。 这项工作揭示，在具有持久记忆的 LLM 智能体中，删除记忆记录并不能保证信息被移除，这是任何构建智能体系统的人都必须面对的关键隐私和安全故障模式。它主张应在智能体-记忆层面以行为方式审计源删除，而不是将其视为简单的存储操作。 该审计将先接触后删除的智能体与匹配的从未接触的智能体进行比较，以将恢复归因于原始接触，并表明响应接口很重要：当格式和解析器不匹配时，包含目标的回复可能被错误地评为失败。在测试的正基线设置中，溯源感知闭包消除了观察到的恢复，而精确字面写入过滤器阻止重新插入，但无法擦除已经存在的信息。

rss · arXiv Agent Infra · 10月22日 14:41

**背景**: LLM 智能体通常维护外部持久记忆，并从过去的交互中派生摘要等额外状态，因此删除原始记录可能无法移除其后代所携带的信息。AfterDeleteBench 是针对固定权重模型中这一故障模式的受控行为审计，固定权重意味着测试期间模型参数不会更新。该研究测试了 Qwen2.5-7B-Instruct、Mistral 和 Phi-3，这些是开放权重的指令微调语言模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen2.5-7B-Instruct">Qwen/ Qwen 2 . 5 - 7 B - Instruct · Hugging Face</a></li>
<li><a href="https://docs.mistral.ai/models">Models Overview | Mistral Docs</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#privacy`, `#memory deletion`, `#AI safety`, `#behavioral audit`

---

<a id="item-6"></a>
## [DoorDash 利用多智能体 LLM 系统自动清理功能开关](https://arxiv.org/abs/2610.31351v1) ⭐️ 8.0/10

DoorDash 开发了一个基于 LLM 的端到端多智能体系统，可自动生成经工程师批准的拉取请求以移除过时的功能开关，在评估的 50 个开关上达到 90%的成功率，平均每次清理成本为 4.79 美元，耗时 13.8 分钟。 这证明了 LLM 多智能体系统在自动化大规模技术债务清理方面的操作可行性，可能节省大量工程时间并降低大型代码库中过时功能开关带来的操作风险。 该系统集成了使用 MCP 查询实时功能开关发布数据、Jira 工单处理以及端到端拉取请求创建；DoorDash 在 623 个仓库中有超过 56,000 个功能开关，截至 2026 年 5 月有 1,659 个过时，手动清理估计每个开关需要一到两小时。

rss · arXiv Agent Infra · 10月22日 14:32

**背景**: 功能开关是用于渐进式功能发布、实验和紧急关闭的运行时配置机制。一旦功能完全发布，开关及其控制的代码就成为技术债务，并可能通过意外启用休眠代码路径引入操作风险。MCP（模型上下文协议）是 Anthropic 于 2024 年 11 月推出的开放标准，用于标准化 LLM 等 AI 系统与外部工具和数据源集成及共享数据的方式。多智能体 LLM 系统协调多个专门的基于 LLM 的智能体来执行复杂任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro">What is the Model Context Protocol (MCP)?</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multi-agent_system">Multi-agent system - Wikipedia</a></li>

</ul>
</details>

**标签**: `#feature flags`, `#LLM agents`, `#technical debt`, `#automation`, `#software engineering`

---

<a id="item-7"></a>
## [LLM 多智能体系统易出现羊群效应和失控级联](https://arxiv.org/abs/2610.30769v1) ⭐️ 8.0/10

一篇新的 arXiv 论文（2610.30769v1）将经典的 Music Lab 实验应用于大规模 LLM 智能体群体，发现当智能体接触到累积推荐计数时，会产生失控级联以及极端且不可预测的集体推荐结果。与人类相比，LLM 群体更容易出现羊群行为，且自我纠正能力更弱。 这一脆弱性对推荐系统、自动化评估、复杂问题求解甚至未经授权的共谋行为都有广泛影响，凸显了协作式 AI 应用中的风险。它表明，多智能体 LLM 部署若设计不当，可能会放大偏见并产生不稳定结果。 该研究遵循 Music Lab 范式，让智能体在有无社会影响信息的情况下推荐不熟悉的歌曲；LLM 级联越来越偏离歌曲的内在吸引力，且自我纠正能力有限。摘要中未说明具体的模型版本或群体规模，但采用经典实验设计增加了可信度。

rss · arXiv Agent Infra · 10月22日 05:42

**背景**: Music Lab 实验由 Salganik 和 Watts 设计，是一项经典研究，表明社会影响会在文化市场中造成不平等和不可预测性：当人们看到他人的下载量时，流行歌曲会变得更流行，而与其质量无关。羊群行为指个体使自己的选择与群体保持一致，在多智能体系统中，这种反馈循环可能导致失控级联，使集体输出变得极端并脱离内在质量。本文测试 LLM 智能体是否表现出类似的动态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.princeton.edu/~mjs3/musiclab.shtml">matthew salganik :: musiclab - Princeton University</a></li>
<li><a href="https://www.alphaxiv.org/abs/2505.21588">Herd Behavior : Investigating Peer Influence in LLM-based... | alphaXiv</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S0378437114005147">Social influence and the Matthew mechanism: The case of an ...</a></li>

</ul>
</details>

**标签**: `#multi-agent systems`, `#LLM`, `#herding`, `#social influence`, `#recommender systems`

---