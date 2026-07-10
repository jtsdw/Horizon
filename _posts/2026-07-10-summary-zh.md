---
layout: default
title: "Horizon Summary: 2026-07-10 (ZH)"
date: 2026-07-10
lang: zh
---

> 从 37 条内容中筛选出 7 条重要资讯。

---

1. [欧盟议会通过聊天控制 1.0](#item-1) ⭐️ 9.0/10
2. [用 Rust 重写的 Postgres 通过全部回归测试](#item-2) ⭐️ 8.0/10
3. [DominoTree：用于快速 LLM 推理的条件树结构草稿生成](#item-3) ⭐️ 8.0/10
4. [实地研究揭示非 GPU AI 加速器的重大障碍](#item-4) ⭐️ 8.0/10
5. [WebSwarm：用于深度网络搜索的递归多智能体框架](#item-5) ⭐️ 8.0/10
6. [LLM 代理市场模拟研究测试市场稳定机制](#item-6) ⭐️ 8.0/10
7. [TRACE：面向 LLM 智能体轨迹的双通道水印](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [欧盟议会通过聊天控制 1.0](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 9.0/10

2026 年 7 月 7 日，欧洲议会允许临时延长聊天控制 1.0 法规，该法规允许在无嫌疑情况下大规模扫描私人信息，尽管投票的多数议员反对（314 票反对，276 票赞成）。该措施被快速推进并通过，因为否决动议未能获得所需的 361 票绝对多数。 这一决定实际上使在 Instagram、Discord 和 Gmail 等主要平台上进行无嫌疑的大规模私人通信监控合法化，直至 2028 年，削弱了端到端加密和数字隐私权。这为欧盟数字权利树立了一个令人担忧的先例，并可能助长全球范围内类似的监控措施。 该法规适用于 Instagram、Discord、Snapchat、Skype、Xbox、Gmail 和 iCloud 等平台上的直接消息，但不影响公共社交媒体帖子或云存储文件，这些内容此前已可被扫描。投票在暑假前的最后一次会议上进行，有 113 名议员缺席，批评者称这是减少反对票的程序性操作。

hackernews · rapnie · 7月9日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=48843923)

**背景**: 聊天控制，正式名称为儿童性虐待法规（CSAR），于 2022 年首次提出，旨在通过数字平台的强制检测和报告来打击在线儿童性虐待。第一版聊天控制 1.0 是一项临时措施，于 2026 年 3 月到期，但在 2026 年 7 月被恢复并快速推进。批评者认为，用于检测未知儿童性虐待材料的技术错误率很高，且大规模扫描侵犯了基本隐私权和端到端加密。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control_1.0">Chat Control 1.0</a></li>
<li><a href="https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/">EU Parliament greenlights Chat Control 1.0 – Breyer: "Our children lose out"</a></li>
<li><a href="https://cybernews.com/security/chat-control-eu-scanning-messages/">Will the EU start scanning your private messages? | Cybernews</a></li>

</ul>
</details>

**社区讨论**: 评论者对通过该措施的程序性策略表示愤怒，例如在暑假前举行投票并要求绝对多数才能否决。许多人认为这是民主的失败，是迈向极权主义的一步，一些人指出欧盟被用来为不受欢迎的监控法律洗白责任。

**标签**: `#privacy`, `#surveillance`, `#EU legislation`, `#digital rights`, `#encryption`

---

<a id="item-2"></a>
## [用 Rust 重写的 Postgres 通过全部回归测试](https://github.com/malisper/pgrust) ⭐️ 8.0/10

一个名为 pgrust 的项目用 Rust 重写了 PostgreSQL，现已通过 100%的官方 Postgres 回归测试，并在重写过程中使用了 LLM 辅助。 这表明基于 Rust 的数据库可以实现与 PostgreSQL SQL 语义的完全兼容，有望在利用 LLM 等现代工具进行快速开发的同时，构建更安全、更高性能的数据库系统。 该项目在不到一个月内生成了超过 7100 次提交，全部由 LLM 完成，这引发了关于代码审查和可维护性的问题。作者目前正在开发一个融入现代数据库技术的新版本。

hackernews · SweetSoftPillow · 7月9日 06:18 · [社区讨论](https://news.ycombinator.com/item?id=48841676)

**背景**: PostgreSQL 是一个有 30 年历史的关系型数据库，拥有全面的回归测试套件来验证 SQL 实现的正确性。用 Rust 重写旨在提高内存安全性和性能，但由于复杂性和引入错误的风险，此类重写很少见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.postgresql.org/docs/current/regress.html">PostgreSQL: Documentation: 18: Chapter 31. Regression Tests</a></li>

</ul>
</details>

**社区讨论**: 社区意见不一：一些人称赞这一技术成就，并建议镜像查询以比较性能；另一些人则批评项目依赖单一个人、使用 LLM 生成代码以及审查 AI 生成提交的困难。还有人提出了对许可证变更的担忧。

**标签**: `#Postgres`, `#Rust`, `#Database`, `#LLM`, `#Rewrite`

---

<a id="item-3"></a>
## [DominoTree：用于快速 LLM 推理的条件树结构草稿生成](https://arxiv.org/abs/2607.08642v1) ⭐️ 8.0/10

DominoTree 提出了一种无需训练的条件树结构草稿生成方法，用于推测解码，在 Qwen3-4B 上相比自回归解码实现了高达 6.6 倍的加速，每轮平均接受长度达到 10.7 个 token。 该方法在不需额外训练的情况下显著提升了 LLM 推理效率，便于实际部署。它在多个基准测试和温度设置下优于现有的草稿树方法（如 DDTree 和 Domino）。 DominoTree 使用基于 GRU 的因果校正使草稿 token 分布具有路径依赖性，并将每个节点的校正限制在 top-M 候选集中以保证实用性。其 GPU 原生的 CUDA-graph 构建器与参考 Python 实现比特一致，确保接受率不变。

rss · arXiv LLM Inference · 7月9日 16:16

**背景**: 推测解码通过快速草稿模型生成多个 token，并与目标模型并行验证，从而加速 LLM 推理。现有方法如 DFlash 生成草稿块但仅建模每个位置的边缘分布，而最佳优先树方法如 DDTree 从这些边缘分布扩展候选树，但无法表示路径相关的分布。DominoTree 通过沿每条根到节点路径引入条件非因子化校正来解决这一限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2604.12989">[2604.12989] Accelerating Speculative Decoding with Block ... OPT-Tree: Speculative Decoding with Adaptive Draft Tree Structure OPT-Tree: Speculative Decoding with Adaptive Draft Tree ... Accelerating Speculative Decoding with Block Diffusion Draft ... Accelerating Speculative Decoding with Block Diffusion Draft ... OPT-Tree: Speculative Decoding with Adaptive Draft Tree Structure</a></li>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency ...</a></li>
<li><a href="https://arxiv.org/html/2401.07851v2">Unlocking Efficiency in Large Language Model Inference:</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#LLM inference`, `#draft tree`, `#GPU acceleration`

---

<a id="item-4"></a>
## [实地研究揭示非 GPU AI 加速器的重大障碍](https://arxiv.org/abs/2607.08215v1) ⭐️ 8.0/10

一项在 16 设备华为 Ascend 910 系统上部署 MoE 和多模态推理的实地研究发现，要使工作负载可靠运行，需要 12 个源码级补丁、禁用高吞吐特性并添加运维保障措施。 该研究记录了将大模型推理迁移出 CUDA 的实际工程成本，为评估华为 Ascend 等非 GPU 加速器的团队提供了可操作的见解。 该研究识别了八类限制，包括不完整的算子支持、底层内核中的数值错误以及不稳定的高级特性，并提供了详细症状和可能原因。

rss · arXiv LLM Inference · 7月9日 08:12

**背景**: 华为 Ascend 等非 GPU AI 加速器越来越多地被用作 NVIDIA GPU 的替代品，特别是在出口限制下。然而，从 CUDA 迁移到 CANN 和 vLLM-Ascend 等平台通常涉及大量工程工作。这项实地研究首次系统性地记录了这些挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.glennklockwood.com/garden/processors/ascend-910">Ascend 910</a></li>
<li><a href="https://github.com/vllm-project/vllm-ascend">GitHub - vllm-project/vllm-ascend: Community maintained ...</a></li>
<li><a href="https://developer.huawei.com/consumer/en/doc/hiai-Guides/introduction-0000001051486804">About the Service-CANN - HUAWEI Developers</a></li>

</ul>
</details>

**标签**: `#AI accelerators`, `#large model inference`, `#Huawei Ascend`, `#MoE`, `#multimodal`

---

<a id="item-5"></a>
## [WebSwarm：用于深度网络搜索的递归多智能体框架](https://arxiv.org/abs/2607.08662v1) ⭐️ 8.0/10

WebSwarm 提出了一种用于多智能体网络搜索的递归委派框架，该框架在推理过程中动态实例化智能搜索节点，以联合处理任务分解、递归扩展和协作。 这解决了现有单智能体和多智能体搜索系统在深度和覆盖范围上的局限性，为复杂的研究型任务提供了更彻底、更准确的信息检索。 WebSwarm 在 BrowseComp-Plus、WideSearch、DeepWideSearch 和 GISA 等基准测试中优于基线，特别是在深度、广泛和交错任务上。它还跨同质兄弟节点重用过程级经验以提高效率。

rss · arXiv Agent Infra · 7月9日 16:28

**背景**: 传统的基于 LLM 的网络搜索智能体通常使用 ReAct 风格的循环，结合推理和工具使用，但受限于单一轨迹和上下文窗口。多智能体系统通过并行执行提高了覆盖范围，但缺乏递归深度和自适应协作。WebSwarm 引入了递归委派，每个搜索节点可以解决自己的目标或委派子节点，从而实现更深更广的探索。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@DanGiannone/demystifying-ai-agents-react-style-agents-vs-agentic-workflows-cedca7e26471">Demystifying AI Agents: ReAct-Style Agents vs Agentic Workflows</a></li>
<li><a href="https://www.ibm.com/think/topics/react-agent">What is a ReAct Agent? | IBM</a></li>
<li><a href="https://openreview.net/forum?id=bQgaTaN2eG">REDEREF: RECURSIVE DELEGATION AND REFLECTION FOR MULTI-TURN LLM AGENT COLLABORATION WITH DYNAMIC CAPABILITY DISCOVERY | OpenReview</a></li>

</ul>
</details>

**标签**: `#multi-agent systems`, `#web search`, `#LLM agents`, `#task decomposition`, `#recursive orchestration`

---

<a id="item-6"></a>
## [LLM 代理市场模拟研究测试市场稳定机制](https://arxiv.org/abs/2607.08652v1) ⭐️ 8.0/10

研究人员使用 18 个 LLM 代理（DeepSeek-V3）模拟了一个多代理市场，评估在对抗性恶意攻击下维持市场稳定的正式机制，发现调解机制最具韧性。 这项研究涉及人工智能、经济学和多代理系统的关键交叉点，对设计稳健的去中心化系统（如 DAO 或自动化市场）具有潜在影响。 最佳对抗性攻击（v6）将诚实代理的效用降低了 13.3%，但未能使市场崩溃，调解机制即使在持续对抗压力下也能实现恢复。

rss · arXiv Agent Infra · 7月9日 16:21

**背景**: 在多代理系统中，自利代理可能在社交困境中背叛，导致合作崩溃。本研究使用 LLM 代理模拟市场，并测试调解等正式机制以对抗恶意攻击，维持稳定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.08652">[2607.08652] Formal Mechanisms for Market Stability in Self ...</a></li>
<li><a href="https://arxiv.org/html/2607.08652">Formal Mechanisms for Market Stability in Self-Interested ...</a></li>

</ul>
</details>

**标签**: `#multi-agent systems`, `#LLM agents`, `#market stability`, `#adversarial robustness`, `#simulation`

---

<a id="item-7"></a>
## [TRACE：面向 LLM 智能体轨迹的双通道水印](https://arxiv.org/abs/2607.08400v1) ⭐️ 8.0/10

TRACE 提出了一种针对 LLM 智能体轨迹的双通道鲁棒归属水印，通过互补嵌入实现删除和重写鲁棒性，能够抵御对日志拥有完全读写权限的对手。 这是首个无失真、删除后自同步且重写后无条件不变性的智能体水印，解决了此前未解决的对抗威胁模型，增强了 AI 安全性和溯源能力。 TRACE 叠加了一个基于局部内容的选取通道和一个基于日志骨架的计数通道，并证明擦除两个通道会迫使转售商破坏轨迹。在 ToolBench 和 ALFWorld 上，它匹配了无水印的成功率，同时在长周期轨迹上达到接近 z=100 的检测分数。

rss · arXiv Agent Infra · 7月9日 12:25

**背景**: LLM 智能体通过可能重新品牌或替换模型的转售商到达用户，使得溯源归属依赖于轨迹日志。现有水印在完全读写权限下失败，因为删除会使基于位置的密钥失同步，重写会改变内容，因此需要来自内容和位置的互补密钥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2602.18700">[2602.18700] Watermarking LLM Agent Trajectories</a></li>
<li><a href="https://arxiv.org/abs/2605.11036">[2605.11036] Sequential Behavioral Watermarking for LLM Agents</a></li>
<li><a href="https://arxiv.org/abs/2604.08336">[2604.08336] Leveraging Complementary Embeddings for Replay ...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#watermarking`, `#AI safety`, `#provenance`, `#adversarial robustness`

---