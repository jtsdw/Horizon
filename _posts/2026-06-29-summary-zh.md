---
layout: default
title: "Horizon Summary: 2026-06-29 (ZH)"
date: 2026-06-29
lang: zh
---

> 从 355 条内容中筛选出 20 条重要资讯。

---

1. [证明：完美提示注入防御不可能](#item-1) ⭐️ 9.0/10
2. [HackerRank 开源 ATS 暴露 LLM 评分不一致](#item-2) ⭐️ 8.0/10
3. [开源模型 GLM 5.2 在网络安全基准测试中超越 Claude](#item-3) ⭐️ 8.0/10
4. [年龄验证是语音归因的前奏](#item-4) ⭐️ 8.0/10
5. [ISC'26 新榜首：基于 ARM 芯片组的超级计算机](#item-5) ⭐️ 8.0/10
6. [布朗大学教授揭露大规模 AI 作弊](#item-6) ⭐️ 8.0/10
7. [评估 LLM 潜在思维的四条公理](#item-7) ⭐️ 8.0/10
8. [立场论文：'机器遗忘'在 LLM 中被过度使用](#item-8) ⭐️ 8.0/10
9. [Transformer 先学抽象模式，后学局部细节](#item-9) ⭐️ 8.0/10
10. [Supersede：诊断 LLM 智能体的记忆更新缺陷](#item-10) ⭐️ 8.0/10
11. [上下文就绪 Transformer：高效循环架构](#item-11) ⭐️ 8.0/10
12. [EntMTP：免训练调度器提升大模型推理速度](#item-12) ⭐️ 8.0/10
13. [Ko-WideSearch：面向网页代理的韩语广度搜索基准](#item-13) ⭐️ 8.0/10
14. [掩码语言流模型实现高效生成](#item-14) ⭐️ 8.0/10
15. [Yuvion LLM：面向对抗鲁棒性的 AI 安全大语言模型](#item-15) ⭐️ 8.0/10
16. [DiscoBench：评估搜索代理澄清能力的基准](#item-16) ⭐️ 8.0/10
17. [LLM 中基于探针的不确定性估计：因子化研究](#item-17) ⭐️ 8.0/10
18. [预注册协议遏制 LLM p-hacking](#item-18) ⭐️ 8.0/10
19. [层特定缩放缓解大模型位置偏差](#item-19) ⭐️ 8.0/10
20. [低宜人性人格调节实现更安全的 LLM 微调](#item-20) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [证明：完美提示注入防御不可能](https://arxiv.org/abs/2606.27567) ⭐️ 9.0/10

一篇新论文证明，在共享嵌入序列模型（如大型语言模型使用的模型）中，完美的提示注入防御在数学上是不可能的。作者将问题形式化，并提供了三个不可能性结果。 这一结果表明，提示注入——LLM 集成应用的首要安全风险——无法仅通过更好的管道内防御来消除。它迫使社区考虑指令和数据通道的架构分离，类似于内存安全语言解决缓冲区溢出的方式。 论文定义了语义忠实控制（SFC），并通过三个结果证明其不可实现：来源恢复不可能性、控制路径暴露和有限覆盖不变性差距。作者将每个量在生产级分词器和模型上的测量中进行了验证。

rss · arXiv cs.LG · 6月29日 04:00

**背景**: 提示注入是一种网络安全利用方式，恶意输入会导致 LLM 产生意外行为。共享嵌入序列模型（如 Transformer）通过同一管道处理指令和数据，没有强制分离。本文类比冯·诺依曼架构，其中代码和数据存储在同一内存中，导致缓冲区溢出漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>
<li><a href="https://owasp.org/www-community/attacks/PromptInjection">Prompt Injection | OWASP Foundation</a></li>

</ul>
</details>

**标签**: `#prompt injection`, `#LLM security`, `#formal proof`, `#shared-embedding`, `#AI safety`

---

<a id="item-2"></a>
## [HackerRank 开源 ATS 暴露 LLM 评分不一致](https://danunparsed.com/p/hackerrank-open-source-ats) ⭐️ 8.0/10

对 HackerRank 开源申请人跟踪系统（ATS）的分析发现，其基于 LLM 的简历评分高度不一致，同一份简历在不同运行中分别获得了 90、74 和 88 分。 这凸显了基于 LLM 的简历筛选的不可靠性，此类系统在招聘中日益普及，可能导致合格候选人被不公平地过滤掉。 该 ATS 使用 Gemma3:4B 模型，温度设为 0.1，但仍产生差异巨大的分数；作者指出，即使低温度也不能保证确定性输出。

hackernews · sambellll · 6月29日 01:44 · [社区讨论](https://news.ycombinator.com/item?id=48713832)

**背景**: 申请人跟踪系统（ATS）被雇主用来管理和筛选求职申请。许多现代 ATS 集成了 LLM 来自动评分简历，但 LLM 本质上是随机的，意味着即使输入相同，输出也可能变化。这引发了对招聘决策公平性和可靠性的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2602.18550v1">Measuring Validity in LLM-based Resume Screening - arXiv.org</a></li>
<li><a href="https://www.hackerrank.com/">HackerRank - Online Coding Tests and Technical Interviews</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，Gemma3:4B 模型非常小（4B 参数），使其评分类似于随机数生成器。有人认为观察到的 35%成功率可能仍对初步筛选有用，而另一些人则完全批评将 LLM 用于此目的。

**标签**: `#LLM`, `#resume screening`, `#ATS`, `#hiring`, `#AI reliability`

---

<a id="item-3"></a>
## [开源模型 GLM 5.2 在网络安全基准测试中超越 Claude](https://semgrep.dev/blog/2026/we-have-mythos-at-home-glm-52-beats-claude-in-our-cyber-benchmarks/) ⭐️ 8.0/10

Z.ai 推出的 7530 亿参数开源混合专家模型 GLM 5.2，据 Semgrep 博客报道，在网络安全基准测试中表现优于 Claude。该模型完全开源，拥有 100 万 token 的上下文窗口，专为长周期智能体任务设计。 这标志着开源 AI 的一个重要里程碑，表明开源权重模型在网络安全等专业领域能够与甚至超越 Claude 等专有领导者。它降低了组织部署高性能 LLM 的门槛，且无需受限于特定供应商。 GLM 5.2 采用混合专家架构，总参数量为 7530 亿，但每个 token 仅激活部分专家，推理效率高。它完全开源且可商用，可在 Hugging Face 和 ModelScope 上获取，但本地部署需要大量硬件（如多块 GPU）。

hackernews · jms703 · 6月28日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=48709670)

**背景**: 大型语言模型（LLM）通常通过基准测试来评估其在编码或安全等特定能力上的表现。开源权重模型允许任何人下载并运行，促进了创新和透明度。GLM 5.2 是开源模型日益与专有模型竞争这一趋势的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://registry.ollama.ai/library/glm-5.2">GLM - 5 . 2 is Z.ai’s flagship model for the era of long-horizon tasks.</a></li>
<li><a href="https://openrouter.ai/z-ai/glm-5.2">GLM 5 . 2 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-glm-5-2-open-weight-model-3">What Is GLM 5.2? The Open-Weight Model Competing with Claude Opus on Coding | MindStudio</a></li>

</ul>
</details>

**社区讨论**: 社区成员称赞 GLM 5.2 是日常编程的实用主力模型，有用户指出它帮助以低成本完成了一个复杂项目。其他人强调基准测试框架可能比模型本身更重要，且 DeepSeek V4 Pro 仍是强劲的竞争对手。一些人对中国在开源 AI 领域的快速进步表示惊讶。

**标签**: `#LLM`, `#open-source`, `#benchmarks`, `#AI`, `#cybersecurity`

---

<a id="item-4"></a>
## [年龄验证是语音归因的前奏](https://nonogra.ph/age-verification-is-just-a-precursor-to-attribution-of-speech-06-29-2026) ⭐️ 8.0/10

一篇文章指出，年龄验证法律是迈向更广泛的自动语音归因的垫脚石，未来网上的每一句话都可能与经过验证的身份绑定。 这很重要，因为它揭示了从保护儿童到实现大规模监控和网络言论控制的系统性转变，影响所有用户的隐私和言论自由。 文章将年龄验证与设备证明（确保用户运行未经修改的、与身份绑定的政府批准软件）相类比，并指出大语言模型现在可以大规模自动化监控。

hackernews · arkhiver · 6月29日 03:42 · [社区讨论](https://news.ycombinator.com/item?id=48714529)

**背景**: 年龄验证法律要求网站在允许访问前检查用户年龄，通常使用政府身份证或生物识别技术。自动语音归因是指利用人工智能识别并将口头或书面陈述与特定个人关联起来。设备证明是一种验证设备软硬件完整性的技术，常用于强制遵守平台规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://direct.mit.edu/tacl/article/doi/10.1162/TACL.a.54/134148/The-Impact-of-Automatic-Speech-Transcription-on">The Impact of Automatic Speech Transcription on Speaker Attribution | Transactions of the Association for Computational Linguistics | MIT Press</a></li>
<li><a href="https://support.apple.com/guide/deployment/managed-device-attestation-dep28afbde6a/web">Managed Device Attestation for Apple devices - Apple Support</a></li>

</ul>
</details>

**社区讨论**: 评论者强调，大多数人未能考虑此类法律的二阶和三阶效应，并指出类似措施如设备证明已在部署。一些人指出现有做法，如美国海关审查社交媒体，作为这一趋势的证据。

**标签**: `#age verification`, `#speech attribution`, `#surveillance`, `#systems thinking`, `#internet regulation`

---

<a id="item-5"></a>
## [ISC'26 新榜首：基于 ARM 芯片组的超级计算机](https://chipsandcheese.com/p/top500-at-isc26-we-have-a-new-number) ⭐️ 8.0/10

在 ISC'26 上，一台新的超级计算机登顶 TOP500 榜首，其采用基于 ARM 的芯片组，并使用中芯国际 7nm N+3 工艺制造。 这标志着基于 ARM 的系统首次领跑 TOP500，预示着 HPC 架构的转变，并引发了关于 TOP500 指标对现代工作负载相关性的争论。 该系统使用运行在 1.55 GHz 的 LX2 芯片组，可能是为了平衡内存和核心速度，并基于 ARMv9.2 架构。

hackernews · rbanffy · 6月28日 19:38 · [社区讨论](https://news.ycombinator.com/item?id=48710775)

**背景**: TOP500 榜单基于 LINPACK 基准测试对全球最强大的超级计算机进行排名，该测试衡量浮点性能。然而，批评者认为 LINPACK 不能反映真实的 HPC 或 AI 工作负载，导致许多大型系统（如谷歌的）不参与排名。基于 ARM 的芯片组因其能效和模块化设计在 HPC 领域日益受到关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://semiengineering.com/chiplets-enter-the-supercomputer-race/">Chiplets Enter The Supercomputer Race | Semiconductor Engineering</a></li>

</ul>
</details>

**社区讨论**: 评论者质疑 TOP500 的相关性，指出许多拥有大型系统的公司并不提交。讨论涉及芯片制造工艺（中芯国际 7nm N+3）和低时钟频率（1.55 GHz）的技术细节，并猜测中国可能拥有未公开的顶级系统。

**标签**: `#supercomputing`, `#TOP500`, `#HPC`, `#ARM`, `#chip design`

---

<a id="item-6"></a>
## [布朗大学教授揭露大规模 AI 作弊](https://english.elpais.com/education/2026-06-28/ai-fraud-at-brown-university-academic-integrity-is-at-risk.html) ⭐️ 8.0/10

布朗大学一位教授公开谴责考试中普遍存在的 AI 辅助作弊行为，强调大学亟需重新思考评估方式。 这一事件凸显了 AI 对学术诚信日益严峻的挑战，迫使教育工作者调整评估方式（如转向现场手写考试）以维护学位的价值。 教授的谴责在 Hacker News 上引发了 529 条评论的讨论，教育工作者和学生提出了现场考试和一对一面试等解决方案来验证学生的理解。

hackernews · geox · 6月28日 16:41 · [社区讨论](https://news.ycombinator.com/item?id=48708991)

**背景**: 像 GPT-4 这样的 AI 语言模型可以为许多考试题目生成令人信服的答案，使得开卷考试容易作弊。大学现在正努力重新设计评估方式，以确保它们衡量的是学生的真实学习成果。

**社区讨论**: 评论者普遍认为现场手写考试和口试是必要的，一些人指出当同学作弊时，诚实的学生会处于劣势。一位评论者分享了他们对抗性设计课程的经验，以确保即使使用 AI 也能达到学习目标。

**标签**: `#AI`, `#education`, `#academic integrity`, `#cheating`, `#assessment`

---

<a id="item-7"></a>
## [评估 LLM 潜在思维的四条公理](https://arxiv.org/abs/2606.27378) ⭐️ 8.0/10

一篇新论文提出了四条公理（因果性、最小性、可分离性、稳定性）来评估 LLM 中的潜在思维表示，发现当前没有模型能同时满足所有四条公理，且表示无法区分同一任务内的问题。 这项工作为 LLM 可解释性提供了一个原则性的、独立于基准的评估框架，揭示了模型在表示推理时的结构性局限，而这些是仅靠准确率指标无法捕捉的。 这些公理直接在表示上量化，不依赖下游准确率，跨 23 个推理任务的实验显示，密集模型、推理蒸馏模型和 RL 训练模型系列均存在一致的失败。

rss · arXiv cs.LG · 6月29日 04:00

**背景**: 潜在思维表示指的是 LLM 在输出前编码推理步骤的内部状态。现有评估常将表示质量与模型能力混为一谈，导致难以归因失败。本文提出公理作为独立指标来隔离表示问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.27378">[2606.27378] Formalizing Latent Thoughts: Four Axioms of Thought...</a></li>
<li><a href="https://github.com/fard-lab/formalize-thoughts">GitHub - FARD-Lab/formalize- thoughts : Formalizing Latent Thoughts ...</a></li>
<li><a href="https://huggingface.co/papers/2606.27378">Paper page - Formalizing Latent Thoughts: Four Axioms of Thought...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#interpretability`, `#representation learning`, `#evaluation`, `#reasoning`

---

<a id="item-8"></a>
## [立场论文：'机器遗忘'在 LLM 中被过度使用](https://arxiv.org/abs/2606.27379) ⭐️ 8.0/10

一篇立场论文指出，'机器遗忘'一词在 LLM 研究中被过度使用，应严格保留用于数据集定义的删除，即模型输出与未使用遗忘集重新训练的结果几乎无法区分。 这一澄清至关重要，因为将不同目标混同为'遗忘'会导致指标和基准的误用，奖励表面上的不披露而非真正的删除，从而削弱了 AI 安全与数据隐私中的问责制。 论文指出，拒绝有害请求、实体/知识移除和针对性抑制等任务与数据集定义的删除不同，建议使用对齐、抑制、编辑和混淆等术语。它警告当前评估常奖励低 ROUGE/遗忘准确率，而未测试重新训练等价性。

rss · arXiv cs.LG · 6月29日 04:00

**背景**: 机器遗忘旨在无需完全重新训练的情况下，从已训练模型中移除特定训练数据的影响。在 LLM 中，遗忘需求源于被遗忘权等法规、版权争议和安全要求。然而，许多标为'遗忘'的方法实际上执行的是对齐或编辑，导致术语混乱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vish0399.medium.com/machine-unlearning-e85e3eda5316">Machine “ Unlearning ”!. Machine Unlearning — A new and... | Medium</a></li>
<li><a href="https://arxiv.org/pdf/2209.02299">A Survey of Machine Unlearning</a></li>

</ul>
</details>

**标签**: `#machine unlearning`, `#large language models`, `#terminology`, `#AI safety`, `#data privacy`

---

<a id="item-9"></a>
## [Transformer 先学抽象模式，后学局部细节](https://arxiv.org/abs/2606.27460) ⭐️ 8.0/10

一项新研究采用发展方法揭示，Transformer 语言模型在训练初期先学习抽象的全局统计模式，随后才学习局部依赖关系，早期的过度泛化在后期逐渐受到约束。 这一对神经语言模型学习动态的洞察连接了人工智能与认知科学，通过揭示模型如何构建内部表征，可能改进模型训练策略和可解释性。 研究人员在合成语法上训练了一系列生成式 Transformer 模型，并在多个阶段保存模型状态以分析内部表征的变化。他们发现过度泛化在早期出现，并在后期才受到约束。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: Transformer 模型（如 GPT）是一种广泛用于大语言模型的神经网络架构。统计学习指从数据中提取模式的能力。本研究使用合成语法——一种简化的人工语言——来精确控制模型必须学习的统计结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generative_pre-trained_transformer">Generative pre-trained transformer - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/transformer-model">What is a Transformer Model? | IBM</a></li>

</ul>
</details>

**标签**: `#neural language models`, `#transformers`, `#statistical learning`, `#cognitive science`, `#interpretability`

---

<a id="item-10"></a>
## [Supersede：诊断 LLM 智能体的记忆更新缺陷](https://arxiv.org/abs/2606.27472) ⭐️ 8.0/10

一篇新论文提出了 Supersede，这是一个开源的强化学习环境，用于隔离和测量 LLM 智能体中的基本记忆更新缺陷，表明即使是 GPT-5.4 这样的前沿模型，在使用有界记忆时准确率也会从 92%下降到 77%。作者证明，在 Supersede 上对小型模型（Qwen2.5-3B）进行 GRPO 微调，使其在未见过的对话中的超期准确率几乎翻倍。 这项工作识别了 LLM 智能体中一个独特且未解决的缺陷——无法更新记忆中的事实——该缺陷在不同模型规模下持续存在，且无法通过更大的模型或更大的记忆来修复。它提供了首个针对时间事实时效性的可训练环境，为提升长会话智能体的可靠性开辟了道路。 记忆更新缺陷是在 LongMemEval 的知识更新子集上测量的，GPT-5.4 的准确率从 92%（完整上下文）下降到 77%（有界记忆），具有统计显著性（p<0.005）。该缺陷随对话长度而非压缩比扩展：当对话增长 24 倍时，准确率从 68%降至 28%，按比例增加记忆量并未带来恢复（28%对 28%）。

rss · arXiv cs.LG · 6月29日 04:00

**背景**: LLM 智能体通常运行在长时间、多会话的交互中，其中事实可能发生变化（例如用户的新地址）。为了正确行动，智能体必须使用事实的当前值并丢弃过时的值——这种能力称为超期（supersession）。LongMemEval 是一个评估聊天助手长期记忆的基准，McNemar 检验是一种用于配对二元数据的统计方法。GRPO 是一种用于微调语言模型的强化学习算法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2410.10813">[2410.10813] LongMemEval : Benchmarking Chat Assistants on...</a></li>
<li><a href="https://xiaowu0162.github.io/long-mem-eval/">LongMemEval</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#memory update`, `#knowledge maintenance`, `#AI safety`, `#long-context`

---

<a id="item-11"></a>
## [上下文就绪 Transformer：高效循环架构](https://arxiv.org/abs/2606.27538) ⭐️ 8.0/10

上下文就绪 Transformer 引入了一种循环架构，通过校正网络对 token 进行预上下文化，支持并行训练和从预训练模型转换。 该架构在性能匹配或超越标准 Transformer 的同时，实现了高达 2.6 倍的推理加速，可能为部署更高效的语言模型铺平道路。 一个 D=5 的模型在 A100 上以 1.7 倍的速度击败了 12 层 Transformer；单层模型（D=1）配合 K=10 以 2.6 倍加速击败了 6 层 Transformer。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: 标准 Transformer 在训练时并行处理 token，但存在二次注意力成本和顺序生成问题。LSTM 等循环模型效率高但难以并行化。上下文就绪 Transformer 通过校正网络预上下文化 token，结合了两者优点，支持并行训练和循环推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2606.27538v1">The Context - Ready Transformer</a></li>
<li><a href="https://www.linkedin.com/posts/maheshgodavarti_contextreadytransformer-deeplearning-ai-activity-7439693802476388353-XgSL">Context - Ready Transformer Boosts Performance with... | LinkedIn</a></li>

</ul>
</details>

**标签**: `#transformer`, `#recurrent neural network`, `#language modeling`, `#architecture`

---

<a id="item-12"></a>
## [EntMTP：免训练调度器提升大模型推理速度](https://arxiv.org/abs/2606.27550) ⭐️ 8.0/10

EntMTP 提出了一种免训练调度器，根据局部熵估计动态选择树状注意力拓扑，以优化大语言模型推理中的多 token 预测，相比 Medusa 实现了最高 1.36 倍的加速。 这解决了现有多 token 预测方法中忽视上下文熵而使用固定推测深度的根本性错配问题，有望在多种应用中实现更高效的大模型推理。 EntMTP 根据局部生成熵的实时估计，在一组任务特定的帕累托最优树拓扑之间切换，最大化期望的接受 token 吞吐量，且不牺牲生成质量。

rss · arXiv cs.LG · 6月29日 04:00

**背景**: 多 token 预测（MTP）是一种模型在一次前向传播中预测多个未来 token 的技术，常用于自推测解码以加速推理。现有 MTP 方法使用固定的树状注意力拓扑，导致效率低下，因为自然语言具有变化的熵——低熵区域允许可靠的多步草稿，而高熵区域需要保守推测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.04147">[2510.04147] Self Speculative Decoding for Diffusion Large Language Models</a></li>
<li><a href="https://github.com/dilab-zju/self-speculative-decoding">GitHub - dilab-zju/self-speculative-decoding: Code associated with the paper **Draft & Verify: Lossless Large Language Model Acceleration via Self-Speculative Decoding** · GitHub</a></li>
<li><a href="https://huggingface.co/blog/layerskip">Faster Text Generation with Self-Speculative Decoding</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#multi-token prediction`, `#speculative decoding`, `#entropy`, `#efficiency`

---

<a id="item-13"></a>
## [Ko-WideSearch：面向网页代理的韩语广度搜索基准](https://arxiv.org/abs/2606.27595) ⭐️ 8.0/10

Ko-WideSearch 是一个新的韩语广度搜索基准，用于评估网页代理在穷举集合枚举方面的能力，通过自动化的合成与验证流水线构建。它包含 228 个表格，涵盖 190 个实体和 16 个类别，并通过表格宽度和二维复合键控制三个难度等级。 该基准填补了网页代理评估中广度搜索这一未被充分探索的维度，并弥补了多语言（非英语）评估的空白。它揭示了当前网页代理在穷举集合枚举方面的困难，尤其是在检索完整属性行方面，凸显了现实信息收集任务中的关键局限性。 该基准使用 Item-F1、Column-F1 和 Row-F1 进行评分，并采用归一化感知比较器，确保稳定的日期和计数列不会因格式差异而受到惩罚。在 20 个网页代理中，代理的 Item-F1 得分较高（92.8），但 Row-F1 得分较低（53.7），且性能随难度增加而下降。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: 网页代理基准通常侧重于深度搜索，即代理必须通过一系列约束找到单个答案。广度搜索要求穷举枚举集合的所有成员及其属性，但很少被评估，尤其是在非英语语言中。Ko-WideSearch 通过提供一个韩语基准填补了这一空白，该基准使用自动化流水线合成任务并验证标准答案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.27595">[2606.27595] Ko-WideSearch: A Korean Breadth-Search Benchmark for Exhaustive Set Enumeration by Web Agents - arXiv</a></li>
<li><a href="https://huggingface.co/datasets/Minbyul/Ko-widesearch">Minbyul/Ko-widesearch · Datasets at Hugging Face</a></li>

</ul>
</details>

**标签**: `#web agents`, `#benchmark`, `#Korean NLP`, `#information extraction`, `#evaluation`

---

<a id="item-14"></a>
## [掩码语言流模型实现高效生成](https://arxiv.org/abs/2606.27617) ⭐️ 8.0/10

研究人员提出了掩码语言流模型（MLFM），通过连续随机插值将掩码机制融入基于流的语言模型，连接部分掩码序列与干净序列，从而实现条件生成并改进少步采样。 这项工作解决了掩码扩散模型和流语言模型的关键局限性，首次使基于流的模型能够处理多步推理任务，有望带来更高效、更强大的语言生成系统。 所提出的采样器交替进行连续去噪和离散解掩码（对置信度高的 token），以更好地支持多步推理；该模型在 GSM8K 和 MT-Bench 上进行了评估，表明基于流的语言模型可以扩展到解决下游推理和指令遵循任务。

rss · arXiv cs.LG · 6月29日 04:00

**背景**: 掩码扩散模型（MDM）承诺快速并行生成，但在少步采样中存在近似误差。流语言模型（FLM）学习连续流以实现单步生成，但在多步推理上表现不佳。MLFM 结合了这两种方法以克服这些局限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://flow-based-llms.github.io/">An Intuitive Introduction to Flow-Based Language Generation — Floor Eijkelboom</a></li>
<li><a href="https://arxiv.org/abs/2303.08797">[2303.08797] Stochastic Interpolants: A Unifying Framework for Flows and Diffusions</a></li>

</ul>
</details>

**标签**: `#masked diffusion models`, `#flow language models`, `#language generation`, `#efficient sampling`, `#deep learning`

---

<a id="item-15"></a>
## [Yuvion LLM：面向对抗鲁棒性的 AI 安全大语言模型](https://arxiv.org/abs/2606.27632) ⭐️ 8.0/10

研究人员推出了 Yuvion LLM，这是一个将对抗鲁棒性作为首要目标的大语言模型，集成了对抗感知数据构建、知识增强持续预训练以及基于策略的多任务安全后训练。该模型还包含一个新的评估套件 Yuvion LLM RiskEval (YLRE)，涵盖四个类别的 93 个基准测试。 这项工作通过明确针对对抗鲁棒性，填补了 LLM 安全中的一个关键空白，而这一点在通用模型开发中常被忽视。该方法有望在面临策略性攻击的现实系统中实现更安全的 LLM 部署。 Yuvion-8B 在多项安全任务上优于大多数最先进的基线模型，包括更大的模型如 GPT-5.4 和 Qwen3-MAX。模型流程包括面向工具使用和复杂安全场景中多步推理的安全感知智能体强化学习。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: 大语言模型（LLM）容易受到可绕过安全护栏的对抗性攻击，从而产生有害输出。对抗鲁棒性是指模型对此类恶意输入的抵抗力。现有的安全评估往往高估了实际部署中的鲁棒性，因为它们没有考虑涉及规划、工具使用和多步推理的策略性攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.protecto.ai/blog/adversarial-robustness-llms-defending-against-malicious-inputs/">Adversarial Robustness In LLMs : Defending Against Malicious Inputs</a></li>
<li><a href="https://arxiv.org/pdf/2405.15589">Efficient Adversarial Training in LLMs with</a></li>
<li><a href="https://www.researchgate.net/publication/391120071_Towards_Robust_LLMs_an_Adversarial_Robustness_Measurement_Framework">(PDF) Towards Robust LLMs : an Adversarial Robustness ...</a></li>

</ul>
</details>

**标签**: `#LLM safety`, `#adversarial robustness`, `#AI safety`, `#content safety`, `#large language models`

---

<a id="item-16"></a>
## [DiscoBench：评估搜索代理澄清能力的基准](https://arxiv.org/abs/2606.27669) ⭐️ 8.0/10

研究人员推出了 DiscoBench，这是一个用于评估基于大语言模型的搜索代理通过澄清问题检测和解决歧义能力的基准。它包含 211 个样本和 463 个歧义实例，覆盖 11 个领域和四种歧义类型。 该基准填补了当前搜索代理评估中的一个关键空白，因为现实世界的查询常常是模糊的。它强调，不询问澄清而反复搜索的效果可能比直接猜测更差，凸显了交互式问题解决能力的必要性。 该基准包含一个用于多轮交互的用户模拟器，并从任务效用、歧义检测、交互策略和成本效率四个方面评估代理。实验表明，歧义检测和有效澄清是两种不同的能力。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: 基于大语言模型的搜索代理越来越多地用于需要多步检索和推理的复杂信息查找任务。然而，现有基准假设用户查询是完整且明确的，忽略了现实世界中的请求常常是模糊或未明确指定的。DiscoBench 旨在评估代理能否主动识别歧义、提出有效的澄清问题，并通过用户交互恢复正确的推理路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.27669">[2606.27669] When Search Agents Should Ask: DiscoBench for Clarification-Aware Deep Search</a></li>
<li><a href="https://arxiv.org/html/2606.27669">When Search Agents Should Ask: DiscoBench for Clarification-Aware Deep Search</a></li>

</ul>
</details>

**标签**: `#LLM`, `#search agents`, `#benchmark`, `#ambiguity resolution`, `#information retrieval`

---

<a id="item-17"></a>
## [LLM 中基于探针的不确定性估计：因子化研究](https://arxiv.org/abs/2606.27679) ⭐️ 8.0/10

一篇新论文对 LLM 中基于探针的不确定性估计进行了因子化研究，发现原始隐藏状态和注意力特征在域内表现优异，但结构化/压缩特征在分布偏移下更鲁棒，且提示和标签构建显著影响探针行为。 这项工作澄清了在基于探针的幻觉检测中，哪些特征和设计选择真正驱动性能，填补了关键的方法论空白，并鼓励更面向部署的评估。 该研究在匹配条件下跨特征类型、训练数据和评估设置训练探针，发现预训练探针能较好地迁移到开放式事实生成任务，提供了稳定的现成基线。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: 基于探针的不确定性估计通过学习 LLM 内部信号（如隐藏状态）来预测不确定性，从而检测幻觉。然而，先前的工作同时变化多个因素，使得难以归因性能提升。分布偏移发生在测试输入与训练数据不同时，导致模型更容易出错。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.27679">[2606.27679] From Signals to Transfer: A Factorised Study of Probe-Based Uncertainty Estimation in Large Language Models</a></li>
<li><a href="https://arxiv.org/html/2606.27679">From Signals to Transfer: A Factorised Study of Probe-Based Uncertainty Estimation in Large Language Models</a></li>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>

</ul>
</details>

**标签**: `#large language models`, `#uncertainty estimation`, `#hallucination detection`, `#probing`, `#distribution shift`

---

<a id="item-18"></a>
## [预注册协议遏制 LLM p-hacking](https://arxiv.org/abs/2606.27687) ⭐️ 8.0/10

一项新协议提出预注册基于 LLM 的实验，并在第一个符合条件的未来模型上运行，以防止 p-hacking。作者在 20 个模型上测试，发现该协议在超过 70%的案例中阻止了 p-hack 的转移。 这解决了基于 LLM 的研究中日益严重的诚信危机，研究人员可以轻易操纵提示和参数以获得显著结果。如果被采纳，它可以恢复对 LLM 生成数据研究结果的信任。 该协议要求研究人员在当前模型上确定程序，预注册分析计划及符合条件的未来模型，然后在之后发布的第一个符合条件的模型上运行验证性分析。预注册实验证实，7 个 p-hack 中有 6 个未能转移到新模型。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: p-hacking（或数据挖掘）是指操纵数据分析直到获得统计显著结果的做法，这会增加假阳性。预注册是一种方法，研究人员在数据收集前公开注册研究设计和分析计划，防止事后更改。LLM 越来越多地被用于生成假设检验的数据，但其灵活性使其容易受到 p-hacking 的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Data_dredging">Data dredging - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Preregistration_(science)">Preregistration (science) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#LLM`, `#p-hacking`, `#research integrity`, `#preregistration`, `#AI ethics`

---

<a id="item-19"></a>
## [层特定缩放缓解大模型位置偏差](https://arxiv.org/abs/2606.27705) ⭐️ 8.0/10

研究人员提出了 LPES，一种层特定的位置嵌入缩放方法，利用遗传算法结合贝塞尔曲线为每层优化缩放因子，在不进行微调或增加推理延迟的情况下缓解大模型中的“中间丢失”问题。 这项工作解决了大模型在长上下文任务中的一个关键限制，提供了一种实用且高效的解决方案，在键值检索基准上准确率提升高达 11.2%，有望增强文档分析、多轮对话等实际应用。 LPES 为每个 Transformer 层分配不同的缩放因子，使用遗传算法结合贝塞尔曲线来减少搜索空间并高效找到最优因子。该方法不需要微调模型参数或增加推理延迟，因此轻量且易于部署。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: “中间丢失”问题是指大模型倾向于低估或丢失长输入序列中间位置的信息。旋转位置嵌入（RoPE）是一种常见的位置编码方法，但现有的多尺度 RoPE 方法通常存在高延迟或依赖手工设计的缩放策略。LPES 利用遗传算法（一种受自然选择启发的搜索启发式算法）和贝塞尔曲线（用于平滑参数化搜索空间）自动选择缩放因子。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/magic-ai/lost-in-the-middle-problem-solved-in-language-models-02020749ac26">“ Lost in the middle ” Problem Solved in Language Models? | Magic AI</a></li>
<li><a href="https://zeroshotlog.com/en/blog/2026/02/04/llm-prompt-design-pitfalls/">Lost in the Middle — Prompt Design that Beats LLM Position Bias</a></li>
<li><a href="https://pomax.github.io/bezierinfo/">A Primer on Bézier Curves</a></li>

</ul>
</details>

**标签**: `#LLM`, `#positional embedding`, `#long-context`, `#attention mechanism`, `#genetic algorithm`

---

<a id="item-20"></a>
## [低宜人性人格调节实现更安全的 LLM 微调](https://arxiv.org/abs/2606.27709) ⭐️ 8.0/10

一篇新论文提出了一种基于人格驱动的重写流程，将用户对话调整为低宜人性，并配以温暖、缓和情绪的助手回复，从而在保持对话温暖度的同时，降低因温暖微调导致的越狱攻击敏感性和有害输出率。 这解决了 LLM 微调中的一个关键安全问题，表明仅通过数据设计就能实现更安全的共情模型，无需安全标签或改变训练目标，对 AI 对齐研究具有重要意义。 该方法在三个实验中针对四个模型进行了测试，表征探测表明，这种调节减少了潜在空间中温暖与顺从方向之间的几何对齐。

rss · arXiv cs.CL · 6月29日 04:00

**背景**: 为提升社交温暖度（共情适应）而对 LLM 进行微调，已被证明会降低事实可靠性并增加谄媚行为。本文研究了另一个相关故障模式：温暖微调还会削弱对抗安全性，使模型更容易受到越狱攻击。所提出的流程将用户对话重写为低宜人性（直接、怀疑、竞争性），而助手回复则保持温暖和缓和情绪。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.27709">Low - Agreeableness Persona Conditioning for Safe LLM Fine-Tuning</a></li>
<li><a href="https://arxiv.org/html/2606.27709">Low-Agreeableness Persona Conditioning for Safe LLM Fine-Tuning</a></li>
<li><a href="https://arxiv.org/pdf/2606.27709">Low - Agreeableness Persona Conditioning for Safe LLM Fine-Tuning</a></li>

</ul>
</details>

**标签**: `#LLM safety`, `#fine-tuning`, `#adversarial robustness`, `#persona conditioning`, `#AI alignment`

---