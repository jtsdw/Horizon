---
layout: default
title: "Horizon Summary: 2026-06-30 (ZH)"
date: 2026-06-30
lang: zh
---

> 从 45 条内容中筛选出 8 条重要资讯。

---

1. [最高法院：地理围栏搜查令需受第四修正案保护](#item-1) ⭐️ 9.0/10
2. [LongCat-2.0：1.6 万亿参数 MoE 模型，每 token 激活 480 亿参数](#item-2) ⭐️ 9.0/10
3. [DiScoFormer：一个跨分布学习密度和分数的 Transformer](#item-3) ⭐️ 8.0/10
4. [TraceLab：面向 LLM 服务的真实编码智能体工作负载](#item-4) ⭐️ 8.0/10
5. [LLM 能排序吗？三元组与分诊的故事](#item-5) ⭐️ 8.0/10
6. [Festina：面向无服务器 LLM 服务的能量感知调度](#item-6) ⭐️ 8.0/10
7. [HMA-Serve：跨异构内存加速器的分离式 LLM 服务](#item-7) ⭐️ 8.0/10
8. [投机解码中的接受理论](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [最高法院：地理围栏搜查令需受第四修正案保护](https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision) ⭐️ 9.0/10

美国最高法院裁定，要求科技公司提供特定区域内所有设备位置数据的地理围栏搜查令，需受第四修正案的宪法保护。 这一里程碑式的裁决将第四修正案的保护范围扩展至数字位置数据，可能限制执法部门无证进行大规模监控，并为数字时代的隐私权树立先例。 该案涉及一起银行抢劫案，谷歌提供了银行周围 150 米内 19 个账户的位置数据。由卡根大法官撰写的法院意见引用了来源，并参考了 2014 年 Riley 诉 California 案关于手机隐私的判决。

hackernews · cdrnsf · 6月29日 15:54 · [社区讨论](https://news.ycombinator.com/item?id=48720924)

**背景**: 地理围栏搜查令是一种搜查令，要求谷歌等公司识别特定地理区域和时间内所有移动设备。第四修正案保护公民免受不合理搜查和扣押，但自 Carpenter 诉 United States 案以来，其对第三方持有的数字数据的适用性一直存在争议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Geofence_warrant">Geofence warrant - Wikipedia</a></li>
<li><a href="https://legalclarity.org/what-is-a-geofence-warrant-and-how-does-it-work/">What Is a Geofence Warrant: Fourth Amendment Challenges</a></li>
<li><a href="https://www.congress.gov/crs_external_products/LSB/PDF/LSB11274/LSB11274.4.pdf">Geofence Warrants and the Fourth Amendment - Congress.gov</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论了技术和法律影响，有人指出即使没有手机，个人也可能通过其他数据（如酒店客人名单）被识别。其他人质疑这一裁决是否会扩展到 Flock 摄像头等监控工具，并赞扬法院在意见中引用了来源。

**标签**: `#privacy`, `#supreme court`, `#fourth amendment`, `#geofence warrants`, `#digital rights`

---

<a id="item-2"></a>
## [LongCat-2.0：1.6 万亿参数 MoE 模型，每 token 激活 480 亿参数](https://www.reddit.com/r/LocalLLaMA/comments/1uj7egu/introducing_longcat20_a_largescale_moe_language/) ⭐️ 9.0/10

LongCat-2.0 是一款大规模混合专家（MoE）语言模型，总参数量达 1.6 万亿，每个 token 激活约 480 亿参数。该模型此前在 Openrouter 上以'owl-alpha'的名称出现。 该模型代表了 MoE 架构扩展的重要里程碑，通过稀疏激活在保持推理成本相对较低的同时实现了巨大的总参数量。它可能推动开源 LLM 能力的边界，并激发高效模型设计的进一步创新。 该模型采用 MoE 架构，每个 token 仅激活总参数的一小部分，从而实现高效推理。总参数 1.6T、激活参数 48B 使其成为迄今为止最大的开源权重模型之一。

reddit · r/LocalLLaMA · /u/AnticitizenPrime · 6月29日 22:42

**背景**: 混合专家（MoE）是一种神经网络架构，将模型划分为多个“专家”子网络，并通过路由器为每个输入 token 选择部分专家。这使得模型可以拥有巨大的总参数量，同时保持每 token 的计算成本较低，因为只有部分参数被激活。LongCat-2.0 基于这一概念，实现了 1.6T 总参数，每 token 仅激活 48B 参数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@sharanharsoor/understanding-mixture-of-experts-moe-the-architecture-powering-next-generation-language-models-49c1d1d467c9">Understanding Mixture of Experts (MoE): The Architecture ...</a></li>
<li><a href="https://www.kamiljozwik.com/posts/llm-parameters">Understand parameters in LLM - kamiljozwik.com</a></li>
<li><a href="https://www.f22labs.com/blogs/active-vs-total-parameters-whats-the-difference/">Active vs Total Parameters: What's the Difference?</a></li>

</ul>
</details>

**标签**: `#LLM`, `#MoE`, `#Large Language Model`, `#Open Source`, `#AI`

---

<a id="item-3"></a>
## [DiScoFormer：一个跨分布学习密度和分数的 Transformer](https://huggingface.co/blog/allenai/discoformer) ⭐️ 8.0/10

Ai2 的研究人员推出了 DiScoFormer，这是一种 Transformer 架构，能够从独立同分布样本中同时估计概率密度函数及其分数（对数密度的梯度），并且可以跨不同分布进行泛化。 这将密度估计和基于分数的生成建模这两个传统上分离的任务统一到一个模型中，可能简化生成式 AI 的工作流程，并实现更灵活的表示学习。 DiScoFormer 是一个置换和仿射等变的 Transformer，将密度估计视为序列到序列问题，将整个样本映射到其密度和分数。它在多个分布上训练，并可作为即插即用的估计器。

rss · Hugging Face Blog · 6月29日 18:02

**背景**: 密度估计旨在从数据中学习概率密度函数，而基于分数的生成模型则学习对数密度的梯度以生成新样本。传统上，这些任务需要单独的模型。Transformer 在序列建模中已取得成功，DiScoFormer 将其改造用于这一统一目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/allenai/discoformer">DiScoFormer : One transformer for density and score, across...</a></li>
<li><a href="https://allenai.org/blog/discoformer">DiScoFormer: One transformer for density and score, across ...</a></li>
<li><a href="https://arxiv.org/abs/2511.05924">[2511.05924] From Kernels to Attention: A Transformer ... DiScoFormer: One transformer for density and score, across ... TraDE: Transformers for Density Estimation - GitHub Pages Autoregressive Density Estimation Transformers for ... A data-driven intelligent predictive maintenance decision ... DiScoFormer: One transformer for density and score, across ...</a></li>

</ul>
</details>

**标签**: `#transformer`, `#generative modeling`, `#density estimation`, `#score-based models`, `#AI research`

---

<a id="item-4"></a>
## [TraceLab：面向 LLM 服务的真实编码智能体工作负载](https://arxiv.org/abs/2606.30560v1) ⭐️ 8.0/10

研究人员发布了 TraceLab，这是一个来自日常使用 Claude Code 和 Codex 的约 4300 个编码智能体会话（35 万次 LLM 步骤和 43 万次工具调用）的追踪数据，并分析了工作负载模式。 该追踪数据通过提供真实的编码智能体工作负载数据，填补了 LLM 服务研究中的关键空白，揭示了长上下文、短输出和多样化工具调用等模式，为服务系统提出了具体的优化方向。 分析显示前缀缓存命中率高但不完美，存在长自主循环和重尾工具调用，指向了诸如感知追加长度的预填充、语义感知的工具延迟预测以及改进的 KV 缓存管理等优化方向。

rss · arXiv LLM Inference · 6月29日 16:59

**背景**: 像 Claude Code 和 Codex 这样的编码智能体是能够自主读取代码、编辑文件和运行命令的 AI 工具。高效服务这些智能体需要了解真实的工作负载模式，但现有的公开追踪数据缺乏多智能体、多会话的数据。前缀缓存是 LLM 推理的关键优化技术，其中 KV 缓存命中率是生产系统的关键指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/overview">Overview - Claude Code Docs</a></li>
<li><a href="https://openai.com/codex/">Codex | AI Coding Partner from OpenAI</a></li>
<li><a href="https://bentoml.com/llm/inference-optimization/prefix-caching">Prefix caching | LLM Inference Handbook</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#coding agents`, `#workload characterization`, `#systems optimization`, `#trace analysis`

---

<a id="item-5"></a>
## [LLM 能排序吗？三元组与分诊的故事](https://arxiv.org/abs/2606.30412v1) ⭐️ 8.0/10

本文提出使用循环三元组和一种新的无模型一致性度量 zeta 来评估 LLM 在成对比较排序任务中判断的可靠性。 作者证明，运行内一致性（zeta）和运行间变异性（如 Kendall's tau）各自独立有价值，应同时使用；他们在两个现实世界的优先排序任务上测试了三个领先的 LLM。

rss · arXiv LLM Inference · 6月29日 14:59

**背景**: 通过成对比较对大型群体进行排序是社会选择理论中的经典方法。循环三元组（竞赛图中的 3-环）表示非传递性偏好，一致性系数 zeta 量化了此类三元组的数量，作为判断可靠性的廉价诊断工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tournament_(graph_theory)">Tournament (graph theory) - Wikipedia</a></li>
<li><a href="https://arxiv.org/pdf/2411.00119">Soft Condorcet Optimization for Ranking of General Agents</a></li>
<li><a href="https://procaccia.info/wp-content/uploads/2020/03/comsoc.pdf">Handbook of Computational Social Choice</a></li>

</ul>
</details>

**标签**: `#LLM`, `#ranking`, `#social choice theory`, `#consistency`, `#AI ethics`

---

<a id="item-6"></a>
## [Festina：面向无服务器 LLM 服务的能量感知调度](https://arxiv.org/abs/2606.30391v1) ⭐️ 8.0/10

该论文提出了 Festina，一个基于性能剖析的功耗感知控制平面，用于最小化共享 GPU 上无服务器 LLM 服务的集群级能耗。它在 TTFT/TBT SLO 约束下协调请求放置、SM 分区和 GPU 工作点。 随着 LLM 推理成为主要云工作负载，能效对于降低运营成本和环境影响至关重要。Festina 在保持 SLO 达标率在 2%以内的同时，实现了高达 56%的能耗降低，为可持续 AI 基础设施提供了实用方案。 Festina 使用轻量级全局调度器，通过离线配置文件和 GPU 状态摘要进行常数时间查找，以及一个相位感知的本地调度器，在每个 GPU 上自适应调整批处理和计算资源。它还通过 SLO 感知迁移执行能量感知的工作负载整合，以减少静态功耗。

rss · arXiv LLM Inference · 6月29日 14:44

**背景**: 无服务器 LLM 服务通过弹性共享 GPU 资源来处理流量波动，但共驻模型在单一设备级功耗状态下运行，使能量优化复杂化。关键指标包括 TTFT（首 token 时间）和 TBT（token 间时间）作为用户体验的 SLO。SM（流式多处理器）分区允许在并发任务之间划分 GPU 计算资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cs.unc.edu/~jbakita/rtas23.pdf">Hardware Compute Partitioning on NVIDIA GPUs*</a></li>
<li><a href="https://arxiv.org/html/2410.14257v1">Revisiting SLO and Goodput Metrics in LLM Serving - arXiv.org</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#energy efficiency`, `#serverless`, `#GPU scheduling`, `#systems`

---

<a id="item-7"></a>
## [HMA-Serve：跨异构内存加速器的分离式 LLM 服务](https://arxiv.org/abs/2606.29986v1) ⭐️ 8.0/10

HMA-Serve 提出了一种分离式 LLM 服务系统，将低成本的 GDDR 加速器用于预填充阶段，与基于 HBM 的 GPU 用于解码阶段配对，相比最先进的同构内存方法，实现了高达 3.2 倍的有效吞吐量和 4.8 倍的每美元有效吞吐量。 这项工作解决了在计算密集的预填充阶段使用昂贵 HBM 内存的低效问题，可能显著降低 LLM 服务成本。它还解决了跨厂商的 KV 格式和软件栈挑战，实现了更灵活、更经济的大语言模型部署。 HMA-Serve 引入了三项关键技术：分阶段量化（预填充用低精度，解码用高精度 BF16）、计算传输流水线（将 KV 缓存传输与后续层预填充重叠）以及延迟反量化（减少网络带宽和 HBM 使用）。该系统在 Qwen3 模型（4B–32B）和三个生产轨迹上进行了评估。

rss · arXiv LLM Inference · 6月29日 09:00

**背景**: LLM 推理包括计算密集的预填充阶段和内存密集的解码阶段。分离式服务将这些阶段分配到不同的硬件上以提高利用率。HBM（高带宽内存）昂贵但提供高带宽，而 GDDR 内存更便宜但带宽较低。跨厂商分离引入了挑战，因为不同厂商使用不兼容的 KV 缓存格式和软件栈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.exxactcorp.com/blog/hpc/gddr6-vs-hbm-gpu-memory">GDDR6 vs HBM - Different GPU Memory Types | Exxact Blog</a></li>
<li><a href="https://aws.amazon.com/blogs/machine-learning/introducing-disaggregated-inference-on-aws-powered-by-llm-d/">Introducing Disaggregated Inference on AWS powered by llm-d | Artificial Intelligence</a></li>
<li><a href="https://huggingface.co/blog/not-lain/kv-caching">KV Caching Explained: Optimizing Transformer Inference Efficiency</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#disaggregated architecture`, `#memory heterogeneity`, `#GPU`, `#systems research`

---

<a id="item-8"></a>
## [投机解码中的接受理论](https://arxiv.org/abs/2606.30265v1) ⭐️ 8.0/10

本文为投机解码中超越精确分布采样的接受准则建立了理论框架，将拒绝区域刻画为目标分布的下水平集，并为贪婪、松弛和树状接受规则推导了 KL 散度界。 这项工作弥合了投机解码中理论与实践之间的差距，为实际 LLM 推理系统中常用的确定性接受规则提供了保证，从而可能带来更高效、更可靠的加速技术。 作者在 Qwen3 模型上评估了他们的保证，结果表明松弛和树状准则显著扩大了可保证接受区域，尤其是在目标模型分布边际较低的解码步骤上。

rss · arXiv Speculative Decoding · 6月29日 13:14

**背景**: 投机解码通过使用快速草稿模型提出候选词元，再由更大的目标模型进行验证，从而加速 LLM 推理。现有理论主要涵盖随机、分布保持的设置，但实际系统常使用贪婪解码或松弛接受规则，这些规则并不保持分布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2606.25097">Speculative Decoding at Temperature Zero: A Scoped...</a></li>
<li><a href="https://arxiv.org/pdf/2502.20704">Fuzzy Speculative Decoding for a Tunable Accuracy-Runtime Tradeoff</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#language model inference`, `#theoretical analysis`, `#LLM acceleration`

---