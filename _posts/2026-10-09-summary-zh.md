---
layout: default
title: "Horizon Summary: 2026-10-09 (ZH)"
date: 2026-10-09
lang: zh
---

> 从 36 条内容中筛选出 2 条重要资讯。

---

1. [2800 美元主机用 8 块 Radeon Pro V620 搭配定制 vLLM 分支运行 Qwen3.8-Flash-Next](#item-1) ⭐️ 8.0/10
2. [LemonSeed 通过外接 AMD R9700 eGPU 在 iPad 上运行 Qwen3.8-27B](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [2800 美元主机用 8 块 Radeon Pro V620 搭配定制 vLLM 分支运行 Qwen3.8-Flash-Next](https://www.reddit.com/r/LocalLLaMA/comments/1x0wnz1/2800_rig_with_8x_radeon_pro_v620_256_gb_vram/) ⭐️ 8.0/10

一位 Reddit 用户用 8 块 AMD Radeon Pro V620 显卡（每块 32 GB，合计 256 GB 显存）搭建了约 2800 美元的主机，并借助带有定制 RDNA2 内核的 vLLM 分支运行 Qwen3.8-Flash-Next，实现了 60-100 tokens/s 的解码速度和超过 3000 tokens/s 的预填充速度。用户表示这比 llama.cpp 在同一硬件上的预填充速度约快 800%，并因此取消了出售显卡的计划。 这表明原本为云游戏设计的廉价旧款企业级 GPU 可以被重新利用，搭建出高显存、高性价比的本地大模型推理主机，挑战了只有 NVIDIA 或最新一代硬件才可行的假设。同时，这也说明定制内核和 vLLM 分支能在非主流硬件上释放出可观的性能，有望让爱好者和小型实验室更容易运行大型 MoE 模型。 该配置采用流水线并行度 4（PP=4），未使用张量并行；路由专家量化为 W4A16，其余层保持 BF16，并启用了 3 token 草稿的 MTP；关闭 MTP 后解码速度降至 40-50 tokens/s。用户指出每块 350 美元的价格可能已不再可得，照片中可见的 RTX 4090 仅用于图像/视频生成，不参与大模型推理。

reddit · r/LocalLLaMA · /u/_TheWolfOfWalmart_ · 10月8日 17:12

**背景**: Radeon Pro V620 是 AMD 于 2021 年 11 月推出的数据中心 GPU，基于 RDNA2 Navi 21 架构，配备 32 GB GDDR6 显存和 512 GB/s 内存带宽，最初面向云游戏工作负载。vLLM 是一款流行的开源推理引擎，以高吞吐服务著称，人们常通过分支或插件为其添加针对特定硬件的定制内核或优化。Qwen3.8-Flash-Next 是阿里巴巴 Qwen 团队发布的多模态混合专家（MoE）模型，作为未来 Qwen4 架构的早期预览。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.amd.com/en/products/accelerators/radeon-pro/amd-radeon-pro-v620.html">AMD Radeon™ PRO V620</a></li>
<li><a href="https://www.techpowerup.com/gpu-specs/radeon-pro-v620.c3846">AMD Radeon PRO V620 Specs | TechPowerUp GPU Database</a></li>
<li><a href="https://github.com/QwenLM/Qwen3.8-Flash-Next/">Qwen3.8-Flash-Next - GitHub</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#vllm`, `#amd-gpu`, `#hardware`, `#inference-optimization`

---

<a id="item-2"></a>
## [LemonSeed 通过外接 AMD R9700 eGPU 在 iPad 上运行 Qwen3.8-27B](https://www.reddit.com/r/LocalLLaMA/comments/1x18e95/qwen3827b_159_toks_on_r9700_64_toks_on_strix_halo/) ⭐️ 8.0/10

LemonSeed Studio 展示了在 iPad Pro 上的端侧大模型推理：它将未经修改的上游 Linux amdgpu + amdkfd 驱动以内核扩展（PCIDriverKit extension）的形式嵌入，并在雷雳（Thunderbolt）外接坞中的 Sapphire Radeon AI PRO R9700 上运行其跨平台 LemonSeed Engine。在 Qwen3.8-27B Q4 模型、Q8 DFlash2 草稿模型和 131k 上下文下，解码速度在 iPadOS 上达到 158.5 tok/s，macOS 上 159.4 tok/s，Linux 上 144.6 tok/s，而在 Linux 下的 Strix Halo（Radeon 8060S）上为 64.4 tok/s。 这是一项值得关注的系统级成果：它在不修改上游驱动的前提下，把完整的桌面级 AMD GPU 软件栈带到了 iPadOS，证明在苹果平板平台上通过外接 GPU 加速本地大模型推理是可行的。它还表明，同一个自动调优引擎可以在 iPadOS、macOS 和 Linux 上提供几乎一致的性能，这可能为本地大模型用户拓宽 NVIDIA 与 Apple Silicon 之外的硬件选择。 该引擎将模型的前向传播记录为计算图，融合算子并为目标 GPU 生成内核，在设备上实测多种内核布局并保留最快的一种；推测解码（MTP 与 DFlash2）会根据实测的接受率和成本动态决定验证多少草稿 token。0.5.8 版本默认启用 DFlash2 草稿树，新增 Strix Halo（gfx1151）的预填充/解码支持（融合 gate/up GEMM、预填充注意力中每个工作组处理两个 query tile），修复了一个启动时的 GPU 故障，并在 Linux 归档中自带 HSA 运行时，因此只需 amdgpu 驱动并具备 /dev/kfd 访问权限即可。

reddit · r/LocalLLaMA · /u/TheOriginalG2 · 10月9日 01:20

**背景**: PCIDriverKit 是苹果提供的用户态框架，用于以 DriverKit 扩展（dext）而非内核扩展的形式编写 PCI 设备驱动，它在 macOS 上支持 Intel 与 Apple Silicon，在 iPadOS 上支持 M 系列芯片设备。推测解码通过让一个小型草稿模型提出若干 token、再由较大的目标模型在一次前向传播中验证，从而加速大模型推理；而内核融合则把相邻的张量运算合并为一个内核，使中间值留在片上，而不必往返设备内存。LemonSeed Engine（LSE）是一个跨平台推理引擎，会针对每台设备自动调优内核；Strix Halo 是 AMD 的高端 APU，集成 Radeon 8060S GPU。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.apple.com/documentation/pcidriverkit">PCIDriverKit | Apple Developer Documentation</a></li>
<li><a href="https://deepwiki.com/chishiki37/dgx-spark-runbooks/6.2-speculative-decoding:-mtp-dflash-and-dspark">Speculative Decoding: MTP, DFlash, and DSpark | chishiki37 ...</a></li>
<li><a href="https://runinfra.ai/glossary/kernel-fusion">Kernel fusion | LLM serving glossary | RunInfra</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#amd-gpu`, `#ipados`, `#speculative-decoding`, `#kernel-fusion`

---