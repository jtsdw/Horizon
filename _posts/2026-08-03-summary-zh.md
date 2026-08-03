---
layout: default
title: "Horizon Summary: 2026-08-03 (ZH)"
date: 2026-08-03
lang: zh
---

> 从 20 条内容中筛选出 2 条重要资讯。

---

1. [阿里 Qwen 发布 Qwen3.8-27B 和 Qwen3.8-Max](#item-1) ⭐️ 8.0/10
2. [中国 DFSX 宣称内存带宽为英伟达 GB200 的两倍](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [阿里 Qwen 发布 Qwen3.8-27B 和 Qwen3.8-Max](https://www.reddit.com/r/LocalLLaMA/comments/1ve0psn/qwen3827b_announced_alongside_qwen38max/) ⭐️ 8.0/10

阿里巴巴 Qwen 团队宣布了两款新模型：Qwen3.8-27B，一个拥有 270 亿参数的密集多模态模型，以及 Qwen3.8-Max，一个拥有 2.4 万亿参数的旗舰模型。该公告通过官方 Alibaba_Qwen 账号的推文发布。 Qwen3.8-27B 的发布对本地部署意义重大，因为其规模在性能和资源需求之间取得了平衡，使开发者和研究人员更容易使用。Qwen3.8-Max 凭借其庞大的规模和多模态能力，突破了 AI 的可能性边界，可能对依赖大规模语言模型的行业产生影响。 Qwen3.8-27B 支持原生 262,144 个 token 的上下文长度，可扩展至 1,010,000 个 token，并采用门控 delta 网络混合注意力和 MTP。Qwen3.8-Max 是 Qwen 首个超过 1 万亿参数、能同时处理图像、视频和文档的模型，具有 100 万上下文长度和三种缓存模式。

reddit · r/LocalLLaMA · /u/TKGaming_11 · 8月3日 02:21

**背景**: Qwen 是阿里巴巴开发的一系列大型语言模型，以其强大的性能和开源可用性而闻名。Qwen3.8 系列代表了演进，其中 27B 模型面向本地部署，Max 模型则追求最先进的能力。该公告是 AI 公司发布越来越强大且具备多模态能力的模型的更广泛趋势的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.6-27B">Qwen/Qwen3.6-27B · Hugging Face</a></li>
<li><a href="https://evolink.ai/blog/qwen3-8-max-preview-features">Qwen3.8 Features, Token Plan & Release Status (2026)</a></li>
<li><a href="https://aitoolsreview.co.uk/insights/qwen-3-8-max">Qwen 3.8 Max Review: Alibaba's 2.4T Model, Tested</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Qwen`, `#AI`, `#Model Release`

---

<a id="item-2"></a>
## [中国 DFSX 宣称内存带宽为英伟达 GB200 的两倍](https://www.reddit.com/r/LocalLLaMA/comments/1vduej3/chinas_dfsx_offers_2x_the_memory_bandwidth_of/) ⭐️ 8.0/10

中国的 DFSX 推出了基于 14 纳米 DF2000 芯片的 TY64 SuperNode，据报道其内存带宽达到 960TB/s，是英伟达 GB200 NVL72 系统 576TB/s 的两倍。这一发布将 DFSX 定位为 AI 硬件市场的潜在挑战者。 这一进展意义重大，因为它表明中国本土 AI 硬件尽管采用较旧的 14 纳米制程技术，但在内存带宽这一对 AI 训练和推理性能至关重要的指标上，可以与领先设计竞争甚至超越。如果得到验证，它可能改变竞争格局，并减少中国市场对英伟达的依赖。 DFSX TY64 SuperNode 由 DF2000 芯片组成，实现了 960TB/s 的内存带宽，而英伟达 GB200 NVL72 为 576TB/s。此前发布的 DF1000 芯片在 BF16 下提供 520 TFLOPS、6.4TB/s 内存带宽和 900GB/s 扩展互连带宽，全部基于 14 纳米工艺。

reddit · r/LocalLLaMA · /u/MundanePercentage674 · 8月2日 21:39

**背景**: 内存带宽对 AI 加速器至关重要，因为它决定了数据馈送到计算单元的速度，直接影响训练和推理速度。英伟达 GB200 采用先进的 HBM3e 内存和 4 纳米工艺，而 DFSX 的 14 纳米芯片通过创新的封装技术（如跳过微凸块的垂直计算-内存塔）实现了更高的带宽。这凸显了一种克服制程技术限制的潜在替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wccftech.com/chinas-dfsx-offers-2x-the-memory-bandwidth-of-nvidias-gb200-nvl72-system-with-a-14nm-supernode-that-skips-microbumps-for-vertical-compute-memory-towers/">China's DFSX Offers 2x The Memory Bandwidth Of NVIDIA's ... - Wccftech</a></li>
<li><a href="https://hellochinatech.com/p/dfsx-14nm-ai-chip-wager">Can China's 14nm AI Chip Challenge 4nm Designs?</a></li>
<li><a href="https://www.nexgencloud.com/blog/case-studies/nvidia-gb200-user-guide-specs-features-and-use-cases">NVIDIA GB200 User Guide: Specs, Features and Use Cases</a></li>

</ul>
</details>

**标签**: `#hardware`, `#AI`, `#memory bandwidth`, `#China`, `#NVIDIA`

---