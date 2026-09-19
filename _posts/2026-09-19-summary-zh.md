---
layout: default
title: "Horizon Summary: 2026-09-19 (ZH)"
date: 2026-09-19
lang: zh
---

> 从 26 条内容中筛选出 2 条重要资讯。

---

1. [Android 17 新增 API 却未向 AOSP 开源](#item-1) ⭐️ 8.0/10
2. [Cloudflare 用数学优化再省 100TB 内存](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Android 17 新增 API 却未向 AOSP 开源](https://grapheneos.social/@GrapheneOS/117282080803799576) ⭐️ 8.0/10

Google 在 Android 17 中仅向 Pixel SDK 添加了新 API，而未将其发布到 Android 开源项目（AOSP），这是自 Android 3.x（Honeycomb）以来首次出现新 API 未立即开源的情况。 这打破了 AOSP 与 Pixel 版本同步获得源码更新的长期惯例，引发了对平台开放性的担忧，并可能使依赖及时获取 AOSP 源码的第三方 ROM（如 GrapheneOS）处于不利地位。 Google 通常每年发布四次 Pixel 更新（含文档和 SDK），而每年仅向 AOSP 和 OEM 发布两次完整的 Android 源码更新；这些新的 Pixel 独占 API 使得相关功能在后续源码发布前无法被基于 AOSP 的构建所使用。

hackernews · theanonymousone · 9月18日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49758736)

**背景**: AOSP 是 Google 维护并以宽松许可证发布的开源代码库，构成了 Android 设备和第三方 ROM 的基础。历史上，Google 会在 Pixel 更新同时或之后不久将新的 Android API 发布到 AOSP，使 GrapheneOS 等项目能够构建兼容且注重隐私的 Android 版本。Android 3.x（Honeycomb）是一个显著的例外，其源码最初被保留，后来才开源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://source.android.com/">Android Open Source Project</a></li>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://en.wikipedia.org/wiki/Android_Honeycomb">Android Honeycomb - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Google 对开源的处理方式表示强烈不满，指出延迟的源码补丁、禁运和认证问题都是 GrapheneOS 面临的障碍。一些人认为转向 Pixel 独占 API 是对以往做法的背离，另一些人则呼吁通过监管确保 AOSP 构建能获得与 Google 签名构建同等的特权。

**标签**: `#Android`, `#AOSP`, `#GrapheneOS`, `#Open Source`, `#Google`

---

<a id="item-2"></a>
## [Cloudflare 用数学优化再省 100TB 内存](https://blog.cloudflare.com/saving-100-tb-of-ram-with-math/) ⭐️ 8.0/10

Cloudflare 发布了一篇后续工程博客，解释其如何通过数学优化在缓存基础设施中再节省 100TB 内存，这是继此前为 1.1.1.1 DNS 缓存节省 100TB 内存之后的又一成果。文章详细介绍了缓存条目存储和哈希处理方式的改动，并在 Hacker News 上引发了 273 分、56 条评论的热烈讨论。 内存是大规模分布式缓存中最大的成本驱动因素之一，因此在整支服务器集群中释放 100TB 内存可直接降低基础设施开支，并可能提升缓存性能。这项工作也反映出，随着内存价格上涨以及 AI 工作负载争抢内存容量，整个行业正重新重视精细优化。 这些优化集中在支撑 1.1.1.1、DNS Firewall 及其他 DNS 服务的 Cloudflare Big Pineapple DNS 缓存平台上，通过一系列改动将每条缓存条目的内存占用削减了超过 50%。节省的内存量相当于约 130 台 Cloudflare Gen 13 服务器的内存总和，而且缓存速度也顺带得到了提升。

hackernews · f311a · 9月18日 18:51 · [社区讨论](https://news.ycombinator.com/item?id=49758580)

**背景**: 一致性哈希是一种分布式哈希技术，它将键和节点映射到一个环形空间上，这样在增加或移除服务器时，只有一小部分键需要重新映射。它被广泛用于内容分发网络和分布式缓存中，以将负载均匀分散到各个分片。Cloudflare 运营着全球最大的边缘网络之一，其 1.1.1.1 公共 DNS 解析器处理着海量查询，因此其缓存的内存占用是一个重要的运营问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/dns-cache-memory-optimization-1111/">How we saved 100 terabytes of memory by optimizing 1.1.1.1’s ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Consistent_hashing">Consistent hashing</a></li>
<li><a href="https://www.techspot.com/news/113665-cloudflare-freed-up-100tb-ram-behind-1111-dns.html">Cloudflare freed up 100TB of RAM behind its 1.1.1.1 DNS ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多赞赏 Cloudflare 的优化系列文章，有人指出这让人回想起开发者必须在内存和 CPU 稀缺条件下发挥创造力的时代。vlovich123 提出了一个值得注意的反驳观点：用基于分区的方案（使用预计算的 SHA-256 哈希和 wyhash）取代一致性哈希和 Ketama，可以再节省 600TiB。其他人则对代码库孤岛化以及 AI 辅助时代软件工程岗位的未来表示担忧。

**标签**: `#cloudflare`, `#memory-optimization`, `#consistent-hashing`, `#distributed-systems`, `#engineering`

---