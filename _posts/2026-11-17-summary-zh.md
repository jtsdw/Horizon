---
layout: default
title: "Horizon Summary: 2026-11-17 (ZH)"
date: 2026-11-17
lang: zh
---

> 从 63 条内容中筛选出 5 条重要资讯。

---

1. [CompCert4Lean 借助并行 LLM 智能体六周内将经过验证的 C 编译器移植到 Lean](#item-1) ⭐️ 9.0/10
2. [vLLM v0.34.0 发布：默认启用可扩展 KV 缓存，移除 Model Runner V1](#item-2) ⭐️ 8.0/10
3. [卡内基梅隆大学推出 CS Learn，在 YouTube 免费提供计算机科学课程讲座](#item-3) ⭐️ 8.0/10
4. [System 1 智能体：本地、可靠、快速且无幻觉工具调用的智能体 AI](#item-4) ⭐️ 8.0/10
5. [ProcReverser：多智能体系统实现黑盒微架构逆向工程自动化](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [CompCert4Lean 借助并行 LLM 智能体六周内将经过验证的 C 编译器移植到 Lean](https://arxiv.org/abs/2611.21084v1) ⭐️ 9.0/10

CompCert4Lean 在约六周内将 CompCert 3.17 的已验证编译器核心从 Rocq 移植到 Lean，由一位专家指挥多个并行 LLM 智能体完成。该移植在不引入项目特定公理的情况下完成了全部 4,908 个证明义务，并生成了可执行的 Linux 二进制文件。 这展示了一种高效的 AI 辅助形式化验证工作流，表明并行 LLM 智能体可以在有限的人工技术指导下支持大规模迁移。它对已验证软件和智能体驱动开发具有重大意义，可能降低移植和维护形式化验证系统的门槛。 在 1,071 次人工交互中，88.8% 涉及工作流和协调，只有三次提供了技术方向。在匹配的 24 小时预算优化活动中，GPT-6-astra 生成的 Lean 候选在 29 个小测试程序上使生成程序运行时间降低 11.7%，而其 Rocq 候选仅降低 2.3%，同时保持了端到端正确性定理。

rss · arXiv Agent Infra · 11月16日 13:32

**背景**: CompCert 是一个经过形式化验证的 C 编译器，其正确性由证明助手进行机器检查，广泛用于安全关键软件。Lean 是一个现代的证明助手和函数式编程语言，而 Rocq 是 Coq 定理证明器自 2024 年起的更名。证明义务是完成形式化正确性证明所需完成的各个引理和条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://compcert.org/">CompCert - Main page</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://github.com/AbsInt/CompCert">AbsInt/ CompCert : The CompCert formally- verified C compiler · GitHub</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#LLM agents`, `#CompCert`, `#Lean`, `#verified compilation`

---

<a id="item-2"></a>
## [vLLM v0.34.0 发布：默认启用可扩展 KV 缓存，移除 Model Runner V1](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM v0.34.0 正式发布，包含来自 412 位贡献者的 1,061 次提交，新增 Mistral Large 4、MiniMax-M3.1-Flash 等 10 个模型，默认启用可扩展 KV 缓存，移除 Model Runner V1，并在 Blackwell 和 MI355X 硬件上实现最高 1.95 倍的解码加速。 作为使用最广泛的开源 LLM 推理引擎之一，vLLM 默认切换到更大、基于实际空闲显存的 KV 缓存，可直接提升高并发服务下的吞吐量并降低首 token 延迟，影响所有在 NVIDIA 或 AMD GPU 上部署模型的用户。同时，移除 Model Runner V1 等多项破坏性变更也迫使运维人员在升级前审查现有配置。 新的 KV 缓存大小基于 CUDA 图捕获和预热后实际空闲的显存来计算，使 MiniMax-M3 在 H200 上的缓存从 433k 增至 672k token，但在并发 128 时部分 H200 模型的单 token 解码延迟可能上升 6–18%；用户可通过 --gpu-memory-utilization 0.9 或 --no-enable-extensible-kv-cache 退出该特性。其他破坏性变更包括默认块大小改为 64（原为 16）、不再发布 ROCm 7.2 产物、要求 huggingface_hub >= 2.0.0，以及移除 QuTLASS/fp_quant 和 Marlin W4A8。

github · khluu · 11月16日 23:22

**背景**: vLLM 是一个围绕 PagedAttention 构建的开源 LLM 服务引擎，该注意力算法受操作系统虚拟内存分页启发，将键值（KV）缓存分块存储，以最大限度减少内存浪费并支持跨请求灵活共享。KV 缓存保存历史注意力的键和值，避免模型重复计算，其大小直接决定可同时服务的并发请求数。Model Runner 是负责模型前向计算、CUDA 图捕获和采样的执行核心；vLLM 一直在从最初的 V1 运行器迁移到更清晰、更模块化的 V2 实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/paged_attention/">Paged Attention - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V 2 Design Document - vLLM</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/gb200-nvl72/">GB200 NVL72 | NVIDIA</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#release`, `#kv-cache`, `#gpu-performance`

---

<a id="item-3"></a>
## [卡内基梅隆大学推出 CS Learn，在 YouTube 免费提供计算机科学课程讲座](https://www.cs.cmu.edu/learn/) ⭐️ 8.0/10

卡内基梅隆大学推出了 CS Learn，在 YouTube 上免费发布当前计算机科学课程完整学期的讲座，本周每天首播一门课程，明年一月还将推出更多课程。 这是一个重要的开放教育里程碑，因为顶尖计算机科学项目分享了当前完整学期的课程内容，而不仅仅是入门级 MOOC，可能在全球范围内扩大高质量计算机科学教育的可及性。 该计划由卡内基梅隆大学格里芬计算机科学学院的 Phillip Compeau 领导，学生开发了自动化大部分制作流程的工具；接下来计划提供包括项目和反馈机制在内的课程材料。

hackernews · pcompeau · 11月16日 20:43 · [社区讨论](https://news.ycombinator.com/item?id=50522980)

**背景**: 开放教育有着悠久历史，麻省理工学院的 OpenCourseWare 于 25 年前推出，edX 和 freeCodeCamp 等平台汇集了数千门免费课程。CS Learn 的不同之处在于发布当前 CMU 课程完整学期的讲座，而不仅仅是存档或入门材料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/@CMULearn">CS Learn at Carnegie Mellon - YouTube</a></li>
<li><a href="https://www.freecodecamp.org/news/free-courses-top-cs-universities/">1200 Free Computer Science Courses from the World’s Top ... Computer Science | MIT Learn edX | Online Courses, Certificates & Degrees from Leading ... 860+ Free Online Programming & Computer Science Courses You ... Computer Science - Open Educational Resources (OER ... Introductory Programming | MIT OpenCourseWare | Free Online ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍热情，讲师参与讨论，校友们请求开设特定课程。一个关键辩论集中在 AI 时代基础知识是否仍然重要，一条高赞评论认为扎实学习基础知识能让 AI 成为强大的工具，而其他人则强调仅有讲座而没有项目和反馈是不够的。

**标签**: `#education`, `#computer-science`, `#open-education`, `#online-learning`, `#CMU`

---

<a id="item-4"></a>
## [System 1 智能体：本地、可靠、快速且无幻觉工具调用的智能体 AI](https://arxiv.org/abs/2611.21053v1) ⭐️ 8.0/10

研究人员提出了一种构建“System 1”智能体的方法，该智能体不生成自由文本即可调用工具：通过确定性编译器将每个工具的 schema 和用户请求转换为多项选择题，再由单遍决策模型作答。在针对 157 个生物医学工具的 1,952 个请求上，最佳 System 1 智能体选择正确工具或正确拒绝的准确率达到 97.0%，优于所有 18 种本地 LLM 智能体设置（最佳 95.2%），并在 6,056 个声明的参数值中填充了 97.0%，且零虚构内容。 该方法解决了临床 AI 中关键的可靠性和隐私问题：云端 LLM 会暴露患者数据，而本地 LLM 会产生虚构值并传播到后续步骤。通过消除幻觉参数并支持完全本地运行，System 1 智能体有望使智能体 AI 在医疗等敏感领域安全应用。 确定性编译器严格从请求和工具 schema 生成多项选择选项，单遍决策模型直接作答而不生成文本。System 1 调用中没有出现虚构内容，而 LLM 调用中该比例为 5.5–19.7%，该框架已在 GitHub 上作为开源软件免费提供。

rss · arXiv Agent Infra · 11月16日 13:05

**背景**: 智能体 AI 系统利用大语言模型自主规划并调用外部工具，但 LLM 生成的工具调用可能包含幻觉参数，从而破坏下游结果。“System 1”源自双过程认知理论，指快速、自动的决策，与较慢的审慎推理相对。该工作用受限的多项选择格式替代自由文本生成，使本地智能体在处理敏感数据时更加可靠。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://michaelbommarito.com/wiki/ai/agents-definitions/">definitions of agents and agentic ai | mike bommarito</a></li>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/agentic-ai/">Agentic AI - GeeksforGeeks</a></li>
<li><a href="https://www.databricks.com/blog/what-is-agentic-ai">What is Agentic AI? - Databricks</a></li>

</ul>
</details>

**标签**: `#agentic AI`, `#local LLMs`, `#tool calling`, `#clinical AI`, `#reliability`

---

<a id="item-5"></a>
## [ProcReverser：多智能体系统实现黑盒微架构逆向工程自动化](https://arxiv.org/abs/2611.20827v1) ⭐️ 8.0/10

ProcReverser 是一个多智能体系统，通过利用执行反馈迭代设计实验和测试程序，自动完成黑盒微架构逆向工程。它在玄铁 C910 上实现了 81.3% 和 93.8% 的 Pass@1 与 Pass@5 分数，在 gem5 RISC-V O3 CPU 模型上达到 83.0% 和 100.0%，并在 SiFive P550 上刻画了相关微架构特性。 这项工作大幅减少了识别与 Spectre 类攻击相关的硬件条件所需的人工投入，从而能够更快速地对多种处理器进行漏洞分析和防御评估。它凸显了 AI 驱动自动化在硬件安全领域的潜力，尤其是在实现细节通常不公开的 RISC-V 处理器上。 该系统聚焦于推测执行、分支预测、内存依赖和缓存行为等对 Spectre 类攻击至关重要的微架构特性。评估在真实硬件（玄铁 C910、SiFive P550）和模拟的 gem5 O3 CPU 模型上进行，同时展示了实际适用性和基于模拟的验证。

rss · arXiv Agent Infra · 11月16日 10:11

**背景**: 微架构逆向工程是指通过黑盒测量推断处理器内部设计细节（如缓存结构、分支预测器行为和推测执行机制）的过程。这些细节对于理解和缓解 Spectre 等侧信道漏洞至关重要，但传统方法需要大量人工实验。多智能体系统（多个 AI 智能体协作解决复杂任务）最近在自动化此类迭代实验工作流方面展现出潜力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gem5.org/documentation/general_docs/cpu_models/O3CPU">gem5: Out of order CPU model</a></li>
<li><a href="https://chipsandcheese.com/p/alibabat-heads-xuantie-c910">Alibaba/T-HEAD's Xuantie C 910 - by Chester Lam</a></li>
<li><a href="https://pacmanattack.com/code/">Tools for cutting-edge microarchitectural security research on Apple...</a></li>

</ul>
</details>

**标签**: `#microarchitectural reverse engineering`, `#hardware security`, `#multi-agent systems`, `#Spectre attacks`, `#RISC-V`

---