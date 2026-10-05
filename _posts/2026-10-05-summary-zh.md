---
layout: default
title: "Horizon Summary: 2026-10-05 (ZH)"
date: 2026-10-05
lang: zh
---

> 从 28 条内容中筛选出 2 条重要资讯。

---

1. [Strata 让 125B Qwen 3.8 Flash Next 在 RTX 4090 上以 100+ tok/s 运行](#item-1) ⭐️ 8.0/10
2. [Qwen3.5 9B/27B INT4 推理在廉价退役矿机 FPGA 上跑通](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Strata 让 125B Qwen 3.8 Flash Next 在 RTX 4090 上以 100+ tok/s 运行](https://github.com/Niko1221/Strata) ⭐️ 8.0/10

一个名为 Strata 的 GitHub 项目（作者 Niko1221）让 125B 参数的 Qwen 3.8 Flash Next 模型能够在 RTX 4090 等消费级 GPU 上以超过 100 tokens/秒的速度运行，用户报告在 4090 上达到 124 tok/s，在配备 64GB 内存的 5090 上使用低位 GGUF 量化时约为 200 tok/s。 这表明 125B 级别的模型可以在不到 800 美元的消费级硬件上运行，甚至可能胜过量化程度较低的 27B 稠密模型，从而降低了本地 LLM 使用的门槛，并加剧了关于激进量化会损失多少质量的争论。 该方法依赖低位 GGUF 量化（如 iq2_xs 和 Q4 变体），并可在 8GB 显存上运行更小的量化版本；但一位用户的基准测试发现，在相同的 GGUF 和视觉适配器下，Strata 的视觉中位误差为 154.8 像素，而 llama.cpp 为 46.5 像素，暗示可能存在质量权衡。

hackernews · snehesht · 10月4日 12:51 · [社区讨论](https://news.ycombinator.com/item?id=49953495)

**背景**: Qwen 3.8 Flash Next 是一个 125B 参数的混合专家（MoE）模型，激活参数为 A6B，专为具有统一内存或大量系统内存的系统进行本地友好设计。量化通过降低模型权重的数值精度来缩小内存占用并加速推理，但低位量化可能会降低输出质量。Strata 是一个推理栈，将这些低位量化与优化执行相结合，使大型模型能够装入消费级 GPU 显存。

**社区讨论**: Hacker News 的讨论总体上对这一技术成就持积极态度，用户分享了实际吞吐量数据（4090 上 124 tok/s、5090 上约 200 tok/s、RTX 6000 Pro 上解码 255 tok/s），但一些人对低于 4-bit 的量化持怀疑态度，认为质量会下降，且一项基准测试显示 Strata 在视觉任务上不如 llama.cpp。

**标签**: `#LLM inference`, `#quantization`, `#consumer hardware`, `#Qwen`, `#performance benchmarking`

---

<a id="item-2"></a>
## [Qwen3.5 9B/27B INT4 推理在廉价退役矿机 FPGA 上跑通](https://www.reddit.com/r/LocalLLaMA/comments/1wxken1/qwen35_arch_implementation_in_fpga_fabric_for/) ⭐️ 8.0/10

Reddit 用户 u/I_am_purrfect 利用退役加密货币矿机 FPGA 卡，在 FPGA 逻辑中实现了 Qwen3.5 9B/27B INT4 推理，单张 280 美元的 SQRL FK33 即可达到约 2 tok/s 的生成速度，并可扩展到 375 美元的双 FPGA SQRL Jungle Cat 方案。该开源 VHDL 实现（MIT 许可）已逐层与 llama.cpp 对齐验证，并预估 4 片 XCVU35P 在 200 MHz 下可达到约 25 tok/s 的生成速度。 这证明了在本地大模型推理场景中，可以用低成本方案替代稀缺且昂贵的 Nvidia GPU，把退役矿机硬件变成有用的 AI 加速器。它为爱好者和小型实验室以极低成本本地运行前沿级 9B-27B 模型开辟了道路，同时也让 FPGA 推理成为一个值得认真对待的研究方向。 9B 模型在两张 FK33 上以 75 MHz 运行，采用流水线切分并由主机处理残差，预填充约 6 tok/s，生成约 2.4-3.2 tok/s；27B 模型仅根据 9B 的逐算子性能曲线建模，尚未实际运行。两片芯片最多支持约 45k 上下文，因为 27B 的 KV 缓存无法与 14.5 GB 权重共存，要跑满 262k 上下文需要四片芯片；此外 Jungle Cat Lite 板缺少 GTY 时钟生成电路，需要自行焊接元件修复。

reddit · r/LocalLLaMA · /u/I_am_purrfect · 10月4日 16:51

**背景**: FPGA（现场可编程门阵列）是可重新配置的芯片，可以编程实现自定义数字逻辑；像 AMD Virtex UltraScale+ XCVU35P 这样的高端型号带有 HBM2 高带宽内存（约 400 GB/s），非常适合受内存带宽限制的大模型推理。INT4 量化把模型权重压缩到 4 位，相比 FP16 可将内存占用减少约 4 倍，从而让大模型装进小设备。SQRL FK33 和 Jungle Cat 卡原本是为加密货币挖矿设计的，如今在二手市场价格低廉，因此很适合被重新用于 AI 计算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://startupfortune.com/builders-are-running-qwen35-on-fpga-boards-scavenged-from-dead-crypto-miners/">Builders Are Running Qwen3.5 on FPGA Boards Scavenged From ...</a></li>
<li><a href="https://www.sevenlab.ai/ai-news/developers-run-qwen35-on-repurposed-crypto-mining-fpga-cards-to-bypass-gpu-scarcity">Developers run Qwen3.5 on repurposed crypto-mining FPGA cards ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 该帖子在 r/LocalLLaMA 中被视为技术深度高、新颖性强的项目，作者公开征求关于向 Jungle Cat 板加载权重的建议，并提到 BC-250 是性价比极高的购买选择。由于未提供具体评论内容，无法详细总结社区的整体观点。

**标签**: `#FPGA`, `#LLM inference`, `#Qwen`, `#hardware acceleration`, `#local AI`

---