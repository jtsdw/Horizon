---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 30 条内容中筛选出 2 条重要资讯。

---

1. [SpaceX 成功捕获星舰助推器，完成第 15 次试飞](#item-1) ⭐️ 9.0/10
2. [Lovable 应用泄露护照信息和 20 万条私人消息](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SpaceX 成功捕获星舰助推器，完成第 15 次试飞](https://www.spacex.com/launches/starship-flight-15) ⭐️ 9.0/10

SpaceX 在第 15 次试飞结束时成功捕获了星舰助推器，这是迈向完全可重复使用火箭的重要一步。 这一里程碑证明了完全可重复使用发射系统的可行性，有望大幅降低太空进入成本，并实现频繁的大规模轨道及更远任务。 此次捕获使用发射塔的“筷子”机械臂完成，该技术首次在第 5 次试飞中成功演示。第 15 次试飞还旨在测试上级的热防护罩，并计划尝试捕获飞船，但助推器捕获是主要成功点。

hackernews · ls612 · 11月14日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=50500963)

**背景**: 星舰是 SpaceX 的下一代完全可重复使用超重型运载火箭，由超重型助推器和星舰飞船组成。助推器返回发射场后由发射塔的机械臂在空中捕获，无需着陆腿，从而实现快速复用。这种方法与航天飞机形成对比，后者仅部分可重复使用，且翻新过程复杂昂贵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thespaceroad.com/articles/how-does-starship-catch-work/">How does the Starship catch work? | The Space Road</a></li>
<li><a href="https://grokipedia.com/page/SpaceX_Starship_Flight_Test_15">SpaceX Starship Flight Test 15</a></li>
<li><a href="https://www.cbsnews.com/news/spacex-launches-starship-flight-rocket/">SpaceX launches milestone Starship flight to... - CBS News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 社区将这一成就誉为历史性里程碑，并与航天飞机对比，强调星舰的完全可重复使用设计和流水线生产。评论者指出，如果热防护罩能保持完好，两级复用将大幅降低成本，还有人讨论了未来同时捕获助推器和飞船的可能性。

**标签**: `#spacex`, `#starship`, `#reusable-rockets`, `#aerospace`, `#spaceflight`

---

<a id="item-2"></a>
## [Lovable 应用泄露护照信息和 20 万条私人消息](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

安全研究员 Crissy Field 报告称，使用 AI 应用构建平台 Lovable 生成的应用因 Supabase 数据库中的行级安全（RLS）配置不足，导致护照信息和超过 20 万条私人消息等敏感数据泄露。 这一事件凸显了 AI 生成应用中的系统性风险：非专业用户可以快速部署采用不安全默认配置的应用，可能导致大规模数据泄露，并引发对平台责任的质疑。 根本原因是 RLS 配置不足，而 Lovable 的安全扫描正是为了捕捉此类问题；该公司免费提供自动扫描和更深入的 SAST 扫描，用户可启用自动修复或阻止发布。据报道，Supabase 已于 10 月 30 日修复了默认 RLS 设置，但一些现有项目可能仍存在不安全的默认配置。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**背景**: 行级安全（RLS）是 PostgreSQL 的一项功能，允许定义策略来控制用户可访问哪些行，Supabase 利用它进行授权。Lovable 是一个 AI 驱动的应用构建器，用户通过自然语言描述即可创建全栈应用。AI 生成的代码常引入安全漏洞，如缺少身份验证或不安全的数据处理，而 Lovable 和 Supabase 等平台的默认安全设置正受到审视。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://supabase.com/docs/guides/database/postgres/row-level-security">Row Level Security - Supabase Docs</a></li>
<li><a href="https://lovable.dev/">App & Website Builder | Build Software in Minutes | Lovable</a></li>
<li><a href="https://www.techtarget.com/cybersecurity/tip/Security-risks-of-AI-generated-code-and-how-to-manage-them">Security risks of AI - generated code and how to manage... | TechTarget</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（743 分，295 条评论）有研究员和 Lovable 安全负责人参与，围绕 Supabase 的默认 RLS 配置及其责任展开辩论。评论者认为平台需要更好的默认拒绝安全策略，AI 生成的应用容易成为简单攻击的目标，也有人指出数据泄露在 AI 之前就存在，但现在数量更多且普通用户更易接触。

**标签**: `#security`, `#AI-generated-code`, `#Supabase`, `#row-level-security`, `#data-breach`

---