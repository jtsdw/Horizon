---
layout: default
title: "Horizon Summary: 2026-11-06 (ZH)"
date: 2026-11-06
lang: zh
---

> 从 18 条内容中筛选出 4 条重要资讯。

---

1. [OpenSSH 'sshole' 漏洞可绕过 musl 系统密码认证](#item-1) ⭐️ 9.0/10
2. [OpenAI 推出 GPT-6 Cyber，专注授权范围内的漏洞研究](#item-2) ⭐️ 9.0/10
3. [Claude Code 在 User-Agent 头中泄露用户邮箱地址](#item-3) ⭐️ 8.0/10
4. [NVIDIA 发布 Cosmos 3 开放模型，用于交互式世界模拟](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenSSH 'sshole' 漏洞可绕过 musl 系统密码认证](https://sshhole.com/) ⭐️ 9.0/10

一个名为“sshole”的新披露 OpenSSH 漏洞（编号 CVE-2026-123158）允许攻击者在使用 musl libc 且未启用 PAM 的 Linux 系统（如 Alpine Linux）上绕过密码认证。该漏洞源于 musl 的 crypt() 函数在出错时返回 '*'，这与 /etc/passwd 中表示“无密码”的 '*' 哨兵值冲突，导致对于哈希为 '*' 的账户，任何长度在 257 到 1024 字节之间的密码都会被接受。OpenSSH 已于 2026 年 11 月 5 日发布 10.6p2 版本以规避此问题。 这是一个影响广泛基础设施的严重认证绕过漏洞，可能允许远程攻击者在受影响系统上以 root 或任何禁用密码的用户身份登录。它凸显了底层 API 中带内信号的危险，并迫使发行版和管理员尽快修补。 该漏洞仅影响使用 musl libc 且未启用 PAM 构建的系统，并且要求攻击者提供长度在 257 到 1024 字节之间的密码。OpenSSH 10.6p2 包含一个规避措施，但根本原因在于 musl 的 crypt() 实现，其 SHA-crypt 路径也存在类似但较轻的问题。管理员应升级到 OpenSSH 10.6p2 并重启 sshd。

hackernews · josemrb · 11月5日 12:19 · [社区讨论](https://news.ycombinator.com/item?id=50378228)

**背景**: OpenSSH 是 SSH 协议最广泛使用的实现，用于安全远程登录。在 Linux 上，密码认证通常涉及调用 C 库的 crypt() 函数对提供的密码进行哈希，并与 /etc/shadow 中存储的哈希比较。在 /etc/passwd 和 /etc/shadow 中，密码字段的 '*' 或 '!' 通常表示未设置密码，应禁用密码登录。musl 是一个轻量级 C 库，被 Alpine Linux 和一些嵌入式系统使用，当哈希失败时（例如输入过长），它会从 crypt() 返回 '*'。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://securityarsenal.com/blog/openssh-sshole-flaw-how-attackers-bypass-password-disabled-linux-accounts-and-how-to-stop-them">OpenSSH "Sshole" Flaw: How Attackers Bypass Password-Disabled ...</a></li>
<li><a href="https://www.decryptiondigest.com/blog/musl-crypt-ssh-bypass-alpine-linux-openssh">Alpine Linux SSH Auth Bypass: 257-Byte Password Logs In as Root</a></li>
<li><a href="https://linuxiac.com/openssh-10-6p2-released-to-fix-critical-password-authentication-bypass/">OpenSSH 10.6p2 Released to Fix Critical Password ... - Linuxiac</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍批评了带内信号的使用，有人指出 '*' 不应同时被用作“无密码”和“哈希出错”的特殊值。另一位评论者指出，musl 已在其 DES crypt 路径中规避了类似问题，但遗漏了 SHA-crypt 路径，还有人主张使用显式失败值或 Result 类型而不是魔法字符串。

**标签**: `#security`, `#openssh`, `#vulnerability`, `#crypt`, `#authentication`

---

<a id="item-2"></a>
## [OpenAI 推出 GPT-6 Cyber，专注授权范围内的漏洞研究](https://openai.com/index/introducing-gpt-6-cyber) ⭐️ 9.0/10

OpenAI 发布了 GPT-6 Cyber，这是一款专注于网络安全的模型，旨在发现可利用漏洞并开发修复方案，同时确保操作不超出授权范围。该发布将该模型定位为面向安全工作的对齐智能体，而非通用助手。 一款专为漏洞发现与修复打造的前沿模型，可能显著加快组织发现和修补可利用缺陷的速度，影响安全团队、软件厂商和漏洞赏金计划。这也表明主要 AI 实验室正在推出面向特定领域、带有安全范围约束的安全模型，而不是依赖通用模型从事接近攻击性的工作。 该模型被明确训练为在授权范围内运作，这是一项关键约束，因为 AI 驱动的漏洞发现若缺乏限制，可能模糊授权测试与未授权入侵之间的界限。OpenAI 的公告提供的技术细节有限，因此仍需对其真实场景下的检测率和误报率进行独立评估。

rss · OpenAI Blog · 11月5日 09:00

**背景**: 网络安全领域的 AI 智能体正越来越多地用于实时威胁检测、自动化响应和漏洞研究，但它们也带来提示注入、工具滥用和数据泄露等风险。与此同时，前沿模型已开始以人类研究员难以企及的速度自主识别可利用的软件漏洞，这催生了 Anthropic 的 Project Glasswing 等项目以及新的漏洞披露争论。GPT-6 Cyber 通过将漏洞发现能力与明确的授权边界相结合，顺应了这一趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.schneier.com/blog/archives/2026/06/vulnerability-disclosure-in-the-age-of-ai.html">Vulnerability Disclosure in the Age of AI - Schneier on Security</a></li>
<li><a href="https://www.tenable.com/blog/why-the-approaching-flood-of-vulnerabilities-changes-everything-and-what-to-do-about-it">How AI-driven vulnerability discovery changes everything ...</a></li>
<li><a href="https://www.simplilearn.com/ai-agents-cybersecurity-article">AI Agents and Cybersecurity : Key Risks and Threats</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#AI`, `#OpenAI`, `#vulnerability-research`, `#model-release`

---

<a id="item-3"></a>
## [Claude Code 在 User-Agent 头中泄露用户邮箱地址](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 8.0/10

GitHub 问题 #107757 报告称，Claude Code 在进行网络搜索时，会在 User-Agent 请求头中把用户的账户邮箱地址发送给第三方网站，导致用户收到垃圾邮件。Anthropic 员工确认正在从模型上下文中移除邮箱地址，并且内置插件 `cc-plugin-privacy`（2.1.317 及以上版本）现已阻止该行为。 这一隐私泄露影响了一款广泛使用的开发者工具，可能使用户面临定向垃圾邮件和钓鱼攻击，削弱人们对代表用户频繁发起网络请求的 AI 编程代理的信任。该事件凸显了在代理式工具中制定更清晰的数据处理政策和退出机制的必要性。 部分情况属于预期行为：SEC EDGAR API 要求 User-Agent 头中包含用户姓名和邮箱，否则会拒绝请求。Anthropic 的修复从提供给模型的上下文中移除了账户邮箱，2.1.317 及以上版本的用户默认启用 `cc-plugin-privacy` 检查，可通过 `/plugins` 切换。

hackernews · motoroco · 11月5日 22:17 · [社区讨论](https://news.ycombinator.com/item?id=50385272)

**背景**: Claude Code 是 Anthropic 推出的代理式编程工具，可以代表用户浏览网页和调用 API。User-Agent 头是标识请求客户端的标准 HTTP 字段，某些 API（如 SEC 的接口）要求在其中包含联系信息。当此类标识符在用户不知情或未经同意的情况下被自动注入时，就会引发隐私担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/anthropics/claude-code/issues/107757">Bug Report: Privacy violation in User-Agent header</a></li>
<li><a href="https://edgrapi.com/blog/sec-edgar-api-key">SEC EDGAR API key: how to get one in 2026 (step by step) — Edgrapi</a></li>
<li><a href="https://explainx.ai/blog/claude-code-leaks-your-email-user-agent-header-how-to-stop-it-2026">Claude Code Leaks Your Email in Headers: 5-Min Fix - explainx.ai</a></li>

</ul>
</details>

**社区讨论**: Hacker News 讨论（839 分，276 条评论）混合了技术澄清和隐私担忧。最高赞评论者 varenc 演示了 SEC API 特别要求在 User-Agent 中包含邮箱，将部分问题重新定义为预期行为；而 mk89 等人报告称切换到 Claude 后个性化垃圾邮件激增。Anthropic 员工（mpoteat、lydia_hallie）回应称已推出内置隐私插件，并确认从上下文中移除邮箱。

**标签**: `#privacy`, `#claude-code`, `#ai-tools`, `#security`, `#developer-tools`

---

<a id="item-4"></a>
## [NVIDIA 发布 Cosmos 3 开放模型，用于交互式世界模拟](https://huggingface.co/blog/nvidia/cosmos-interactive-world-simulation) ⭐️ 8.0/10

NVIDIA 发布了 Cosmos 3，一套用于交互式世界模拟的开放权重模型，为其 Cosmos 世界模型开发平台新增了四个检查点。这些模型能够为 AI 训练和研究生成逼真且可控的虚拟环境，包括多传感器多视角驾驶场景生成。 此次发布具有重要意义，因为它提供了能够模拟物理环境的开放模型，这对于在安全、多样且可扩展的虚拟环境中训练机器人和自主系统至关重要。它可能加速机器人、自动驾驶和生成式模拟领域的研究与应用，影响物理 AI 领域的开发者和研究人员。 四个新检查点包括 Cosmos3-Nano-Transfer-Auto，用于生成具有不同天气和光照条件的多视角驾驶数据，以及 Cosmos3-Nano-Sim-Auto，用于流式传输同步的摄像头和 LiDAR 数据。Cosmos 3 在 R-Bench、Artificial Analysis、RoboLab 和 RoboArena 等基准测试中，在文本到图像、图像到视频和机器人策略任务上排名开放模型第一。

rss · Hugging Face Blog · 11月5日 19:35

**背景**: 世界模型是模拟环境动态（包括物理、物体交互和因果关系）的 AI 系统，超越了简单的分类或生成。它们被用于机器人、自动驾驶和交互式视频生成，以在模拟环境中训练和评估 AI 智能体。NVIDIA Cosmos 是一个用于构建物理 AI 的开放平台，提供世界模型、数据集和训练框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/nvidia/cosmos-interactive-world-simulation">New NVIDIA Cosmos 3 Open Models for Interactive World Simulation</a></li>
<li><a href="https://research.nvidia.com/labs/cosmos-lab/cosmos3/">Cosmos 3 — Cosmos Lab - research.nvidia.com</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/world-models/">What Is a World Model? | NVIDIA Glossary</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#world simulation`, `#open models`, `#AI`, `#generative models`

---