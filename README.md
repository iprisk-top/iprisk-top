<div align="center">

# 🛡️ IPRisk.top

**免费 IP 纯净度检测工具 — 聚合 16 类独立数据源，一键生成 0-100 参考评分**

**Free IP Reputation Checker — 16 Data Source Categories, One 0-100 Reference Score**

[🌐 立即检测 / Start Check](https://iprisk.top) · [🔍 浏览器环境检测 / Browser Scan](https://iprisk.top/env) · [🧩 浏览器插件 / Extension](https://iprisk.top/extension) · [🛡️ 代理方案 / Proxy Guide](https://iprisk.top/proxy) · [🤖 Telegram Bot](https://t.me/iprisk_top_bot)

</div>

---

## 这是什么 / What is this

IPRisk.top 是一个免费的 IP 纯净度检测工具。输入任意公网 IP，即可查询网络类型、代理/VPN/Tor 信号、黑名单、ASN、地理归属、威胁情报、端口暴露和历史风险记录，并合并为一个 0-100 的纯净度参考评分。

IPRisk.top is a free IP reputation checker. Enter any public IP address to review network type, proxy/VPN/Tor signals, blacklists, ASN, geolocation, threat intelligence, port exposure, and historical risk records, then combine them into a 0-100 reference score.

评分用于帮助你判断一个 IP 当前可观察到的网络信誉信号，适合用于代理、VPS、固定 IP、浏览器环境和跨境业务前的排查。它不是任何第三方平台的放行、登录、注册、付款或流量结果保证。

The score helps you understand currently observable IP reputation signals before using a proxy, VPS, fixed IP, browser profile, or cross-border workflow. It is not an approval, login, registration, payment, or traffic guarantee from any third-party platform.

---

## 为什么做这个 / Why this exists

市面上的 IP 检测工具大多只查一个数据源。问题是：同一个 IP，A 来源可能标记为住宅，B 来源可能标记为代理或机房。只看一家，很难判断分歧来自数据延迟、网络归属变化，还是 IP 本身存在历史污染。

IPRisk 的做法是把多个来源的结果集中到同一份报告里：保留每个来源的原始标签，同时对代理、VPN、Tor、黑名单、欺诈评分、网段邻居质量、BGP、端口和威胁情报做加权汇总。用户可以先看总分，再展开来源明细复核原因。

Most IP checkers rely on one source. The same IP may be labeled residential by one database and proxy or datacenter by another. IPRisk puts multiple source findings into one report: source-level labels remain visible, while proxy, VPN, Tor, blacklist, fraud score, subnet quality, BGP, port exposure, and threat intelligence are aggregated into a weighted score.

---

## 适合谁用 / Who it's for

| 用户群 / User Group | 适合解决的问题 / Use Case |
|---|---|
| 🤖 **AI 用户** — ChatGPT / Claude / Gemini | 使用前核对出口地区、IP 类型和代理/黑名单信号 / Review exit region, IP type, and proxy/blacklist signals before use |
| 🛒 **跨境电商卖家** — Amazon / Shopee / eBay | 为店铺或浏览器环境记录固定出口、网络类型和风险来源 / Record fixed exits, network type, and risk evidence for each workspace |
| 📱 **TikTok / 社媒运营** | 同时排查 IP、DNS、WebRTC、时区和语言是否一致 / Check IP, DNS, WebRTC, timezone, and language consistency |
| 🔧 **VPS / 固定 IP 用户** | 购买前后核对 ASN、机房属性、端口暴露和历史风险 / Review ASN, datacenter signals, exposed ports, and history before or after purchase |
| 🕵️ **指纹浏览器用户** — AdsPower / Multilogin | 验证每个 profile 使用的代理或固定出口当前表现 / Validate current reputation of proxies or fixed exits used by each profile |

---

## 在线工具 / Tools

| 工具 / Tool | 链接 / URL | 说明 / Description |
|---|---|---|
| IP 纯净度检测 | [iprisk.top](https://iprisk.top) | 16 类来源聚合 IP 信誉评分（0-100）/ 16-source-category IP reputation score |
| 浏览器环境检测 | [iprisk.top/env](https://iprisk.top/env) | WebRTC、DNS、时区、语言、国内外出口与浏览器指纹检测 / WebRTC, DNS, timezone, language, route, and browser signal scan |
| 浏览器插件 | [iprisk.top/extension](https://iprisk.top/extension) | Chrome/Edge 插件，持续比对出口 IP、DNS 与 WebRTC 基准 / Chrome/Edge extension for exit IP, DNS, and WebRTC baseline monitoring |
| 代理方案参考 | [iprisk.top/proxy](https://iprisk.top/proxy) | 按 AI、电商、社媒和固定出口场景整理代理/VPS/环境工具 / Proxy, VPS, and browser-environment options organized by use case |
| 安全学院 | [iprisk.top/academy](https://iprisk.top/academy) | IP 信誉、代理类型、DNS/WebRTC 泄露和环境排查指南 / Guides for IP reputation, proxy types, DNS/WebRTC leaks, and environment checks |

---

## 评分怎么算 / How the score works

每次检测会同时查询多个独立来源，包括网络属性、商业风控、威胁情报、Tor/代理识别、黑名单、ASN/BGP、地理位置、端口暴露和网段信誉信号。网络类型决定基础上限，代理、VPN、Tor、黑名单、欺诈、滥用、端口和网段邻居质量会继续影响最终分数。

Each check queries independent source categories covering network classification, commercial fraud signals, threat intelligence, Tor/proxy detection, blacklists, ASN/BGP, geolocation, port exposure, and subnet reputation. Network type sets the base ceiling, while proxy, VPN, Tor, blacklist, fraud, abuse, port, and subnet-neighbor signals adjust the final score.

| 分数 / Score | 含义 / Meaning |
|---|---|
| 85-100 | 🟢 风险信号较少，通常为住宅、移动、多源 ISP 或非常干净的企业网络 / Few risk signals, usually residential, mobile, multi-source ISP, or very clean business networks |
| 70-84 | 🟢 整体信号较少，存在个别需要确认的项目 / Generally low signal count, with a few items worth checking |
| 55-69 | 🟡 存在多项风险或网络属性信号，建议查看扣分原因 / Multiple risk or network-attribute signals; review deductions |
| 40-54 | 🟠 多个来源出现负面记录，需要进一步核对 / Negative records from multiple sources; further review needed |
| 20-39 | 🔴 风险信号集中，使用前应核对黑名单和代理记录 / Concentrated risk signals; review blacklist and proxy records before use |
| 0-19 | 🔴 检测到大量高权重风险信号，不建议仅凭分数判断原因 / Many high-weight risk signals; do not rely on the score alone to identify the cause |

### 干净 IP 的类型参考 / Clean-IP Type Reference

| 类型 / Type | 干净时建议分 / Clean-score range |
|---|---:|
| 真实住宅宽带，多源确认 / Real residential broadband, multi-source confirmed | 100 |
| 多源 ISP/运营商确认，无污染 / Multi-source ISP confirmed, no contamination | 95-100 |
| 移动网络，干净 / Clean mobile network | 96-100 |
| Static residential / ISP proxy | 90-97 |
| 企业/Business 干净 IP / Clean business IP | 75-88 |
| 普通机房干净 IP / Clean generic datacenter IP | 45-65 |
| 已知 VPN / Known VPN | 20-50 |
| 已知 Proxy/Open Proxy / Known proxy or open proxy | 0-35 |
| Tor/恶意/多黑名单 / Tor, malicious, or multiple blacklist matches | 0-10 |

---

## 数据来源 / Data Sources

| 类型 / Type | 当前使用的来源 / Current Sources |
|---|---|
| IP 类型与地理位置 / Network type & geolocation | ipapi.is, ip-api.com, ipinfo.io, IP2Location, proxycheck.io |
| ASN / BGP / 网段 / ASN, BGP & prefix | RIPE STAT, ipapi.is, proxycheck.io |
| 代理 / VPN / Tor / Proxy, VPN & Tor | proxycheck.io, TorProject, ipapi.is, ip-api.com, IP2Location, Scamalytics, Maltiverse |
| 威胁情报 / Threat intelligence | Pulsedive, ThreatFox, DShield, Maltiverse |
| 黑名单与滥用 / Blacklists & abuse | DNSBL, Blocklist.de, DShield, Scamalytics |
| 端口与共享暴露 / Port & shared-host exposure | Shodan, HackerTarget |

不同来源的结果可能有延迟或分歧。IPRisk 会保留来源明细，方便用户查看每个结论来自哪里。

Sources may disagree or update at different times. IPRisk keeps source-level details visible so users can review where each signal came from.

---

## 🏷️ 嵌入徽章 / Embed Badge

在你的网站、博客或 README 中展示 IP 纯净度评分，一行代码嵌入。

Embed IP reputation scores on your website, blog, or README. One line of code.

### SVG 徽章 / Badge

[![IPRisk](https://iprisk.top/badge/1.1.1.1)](https://iprisk.top/ip/1.1.1.1)

```html
<a href="https://iprisk.top/ip/YOUR_IP" target="_blank">
  <img src="https://iprisk.top/badge/YOUR_IP" alt="IPRisk Score" />
</a>
```

```markdown
[![IPRisk](https://iprisk.top/badge/YOUR_IP)](https://iprisk.top/ip/YOUR_IP)
```

### 信任印章 / Trust Seal

[![IP Verified](https://iprisk.top/badge/trust-seal.svg)](https://iprisk.top)

```html
<a href="https://iprisk.top" target="_blank">
  <img src="https://iprisk.top/badge/trust-seal.svg" width="160" />
</a>
```

### 分享卡片 / Share Card (1200×630)

适合 Telegram / 社交媒体分享 / For Telegram & social media sharing:

```text
https://iprisk.top/badge/card/YOUR_IP
```

📖 完整嵌入文档 / Full embed guide: [iprisk.top/badge/doc](https://iprisk.top/badge/doc)

---

## 🔗 社区与链接 / Community & Links

- 🌐 [IPRisk.top](https://iprisk.top)
- 🔍 [浏览器环境检测](https://iprisk.top/env)
- 🧩 [浏览器插件 IPRisk Sentinel](https://iprisk.top/extension)
- 🛡️ [代理方案参考 / Proxy Guide](https://iprisk.top/proxy)
- 📖 [安全学院 Q&A](https://iprisk.top/academy)
- 📝 [关于 IPRisk.top](https://iprisk.top/about)
- 🤖 [Telegram Bot — 发送 IP 即查纯净度](https://t.me/iprisk_top_bot)
- 📢 [Telegram 频道 — IP 情报与网络排查](https://t.me/iprisk_top_channel)

---

*欢迎提交 PR 补充更多工具和资源。/ PRs welcome to add more tools and resources.*
