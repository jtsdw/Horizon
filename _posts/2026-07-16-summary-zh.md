---
layout: default
title: "Horizon Summary: 2026-07-16 (ZH)"
date: 2026-07-16
lang: zh
---

> 从 45 条内容中筛选出 8 条重要资讯。

---

1. [Hugging Face Transformers v5.14.0 加入 Inkling 多模态模型](#item-1) ⭐️ 9.0/10
2. [LLM 代理在 Lean 中形式化 Shor 算法，攻击 RSA-2048 和 P-256](#item-2) ⭐️ 9.0/10
3. [TensorRT-LLM v1.3.0rc21 弃用 AutoDeploy，列出 DeepSeek 问题](#item-3) ⭐️ 8.0/10
4. [GPT-Red：通过自对弈红队测试提升 AI 鲁棒性](#item-4) ⭐️ 8.0/10
5. [构建 Shippy AI 智能体的经验教训](#item-5) ⭐️ 8.0/10
6. [PhysClaw-0：通过可复用的语言纠正实现机器人自主性](#item-6) ⭐️ 8.0/10
7. [TRACE：面向长周期智能体的回合级奖励分配方法](#item-7) ⭐️ 8.0/10
8. [SkillSec-Eval：LLM 代理技能的生命周期安全评估](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Hugging Face Transformers v5.14.0 加入 Inkling 多模态模型](https://github.com/huggingface/transformers/releases/tag/v5.14.0) ⭐️ 9.0/10

Hugging Face Transformers v5.14.0 加入了 Inkling 多模态模型（总参数 975B，激活参数 41B），权重开放，支持文本、图像和音频输入并生成文本输出。该版本还包括 TIPSv2 模型、性能改进以及 GPTNeoX 和 GPTBigCode 的破坏性变更。 Inkling 是支持音频的最大开放权重多模态模型，代表了开源 AI 研究和可访问性的重要一步。它集成到 Transformers 中，使开发者能够轻松实验和微调以用于各种应用。 Inkling 总参数为 975B，但每次推理仅激活 41B，采用混合专家架构。该模型面向通用用途，包括智能体系统、编程助手和 RAG，并以开放权重发布，用于研究和微调。

github · ArthurZucker · 7月15日 19:02

**背景**: Hugging Face Transformers 是一个广泛使用的开源库，用于自然语言处理和多模态 AI，提供数千个预训练模型。Inkling 由 Thinking Machines Lab 开发，这是一家由前 OpenAI CTO Mira Murati 创立的 AI 初创公司，是其首个生产级模型发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our open-weights model - Thinking Machines Lab</a></li>
<li><a href="https://huggingface.co/blog/thinkingmachines-inkling">Welcome Inkling by Thinking Machines - Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/Thinking_Machines_Lab">Thinking Machines Lab - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区成员对 Inkling 的多模态能力（尤其是音频支持）感到兴奋，并分享通过 llama.cpp 和 Unsloth 进行本地部署的资源。一些人希望 Thinking Machines 能成为美国领先的开放权重 AI 实验室，而另一些人则质疑该模型与现有模型相比的微调性能。

**标签**: `#transformers`, `#multimodal`, `#open-source`, `#AI`, `#model-release`

---

<a id="item-2"></a>
## [LLM 代理在 Lean 中形式化 Shor 算法，攻击 RSA-2048 和 P-256](https://arxiv.org/abs/2607.14082v1) ⭐️ 9.0/10

研究人员利用基于 LLM 的代理系统在 Lean 定理证明器中形式化了 Shor 算法，生成了针对 RSA-2048 和椭圆曲线 P-256 的量子攻击的机器验证证明。 这项工作展示了 AI 辅助形式化验证与量子密码分析的新颖结合，可能加速经过验证的量子算法的开发，并影响广泛使用的密码标准的安全性评估。 形式化工作涵盖了求阶算法以及用于模运算和椭圆曲线算术的可逆量子电路，并基于先前的量子资源分析，提供了攻击 RSA-2048 和 P-256 的逻辑资源估计。

rss · arXiv Agent Infra · 7月15日 17:56

**背景**: Shor 算法是一种量子算法，可以在多项式时间内分解大整数和计算离散对数，威胁到 RSA 和椭圆曲线密码学。Lean 是一种证明助手，允许对数学定理和算法进行形式化验证。代理形式化利用 LLM 代理自动搜索、编写和修复证明，减少人工工作量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://en.wikipedia.org/wiki/Shor's_algorithm">Shor's algorithm</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#quantum computing`, `#Shor's algorithm`, `#Lean`, `#cryptography`

---

<a id="item-3"></a>
## [TensorRT-LLM v1.3.0rc21 弃用 AutoDeploy，列出 DeepSeek 问题](https://github.com/NVIDIA/TensorRT-LLM/releases/tag/v1.3.0rc21) ⭐️ 8.0/10

NVIDIA 发布了 TensorRT-LLM v1.3.0rc21，该版本弃用了 AutoDeploy 后端，并记录了 DeepSeek V3 和分离式服务（disaggregated serving）的已知问题。该版本还新增了对 DeepSeek V4、Cosmos3 和 Gemma 4 等新模型的支持。 此版本标志着 NVIDIA 转向基于 PyTorch 的后端，并凸显了 DeepSeek V3 等前沿模型在多 GPU 配置下的稳定性挑战。依赖 TensorRT-LLM 进行生产推理的用户应关注弃用和已知问题，以规划迁移。 AutoDeploy 后端被弃用，转而采用 PyTorch 后端的代理方法；使用该方法在一周内实现了对 Minimax M3 的支持。已知问题包括 DeepSeek V3 在 H200 上出现 GPU OOM 和挂起、B300 上 NVFP4 精度失败，以及 DeepSeek V3 Lite 在 H100/H20 上的分离式服务错误。

github · mikeiovine · 7月15日 22:46

**背景**: TensorRT-LLM 是 NVIDIA 用于在其 GPU 上优化大语言模型推理的库。AutoDeploy 是一个原型后端，可自动将模型部署到 TensorRT-LLM。分离式服务将预填充和解码阶段分离到不同的 GPU 上以提高吞吐量。NVFP4 是 NVIDIA Blackwell 架构引入的一种 4 位浮点格式，用于高效的低精度推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nvidia.github.io/TensorRT-LLM/torch/auto_deploy/auto-deploy.html">AutoDeploy — TensorRT LLM</a></li>
<li><a href="https://nvidia.github.io/TensorRT-LLM/latest/features/disagg-serving.html">Disaggregated Serving — TensorRT LLM</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>

</ul>
</details>

**标签**: `#TensorRT-LLM`, `#NVIDIA`, `#LLM inference`, `#DeepSeek`, `#release notes`

---

<a id="item-4"></a>
## [GPT-Red：通过自对弈红队测试提升 AI 鲁棒性](https://openai.com/index/unlocking-self-improvement-gpt-red) ⭐️ 8.0/10

OpenAI 推出了 GPT-Red，这是一个利用自对弈强化学习的自动化红队测试系统，旨在提升 AI 的安全性、对齐性以及对抗提示注入攻击的鲁棒性。 该方法解决了扩展红队测试工作以跟上日益强大的 AI 模型步伐的关键挑战，可能减少对人类红队测试人员的需求，并使 AI 系统更能抵御对抗性攻击。 GPT-Red 通过自对弈进行训练，模型生成越来越强的提示注入攻击，同时防御模型学习抵抗这些攻击，从而形成一个对抗性共同进化过程。

rss · OpenAI Blog · 7月15日 10:00

**背景**: 红队测试是一种安全专家模拟攻击以发现 AI 系统漏洞的做法。提示注入是排名第一的 AI 安全风险，恶意输入会诱使模型绕过安全防护。自动化红队测试旨在扩展这一过程，而自对弈是一种 AI 通过与自己竞争来改进的技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/unlocking-self-improvement-gpt-red/">GPT-Red: Unlocking Self-Improvement for Robustness | OpenAI</a></li>
<li><a href="https://decrypt.co/373613/openai-ai-red-team-strengthen-gpt-5-6-prompt-injection-attacks">OpenAI Uses AI Red Team to Strengthen GPT-5.6 Against Prompt Injection Attacks - Decrypt</a></li>
<li><a href="https://genai.owasp.org/llmrisk/llm01-prompt-injection/">LLM01:2025 Prompt Injection - OWASP Gen AI Security Project</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#red teaming`, `#self-play`, `#prompt injection`, `#OpenAI`

---

<a id="item-5"></a>
## [构建 Shippy AI 智能体的经验教训](https://huggingface.co/blog/allenai/shippy-tech-blog) ⭐️ 8.0/10

Ai2 发布了一篇技术深度博客，详细介绍了构建 Shippy（一个用于实时海洋情报的海事 AI 智能体）时的架构、设计决策和遇到的挑战。 Shippy 基于 Ai2 的 Skylight 海洋监测平台构建，能够回答自然语言查询、引用数据来源，并且免费使用。博客涵盖了智能体架构、工具集成以及经验教训。

rss · Hugging Face Blog · 7月15日 17:29

**背景**: AI 智能体是利用大型语言模型自主执行任务的软件系统，通常通过调用外部工具或 API 来实现。Shippy 是一个专门用于海事领域感知的智能体，帮助分析师利用实时数据监控船舶活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://allenai.org/blog/shippy-deep-dive">What building Shippy taught us about building agents | Ai2</a></li>
<li><a href="https://skylight.global/news/shippy-launch">Meet Shippy: Agent Built for Ocean Intelligence</a></li>
<li><a href="https://www.geekwire.com/2026/ai2s-skylight-project-launches-shippy-an-ai-agent-that-dives-into-ocean-data/">Ai2’s Skylight project launches ‘Shippy,’ an AI agent that ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#software engineering`, `#Hugging Face`, `#deep-dive`

---

<a id="item-6"></a>
## [PhysClaw-0：通过可复用的语言纠正实现机器人自主性](https://arxiv.org/abs/2607.14047v1) ⭐️ 8.0/10

PhysClaw-0 提出了一种人机共生系统，将语言纠正存储在“纠正记忆”中并重复使用，在桌面清理任务中将人工监督时间降至 16%，同时保持与遥操作相当的成功率。 这项工作通过消除对重复故障重新发出纠正的需求，大幅降低了机器人操作数据收集的人力成本，有望加速机器人领域的可扩展策略学习。 该系统使用 LLM 解析器将自然语言纠正转换为存储在“纠正记忆”中的结构化调整，在四种设置下将单次尝试成功率从 12.5%提升至 47.5%。

rss · arXiv Agent Infra · 7月15日 17:16

**背景**: 机器人操作自主数据收集通常依赖人工监督来纠正故障，但现有流程需要对每次重复故障重新发出纠正，导致人力成本不断上升。PhysClaw-0 通过将纠正存储在记忆模块中来解决这一问题，使机器人能够自主避免之前纠正过的错误。

**标签**: `#robotics`, `#human-robot interaction`, `#autonomous data collection`, `#LLM`, `#manipulation`

---

<a id="item-7"></a>
## [TRACE：面向长周期智能体的回合级奖励分配方法](https://arxiv.org/abs/2607.13988v1) ⭐️ 8.0/10

TRACE 提出了一种密集信用分配方法，利用冻结参考模型的对数概率，通过时序差分学习计算每个动作的奖励，无需额外的评论家或过程标签。 这解决了长周期智能体强化学习中的基本挑战，即稀疏的结果奖励不足。它在复杂搜索基准上显著提升了工具使用能力，在 BrowseComp-Plus 上将 Qwen3-4B 从 7.2 提升至 35.6。 TRACE 将轨迹表示为工具调用边界处的状态转移，将正确答案的对数概率转换为对数比率状态值，并使用时序差分变化推导每个动作的奖励。它不需要冷启动监督微调或智能体中间训练。

rss · arXiv Agent Infra · 7月15日 16:16

**背景**: 信用分配是强化学习中的一个关键挑战：确定长序列中哪些动作导致了最终结果。在长周期任务中，仅基于结果的奖励变得稀疏且高方差，并且可能错误地将信用分配给有用的中间动作。时序差分学习通过从未来预测中自举来估计状态值，而冻结参考模型提供稳定的对数概率，用于 DPO 等方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.baeldung.com/cs/credit-assignment-problem">What Is the Credit Assignment Problem? - Baeldung From Reasoning to Agentic: Credit Assignment in Reinforcement ... GitHub - xxzcc/Awesome-Credit-Assignment-in-LLM-RL Credit Assignment in Long-Horizon Reinforcement Learning From Reasoning to Agentic: Credit Assignment in Reinforcement ... Deep reinforcement learning with credit assignment for ... The Credit Assignment Problem in Reinforcement Learning</a></li>
<li><a href="https://en.wikipedia.org/wiki/Temporal_difference_learning">Temporal difference learning - Wikipedia</a></li>
<li><a href="https://www.reinforcement-learning.com/kb/dpo-preference-optimization">DPO & Preference Optimization, Explained</a></li>

</ul>
</details>

**标签**: `#reinforcement learning`, `#credit assignment`, `#multi-turn agents`, `#AI agents`, `#post-training`

---

<a id="item-8"></a>
## [SkillSec-Eval：LLM 代理技能的生命周期安全评估](https://arxiv.org/abs/2607.13987v1) ⭐️ 8.0/10

本文提出了 SkillSec-Eval，一个生命周期感知的框架，用于系统评估可重用 LLM 代理技能在多个阶段（超越执行阶段）的安全风险。作者构建了一个涵盖仓库准入、语义检索、规划器选择、执行和技能演化的威胁分类法，并在 327 个真实技能上进行了实证评估。 随着可重用技能成为 LLM 代理的基础构建块，现有安全研究仅关注提示注入和运行时执行，忽略了更广泛的生命周期风险。这项工作强调了生命周期感知安全分析的必要性，可能影响未来的代理开发和安全实践。 威胁分类法包括五个阶段：仓库准入、语义检索、规划器选择、执行和技能演化。实证评估使用了 327 个真实技能的仓库，展示了执行阶段之外多个生命周期阶段的漏洞。

rss · arXiv Agent Infra · 7月15日 16:15

**背景**: LLM 代理使用可重用技能——可在不同应用间共享和复用的打包能力。当前安全研究主要关注提示注入和运行时攻击，但从技能创建到演化的完整生命周期引入了额外风险，如供应链妥协和检索操纵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.13987">[2607.13987] Agent Skill Security: Threat Models, Attacks ...</a></li>
<li><a href="https://skillsec.io/methodology">Methodology - skillsec.io</a></li>
<li><a href="https://hacking-and-security.de/newsletter/paper/2602.20867v1">SoK: Agentic Skills -- Beyond Tool Use in LLM Agents - AI Security...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#security`, `#threat modeling`, `#AI safety`, `#evaluation`

---