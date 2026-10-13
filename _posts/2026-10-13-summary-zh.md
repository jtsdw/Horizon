---
layout: default
title: "Horizon Summary: 2026-10-13 (ZH)"
date: 2026-10-13
lang: zh
---

> 从 28 条内容中筛选出 2 条重要资讯。

---

1. [黑客远程触发欧洲超市冷柜除霜，冷链遭重创](#item-1) ⭐️ 8.0/10
2. [开发者将 WiFi 7 路由器改造成 320 Msps 软件定义无线电接收机](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [黑客远程触发欧洲超市冷柜除霜，冷链遭重创](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

攻击者远程激活了法国多家连锁超市（包括 Intermarché）商用制冷控制器的自动除霜功能，迫使门店关闭冷藏柜并销毁易腐库存。该事件于 2026 年 10 月被报道，还波及配送和门店定价系统，并被指与老旧的 Danfoss 制冷控制器漏洞有关。 这是一起罕见的针对关键基础设施的真实网络物理攻击，表明不安全的工业控制系统能造成直接的物理和经济损失。它凸显了联网 OT 设备日益扩大的攻击面，以及零售供应链中削减成本与保障安全之间的矛盾。 疑似存在漏洞的设备包括已服役 15 至 20 年的控制器，如 Danfoss SM800（2021 年停止支持）和 SC355（2016 年停止支持），Claroty 的 Team82 此前披露了 Danfoss AK-SM 800A Web 管理界面中的多个漏洞。针对三款 Danfoss 控制器的补丁自 9 月 18 日起已可用，但许多已部署设备仍未修补。

hackernews · Zeekaas · 10月12日 12:16 · [社区讨论](https://news.ycombinator.com/item?id=50055304)

**背景**: 商用制冷控制器是管理超市冷链中压缩机、蒸发器和除霜循环的嵌入式 OT 设备。许多设备接入互联网，以便运营商远程诊断问题并比较各门店的能效，但这种便利也使它们暴露于攻击之下。老旧控制器往往缺乏现代安全功能，却因更换难以带来利润收益而继续服役。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.claroty.com/team82/research/freeze-the-controller-defrost-the-food-uncovering-vulnerabilities-in-danfoss-refrigeration-controllers">Freeze the Controller , Defrost the Food: Uncovering Vulnerabilities in...</a></li>
<li><a href="https://cybernews.com/security/danfoss-refrigeration-hack-france-supermarkets/">Refrigeration Cyberattack Hits French Supermarkets | Cybernews</a></li>
<li><a href="https://securityarsenal.com/blog/danfoss-refrigeration-controller-hack-defrosts-french-supermarkets-ot-defense-and-detection-guide">Danfoss Refrigeration Controller Hack Defrosts French ...</a></li>

</ul>
</details>

**社区讨论**: 评论者指出涉事设备是服役 15 至 20 年的 Danfoss 控制器，并认为轮班工人缺乏进行安全审查或硬件更新换代的资源。还有人强调，订阅锁定的实验室设备和远程管理带来的成本节约推动了不安全的互联网连接，也有人猜测此次攻击可能与 2026 年 8 月美国军事基地的类似事件有关。

**标签**: `#cybersecurity`, `#IoT`, `#critical-infrastructure`, `#industrial-control-systems`, `#supply-chain`

---

<a id="item-2"></a>
## [开发者将 WiFi 7 路由器改造成 320 Msps 软件定义无线电接收机](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 8.0/10

开发者 h0m3us3r 在 GitHub 上发布了 w1700k-sdr 项目，将一台 WiFi 7 路由器改造成软件定义无线电接收机，能够以每秒 3.2 亿次采样（320 Msps）的速率捕获信号。该开发者此前还曾用 ESP32 Wi-Fi 微控制器搭建过 SDR，显示出将廉价无线硬件转化为低成本射频工具的一贯思路。 这表明常见的 WiFi 7 硬件可以被改造成高速射频采集设备，成本远低于专用 SDR 接收机，有望让低成本射频实验惠及更广泛的群体。这也意味着随着 WiFi 芯片组性能提升，普通笔记本电脑和路由器都可能成为业余爱好者和研究人员的廉价 SDR 平台。 该接收机只能在窄带范围内工作，这限制了它在许多需要宽带覆盖的传统 SDR 应用中的实用性。社区成员指出，由于 Banana Pi R4 采用相同的芯片组，该方法可能也适用于该开发板，后者内置了用于 NVMe 的 PCIe 接口。

hackernews · djfergus · 10月12日 12:41 · [社区讨论](https://news.ycombinator.com/item?id=50055593)

**背景**: 软件定义无线电（SDR）是一种用软件而非专用硬件进行无线电信号处理的技术，使单一设备能够接收或发送多种频率和协议。Airspy、HackRF 等传统 SDR 接收机是专用设备，而该项目则利用了 WiFi 7 路由器中已有的高速模数转换器。WiFi 7 是最新的 IEEE 802.11be 标准，相比前几代提供更高吞吐量和更先进的射频前端。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://airspy.com/">Airspy SDR - High Quality Software - Defined Radio , Redefined</a></li>
<li><a href="https://www.nooelec.com/store/sdr.html">Nooelec - Software Defined Radio</a></li>
<li><a href="https://www.cnet.com/home/internet/best-wifi-7-routers/">Best Wi-Fi 7 Routers for 2026: Future-Proof Your Home ... - CNET Best Wi-Fi 7 Router for Home and Homelab: 8 Picks ... 12 Best WiFi 7 Routers (October 2026) Complete Guide 6 Best Wi-Fi 7 Routers (October 2026 Tested Reviews 8 Best WiFi 7 Routers (October 2026) Tested - fypower.org Best Wi-Fi 7 Routers Tested and Reviewed 2026 10 Best WiFi 7 Routers (October 2026) Expert Tested Reviews</a></li>

</ul>
</details>

**社区讨论**: 评论者大多热情高涨，有人称其“超级酷”，并指出这是获得 5 GHz 下 320 Msps 接收机的最便宜方式。也有人提出警告：窄带限制使其无法用于许多 SDR 场景，还有评论者认为由于芯片组相同，它应该也能在 Banana Pi R4 上运行。一位硬件爱好者设想添加衰减器、滤波器和上下变频器，将其变成完整的服务监测仪。

**标签**: `#SDR`, `#WiFi`, `#hardware hacking`, `#RF`, `#embedded systems`

---