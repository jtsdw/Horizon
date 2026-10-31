---
layout: default
title: "Horizon Summary: 2026-10-31 (ZH)"
date: 2026-10-31
lang: zh
---

> 从 26 条内容中筛选出 2 条重要资讯。

---

1. [Cursor 市场中的恶意 Claude Code 扩展植入 SSH 后门](#item-1) ⭐️ 9.0/10
2. [多租户 PaaS 提供商 Northflank 遭遇安全漏洞](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cursor 市场中的恶意 Claude Code 扩展植入 SSH 后门](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 9.0/10

一名恶意攻击者在 Cursor 市场上发布了被篡改的 Claude Code VS Code 扩展，该扩展会将一个标记为“svc-telemetry”的攻击者 SSH 公钥添加到用户的 ~/.ssh/authorized_keys 文件中。该恶意扩展在周四上线约 11 小时（太平洋时间约凌晨 2:27 至下午 1:35），Cursor 估计可能有多达 5,000 名用户受到影响，随后市场被暂停并替换为干净版本。 这是一起影响广泛使用的 AI 编程助手的供应链安全事件，表明市场发布权限可能被滥用来在开发者机器上植入后门并获取远程访问权限。它凸显了 Open VSX 和 Cursor 市场等第三方扩展注册表的风险，并促使 Anthropic 官方回应，澄清其自身系统和官方渠道并未被攻破。 用户可以在 macOS 上运行 `grep -qs svc-telemetry ~/.ssh/authorized_keys`（Windows 上类似命令）来检查是否存在恶意密钥。Anthropic 的 Felix Rieseberg 表示，此次事件并非 Anthropic 系统或员工笔记本电脑被攻破，官方渠道的版本不受影响，仅 Cursor 用户受到影响。

hackernews · _chall · 10月30日 07:09 · [社区讨论](https://news.ycombinator.com/item?id=50300683)

**背景**: Claude Code 是 Anthropic 的 AI 编程助手，提供终端 CLI 和 VS Code 扩展两种形式。Cursor 是一款 AI 驱动的代码编辑器，使用 Open VSX 扩展注册表而非微软 VS Code 市场，因此发布在该注册表上的扩展可以触达 Cursor 用户。SSH 的 authorized_keys 文件列出了允许登录某账户的公钥，因此将攻击者的密钥添加进去就会创建持久的远程登录后门。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cursor.com/help/customization/extensions">Extensions | Cursor Docs</a></li>
<li><a href="https://marketplace.visualstudio.com/items?itemName=anthropic.claude-code">Claude Code for VS Code - Visual Studio Marketplace Official Claude Code Extension on Cursor Marketplace ... Claude Code in VS Code: The Official Extension, Set Up ... Claude Code CLI vs VS Code Extension: Which Should You Use? GitHub - OlegCIB/claude-code-vscode Malicious Claude Code extension on Cursor planted SSH backdoors</a></li>
<li><a href="https://fahmifj.github.io/blog/linux-backdoors-and-where-to-find-them/">Linux Backdoors and Where to Find Them | Ef's log</a></li>

</ul>
</details>

**社区讨论**: 评论者希望澄清该扩展是否来自 Anthropic，Felix Rieseberg 澄清这是通过 Cursor 市场发布的篡改副本，并非 Anthropic 被攻破。其他人分享了检测命令并引用了最初的 Phorion 报告和 Cursor 博客，还有人讨论微软官方注册表是否也受影响，普遍认为官方构建似乎是干净的。

**标签**: `#security`, `#supply-chain`, `#VS Code`, `#AI coding assistant`, `#Cursor`

---

<a id="item-2"></a>
## [多租户 PaaS 提供商 Northflank 遭遇安全漏洞](https://status.northflank.com/) ⭐️ 8.0/10

多租户平台即服务（PaaS）提供商 Northflank 通过其状态页面披露了一起安全漏洞事件，这是自 9 月以来针对基础设施初创公司的一系列攻击中的最新一起。 此次漏洞凸显了多租户云平台日益增长的安全风险，并可能加速企业客户回归超大规模云服务商，因为对小型基础设施提供商的信任受到侵蚀。 Northflank 的平台基于 Kubernetes 构建，提供托管云和客户自有云部署选项；此次漏洞似乎影响了客户环境，但具体技术细节和受影响客户数量尚未公开确认。

hackernews · js4ever · 10月30日 15:10 · [社区讨论](https://news.ycombinator.com/item?id=50305025)

**背景**: Northflank 是一家平台即服务（PaaS）提供商，简化了在 Kubernetes 上的应用部署，提供托管和自托管选项。多租户模式下，多个客户共享同一基础设施，如果隔离不足，会引入跨租户漏洞和数据泄露等安全风险。此次事件紧随 Railway 和 Zeabur 等其他基础设施初创公司的类似漏洞之后，引发了对快速发展的基础设施初创领域安全实践的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://northflank.com/blog/what-is-paas-hosting">What is PaaS hosting? Benefits and how it works | Blog — Northflank</a></li>
<li><a href="https://northflank.com/blog/best-paas-for-enterprises">Best PaaS for enterprises in 2026 | Blog — Northflank</a></li>

</ul>
</details>

**社区讨论**: 评论者对多租户即服务供应商遭受攻击的频率表示震惊，一些人预测出于安全考虑将回归超大规模云服务商。其他人分享了加密环境变量等缓解策略，并讨论了技术安全的更广泛影响。

**标签**: `#security`, `#cloud-infrastructure`, `#SaaS`, `#multi-tenancy`, `#breach`

---