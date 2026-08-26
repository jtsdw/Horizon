---
layout: default
title: "Horizon Summary: 2026-08-26 (ZH)"
date: 2026-08-26
lang: zh
---

> 从 28 条内容中筛选出 5 条重要资讯。

---

1. [OpenAI 的 Jalapeño 芯片树立 AI 推理速度与效率新标杆](#item-1) ⭐️ 9.0/10
2. [llama.cpp v0.3.0 新增多模态、MTP 和 tensor-split 支持](#item-2) ⭐️ 8.0/10
3. [FDA 批准首款连续监测酮体和葡萄糖的可穿戴设备](#item-3) ⭐️ 8.0/10
4. [IBM Granite 4.2 大语言模型：架构、训练与推理模式](#item-4) ⭐️ 8.0/10
5. [量化感知修复：4 位模型性能超越全精度原版](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 的 Jalapeño 芯片树立 AI 推理速度与效率新标杆](https://openai.com/index/jalapeno-first-results) ⭐️ 9.0/10

OpenAI 宣布了与博通合作开发的定制推理芯片 Jalapeño，为 AI 模型提供业界领先的速度和效率。该芯片每个加速器在 MXFP4 下可实现 13.4 petaFLOPS，并采用机架级设计，每机架配备 128 个加速器。 这标志着 OpenAI 进入定制芯片领域，可能减少对 Nvidia GPU 的依赖，重塑 AI 基础设施格局。该芯片专注于推理效率，可能降低大规模 AI 部署的成本和能耗，影响云服务提供商和企业。 该芯片是一款在九个月内开发完成的掩模版尺寸 ASIC，旨在解决数据移动等瓶颈，并平衡计算、内存和网络资源。它采用类似于 Nvidia NVL72 的机架级架构，每个机架包含 128 个 Jalapeño 加速器。

rss · OpenAI Blog · 8月25日 07:00

**背景**: AI 推理，即运行训练好的模型进行预测的过程，随着 AI 应用的普及而成为关键工作负载。传统上，Nvidia H100 等 GPU 同时用于训练和推理，但像 Google TPU 以及现在的 OpenAI Jalapeño 这样的定制芯片旨在专门优化推理，提供更好的每瓦性能和更低的延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/openai-broadcom-jalapeno-inference-chip/">OpenAI and Broadcom unveil LLM-optimized inference chip | OpenAI</a></li>
<li><a href="https://www.theregister.com/systems/2026/08/25/openais-upcoming-jalapeno-chip-looks-like-itll-be-an-inference-beast/5292052">OpenAI's upcoming Jalapeño chip looks like it'll be an inference beast</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/broadcom-and-openai-unveil-custom-built-jalapeno-inference-processor-openais-first-chip-is-a-massive-reticle-sized-asic-built-in-an-ultra-fast-nine-month-development-cycle">Broadcom and OpenAI unveil custom-built Jalapeño inference processor — OpenAI's first chip is a massive reticle-sized ASIC built in an ultra-fast nine-month development cycle | Tom's Hardware</a></li>

</ul>
</details>

**社区讨论**: 社区评论对推理芯片的潜力表示兴奋，将其与早期显卡竞争相提并论。一些人注意到与人类语音的效率对比，另一些人质疑芯片尺寸和性能声明，还有少数人强调 FP4 精度的新颖性。

**标签**: `#AI inference`, `#hardware`, `#OpenAI`, `#chip design`

---

<a id="item-2"></a>
## [llama.cpp v0.3.0 新增多模态、MTP 和 tensor-split 支持](https://github.com/ggml-org/llama.cpp/releases/tag/v0.3.0) ⭐️ 8.0/10

llama.cpp v0.3.0 引入了对 dots3-note 多模态模型的支持，并新增了 DSA-ISWA KV 缓存类型；为 GLM-4.5-Air 增加了多 token 预测（MTP）支持；为 DeepSeek 4 启用了通过 `-sm tensor` 的 tensor-split 模式。该版本还将 ggml 升级到 v0.22.0，其中包含 meta-backend tensor split 和带并行编译的逐算子 Metal 内核。 此版本显著扩展了 llama.cpp 的功能，使其在本地硬件上运行 GLM-4.5-Air 和 DeepSeek 4 等先进模型时更加灵活。新的多模态支持和性能优化将使依赖 llama.cpp 进行高效 LLM 推理的开发者和研究人员受益。 DSA-ISWA KV 缓存是为 dots3-note 模型引入的新缓存类型，可能提供更好的内存效率。DeepSeek 4 的 tensor-split 模式允许将模型层分布到多个 GPU 上，并且该版本还修复了多序列回滚问题。此外，服务器新增了 `LLAMA_SERVER_SLOTS_N_DIFF` 调试旋钮，Web UI 现在支持标签式聊天导航。

github · github-actions[bot] · 8月25日 10:22

**背景**: llama.cpp 是一个流行的开源 C++ 库，用于在本地以优化性能运行大型语言模型（LLM）。多 token 预测（MTP）是一种模型同时预测多个未来 token 的技术，可提高推理速度。张量分割是一种将模型分布到多个 GPU 上的方法，以处理超出单个 GPU 内存的模型。ggml 库是 llama.cpp 使用的底层张量库，用于高效计算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://korshunov.ai/en/article/20686-llama-cpp-0-3-0-adds-dots3-note-model-and-tensor-split-for-deepseek-4/">llama.cpp 0.3.0 adds dots3-note model and tensor-split for DeepSeek 4</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp/blob/master/docs/multi-gpu.md">llama . cpp /docs/multi-gpu.md at master · ggml-org/ llama . cpp · GitHub</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-4.5-Air-FP8">zai-org/GLM-4.5-Air-FP8 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#LLM inference`, `#multimodal`, `#ggml`, `#release`

---

<a id="item-3"></a>
## [FDA 批准首款连续监测酮体和葡萄糖的可穿戴设备](https://www.fda.gov/news-events/press-announcements/fda-authorizes-first-wearable-device-continuously-monitors-both-ketone-levels-and-blood-sugar) ⭐️ 8.0/10

美国 FDA 已批准首款可穿戴设备 Libre Duo 10 Day，该设备可在单一设备中连续监测酮体水平和血糖（葡萄糖）。这是美国批准的首款此类设备，也是全球首款将两者结合的设备。 此次批准是一个重要的监管里程碑，可能通过提供葡萄糖和酮体的实时数据来改变糖尿病管理，有助于预防糖尿病酮症酸中毒等危险状况。这也可能为更集成的可穿戴健康监测设备铺平道路。 该设备像连续血糖监测仪（CGM）一样植入皮下，提供连续读数。尽管它带来了显著益处，但一些专家指出，酮体监测可能对特定人群（如极低碳水饮食者或血糖控制不佳者）最有用，而非普通糖尿病患者。

hackernews · sunnynagra · 8月25日 19:07 · [社区讨论](https://news.ycombinator.com/item?id=49439017)

**背景**: 连续血糖监测仪（CGM）是一种小型可穿戴传感器，可实时追踪血糖水平，帮助糖尿病患者管理病情。酮体是身体燃烧脂肪产生能量时生成的化学物质，水平升高可能表明出现严重的并发症——糖尿病酮症酸中毒（DKA）。此前，酮体监测需要指尖采血或尿试纸，而这款新设备将葡萄糖和酮体监测集成到一个可穿戴设备中，提供更全面的代谢健康信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fda.gov/news-events/press-announcements/fda-authorizes-first-wearable-device-continuously-monitors-both-ketone-levels-and-blood-sugar">FDA Authorizes First Wearable Device That Continuously Monitors ...</a></li>
<li><a href="https://www.healthcentral.com/news/type-1-diabetes/continuous-ketone-monitoring">Why Experts Say Continuous Ketone Monitoring Is the Next Frontier...</a></li>
<li><a href="https://www.npr.org/2025/06/11/nx-s1-5418465-e1/should-you-track-your-blood-sugar-with-a-continuous-glucose-monitor">Should you track your blood sugar with a continuous glucose monitor ?</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了个人情感、技术怀疑和实际担忧的混合情绪。一位用户分享了一位朋友因糖尿病酮症酸中毒去世的个人故事，并对这一进展表示感激。另一位用户对无创血糖传感持怀疑态度，但欢迎这一新工具，并希望改善报销问题。一些人质疑“可穿戴”一词，因为它是植入皮下的，还有人指出酮体监测可能对控制良好的普通糖尿病患者用处不大。

**标签**: `#FDA`, `#wearable`, `#diabetes`, `#healthtech`, `#medical devices`

---

<a id="item-4"></a>
## [IBM Granite 4.2 大语言模型：架构、训练与推理模式](https://huggingface.co/blog/ibm-granite/granite-4-2) ⭐️ 8.0/10

IBM 发布了 Granite 4.2 系列大语言模型，提供 3B、8B 和 30B 三种尺寸，引入了显式推理能力，支持思维链生成以及多种思考模式（思考、非思考、低努力）。这些模型共享统一的架构和训练流程，包括从零预训练、监督微调以及多阶段强化学习。 此次发布标志着 IBM 在企业级大语言模型中引入显式推理能力的重要进展，有望提升复杂任务的表现，同时在计算成本上提供灵活性。这增强了 IBM 在竞争激烈的 AI 领域的地位，为企业提供更高效、更强大的模型。 Granite 4.2 模型可以在思考或非思考模式下运行，并设有低努力模式，为简单问题分配较短的推理预算。该架构基于 Granite 4.0 中引入的混合 Mamba-2/Transformer 设计，结合注意力层和状态空间层以提高效率。

rss · Hugging Face Blog · 8月25日 15:14

**背景**: Granite 是 IBM 的 decoder-only AI 基础模型系列，训练数据涵盖互联网文本、学术出版物、代码以及法律和金融文档。早期的 Granite 版本是强大的指令跟随助手，Granite 4.2 增加了显式推理能力。混合架构采用大部分 Mamba-2 层和少量 transformer 注意力层，旨在平衡性能和计算效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/ibm-granite/granite-4-2">Granite 4.2 LLMs: How They're Built</a></li>
<li><a href="https://www.ibm.com/new/announcements/ibm-granite-4-0-hyper-efficient-high-performance-hybrid-models">IBM Granite 4.0: Hyper-efficient, High Performance Hybrid Models for Enterprise</a></li>
<li><a href="https://en.wikipedia.org/wiki/IBM_Granite">IBM Granite - Wikipedia</a></li>

</ul>
</details>

**标签**: `#LLM`, `#IBM`, `#Hugging Face`, `#model architecture`, `#AI research`

---

<a id="item-5"></a>
## [量化感知修复：4 位模型性能超越全精度原版](https://huggingface.co/blog/MultiverseComputingCAI/quantization-aware-healing) ⭐️ 8.0/10

一种名为“量化感知修复”的新方法生成了一个 4 位压缩模型，其性能超越了全精度原始模型。该方法应用于将 GPT-OSS 120B 模型压缩至 60B 参数时，比传统的量化感知训练恢复性能更快、更稳定。 这一进展可能显著提高模型压缩效率，使得在资源受限的设备上部署高性能模型成为可能。它挑战了模型大小与准确性之间的传统权衡，可能重塑大型语言模型在实际应用中的优化方式。 该方法直接从原始未压缩模型进行蒸馏，而不是在前向传播中插入伪量化器。它实现了 4 位量化，通常可提供 8 倍压缩和 3.7 倍计算增益，但性能恢复效果更好。

rss · Hugging Face Blog · 8月25日 11:39

**背景**: 量化是一种将模型中的数字精度从 32 位浮点数降低到 4 位整数等技术，以减少内存和计算需求。传统的量化感知训练（QAT）在前向传播中插入伪量化器，并在任务损失下继续训练，但可能面临不稳定性或收敛速度慢的问题。量化感知修复提供了一种替代方案，通过从原始模型进行蒸馏，可能保留更多原始模型的知识。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.20953v1">Quantization - Aware Healing : A Practical Recipe for Recovering...</a></li>
<li><a href="https://paperswithcode.co/paper/2608.20953">Quantization - Aware Healing : A Practical Recipe... | Papers with Code</a></li>
<li><a href="https://huggingface.co/papers/2608.20953">Paper page - Quantization - Aware Healing : A Practical Recipe for...</a></li>

</ul>
</details>

**标签**: `#quantization`, `#model compression`, `#AI/ML`, `#efficiency`

---