---
layout: default
title: "Horizon Summary: 2026-10-10 (ZH)"
date: 2026-10-10
lang: zh
---

> 从 36 条内容中筛选出 2 条重要资讯。

---

1. [Cloudflare 收购 Deno，一年后将停止开发](#item-1) ⭐️ 9.0/10
2. [YouTuber 打造 Flock 式摄像头追踪警察，遭警方上门](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare 收购 Deno，一年后将停止开发](https://deno.com/blog/cloudflare) ⭐️ 9.0/10

Cloudflare 已收购由 Node.js 创始人 Ryan Dahl 联合创建的 JavaScript/TypeScript 运行时 Deno，并宣布仅再支持该运行时一年，期间提供每月的错误修复和安全更新，之后将终止所有开发。一年后 Deno 仍将保持开源，但除非有外部贡献者接手，否则将不再获得官方支持。 此次收购实际上终结了最具创新性的 JavaScript 运行时之一的独立开发，移除了 Node.js 的一个重要替代方案，可能削弱运行时生态的竞争与创新。投资于 Deno 生态的开发者如今面临长期支持的不确定性，可能不得不迁移到 Node.js、Bun 或 Cloudflare 自家的 workerd 运行时。 Cloudflare 将在一年内继续每月发布 Deno 版本，提供错误修复和安全更新，之后开发将完全停止；该运行时保持开源，Cloudflare 欢迎其他人继续开发。公告以“Deno + Cloudflare”合作的口吻呈现，但因细则中透露出 Deno 实际被终止而招致批评。

hackernews · ilreb · 10月9日 13:03 · [社区讨论](https://news.ycombinator.com/item?id=50019911)

**背景**: Deno 是一个基于 V8 引擎和 Rust 语言构建的 JavaScript、TypeScript 和 WebAssembly 运行时，由 Node.js 的原作者 Ryan Dahl 与 Bert Belder 联合创建。它被设计为 Node.js 更安全、更现代的替代品，内置 TypeScript 支持、npm 兼容性以及默认安全的权限机制。Cloudflare 运营着无服务器边缘计算平台 Workers，此次收购被普遍视为一次“人才收购”，旨在将 Deno 的团队和安全技术整合进 Cloudflare 的技术栈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Deno_(software)">Deno (software) - Wikipedia</a></li>
<li><a href="https://www.cloudflare.com/products/workers/">Cloudflare Workers - Global Serverless Functions Platform</a></li>
<li><a href="https://betterstack.com/community/guides/scaling-nodejs/nodejs-vs-deno-vs-bun/">Node.js vs Deno vs Bun: Comparing JavaScript Runtimes</a></li>

</ul>
</details>

**社区讨论**: 社区反应 overwhelmingly 负面，许多评论者表示悲伤，并认为公告的正面措辞具有误导性，有人指出“Deno 开发实际上因 Cloudflare 的人才收购而关闭”会是更诚实的标题。多位长期用户表示，当 Deno 将 npm 兼容性置于其原本简洁设计之上时，他们就已经预见到这一结局，也有人希望 Cloudflare 的 workerd 能采纳 Deno 的安全机制。

**标签**: `#Deno`, `#Cloudflare`, `#JavaScript`, `#Runtime`, `#Acquisition`

---

<a id="item-2"></a>
## [YouTuber 打造 Flock 式摄像头追踪警察，遭警方上门](https://gizmodo.com/youtuber-says-cops-paid-him-a-visit-after-he-built-flock-style-camera-to-track-cops-2000824306) ⭐️ 8.0/10

据 Gizmodo 报道，一位 YouTuber 声称，在他打造了一套用于追踪警车的 Flock 式摄像头系统后，警方上门找了他。该事件在 Hacker News 上引发了热烈讨论，获得 502 个赞和 282 条评论，聚焦于监控、隐私和法律边界。 这一事件凸显了日益普及的监控技术（如 Flock Safety 的车牌识别摄像头）与公众将同样工具反向用于执法部门之间的紧张关系。它引发了重要的公民自由问题：谁有权追踪谁，以及现有法律能否充分应对这种反向监控。 这位 YouTuber 专门打造了一套个人 Flock 式摄像头系统来监控警车，而警方的上门表明执法部门可能将这种公民监控视为法律或安全问题。Hacker News 的讨论引用了新罕布什尔州的法律，该法律禁止收集所有车牌用于后续分析，要求 3 分钟内删除未命中的车牌图像，并禁止将未命中的摄像头图像上传到设备外。

hackernews · gumby · 10月9日 21:06 · [社区讨论](https://news.ycombinator.com/item?id=50026555)

**背景**: Flock Safety 是一家成立于 2017 年的美国私营公司，生产并运营监控硬件和软件，尤其是自动车牌识别（ALPR）摄像头、大规模视频监控和枪声定位系统，并与执法机构签订合同。ALPR 技术能自动读取车牌，被警方用于追踪车辆，这引发了公民自由倡导者的隐私担忧。这则新闻涉及一名公民使用类似技术来监控警察，从而引发了关于反向监控合法性和伦理的辩论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automatic_number-plate_recognition">Automatic number- plate recognition - Wikipedia</a></li>
<li><a href="https://www.security.org/security-cameras/legality/">Legality of Security Camera Usage & Placement in 2026 | Security.org</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了各种观点：一些人指出新罕布什尔州严格的 ALPR 法律是模范解决方案，另一些人则认为 Flock 是供执法部门使用的，追踪警察与 Flock 的初衷不同，还有人建议采取极端的反监控措施或立法限制数据访问。少数评论者表达了愤怒，并将此比作反乌托邦式的监控国家，而其他人则提议构建一个“OpenFlock”来追踪投票支持 Flock 摄像头的市议员。

**标签**: `#surveillance`, `#privacy`, `#civil-liberties`, `#ALPR`, `#law-enforcement`

---