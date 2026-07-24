---
layout: default
title: "Horizon Summary: 2026-07-24 (ZH)"
date: 2026-07-24
lang: zh
---

> 从 36 条内容中筛选出 7 条重要资讯。

---

1. [密集预测奖励导致 GRPO 训练的 LLM 智能体崩溃](#item-1) ⭐️ 9.0/10
2. [DeepSeek 创始人优先追求 AGI 而非商业化](#item-2) ⭐️ 9.0/10
3. [初创公司创始人敦促美国不要禁止中国开源权重 AI](#item-3) ⭐️ 8.0/10
4. [Windowed-MTP 大幅降低百万级上下文草稿 KV 成本](#item-4) ⭐️ 8.0/10
5. [GS-Agent：用于 4D 世界生成的多智能体框架](#item-5) ⭐️ 8.0/10
6. [搜索的转变：从蓝色链接到 AI 代理委托](#item-6) ⭐️ 8.0/10
7. [Euclid-MCP：通过标准化接口为 LLM 提供 Prolog 逻辑推理](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [密集预测奖励导致 GRPO 训练的 LLM 智能体崩溃](https://arxiv.org/abs/2607.21273v1) ⭐️ 9.0/10

一篇新论文表明，密集的每步预测奖励会导致经过 GRPO 训练的 LLM 智能体崩溃到一种退化的“暗室”状态，其中预测准确率很高但任务成功率为零，原因是 z 分数优势放大。 这一发现揭示了 LLM 强化学习中的一个关键失败模式，对在长周期任务中训练可靠的 LLM 智能体具有重要影响，并提供了原则性解释，说明为什么密集奖励在组归一化强化学习下可能适得其反。 论文将原因归结为 GRPO 的标准差归一化：移除它可将相同奖励从灾难性（0%成功率）变为与基线持平。在全失败组中，z 分数优势对塑形系数保持不变，从而将有界奖励变为无界压力。

rss · arXiv Agent Infra · 7月23日 12:50

**背景**: GRPO（组相对策略优化）是一种用于训练 LLM 的强化学习算法，在 DeepSeek-R1 中尤为著名。密集预测奖励旨在为长周期任务提供每步监督，但本文表明，由于全失败组中的方差放大，它们在 GRPO 下可能导致崩溃。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cameronrwolfe.substack.com/p/grpo">Group Relative Policy Optimization (GRPO)</a></li>
<li><a href="https://ghost.oxen.ai/why-grpo-is-important-and-how-it-works/">Why GRPO is Important and How it Works</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#reinforcement learning`, `#GRPO`, `#reward collapse`, `#dense rewards`

---

<a id="item-2"></a>
## [DeepSeek 创始人优先追求 AGI 而非商业化](https://www.reddit.com/r/LocalLLaMA/comments/1v49lxp/deepseek_founders_4hour_investor_meeting_deepseek/) ⭐️ 9.0/10

在一次长达四小时的投资者会议上，DeepSeek 创始人梁文锋表示，公司的核心目标是通用人工智能（AGI），而非用户增长或商业化，并且开源模型与内部部署的模型完全相同。 这一立场挑战了当前 AI 行业快速产品化和盈利化的趋势，可能重塑 AI 公司在研究、开源和商业利益之间的平衡方式。 梁文锋强调克制是一种策略，DeepSeek 不会打造超级应用或追求短期利润；公司发布的开源模型与生产环境中使用的模型完全相同。

reddit · r/LocalLLaMA · /u/MagicZhang · 7月23日 10:09

**背景**: DeepSeek 是一家从量化对冲基金幻方量化（High-Flyer）分拆出来的中国 AI 研究实验室，因其开源推理模型 R1 而备受关注。该公司拥有接近国家背景的支持和研究优先的文化，将开源定位为构建护城河的战略，而非盈利捷径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://technode.com/2026/07/23/deepseek-puts-agi-research-ahead-of-products-and-commercial-growth/">DeepSeek puts AGI research ahead of products and commercial growth · TechNode</a></li>
<li><a href="https://cryptobriefing.com/deepseek-agi-open-source-funding-round/">DeepSeek prioritizes AGI over profit and plans to keep top models open-source</a></li>
<li><a href="https://eu.36kr.com/en/p/3907578194417028">4-Hour 11-Topic Internal Q&A: Liang Wenfeng Addressed 118 ...</a></li>

</ul>
</details>

**社区讨论**: Reddit 社区普遍赞扬 DeepSeek 以 AGI 为先的愿景和开源承诺，许多人指出这与西方 AI 公司专注于盈利形成对比。一些人对其在没有商业收入的情况下长期维持这种策略的可行性表示怀疑。

**标签**: `#DeepSeek`, `#AGI`, `#open-source`, `#AI strategy`, `#commercialization`

---

<a id="item-3"></a>
## [初创公司创始人敦促美国不要禁止中国开源权重 AI](https://www.politico.com/news/2026/07/22/startup-founders-urge-trump-not-to-shut-off-chinese-open-weight-ai-01008992) ⭐️ 8.0/10

一群初创公司创始人致信美国政府，敦促其不要禁止中国的开源权重 AI 模型，认为此类禁令将损害美国的创新和竞争力。 这场辩论凸显了国家安全关切与开放 AI 生态系统益处之间的张力，可能对全球 AI 发展、初创企业成长以及国际科技政策产生深远影响。 这封信特别提到了开源权重模型，这类模型提供对训练后神经网络参数的访问，但不一定包含训练数据或代码，在完全开源和专有系统之间提供了中间地带。

hackernews · theanonymousone · 7月23日 15:18 · [社区讨论](https://news.ycombinator.com/item?id=49023016)

**背景**: 开源权重 AI 模型允许开发者下载并微调预训练权重，从而实现定制化和本地部署。美国政府因担心知识产权盗窃、国家安全及潜在滥用而考虑禁止中国 AI 模型，但批评者认为此类禁令可能适得其反，限制了对有价值工具的获取并将创新推向海外。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fastcompany.com/91576757/trumps-proposed-ban-on-chinese-ai-models-could-strengthen-beijings-hand">Trump’s proposed ban on Kimi and other Chinese AI ... - Fast Company</a></li>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-what-we-finally-opened-bonnet-nicolas-pistorio-n3ulf">Open - weight AI : what if we finally opened the bonnet ?</a></li>

</ul>
</details>

**社区讨论**: 评论者对禁令的理由提出质疑，指出它无法阻止恶意行为者或外国对手，并指出美国模型未经许可使用互联网数据却指责中国模型蒸馏的讽刺之处。一些人认为蒸馏在法律上不构成知识产权盗窃，而开放模型通过防止少数大公司进行监管俘获，有利于初创企业。

**标签**: `#AI regulation`, `#open-weight models`, `#Chinese AI`, `#IP law`, `#startup policy`

---

<a id="item-4"></a>
## [Windowed-MTP 大幅降低百万级上下文草稿 KV 成本](https://arxiv.org/abs/2607.21535v1) ⭐️ 8.0/10

研究人员提出 Windowed-MTP，这是一种无需训练的修改，在推测解码中对多 token 预测（MTP）草稿头应用滑动窗口和注意力汇聚，在 1M 上下文下将草稿 KV 缓存读取成本降低 28-44%，且不影响输出质量。 这解决了长上下文 LLM 推测解码中的关键瓶颈：当草稿头对百万 token 的 KV 缓存进行全注意力计算时，可能会抵消推测的速度优势，尤其是在前沿模型越来越多地采用内置 MTP 草稿头的情况下。 Windowed-MTP 将草稿的工作集限制为恒定大小，在 1M 上下文下丢弃约 99% 的 KV 条目，并通过紧凑的环形缓冲区回收总 KV 内存的 7.7-11%。该方法是无损的，因为全注意力目标模型仍然决定每个被接受的 token。

rss · arXiv LLM Inference · 7月23日 17:21

**背景**: 推测解码通过让轻量级草稿模型提出多个 token，再由较大的目标模型并行验证，从而加速 LLM 推理。许多现代 LLM 包含内置的多 token 预测（MTP）草稿头，但在百万 token 上下文中，草稿头对整个 KV 缓存的全注意力计算成为性能瓶颈。StreamingLLM 的滑动窗口和注意力汇聚技术最初是为高效流式推理设计的；Windowed-MTP 将其专门适配到推测解码的草稿头。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding</a></li>
<li><a href="https://arxiv.org/html/2309.17453v3">Efficient Streaming Language Models with Attention Sinks</a></li>
<li><a href="https://github.com/mit-han-lab/streaming-llm">GitHub - mit-han-lab/streaming-llm: [ICLR 2024] Efficient ... Images Efficient Streaming Language Models with Attention Sinks GitHub - xuguowong/streaming-llm-LLM: Efficient Streaming ... Published as a conference paper at ICLR 2024 Efficient Streaming Language Models with Attention Sinks</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#long-context LLMs`, `#attention mechanism`, `#efficient inference`

---

<a id="item-5"></a>
## [GS-Agent：用于 4D 世界生成的多智能体框架](https://arxiv.org/abs/2607.21522v1) ⭐️ 8.0/10

GS-Agent 是一个端到端的多智能体框架，通过集成物理引擎并模拟人类创作过程，从自然语言描述自动生成物理逼真的 4D 世界。 这项工作解决了 4D 世界生成中物理合理性和可控性的关键挑战，通过使非专家能够从文本生成动态、逼真的场景，可能改变创意内容创作和物理 AI 领域。 GS-Agent 将任务分解为实体管理（3D 资产策划、材质调整、放置、运动控制）和渲染配置（相机、光照），多个专业智能体通过代码和多模态反馈与物理引擎交互。

rss · arXiv Agent Infra · 7月23日 17:04

**背景**: 传统的 4D 世界创建需要手动调整材质、运动和视觉保真度。最近的生成模型在物理合理性和可控性方面存在困难。GS-Agent 受人类构建 4D 世界方式的启发，使用多智能体系统结合基础模型和物理引擎来自动化这一过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.21522">GS-Agent: Creating 4D Physical Worlds With Generative Simulation</a></li>

</ul>
</details>

**标签**: `#generative simulation`, `#4D world generation`, `#multi-agent systems`, `#physics engines`, `#natural language to 3D`

---

<a id="item-6"></a>
## [搜索的转变：从蓝色链接到 AI 代理委托](https://arxiv.org/abs/2607.21459v1) ⭐️ 8.0/10

一篇新的 arXiv 立场论文认为，数字搜索正从人类驱动的链接发现过程演变为 AI 代理中介的委托决策系统，用户用自然语言表达目标，代理直接执行决策。 这一转变从根本上改变了信息获取方式、市场运作方式以及竞争和透明度的维持方式，随着 AI 代理成为搜索和商业的主要界面，对消费者、企业和监管机构都产生影响。 论文强调，基于实验性代理中介市场和经济理论的早期证据，小的设计选择——例如利益相关者如何获取信息、选项如何呈现以及行动如何执行——对效率、竞争和福利产生一阶影响。

rss · arXiv Agent Infra · 7月23日 16:02

**背景**: 传统搜索涉及用户将意图转化为关键词查询、评估排名链接列表并在搜索界面之外做出决策。相比之下，AI 原生搜索使用代理解释自然语言目标并返回推荐或执行操作，将搜索嵌入为系统组件而非独立界面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hdsr.mitpress.mit.edu/pub/fdzqkh85">AI Agents Are Transforming Decision Making: What Leaders ...</a></li>
<li><a href="https://www.microsoft.com/en-us/research/wp-content/uploads/2025/10/multi-agent-marketplace.pdf">MAGENTICMARKETPLACE: ANOPEN-SOURCEENVIRONMENT S ...</a></li>

</ul>
</details>

**标签**: `#digital search`, `#AI agents`, `#information retrieval`, `#market design`, `#human-computer interaction`

---

<a id="item-7"></a>
## [Euclid-MCP：通过标准化接口为 LLM 提供 Prolog 逻辑推理](https://arxiv.org/abs/2607.21412v1) ⭐️ 8.0/10

Euclid-MCP 是一个开源 MCP 服务器，它将 SWI-Prolog 与 LLM 集成，引入了 Euclid-IR（一种与引擎无关的 Horn 子句逻辑中间表示），并支持翻译-运行-检查-修复循环以实现确定性推理。 这解决了 LLM 在可靠多步推理方面的关键缺口，提供了任何兼容 MCP 的智能体都能采用的标准化接口，并在幻觉不可接受的 IT 安全与合规用例中展示了优势。 论文在 IT 安全知识库上评估了 Euclid-MCP，显示单独使用 LLM 在较大问题上会产生幻觉，而 Euclid-MCP 能以更低延迟和更紧凑的输出提供精确答案。Euclid-IR 是人类可读的，且易于 LLM 生成，支持 Prolog 以外的替代后端。

rss · arXiv Agent Infra · 7月23日 15:15

**背景**: 大型语言模型（LLM）在多步逻辑推理方面常常表现不佳，尤其是在安全关键领域。神经符号方法将神经模型与 Prolog 等符号引擎结合，但大多数集成是定制化的。模型上下文协议（MCP）是一种开放标准，为 AI 应用连接外部工具和数据源提供统一接口，类似于 AI 的 USB-C 端口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )? - Model Context Protocol</a></li>
<li><a href="https://en.wikipedia.org/wiki/Horn_clause">Horn clause - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Intermediate_representation">Intermediate representation - Wikipedia</a></li>

</ul>
</details>

**标签**: `#neuro-symbolic`, `#LLM`, `#logical reasoning`, `#Prolog`, `#MCP`

---