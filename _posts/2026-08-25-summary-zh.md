---
layout: default
title: "Horizon Summary: 2026-08-25 (ZH)"
date: 2026-08-25
lang: zh
---

> 从 23 条内容中筛选出 3 条重要资讯。

---

1. [MS Paint 和照片应用在 AI 图像中嵌入隐形 GUID 水印](#item-1) ⭐️ 8.0/10
2. [旧金山被重现为交互式 3D 网页游戏](#item-2) ⭐️ 8.0/10
3. [OpenAI 在 Kiro 中推出 GPT-5.6，提升性价比](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [MS Paint 和照片应用在 AI 图像中嵌入隐形 GUID 水印](https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/) ⭐️ 8.0/10

微软的画图（Paint）和照片（Photos）应用现在会在经过 AI 处理的图像中静默嵌入一个不可见的 GUID 水印，即使 AI 处理是在设备本地进行的。该水印在用户不知情的情况下添加，且无法关闭。 这引发了重大的隐私和匿名性担忧，因为隐形水印可能使微软或第三方能够将图像追溯到用户的微软账户，从而可能将匿名内容与真实身份关联起来。这也对内容溯源和版权执法产生影响。 该水印是一个服务器颁发的 GUID，嵌入在像素级别，与 C2PA 清单分离，移除清单并不会删除它。在 Copilot+ PC 上，图像生成是本地进行的，但提示词审核仍是远程的，并且用户无法选择关闭隐形水印。

hackernews · ComputerGuru · 8月24日 15:28 · [社区讨论](https://news.ycombinator.com/item?id=49421158)

**背景**: 隐形水印是一种将数据嵌入数字内容的技术，人类无法察觉，但软件可以检测到。它常用于版权保护和内容认证。微软已将 AI 功能集成到画图和照片应用中，这种水印似乎是其内容溯源工作的一部分，但缺乏透明度引发了争议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://byteiota.com/ms-paint-invisible-server-guid-watermark-ai-image/">MS Paint Embeds Invisible Server GUIDs in Every AI Image | byteiota</a></li>
<li><a href="https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/">Microsoft Paint and Photos Embed Server-Issued GUIDs ... :: Xusheng Li</a></li>

</ul>
</details>

**社区讨论**: 社区评论对画图应用从简单的像素编辑器演变而来表示震惊，并批评微软秘密在用户创建的图像中添加唯一标识符，认为这是对互联网匿名性的威胁。一些用户指出微软过去错误应用水印的情况，导致不信任并建议避免使用这些应用。

**标签**: `#privacy`, `#watermarking`, `#Microsoft`, `#AI`, `#security`

---

<a id="item-2"></a>
## [旧金山被重现为交互式 3D 网页游戏](https://sf.thijs.gg/) ⭐️ 8.0/10

一个基于网页的交互式 3D 旧金山重建项目已在 sf.thijs.gg 上线，利用地图数据构建，让用户以类似电子游戏的环境探索城市。社区讨论中提到，该项目使用了 retroplasma 代码和苹果地图数据。 该项目展示了基于浏览器的 3D 城市渲染的潜力，可能激发游戏、城市规划和虚拟旅游等领域的应用。它也凸显了利用真实地图数据创建沉浸式数字体验的日益增长的趋势。 该重建项目基于地图数据构建，可能使用了 retroplasma 逆向工程的苹果地图数据，但社区指出 retroplasma 仓库已过时。基于网页的方式无需下载即可轻松访问，社区成员建议增加街道名称、地标和传送等功能。

hackernews · centrosphere · 8月24日 17:05 · [社区讨论](https://news.ycombinator.com/item?id=49422784)

**背景**: 随着 MapLibre GL JS 和 deck.gl 等成熟技术的出现，基于网页的 3D 城市渲染变得更加可行，这些技术利用 GPU 渲染实现实时可视化。像 map3d 这样的项目可以从 OpenStreetMap 数据生成 3D 城市模型，而 Google Maps 等平台提供 3D 地图 API 用于交互式体验。该项目利用类似概念创建了类似游戏的探索环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medevel.com/16-open-source-library-frameworks-to-build-3d-maps-and-3d-globe/">16 Open-source Library and Frameworks to Build 3D Maps and 3D ...</a></li>
<li><a href="https://geo.malagis.com/generate-3d-city-models-from-openstreetmap-data-in-the-browser-with-map3d.html">Generate 3D City Models from OpenStreetMap Data in the ...</a></li>
<li><a href="https://mapsplatform.google.com/maps-products/3d-maps/">3D Maps API for Web and Apps | Google Maps Platform</a></li>

</ul>
</details>

**社区讨论**: 社区情绪非常积极，用户表达了情感共鸣和对技术实现的兴奋。一些人讨论 retroplasma 代码及其局限性，而另一些人则设想 GTA 风格地图或 MMO 等应用。少数用户分享了相关项目，如费城的一个游戏，表明对该领域的积极兴趣。

**标签**: `#3D rendering`, `#web-based`, `#city simulation`, `#map data`, `#interactive`

---

<a id="item-3"></a>
## [OpenAI 在 Kiro 中推出 GPT-5.6，提升性价比](https://openai.com/index/gpt-5-6-in-kiro) ⭐️ 8.0/10

OpenAI 宣布 GPT-5.6 现已在 Kiro 中可用，Kiro 是一款 AI 驱动的开发工具，为开发者在规划、构建、审查和测试软件时提供更好的性价比。该模型每个 token 能完成更多有用工作，每美元性能更强，并具备处理复杂任务的按需能力。 此次发布意义重大，因为它直接解决了开发者在 AI 模型使用中的成本和效率问题，可能降低将先进 AI 集成到软件开发工作流程中的门槛。这也表明 OpenAI 持续关注优化模型以适应开发者为中心的实际应用场景，可能影响 AI 编程助手市场的竞争格局。 GPT-5.6 已集成到 Kiro 中，Kiro 是由 AWS 开发的智能体 IDE 和 CLI，强调规范驱动开发，在生成代码前先将想法转化为书面计划。该模型在 Kiro 中可用，Artificial Analysis 等性能分析将其与其他模型在质量、价格和每秒 token 数等指标上进行对比。

rss · OpenAI Blog · 8月24日 12:00

**背景**: Kiro 是由亚马逊网络服务（AWS）开发的 AI 驱动的集成开发环境（IDE）和命令行界面（CLI）。它采用规范驱动的方法，开发者首先定义需求和设计，然后 AI 代理据此生成代码。GPT-5.6 是 OpenAI 最新的模型迭代，其集成到 Kiro 旨在为开发者提供一种更具成本效益的方式，利用 AI 完成软件开发任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/gpt-5-6-in-kiro/">Advancing price - performance for developers with GPT ‑ 5 . 6 in... | OpenAI</a></li>
<li><a href="https://artificialanalysis.ai/models/gpt-5-6-sol">GPT - 5 . 6 Sol (max) - Intelligence, Performance & Price Analysis</a></li>
<li><a href="https://toolquestor.com/tool/kiro">Kiro – AWS Agentic IDE for Spec-Driven Coding</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5.6`, `#AI model`, `#developer tools`, `#price-performance`

---