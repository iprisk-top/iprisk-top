<div align="center">

# 🛡️ IPRisk.top

**免费 IP 纯净度检测工具 — 聚合 16 个独立数据源，一键生成 0-100 评分**

**Free IP Purity Detection Tool — 16 Data Sources, One 0-100 Score**

[🌐 立即检测 / Start Check](https://iprisk.top) · [🔍 浏览器环境检测 / Browser Scan](https://iprisk.top/env) · [🤖 Telegram Bot](https://t.me/iprisk_top_bot) · [📢 频道 / Channel](https://t.me/iprisk_top_channel) · [📖 关于 / About](https://iprisk.top/about)

</div>

---

## 这是什么 / What is this

IPRisk.top 是一个免费的 IP 纯净度检测工具。输入任意 IP，同时查询 16 个独立的安全数据库，合并出一个 0-100 的纯净度评分，告诉你这个 IP 是不是机房、是不是在黑名单、适不适合登 ChatGPT / Claude / TikTok / 亚马逊这类对 IP 敏感的平台。

IPRisk.top is a free IP purity detection tool. Enter any IP address — we check it against 16 independent security databases simultaneously, then produce a single 0–100 purity score with transparent per-source attribution. Know instantly whether an IP is datacenter, blacklisted, or safe for IP-sensitive platforms like ChatGPT, Claude, TikTok, and Amazon.

---

## 为什么做这个 / Why this exists

市面上的 IP 检测工具大多只查一个数据源。问题是：同一个 IP，A 来源说是住宅，B 来源说是高风险代理——只看一家你根本不知道该信谁。我们的做法很简单：把 16 家数据源的结果全部拉回来，合并去重，给你一个综合评分和每个来源的具体标签。一眼看清全貌，不用自己一个个查。

这个工具最初是给自己用的——我们在被 Claude 封号、ChatGPT 降智的问题上踩过坑，查了半天才发现根源是 IP 不干净，账号本身没毛病。

Most IP checkers only query a single data source. The problem is: the same IP can show up as "residential" on one source and "high-risk proxy" on another — with just one source, you have no idea which to trust. What we do is simple: pull results from all 16 sources, deduplicate, and give you one aggregate score with per-source tags. Full picture at a glance, no need to check them one by one.

This tool was originally built for ourselves — we got burned by Claude bans and ChatGPT throttling, and after digging around, realized the root cause was a dirty IP, not the account itself.

---

## 适合谁用 / Who it's for

| 用户群 / User Group | 痛点 / Pain Point |
|---|---|
| 🤖 **AI 用户** — ChatGPT / Claude / Gemini | 登录前确认 IP 不是机房或脏代理，降低降智和封号概率 / Verify exit IP before login to reduce throttling and bans |
| 🛒 **跨境电商卖家** — 亚马逊 / Shopee / eBay | 给每个店铺挑纯净度高的独立住宅 IP，避免关联封店 / Pick high-purity residential IPs per store to avoid account-linking bans |
| 📱 **TikTok / 社媒运营** | IP / 时区 / 语言三件套里，IP 是最容易被忽视的一环 / IP is the most overlooked piece among IP/timezone/language consistency |
| 🔧 **技术爱好者 / 自建梯子** | 买 VPS 前先查目标 IP 段纯不纯净，省得上线才发现段脏 / Check target IP ranges before VPS purchase |
| 🕵️ **指纹浏览器用户** — AdsPower / Multilogin | 验证每个 profile 挂的代理 IP 在 16 源下的真实表现 / Validate real 16-source reputation of proxy IPs behind each profile |

---

## 在线工具 / Tools

| 工具 / Tool | 链接 / URL | 说明 / Description |
|---|---|---|
| IP 纯净度检测 | [iprisk.top](https://iprisk.top) | 16 源聚合 IP 风险评分（0-100）/ 16-source aggregated IP risk score |
| 浏览器环境检测 | [iprisk.top/env](https://iprisk.top/env) | WebRTC 泄露、DNS 泄露、时区/语言不匹配检测 / WebRTC leak, DNS leak, timezone & language mismatch |
| 浏览器插件 | [iprisk.top/extension](https://iprisk.top/extension) | Chrome/Edge 插件，实时监测 IP 漂移 / Real-time IP drift alerts |
| 安全学院 | [iprisk.top/academy](https://iprisk.top/academy) | IP 纯净度、代理类型、账号安全 Q&A / Plain-language Q&A on IP purity and security |

---

## 评分怎么算 / How the score works

每次检测同时向 16 个独立来源发起请求，包括威胁情报、商业风控 API、开源 ASN 数据库、IP 地理库、Tor/代理节点公开黑名单等。每个来源返回的信号会映射为加分或扣分，最终合并成 0-100 的评分。检测结果至少需要 10 个数据源成功返回才会入库，12 源以上才会缓存。

Each check fires parallel requests to 16 independent sources. Signals are deduplicated and combined into a 0–100 score. A result is only persisted when at least 10 sources return successfully, and only cached when 12+ succeed.

| 分数 / Score | 含义 / Meaning |
|---|---|
| 90-100 | 🟢 纯净住宅 / 干净 ISP — 适合所有平台 / Clean residential — safe for all platforms |
| 70-89 | 🟢 轻微标记 — 普通用途可以，敏感账号需小心 / Minor flags — fine for general use |
| 40-69 | 🟡 明显代理/机房特征 — 易触发二次验证 / Clear proxy/DC signals — likely triggers 2FA |
| 0-39 | 🔴 高风险 — 多源认定已知滥用，不建议使用 / High risk — flagged by multiple sources, avoid |

---

## 数据来源 / Data Sources

| 类型 / Type | 说明 / Description | 示例 / Examples |
|---|---|---|
| 商业风控 API | 专业的 IP 欺诈评分服务 | Scamalytics, IPQualityScore, proxycheck.io |
| 威胁情报 | 安全社区的 IP 信誉数据 | AbuseIPDB, Pulsedive, GreyNoise, DShield |
| ASN / 地理数据库 | IP 归属和地理位置 | ip-api.com, ipapi.is, IP2Location |
| 黑名单 / DNSBL | 已知恶意 IP 清单 | Spamhaus, SORBS, Barracuda |
| 匿名网络 | Tor / 代理节点公开列表 | TorProject exit list, VPN detection feeds |

---

## 🏷️ 嵌入徽章 / Embed Badge

在你的网站、博客或 README 中展示 IP 纯净度评分，一行代码嵌入。

Embed IP purity scores on your website, blog, or README. One line of code.

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

### Shields.io 端点

```markdown
[![IPRisk](https://img.shields.io/endpoint?url=https://iprisk.top/badge/shields/YOUR_IP&style=flat-square)](https://iprisk.top/ip/YOUR_IP)
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

```
https://iprisk.top/badge/card/YOUR_IP
```

📖 完整嵌入文档 / Full embed guide: [iprisk.top/badge/doc](https://iprisk.top/badge/doc)

---

## 🔗 社区与链接 / Community & Links

- 🌐 [IPRisk.top](https://iprisk.top)
- 🔍 [浏览器环境检测](https://iprisk.top/env)
- 📖 [安全学院 Q&A](https://iprisk.top/academy)
- 📝 [关于 IPRisk.top](https://iprisk.top/about)
- 🤖 [Telegram Bot — 发送 IP 即查纯净度](https://t.me/iprisk_top_bot)
- 📢 [Telegram 频道 — 安全上网指南](https://t.me/iprisk_top_channel)

---

*欢迎提交 PR 补充更多工具和资源。/ PRs welcome to add more tools and resources.*
