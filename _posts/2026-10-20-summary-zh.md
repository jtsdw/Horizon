---
layout: default
title: "Horizon Summary: 2026-10-20 (ZH)"
date: 2026-10-20
lang: zh
---

> 从 60 条内容中筛选出 3 条重要资讯。

---

1. [虚假新闻标题对 LLM 交易代理的操纵远超提示注入](#item-1) ⭐️ 8.0/10
2. [CXBench 基准揭示：多数看似合规的 LLM 智能体跳过必要流程](#item-2) ⭐️ 8.0/10
3. [编码智能体在代码空间中搜索，设计更优的多智能体路径规划策略](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [虚假新闻标题对 LLM 交易代理的操纵远超提示注入](https://arxiv.org/abs/2610.26438v1) ⭐️ 8.0/10

一项新的系统性基准评估了针对 LLM 交易代理的信息注入攻击，结果显示虚假新闻标题的攻击成功率（ASR）达到 62%，而提示注入仅为 14%，其中两个 30 词模板在全部 15 只测试美股上均达到 100%的 ASR。该研究涵盖五种注入向量和七类事件，共约 10,000 次交易决策。 这项研究揭示了一个关键的安全漏洞：以新闻作为证据的 LLM 交易代理极易受到虚假信息的影响，可能导致协同市场操纵和实际财务损失。它挑战了提示注入是主要威胁的普遍假设，并强调需要针对金融 AI 系统中的证据投毒专门设计防御措施。 对于事实投毒模板，表面形式比内容更重要：移除可信度线索（如具名来源或“BREAKING”标签）会使 ASR 从 100%降至 0%，而虚假声明本身保持不变。攻击成功率还取决于代理的状态，虚假指标面板对即将持有的代理成功率为 91%，但对即将买入的代理仅为 12%；大多数攻击能绕过标准防御，只有分层聚合能降低 ASR。

rss · arXiv Agent Infra · 10月19日 13:58

**背景**: LLM 交易代理是读取新闻推送并做出交易决策的 AI 系统，通常使用大语言模型将标题解释为证据。提示注入是一种众所周知的攻击方式，将恶意指令插入模型输入以劫持行为，而信息注入则针对代理所信任的证据，例如捏造的新闻报道。攻击成功率（ASR）是衡量对抗攻击达成目标频率的标准指标，常用于 HarmBench 等 LLM 安全基准测试中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://genai.owasp.org/llmrisk/llm01-prompt-injection/">LLM01:2025 Prompt Injection - OWASP Gen AI Security Project</a></li>
<li><a href="https://github.com/jackson-cmd/feedhijack">jackson-cmd/feedhijack: Research artifact: information - injection ...</a></li>
<li><a href="https://www.emergentmind.com/topics/harmbench-attack-success-rate">HarmBench Attack Success Rate Metrics</a></li>

</ul>
</details>

**标签**: `#LLM security`, `#adversarial attacks`, `#financial trading agents`, `#information injection`, `#AI safety`

---

<a id="item-2"></a>
## [CXBench 基准揭示：多数看似合规的 LLM 智能体跳过必要流程](https://arxiv.org/abs/2610.25954v1) ⭐️ 8.0/10

研究人员推出了 CXBench 基准，在六个受监管的客户体验领域中，分别评估使用工具的 LLM 智能体的任务结果与流程合规性。在七个模型和 120 项任务中，840 次保留执行里有 55.5%属于“假通过”，即达到了正确的最终状态但违反了规定流程，只有 13.8%同时通过结果检查和流程检查。 这项工作揭示了智能体评估中的一个重大盲点：仅看结果的评分可能掩盖在金融、医疗和保险等受监管行业中不可接受的违规行为。80.1%的结果通过运行属于“假通过”这一发现表明，当前基准可能大幅高估了智能体在真实世界部署中的准备程度。 CXBench 使用规则卡片将引用的监管义务与可观察的轨迹证据关联起来，并采用混合评分器，将针对顺序和权限的确定性检查与针对语义要求的 LLM 评判相结合。作者将“假通过”定义为通过结果检查但未通过流程检查的运行，并指出包含流程的评估会改变观察到的模型排序，揭示仅看结果评分所隐藏的差异。

rss · arXiv Agent Infra · 10月19日 07:46

**背景**: LLM 智能体越来越多地被用于处理多步骤客户服务工作流，它们必须调用工具、获得同意、提供披露信息并遵循规定程序。现有的工具智能体基准通常只对最终业务状态评分，因此智能体可以通过任何路径成功，即使该路径违反监管要求。流程合规性已成为企业部署的关键关注点，但很少有基准明确衡量它。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2507.21504v1">Evaluation and Benchmarking of LLM Agents: A Survey - arXiv.org</a></li>
<li><a href="https://openreview.net/forum?id=edhc5pD8Sh">CXBench: A Benchmark for Process-Compliant LLM Agents in ...</a></li>
<li><a href="https://kam-ai.com/blog/deterministic-graders-before-llm-judge">Deterministic Graders Before LLM Judges - Kam AI Blog</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#benchmark`, `#process compliance`, `#regulated workflows`, `#agent evaluation`

---

<a id="item-3"></a>
## [编码智能体在代码空间中搜索，设计更优的多智能体路径规划策略](https://arxiv.org/abs/2610.25946v1) ⭐️ 8.0/10

一篇新的 arXiv 论文展示了一种由人类引导的工作流，其中编码智能体在代码空间中迭代地提出、实现、评估并改进多智能体路径规划（MAPF）算法。在 2024 年 League of Robot Runners 的一张地图上，两天的搜索找到了比本地复现的竞赛方案好 35.0% 的策略；在模拟仓库中为期一周的搜索发现了一类新算法，其吞吐量比经过校准的专有解决方案高 58.9%。 这提供了介于劳动密集型人工算法设计与不透明的强化学习之间的第三条路径，将自动优化与可解释、可验证的代码相结合。它可能显著影响自动算法设计，并使高性能 MAPF 解决方案更易于在物流和仓库机器人中应用。 该工作流包含显式的正确性验证，作者证明在所述假设下，新仓库算法无碰撞并在有限时间内完成每个被接受的目标。该方法依赖最先进的编码智能体和人类指导，35.0% 的提升是在最密集实例上测得的，并且还能泛化到未见过的地图实例。

rss · arXiv Agent Infra · 10月19日 07:39

**背景**: 多智能体路径规划（MAPF）是为一组智能体计算从起点到目标的无碰撞路径的问题，在自动化仓库和物流中至关重要。League of Robot Runners 是一个在模拟仓库实例上对 MAPF 解决方案进行基准测试的竞赛。传统上，协调策略要么由专家手工设计，要么通过强化学习获得，后者往往不透明且针对特定任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Multi-agent_pathfinding">Multi-agent pathfinding</a></li>
<li><a href="https://idm-lab.org/bib/abstracts/papers/icaps24e.pdf">The League of Robot Runners</a></li>

</ul>
</details>

**标签**: `#multi-agent pathfinding`, `#code generation`, `#policy search`, `#autonomous coding agents`, `#interpretable AI`

---