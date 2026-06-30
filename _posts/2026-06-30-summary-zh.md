---
layout: default
title: "Horizon Summary: 2026-06-30 (ZH)"
date: 2026-06-30
lang: zh
---

> 从 45 条内容中筛选出 8 条重要资讯。

---

1. [最高法院：地理围栏搜查令需受宪法保护](#item-1) ⭐️ 9.0/10
2. [LongCat-2.0：1.6 万亿参数 MoE 模型，每 token 激活 48B 参数](#item-2) ⭐️ 9.0/10
3. [DiScoFormer：统一密度与得分的 Transformer](#item-3) ⭐️ 8.0/10
4. [TraceLab：面向 LLM 服务的真实编码智能体工作负载分析](#item-4) ⭐️ 8.0/10
5. [用社会选择理论评估 LLM 排序可靠性](#item-5) ⭐️ 8.0/10
6. [Festina：面向无服务器 LLM 服务的能量感知调度](#item-6) ⭐️ 8.0/10
7. [HMA-Serve：异构内存上的 LLM 解耦服务](#item-7) ⭐️ 8.0/10
8. [投机解码中的接受理论](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [最高法院：地理围栏搜查令需受宪法保护](https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision) ⭐️ 9.0/10

美国最高法院裁定，要求科技公司识别特定区域内所有设备的地理围栏搜查令，必须受到第四修正案的宪法保护。这一里程碑式的裁决为数字隐私设立了重要先例。 这一裁决极大地限制了执法部门在没有个别嫌疑的情况下进行大规模数字搜捕的能力，影响了警方调查犯罪的方式以及科技公司处理用户数据的方式。它强化了数字时代的第四修正案保护，影响了数百万智能手机用户。 该案涉及一起银行抢劫案，谷歌提供了地理围栏内 19 台设备的数据，导致定罪。法院认为，此类搜查令必须满足第四修正案关于具体性和可能原因的要求，政府不能简单地要求获取某一区域内的所有设备数据。

hackernews · cdrnsf · 6月29日 15:54 · [社区讨论](https://news.ycombinator.com/item?id=48720924)

**背景**: 地理围栏搜查令是一种搜查令，要求谷歌等公司识别特定时间段内特定地理区域内的所有移动设备。执法部门越来越多地使用这种搜查令来识别嫌疑人，但批评者认为，它们通过收集无辜旁观者的数据，违反了第四修正案禁止不合理搜查的规定。最高法院的裁决建立在早期数字隐私案件（如 Riley 诉 California 案和 Carpenter 诉 United States 案）的基础上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Geofence_warrant">Geofence warrant - Wikipedia</a></li>
<li><a href="https://www.congress.gov/crs-product/LSB11274">Geofence Warrants and the Fourth Amendment | Congress.gov | Library of Congress</a></li>
<li><a href="https://www.nacdl.org/Content/Geofence-Warrants">NACDL - Geofence Warrants</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调了意见的详尽性，一位用户指出卡根大法官为事实主张引用了来源。另一位评论者讨论了 Paula Broadwell 案作为无需手机即可识别的例子，而其他人则质疑这一裁决是否会扩展到其他监控技术，如 Flock 摄像头。总体情绪积极，认为该决定是对数字监控的必要制衡。

**标签**: `#privacy`, `#supreme court`, `#fourth amendment`, `#geofence warrants`, `#digital rights`

---

<a id="item-2"></a>
## [LongCat-2.0：1.6 万亿参数 MoE 模型，每 token 激活 48B 参数](https://www.reddit.com/r/LocalLLaMA/comments/1uj7egu/introducing_longcat20_a_largescale_moe_language/) ⭐️ 9.0/10

LongCat-2.0 是一款大规模混合专家（MoE）语言模型，总参数达 1.6 万亿，每个 token 激活约 480 亿参数。该模型此前在 OpenRouter 上以“owl-alpha”名称出现。 该模型代表了开源权重语言模型的重要进步，通过 MoE 实现了大规模与高效推理的结合。它可能降低研究人员和开发者实验万亿参数模型的门槛。 LongCat-2.0 采用混合专家架构，每个 token 仅激活约 480 亿个参数（总参数 1.6 万亿）。该模型此前在 OpenRouter 上以“owl-alpha”名称提供，支持 100 万 token 上下文窗口和工具调用。

reddit · r/LocalLLaMA · /u/AnticitizenPrime · 6月29日 22:42

**背景**: 混合专家（MoE）是一种机器学习技术，将问题划分为由专门专家网络处理的区域，从而以亚线性计算成本实现大型模型。像 Google 的 SwitchTransformer 这样的万亿参数模型已经展示了这种方法的潜力。LongCat-2.0 通过开源权重发布延续了这一趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://openrouter.ai/openrouter/owl-alpha">Owl Alpha - API Pricing & Providers | OpenRouter</a></li>

</ul>
</details>

**标签**: `#MoE`, `#large language model`, `#open-source`, `#AI research`

---

<a id="item-3"></a>
## [DiScoFormer：统一密度与得分的 Transformer](https://huggingface.co/blog/allenai/discoformer) ⭐️ 8.0/10

AI2 的研究人员推出了 DiScoFormer，这是一种 Transformer 模型，能够跨不同分布联合学习密度函数和得分函数，在单一架构中同时实现密度估计和基于得分的生成建模。 这种统一简化了生成式 AI 的流程，可能为图像生成和异常检测等任务带来更高效、更灵活的模型，连接了此前两个独立的研究方向。 DiScoFormer 利用 Transformer 架构参数化密度函数和得分函数，无需重新训练即可处理多个分布。该模型在合成和真实数据集上展示了密度估计和样本生成方面的竞争性能。

rss · Hugging Face Blog · 6月29日 18:02

**背景**: 基于得分的生成模型（也称为扩散模型）通过使用估计的得分函数（对数密度的梯度）逆转噪声过程来生成数据。密度估计旨在学习数据的概率分布。传统上，这些任务需要单独的模型。DiScoFormer 将它们结合到一个 Transformer 中，利用了 Transformer 处理多样化数据分布的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Diffusion_model">Diffusion model - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2011.13456">[2011.13456] Score-Based Generative Modeling through Stochastic Differential Equations</a></li>
<li><a href="https://fanpu.io/blog/2023/score-based-diffusion-models/">Score-Based Diffusion Models | Fan Pu Zeng</a></li>

</ul>
</details>

**标签**: `#transformer`, `#generative modeling`, `#density estimation`, `#score-based models`, `#AI research`

---

<a id="item-4"></a>
## [TraceLab：面向 LLM 服务的真实编码智能体工作负载分析](https://arxiv.org/abs/2606.30560v1) ⭐️ 8.0/10

研究人员发布了 TraceLab，这是一个包含 4,300 个编码智能体会话的追踪数据集，涵盖来自日常使用 Claude Code 和 Codex 的 35 万次 LLM 步骤和 43 万次工具调用，揭示了 LLM 服务优化的关键工作负载模式。 这是首个捕获跨多个智能体和模型家族的真实日常编码智能体使用情况的公开追踪数据集，能够实现如感知追加长度的预填充和改进 KV 缓存管理等具体优化，从而显著降低服务成本和延迟。 分析显示编码智能体工作负载具有长自主循环、长上下文短输出、多样且重尾的工具调用，以及高但不完美的前缀缓存命中率，指出了降低工具调用开销和语义感知工具延迟预测等优化机会。

rss · arXiv LLM Inference · 6月29日 16:59

**背景**: LLM 服务系统处理大型语言模型的推理请求，高效服务需要 KV 缓存和前缀缓存等优化以减少冗余计算。编码智能体是一种快速增长的应用，其中 LLM 自主执行软件工程任务，但其独特的工作负载模式（如长上下文和频繁工具调用）未被现有基准充分捕获。TraceLab 通过提供真实世界的追踪数据填补了这一空白，用于系统分析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bentoml.com/llm/inference-optimization/prefix-caching">Prefix caching | LLM Inference Handbook</a></li>
<li><a href="https://arxiv.org/abs/2601.11589">[2601.11589] LAPS: A Length-Aware-Prefill LLM Serving System</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#coding agents`, `#workload characterization`, `#systems optimization`

---

<a id="item-5"></a>
## [用社会选择理论评估 LLM 排序可靠性](https://arxiv.org/abs/2606.30412v1) ⭐️ 8.0/10

一篇新论文提出使用社会选择理论中的一致性系数ζ来衡量 LLM 在成对排序任务中的可靠性，并在无家可归者分配和急诊分诊任务中进行了验证。 这项工作填补了高风险决策中 AI 可靠性的关键空白，提供了一种廉价、无模型的诊断方法，可在将 LLM 作为排序稀缺资源的评判者之前使用。 系数ζ通过计算竞赛图中的循环三元组来衡量运行内一致性，而 Kendall's τ衡量运行间变异性；三个领先的 LLM 在不同任务上表现出不同的一致性特征。

rss · arXiv LLM Inference · 6月29日 14:59

**背景**: LLM 越来越多地被用于对稀缺资源（如住房或医疗分诊）进行人员排序，但其可靠性尚不确定。社会选择理论提供了一致性系数ζ等工具，该系数最初通过检测成对比较中的循环三元组（非传递偏好）来衡量评判者可靠性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tournament_(graph_theory)">Tournament (graph theory) - Wikipedia</a></li>
<li><a href="https://www.goodreads.com/book/show/25585548-topics-on-tournaments-in-graph-theory">Topics on Tournaments in Graph Theory by John W. Moon | Goodreads</a></li>

</ul>
</details>

**标签**: `#LLM`, `#ranking`, `#social choice theory`, `#AI reliability`, `#ethics`

---

<a id="item-6"></a>
## [Festina：面向无服务器 LLM 服务的能量感知调度](https://arxiv.org/abs/2606.30391v1) ⭐️ 8.0/10

研究人员提出了 Festina，这是一个基于性能分析、功耗感知的控制平面，通过在延迟 SLO 下联合协调请求放置、SM 分区和 GPU 工作点，最小化无服务器 LLM 服务的集群能耗。 随着 LLM 推理成为主要云工作负载，降低其能耗对可持续性和成本至关重要。Festina 的协调方法在保持 SLO 达标的同时实现了高达 56%的能耗降低，为节能 LLM 服务树立了新标准。 Festina 使用轻量级全局调度器，通过离线配置文件和 GPU 状态摘要进行常数时间查找，以及一个相位感知的本地调度器，在每个 GPU 上调整任务批处理和计算资源。它还执行 SLO 感知的工作负载整合以减少静态功耗。

rss · arXiv LLM Inference · 6月29日 14:44

**背景**: 无服务器 LLM 服务允许多个模型弹性共享 GPU 资源，但共驻模型必须在单一设备级工作点下运行，这使能耗优化变得复杂。关键概念包括 SM 分区（在任务间划分 GPU 流式多处理器）和 TTFT/TBT SLO（首令牌时间和令牌间延迟目标）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cs.unc.edu/~jbakita/rtas23.pdf">Hardware Compute Partitioning on NVIDIA GPUs*</a></li>
<li><a href="https://arxiv.org/pdf/2504.20828">Ascendra: Dynamic Request Prioritization for Efficient LLM Serving</a></li>
<li><a href="https://serverlessllm.github.io/docs/intro/">Serverless LLM | ServerlessLLM</a></li>

</ul>
</details>

**标签**: `#LLM`, `#energy efficiency`, `#serverless`, `#GPU scheduling`, `#cloud computing`

---

<a id="item-7"></a>
## [HMA-Serve：异构内存上的 LLM 解耦服务](https://arxiv.org/abs/2606.29986v1) ⭐️ 8.0/10

HMA-Serve 提出了一种解耦的 LLM 服务系统，将基于 GDDR 的高性价比加速器用于预填充阶段，将基于 HBM 的 GPU 用于解码阶段，并克服了跨厂商的 KV 格式和软件栈挑战。 该方法通过在计算密集的预填充阶段使用更便宜的 GDDR 内存（HBM 带宽在此阶段利用率低），同时为内存密集的解码阶段保持高性能，从而显著降低服务成本。与最先进的方法相比，其每美元有效吞吐量提升高达 4.8 倍。 HMA-Serve 采用分阶段量化（预填充使用低精度，解码使用 BF16）、计算-传输流水线（将 KV 缓存传输与预填充重叠）以及延迟反量化（减少网络带宽和 HBM 使用）。它在四个 Qwen3 模型（4B–32B）和三个生产轨迹上进行了评估。

rss · arXiv LLM Inference · 6月29日 09:00

**背景**: LLM 推理包括计算密集的预填充阶段和内存密集的解码阶段。最近的系统将这两个阶段解耦到不同的硬件上，但通常使用同构的基于 HBM 的 GPU，这成本高昂且在预填充阶段 HBM 带宽闲置。GDDR 内存更便宜但带宽较低，适合预填充但不适合解码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.exxactcorp.com/blog/hpc/gddr6-vs-hbm-gpu-memory">GDDR 6 vs HBM - Different GPU Memory Types | Exxact Blog</a></li>
<li><a href="https://arxiv.org/pdf/2407.00079">Mooncake: A KVCache-centric Disaggregated Architecture for LLM ...</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#disaggregated architecture`, `#memory heterogeneity`, `#GPU`, `#systems`

---

<a id="item-8"></a>
## [投机解码中的接受理论](https://arxiv.org/abs/2606.30265v1) ⭐️ 8.0/10

本文提出了一个超越标准分布保持设置的投机解码接受准则理论框架，涵盖了贪婪解码、宽松接受和基于树的候选集。它将拒绝区域刻画为目标分布的下水平集，并为各种实际场景提供了精确的 KL 散度界限。 这项工作弥合了投机解码中理论与实践之间的差距，提供了精确的证书和紧的界限，可指导更高效的大语言模型推理系统设计。它通过为常用接受规则提供严格保证，直接影响大语言模型的加速。 论文推导了严格贪婪解码、加性和乘性宽松接受、top-(m)宽松准则以及熵阈值接受的精确证书。它还将框架扩展到贪婪树解码，为目标贪婪令牌仍被草稿模型 top-(m)候选覆盖的情况提供了精确和仅边际证书。

rss · arXiv Speculative Decoding · 6月29日 13:14

**背景**: 投机解码通过使用快速草稿模型提出候选令牌，然后由更大的目标模型验证，从而加速大语言模型推理。标准理论假设分布保持的接受采样以精确匹配目标分布，但实际系统通常使用贪婪或宽松接受规则，优先考虑速度而非精确的分布相等性。本文针对这些实际场景进行了理论分析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2502.20704">Fuzzy Speculative Decoding for a Tunable Accuracy-Runtime Tradeoff</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#language model inference`, `#theoretical computer science`, `#machine learning`, `#LLM acceleration`

---