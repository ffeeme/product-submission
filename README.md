# ffee.me product-submission 外链提交工作台

> 一个本地优先（local-first）、中英双语的外链提交管理工具，帮助独立开发者与 SEO 从业者管理多项目物料、筛选推广平台、记录外链并跟踪目标进度。**所有数据仅保存在浏览器本地，无需登录，不上传服务器。**

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#license)
[![Made with Vanilla JS](https://img.shields.io/badge/Made%20with-Vanilla%20JS-yellow.svg)](#技术栈)
[![Data Stays Local](https://img.shields.io/badge/Privacy-Local%20Only-success.svg)](#隐私与数据)

---

## 目录

- [项目简介](#项目简介)
- [核心功能](#核心功能)
- [快速开始](#快速开始)
- [使用指南](#使用指南)
- [隐私与数据](#隐私与数据)
- [技术栈](#技术栈)
- [相关工具（Web & SEO 精选）](#相关工具web--seo-精选)
- [贡献指南](#贡献指南)
- [License](#license)

---

## 项目简介

做产品推广时，最麻烦的往往不是"发外链"本身，而是**物料散落各处、平台清单记不清、发了哪些、进度到哪一步全靠脑补**。这个工作台把三件事塞进了一个纯前端页面里：

1. **多项目物料库** —— 每个产品独立保存名称、官网、一句话介绍、详细描述，一键复制。
2. **平台清单与筛选** —— 内置 500+ 推广平台（产品发布、AI 目录、SaaS 评测、开发者社区、Reddit、搜索引擎提交入口等），可按分类、状态、Dofollow、是否需要反链、是否免费提交筛选。
3. **外链记录与目标** —— 记录每条外链的 URL、标题和发布日期，并按周 / 月 / 季度 / 年统计目标达成进度。

整个工具就是一个 HTML 文件，双击即用，也可以直接托管到 GitHub Pages。

---

## 核心功能

### 📁 多项目物料库
- 每个项目独立管理：产品名称、官网链接、一句话介绍、详细描述
- 单字段复制 / 整项目一键复制
- 自动识别官网域名，项目可折叠、可删除

### 🔍 500+ 推广平台清单
平台按分类整理，覆盖：
- **产品发布创业**：Product Hunt、BetaList、Indie Hackers、Peerlist、Fazier 等
- **AI 工具目录**：There's An AI For That、Toolify、Futurepedia、Dang.ai 等
- **SaaS 软件评测**：G2、Capterra、AlternativeTo、SaaSHub 等
- **开发者技术**：GitHub、Hacker News、DEV Community、Stack Overflow 等
- **社区推广**：17 个 Reddit 社区（r/SideProject、r/SaaS、r/startups 等）及 Growth Hackers、Lobsters
- **搜索引擎提交入口**：Google Search Console、Bing Webmaster、Yandex、百度搜索资源平台、Naver、Seznam、IndexNow
- **社交内容平台 / 商业企业 PR / 其他渠道**

### 🏷️ 属性筛选
每个平台带三个可切换的属性标记，点击表格中的圆点循环切换（灰=待确认 / 绿=是 / 红=否）：
- **D** — Dofollow
- **B** — 需要反链
- **F** — 免费提交

支持按搜索词、分类、状态、三个属性任意组合筛选与分页。

### 🔗 外链记录
- 每个平台可记录多条外链：URL、标题 / 备注、发布日期
- 状态管理：待提交 / 已提交 / 已通过 / 被拒绝
- 跟进日期设置，逾期未处理的平台会高亮提醒

### 🎯 目标进度
- 按本周 / 本月 / 本季度 / 本年设定外链数量目标
- 自动统计所选周期内已发布的外链数
- 进度条 + 剩余天数 + 智能提示语（落后、持平、超前、已达成）

### 🌐 其他
- 简体中文 / English 一键切换
- 全量 JSON 导入 / 导出，支持旧版 localStorage 数据迁移
- 响应式布局，手机端可用

---

## 快速开始

### 方式一：直接使用（推荐）

1. 下载本仓库中的 `index.html`
2. 用浏览器打开即可，无需安装任何依赖

### 方式二：GitHub Pages 部署

```bash
# Fork 或克隆本仓库
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

进入仓库 **Settings → Pages**，选择分支和根目录，保存后即可通过 `https://<your-username>.github.io/<repo-name>/` 访问。

### 方式三：本地起服务

```bash
# Python 3
python -m http.server 8080

# 或 Node.js
npx serve .
```

然后访问 `http://localhost:8080`。

---

## 使用指南

1. **准备物料**：在「项目物料库」中填写产品信息，点击「添加项目」可管理多个产品。
2. **筛选平台**：在「推广平台」区域按分类、Dofollow、免费提交等条件筛选目标平台。
3. **记录进度**：把平台状态从「待提交」改为「已提交 / 已通过」，填写跟进日期和备注。
4. **登记外链**：点击「管理外链」展开面板，添加已发布的外链 URL 和发布日期。
5. **查看目标**：顶部「数据概览」会根据外链发布日期自动统计周期目标达成情况。
6. **备份数据**：定期点击右上角「导出」保存 JSON 备份；换设备时用「导入」恢复。

> 💡 提示：属性标记（D/B/F）默认是「待确认」，建议在提交过程中逐步完善，形成你自己的平台情报库。

---

## 隐私与数据

- 所有数据保存在浏览器 **localStorage** 中，键名前缀为 `ffee_console_v10_`
- **不上传任何服务器**，无需注册登录，无追踪脚本
- 清除浏览器数据或更换浏览器会导致本地数据丢失，请务必定期使用「导出」功能备份
- 导入会覆盖当前全部平台、项目物料和目标设置，操作前会有确认提示

---

## 技术栈

- **纯前端**：单个 HTML 文件，内联 CSS + 原生 JavaScript（ES6+）
- **无构建、无依赖、无框架**，开箱即用
- 使用 `localStorage` 做持久化，`navigator.clipboard` 做剪贴板操作，`Intl` 做本地化格式化
- 内置 SEO：`meta` 标签、Open Graph、Twitter Card、JSON-LD 结构化数据

---

## 相关工具（Web & SEO 精选）

ffee.me 本身是一个内置 **1000+ 免费在线工具** 的多语言工具箱，所有工具同样在浏览器本地处理文件、不上传服务器。下面挑选了与外链建设、SEO、Web 开发最相关的一批工具，可以作为提交物料制作、落地页优化、结构化数据校验时的配套利器。

### 🔎 SEO 与站点优化
| 工具 | 说明 | 链接 |
|---|---|---|
| Robots.txt 生成器 | 按 User-agent 分组生成 Allow / Disallow 规则与 Sitemap 行 | https://ffee.me/tools/robots-txt-generator/ |
| Robots Meta 生成器 | 组合 index/noindex、follow/nofollow 等指令，输出 meta 标签或响应头 | https://ffee.me/tools/robots-meta-generator/ |
| 站点地图生成器 | 把 URL 列表转成带 lastmod / changefreq / priority 的 sitemap XML | https://ffee.me/tools/sitemap-generator/ |
| Canonical 标签生成器 | 从任意 URL 生成干净的 canonical link 标签 | https://ffee.me/tools/canonical-tag-generator/ |
| Canonical 校验器 | 一次性排查协议、主机、斜杠、查询串、大小写等 canonical 错误 | https://ffee.me/tools/canonical-validator/ |
| Hreflang 标签生成器 | 生成多语言 alternate link 标签，含 x-default 回退 | https://ffee.me/tools/hreflang-tag-generator/ |
| Hreflang 校验器 | 检查缺失自引用、缺失 x-default、重复语言码、缺回链等问题 | https://ffee.me/tools/hreflang-validator/ |
| Meta 标签生成器 | 生成 title、description、canonical、OG、Twitter Card 全套标签 | https://ffee.me/tools/meta-tag-generator/ |
| Meta 描述分析器 | 测量字符数与像素宽度，检查 CTA 与关键词，预览截断效果 | https://ffee.me/tools/meta-description-analyzer/ |
| 标题标签分析器 | 测量标题长度、关键词位置、品牌位置并给出改写建议 | https://ffee.me/tools/title-tag-analyzer/ |
| SERP 摘要预览 | 在桌面端与移动端预览标题、网址、描述在 Google 结果中的样子 | https://ffee.me/tools/serp-snippet-preview/ |
| SERP 特性检查清单 | 逐项检查 title、meta、heading、结构化数据、移动端与性能 | https://ffee.me/tools/serp-feature-checklist/ |
| 页面速度检查清单 | 按图片、CSS/JS、字体、服务器与缓存四组逐项检查前端性能 | https://ffee.me/tools/page-speed-checklist/ |
| 关键词密度检查器 | 统计一、二、三词短语密度，发现过度优化与高频词 | https://ffee.me/tools/keyword-density-checker/ |
| 关键词提取器 | 从任意文本提取关键词，支持单词/双词模式与词频统计 | https://ffee.me/tools/keyword-extractor/ |
| 可读性计算器 | Flesch、Flesch-Kincaid、Gunning Fog、SMOG、Coleman-Liau、ARI | https://ffee.me/tools/readability-calculator/ |
| UTM 链接构建器 | 为任意 URL 添加 utm_source/medium/campaign 等参数 | https://ffee.me/tools/utm-link-builder/ |

### 🧩 结构化数据（Schema）
| 工具 | 说明 | 链接 |
|---|---|---|
| Schema 标记生成器 | 按类型填写信息，生成 JSON-LD（页面、文章、产品、企业） | https://ffee.me/tools/schema-markup-generator/ |
| FAQ Schema 生成器 | 由问答生成 FAQPage JSON-LD | https://ffee.me/tools/faq-schema-generator/ |
| 面包屑 Schema 生成器 | 生成 BreadcrumbList JSON-LD | https://ffee.me/tools/breadcrumb-schema-generator/ |
| 结构化数据测试器 | 粘贴 JSON-LD 即时校验 | https://ffee.me/tools/structured-data-tester/ |

### 🌐 Web 开发与部署
| 工具 | 说明 | 链接 |
|---|---|---|
| HTML Boilerplate 生成器 | 生成完整 HTML5 起始文档（charset、viewport、OG、favicon 等） | https://ffee.me/tools/html-boilerplate-generator/ |
| Open Graph 生成器 | 生成可粘贴的 og meta 标签 | https://ffee.me/tools/open-graph-generator/ |
| Open Graph 预览 | 预览链接卡片在社交媒体上的显示效果 | https://ffee.me/tools/open-graph-preview/ |
| Twitter Card 预览 | 预览 Twitter 卡片展示效果 | https://ffee.me/tools/twitter-card-preview/ |
| .htaccess 生成器 | HTTPS、规范主机名、压缩、缓存、防盗链等 Apache 指令 | https://ffee.me/tools/htaccess-generator/ |
| nginx 配置生成器 | server 块、location、反向代理、gzip、缓存、安全响应头 | https://ffee.me/tools/nginx-config-generator/ |
| 重定向生成器 | 生成 htaccess / nginx / Netlify / Vercel 重定向规则 | https://ffee.me/tools/redirect-generator/ |
| HTTP 状态码查询 | 查询任意状态码的名称、含义与常见原因 | https://ffee.me/tools/http-status-code-lookup/ |
| HTTP 响应头解析器 | 把原始响应头整理成对齐表格并提示重复字段 | https://ffee.me/tools/http-header-parser/ |
| CSP 响应头生成器 | 按指令选择来源，生成严格或 report-only 策略 | https://ffee.me/tools/csp-header-generator/ |
| Favicon HTML 生成器 | 生成页面所需的全部 favicon link 与 meta 标签 | https://ffee.me/tools/favicon-html-generator/ |
| Web Manifest 生成器 | 生成 site.webmanifest（名称、图标、颜色、显示模式） | https://ffee.me/tools/web-manifest-generator/ |
| humans.txt 生成器 | 生成团队与站点致谢文件 | https://ffee.me/tools/humans-txt-generator/ |
| security.txt 生成器 | 生成含联系方式、过期日期、政策链接的 security.txt | https://ffee.me/tools/security-txt-generator/ |

### 📊 数据分析与内容辅助
| 工具 | 说明 | 链接 |
|---|---|---|
| JSON 格式化与校验 | 美化、压缩、校验 JSON | https://ffee.me/tools/json-formatter/ |
| JSON 转 CSV | 把 JSON 数组转成 CSV | https://ffee.me/tools/json-to-csv/ |
| CSV 转 JSON | CSV 转结构化 JSON | https://ffee.me/tools/csv-to-json/ |
| CSV 校验器 | 检查列数一致性与表头重复 | https://ffee.me/tools/csv-validator/ |
| 文本统计 | 字符、词、句、段计数与平均长度、阅读时间 | https://ffee.me/tools/text-statistics/ |
| 文本摘要器 | 基于词频、位置、长度的抽取式摘要 | https://ffee.me/tools/text-summarizer/ |
| 词频统计器 | 统计每个单词出现次数 | https://ffee.me/tools/word-frequency-counter/ |
| N-Gram 生成器 | 生成 1–4 元词组及出现次数 | https://ffee.me/tools/ngram-generator/ |
| 句子拆分器 | 智能处理缩写，每行一句 | https://ffee.me/tools/sentence-splitter/ |
| 句子长度分析器 | 逐句词数、平均/最长/最短与可读性提示 | https://ffee.me/tools/sentence-length-analyzer/ |

### 🔐 安全与编码（提交物料常用）
| 工具 | 说明 | 链接 |
|---|---|---|
| URL 编码器 | 百分号编码 / 解码 URL 与查询串 | https://ffee.me/tools/url-encoder/ |
| URL 解析器 | 拆分协议、主机、端口、路径、查询、片段 | https://ffee.me/tools/url-parser/ |
| Base64 编码器 | 文本 Base64 编解码，完整 UTF-8 支持 | https://ffee.me/tools/base64-encoder/ |
| 哈希生成器 | MD5 / SHA-1 / SHA-256 / SHA-512 | https://ffee.me/tools/hash-generator/ |
| JWT 解码器 | 本地查看 JWT header、payload 与 claims | https://ffee.me/tools/jwt-decoder/ |
| QR 码生成器 | 把链接或文本生成可下载 PNG 二维码 | https://ffee.me/tools/qr-code-generator/ |

> 以上仅为精选。完整 1000+ 工具列表见 [ffee.me](https://ffee.me/)，所有工具均在浏览器本地处理，无需登录、不上传文件。

---

## 贡献指南

欢迎提交 Issue 与 Pull Request：

- **补充平台**：在 `REAL_PLATFORMS` 数组中按现有格式追加 `{ name, url, category }` 即可，分类需属于 `CATEGORIES` 中的一项。
- **修正属性**：如果知道某平台的 Dofollow / 反链 / 免费提交情况，欢迎在 PR 中说明依据。
- **新增语言**：i18n 字典位于 `I18N` 对象，可参照 `zh` / `en` 结构扩展。
- **UI / 功能改进**：请尽量保持单文件、零依赖、本地优先的设计约束。

提交前请确认：
1. 页面在最新版 Chrome / Firefox / Safari 中正常渲染
2. 导入导出、语言切换、筛选、外链增删等功能正常
3. 未引入任何外部追踪或数据上传逻辑

---

## License

本项目基于 [MIT License](LICENSE) 开源。

> 平台清单中的名称与链接归各自所有者所有，本项目仅作索引与整理。属性标记（Dofollow / 反链 / 免费提交）为社区维护的参考信息，可能随时间变化，请以平台实际规则为准。

---

<p align="center">
  <sub>Built with ❤️ by <a href="https://ffee.me/">ffee.me</a> · 数据仅保存在你的浏览器里</sub>
</p>
```
