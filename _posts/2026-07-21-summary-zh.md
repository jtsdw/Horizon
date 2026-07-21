---
layout: default
title: "Horizon Summary: 2026-07-21 (ZH)"
date: 2026-07-21
lang: zh
---

> 从 46 条内容中筛选出 8 条重要资讯。

---

1. [黑客清空罗马尼亚土地登记数据库](#item-1) ⭐️ 9.0/10
2. [中国开源 AI 模型挑战西方定价策略](#item-2) ⭐️ 8.0/10
3. [OpenAI 分享长期运行 AI 模型的安全经验](#item-3) ⭐️ 8.0/10
4. [NVIDIA 推出面向边缘 AI 的 Cosmos 3 Edge](#item-4) ⭐️ 8.0/10
5. [FlashRT：用于实时多模态部署的智能体框架](#item-5) ⭐️ 8.0/10
6. [HyMCache：利用 CXL 混合内存高效扩展 KV 缓存](#item-6) ⭐️ 8.0/10
7. [SelectInfer：面向设备端 LLM 的选择性神经元加载](#item-7) ⭐️ 8.0/10
8. [MXSens：面向 LLM 的敏感度感知混合精度量化](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [黑客清空罗马尼亚土地登记数据库](https://news.risky.biz/risky-bulletin-hacker-wipes-romanias-entire-land-registry-database/) ⭐️ 9.0/10

一名黑客清空了罗马尼亚整个土地登记数据库，但离线备份可能避免了财产记录的灾难性丢失。 此事件凸显了关键政府基础设施的脆弱性，以及丢失土地所有权记录可能导致的混乱，影响数百万房产所有者。 黑客被确认为来自阿尔及利亚的 Zakaria Mahdjoub，声称已删除备份，但该机构似乎拥有离线副本。官员们正在从头重建网络并迁移至罗马尼亚政府云。

hackernews · speckx · 7月20日 13:28 · [社区讨论](https://news.ycombinator.com/item?id=48978605)

**背景**: 土地登记数据库对于证明财产所有权和促进房地产交易至关重要。离线备份（也称为气隙备份）存储在不连接互联网的设备上，可防范勒索软件和远程攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Online_Backup">Online Backup</a></li>
<li><a href="https://www.linkedin.com/posts/technologyparadises_why-keeping-offline-backup-copies-still-matters-activity-7448625941800607744-1YME">Why Keeping Offline Backup Copies Still Matters in a Cloud-First...</a></li>

</ul>
</details>

**社区讨论**: 社区评论认为此次黑客攻击可能与政府 IT 合同中的腐败有关，关系户未能实施适当的安全措施。还讨论了黑客的身份以及阿尔及利亚与罗马尼亚之间的引渡条约。

**标签**: `#cybersecurity`, `#data breach`, `#infrastructure`, `#ransomware`, `#government`

---

<a id="item-2"></a>
## [中国开源 AI 模型挑战西方定价策略](https://stratechery.com/2026/whos-afraid-of-chinese-models/) ⭐️ 8.0/10

中国开源 AI 模型（如阿里巴巴的 Qwen-Image）通过免费提供接近前沿的能力，削弱了 OpenAI 和 Anthropic 等西方前沿实验室的溢价 API 定价策略。 这可能重塑 AI 行业的经济格局，迫使西方实验室降价，并可能降低其基于溢价定价假设的天价估值——Anthropic 估值 1.2 万亿美元，OpenAI 目标 8500 亿美元。 MIT 的一项研究发现，中国开源模型的总下载量已超过美国模型，开发者现在可以以低成本或零成本获得接近前沿的 AI 能力，增加了西方实验室的竞争压力。

hackernews · mfiguiere · 7月20日 11:05 · [社区讨论](https://news.ycombinator.com/item?id=48977128)

**背景**: OpenAI 和 Anthropic 等西方前沿 AI 实验室一直依赖溢价 API 定价和高订阅费来支撑其巨额估值。阿里巴巴等中国公司免费发布强大的开源模型，旨在将 AI 软件商品化并抢占生态系统份额。这一策略威胁到西方实验室的收入模式，并可能导致价格战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://qwenimages.com/">Qwen-Image - Alibaba's Open - Source AI Image Generation Model ...</a></li>
<li><a href="https://www.linkedin.com/posts/spollak_whats-next-for-chinese-open-source-ai-activity-7436413066386452480-ueoY">China 's Open Source AI Models Gain Momentum | LinkedIn</a></li>
<li><a href="https://www.centific.com/blog/ai-token-consumption-costs">The 25x subscription trap: why frontier labs can no longer subsidize your AI - Centific</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，以高估值投资 Anthropic 和 OpenAI 的风险投资家最为担忧，因为中国模型削弱了其溢价定价的前提。一些人注意到地缘政治风险，例如中国模型可能包含关于台湾和香港的偏见信息。另一些人则认为模型切换成本很低，并引用个人轻松在 Claude Code 和 Codex 之间切换的经历。

**标签**: `#AI`, `#Chinese AI models`, `#Open source`, `#Valuation`, `#Geopolitics`

---

<a id="item-3"></a>
## [OpenAI 分享长期运行 AI 模型的安全经验](https://openai.com/index/safety-alignment-long-horizon-models) ⭐️ 8.0/10

OpenAI 发布了一份报告，详细介绍了长期运行 AI 模型的部署经验，指出了目标泛化错误和奖励黑客等新的安全风险，并描述了通过迭代部署改进的防护措施。 随着 AI 系统越来越多地处理长时间、多步骤的复杂任务，理解和缓解新的安全风险对于负责任地部署和建立对 AI 的信任至关重要。 报告涵盖了长期运行模型中观察到的失败，如子目标执着和意外副作用，并详细介绍了新的对齐技术，包括针对长序列的奖励塑形和对抗训练。

rss · OpenAI Blog · 7月20日 10:00

**背景**: 长期运行模型是旨在长时间自主执行任务的 AI 系统，不同于响应单个提示即结束的经典模型。安全与对齐旨在引导 AI 系统朝着预期目标和伦理原则发展，随着任务持续时间的增加，这一挑战变得更加严峻。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://24-ai.news/en/news/2026-07-20/openai-long-horizon-model-safety/">OpenAI: Long - Horizon AI Model Safety | 24 AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#alignment`, `#long-horizon models`, `#deployment`, `#OpenAI`

---

<a id="item-4"></a>
## [NVIDIA 推出面向边缘 AI 的 Cosmos 3 Edge](https://huggingface.co/blog/nvidia/cosmos3edge) ⭐️ 8.0/10

NVIDIA 发布了 Cosmos 3 Edge，这是一系列针对边缘优化的视觉模型，专为在 Jetson 等设备上高效推理而设计。这些模型通过共享多模态注意力机制，结合了自回归和扩散 transformer 模块，能够在单一模型中实现感知、预测、模拟和行动。 此次发布将强大的世界模型能力直接带到边缘设备，减少了对云连接的依赖，并支持机器人和自主系统的实时决策。它显著降低了在资源受限环境中部署先进 AI 的门槛。 Cosmos 3 Edge 是一个 40 亿参数的世界模型，可在 NVIDIA Jetson 边缘设备上运行，提供高达 275 TOPS 的性能。它于 2026 年 7 月 16 日在东京发布，并作为开放模型在 Hugging Face 上提供。

rss · Hugging Face Blog · 7月20日 15:58

**背景**: 边缘 AI 是指在设备本地而非云端运行人工智能算法，从而实现低延迟和隐私保护的应用。NVIDIA 的 Jetson 平台是一系列专为边缘 AI 设计的嵌入式计算板，广泛应用于机器人、工业物联网和智慧城市。世界模型是能够理解和预测环境的 AI 系统，结合感知与模拟实现自主决策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://unrollnow.com/status/2079236204743053592">Thread By @NVIDIAAI - Introducing Cosmos 3 Edge : our open...</a></li>
<li><a href="https://spoonai.me/posts/2026-07-19-nvidia-cosmos3-edge-robot-world-model-jul2026-en">Nvidia put a world model inside the robot itself — Cosmos 3 Edge , and...</a></li>
<li><a href="https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/jetson-nano/product-development/">Jetson Nano Brings the Power of Modern AI to Edge Devices | NVIDIA</a></li>

</ul>
</details>

**标签**: `#edge AI`, `#computer vision`, `#NVIDIA`, `#model optimization`, `#Jetson`

---

<a id="item-5"></a>
## [FlashRT：用于实时多模态部署的智能体框架](https://arxiv.org/abs/2607.18171v1) ⭐️ 8.0/10

FlashRT 是一个智能体框架，采用链式编程范式引导编码智能体将简单的参考实现自动转化为优化的多 GPU 部署，用于实时多模态应用。 这填补了服务系统中的一个关键空白，通过自动化多模态 AI 流水线中复杂的、特定于应用的部署决策，在 NVIDIA B200 GPU 上可实现高达 70 倍的延迟降低和 2.8 倍的吞吐量提升。 FlashRT 生成中间表示（IR）以捕获数据依赖和持久状态范围，通过顺序解释器进行验证，然后在测量门控循环中迭代优化部署。在 AMD MI355X GPU 上，它实现了高达 3.6 倍的吞吐量提升，并达到了相同的峰值延迟降低。

rss · arXiv LLM Inference · 7月20日 17:12

**背景**: 实时多模态应用（如语音智能体和交互式视频生成）将多个 AI 模型组合成流水线，需要仔细的放置、流式传输和并行化决策才能高效部署。现有的服务系统和自动并行编译器通常依赖固定假设，迫使开发者为每个新应用手动优化。智能体框架是围绕模型构建的系统，使其成为功能型智能体，为工具使用和决策提供基础设施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/aws/what-is-an-agent-harness-a-hands-on-guide-with-agentcore-harness-1h33">What is an Agent Harness? A Hands-On Guide With AgentCore harness - DEV Community</a></li>
<li><a href="https://www.langchain.com/blog/the-anatomy-of-an-agent-harness">The Anatomy of an Agent Harness</a></li>
<li><a href="https://github.com/HKUDS/OpenHarness">GitHub - HKUDS/OpenHarness: "OpenHarness: Open Agent Harness with a Built-in Personal Agent--Ohmo!" · GitHub</a></li>

</ul>
</details>

**标签**: `#multimodal AI`, `#serving systems`, `#agent harness`, `#real-time deployment`, `#parallelism`

---

<a id="item-6"></a>
## [HyMCache：利用 CXL 混合内存高效扩展 KV 缓存](https://arxiv.org/abs/2607.18141v1) ⭐️ 8.0/10

HyMCache 是一个 KV 缓存框架，利用 CXL 混合内存（CXL-HM）高效扩展基于 SSD 的 KV 复用，用于多轮 LLM 服务，在相同 DRAM 预算下比本地 LMCache 实现 3.0 倍加速。 这解决了 LLM 服务中的关键内存瓶颈，以 SSD 级别的成本实现 TB 级 KV 缓存复用，在保持性能的同时大幅降低 DRAM 需求，对扩展长上下文和智能体工作负载至关重要。 HyMCache 使用请求级前缀预取和机会性写缓冲将延迟关键读取暂存到设备 DRAM 中，与 1 TB 分布式 DRAM Mooncake 相比，性能低约 30%，但 DRAM 使用量减少 16 倍。

rss · arXiv LLM Inference · 7月20日 16:35

**背景**: KV 缓存存储先前 token 的键值对以避免 LLM 推理中的重复计算，但会消耗大量内存（例如，70B 模型处理 128K 上下文时需 40GB 以上）。CXL 混合内存通过 CXL 接口将少量 DRAM 与大容量 SSD 结合，提供经济高效的内存层级。HyMCache 利用多轮 KV 缓存的读主导、可预测和仅追加访问模式来优化 CXL-HM 的使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/pc-components/cpus/worlds-first-hybrid-cxl-device-combines-flash-memory-and-dram-storage-tiering-comes-to-remote-memory-over-pcie">World's first hybrid CXL device combines flash memory and DRAM — storage tiering comes to remote memory over PCIe | Tom's Hardware</a></li>
<li><a href="https://en.wikipedia.org/wiki/Compute_Express_Link">Compute Express Link - Wikipedia</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#KV-cache`, `#CXL memory`, `#memory hierarchy`, `#systems`

---

<a id="item-7"></a>
## [SelectInfer：面向设备端 LLM 的选择性神经元加载](https://arxiv.org/abs/2607.18081v1) ⭐️ 8.0/10

SelectInfer 提出了一种神经元级优化框架，在边缘设备上的 LLM 推理过程中仅选择性加载和计算重要神经元，无需重新训练即可减少内存和计算量。 这项工作直接解决了阻碍大语言模型在资源受限边缘设备上运行的内存和计算瓶颈，有望在手机和物联网设备上实现私密、低延迟的 AI 应用。 SelectInfer 使用离线分析器识别任务特定神经元和通用神经元，然后应用选择性加载以减少内存占用，并在运行时动态计算仅相关的神经元。

rss · arXiv LLM Inference · 7月20日 15:48

**背景**: 大语言模型（LLM）需要大量内存和计算资源，使其在边缘设备上部署面临挑战。传统的剪枝和量化等压缩方法通常需要重新训练或牺牲准确性。神经元级优化提供了更细的粒度，有望在减少资源消耗的同时保持模型性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openreview.net/forum?id=3sbM94O8Ts">PartInfer: Enabling LLM Inference On Edge Devices | OpenReview</a></li>

</ul>
</details>

**标签**: `#LLM`, `#edge computing`, `#model optimization`, `#neuron pruning`, `#efficient inference`

---

<a id="item-8"></a>
## [MXSens：面向 LLM 的敏感度感知混合精度量化](https://arxiv.org/abs/2607.17733v1) ⭐️ 8.0/10

MXSens 提出了一种无需训练、敏感度引导的混合精度量化方法，根据列和层对异常值的敏感度分配不同的尾数位宽（4/6/8），并利用硬件友好的 MXINT 格式。 这项工作解决了 4 位 LLM 量化中因异常值导致的精度严重下降问题，在 LLaMA-2-70B 和 LLaMA-3-8B 等大模型上取得了最先进的困惑度，对于在资源受限环境中高效部署 LLM 至关重要。 在 W4A4KV4 设置下，MXSens 在 WikiText-2 上对 LLaMA-2-70B 和 LLaMA-3-8B 分别实现了 3.77 和 7.63 的困惑度，显著优于现有基线。该方法无需训练，并利用了 MXINT 格式的块状结构。

rss · arXiv LLM Inference · 7月20日 09:23

**背景**: 4 位量化可减少 LLM 推理的内存和计算，但会因异常值（激活值或权重中异常大的值）导致精度损失。先前的方法如数据旋转或混合精度整数量化通常带来软件开销。MXINT 格式在硬件中编码缩放因子，实现高效推理，但与基于旋转的异常值缓解方法不兼容。MXSens 将敏感度分析与 MXINT 的块状结构相结合，无需训练即可分配可变的尾数位宽。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/microsoft/microxcaling">GitHub - microsoft/microxcaling: PyTorch emulation library for Microscaling (MX)-compatible data formats · GitHub</a></li>
<li><a href="https://arxiv.org/html/2405.07135v3">Post Training Quantization of Large Language Models with Microscaling Formats</a></li>
<li><a href="https://openreview.net/forum?id=rLX7Vyyzus">Systematic Outliers in Large Language Models | OpenReview</a></li>

</ul>
</details>

**标签**: `#LLM`, `#quantization`, `#efficient inference`, `#mixed-precision`, `#MXINT`

---