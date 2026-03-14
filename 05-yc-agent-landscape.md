# YC 投资的 AI Agent 基础设施与市场全景 (2024-2025)

> S25 的 50%+ 是 agentic AI 创业公司。基础设施优先于应用层是主导押注。

## 1. YC S25 Batch 概览

**Demo Day**：2025 年 9 月 9 日 — 160+ 创业公司，每家 1 分钟 / 1 张 slide。

**AI 主导**：141 家创业公司（88%）为 AI-native — YC 历史最高。50%+ 是 "agentic AI" 创业公司。

**关键主题**：
- **垂直 AI agent** 胜过水平 — 保险理赔、抵押贷款、仓储物流等领域专用 agent
- **MCP 成为标准基础设施** — 多家创业公司围绕 Anthropic 的 MCP 构建 gateway、runtime、工具
- **Agent 安全/治理**成为独立类别
- **基础设施优先于应用** — 从"构建 agent"到"构建 agent 的管道"的显著转变
- Garry Tan："AI agent 不是功能，而是全新公司和行业的核心操作系统"

**最抢手的 S25 创业公司**（TechCrunch）：Dedalus Labs（agent 部署）和 Autumn（AI 计费）位列 9 家最受追捧的公司。

---

## 2. Agent 基础设施公司 — 详细档案

### a) Composio — AI Agent 的 Skills 层

| 详情 | 数据 |
|------|------|
| 融资 | **$29M 总计**（$25M Series A，Lightspeed 领投，2025 年 7 月） |
| 成立 | 2023 年，IIT Bombay 校友 Soham Ganatra & Karan Vaidya |
| 规模 | 100K+ 开发者，200+ 企业，1,000+ app 集成 |
| 投资人 | Lightspeed, Elevation Capital, SV Angel。天使：Guillermo Rauch (Vercel CEO), Dharmesh Shah (HubSpot CTO) |

**核心技术**：AI agent 的共享学习/skill 层 — 当一个 agent 学会了边缘场景（Salesforce 集成、GitHub workflow、Supabase MCP），这些知识对所有其他 agent 可用。Just-in-time tool calls、安全委托认证、沙箱环境、并行执行。

**战略定位**：从"集成层"走向"学习层" — RL 组件在 agent 积累经验时创造网络效应。

> Sources: [Composio Series A](https://composio.dev/blog/series-a) | [Lightspeed 论点](https://lsvp.com/stories/investing-in-composio-building-the-backbone-of-ai-agent-intelligence/) | [Together Fund](https://www.together.fund/perspectives/insights/investing-in-composio-building-the-learning-layer-for-agentic-ai)

---

### b) Arcade.dev — 安全 Agent 认证的 MCP Runtime

| 详情 | 数据 |
|------|------|
| 融资 | **$12M seed**（2025 年 3 月） |
| 成立 | 2024 年 2 月，Alex Salazar (前 Okta) 和 Sam Partee (前 Cray/HPE/Redis) |
| 投资人 | Laude Ventures (Pete Sonsini, Perplexity 联创), Flybridge (Chip Hazard — MongoDB, Firebase), Hanabi Capital (Mike Volpi — Cohere, Scale AI) |

**核心问题**：认证是生产级 AI agent 的 #1 阻碍。当 agent 需要代表用户在 Gmail、Slack、Salesforce 中操作时，没有标准的安全认证方式。

**关键贡献**：撰写了被 MCP 规范接纳的 SEP，直接与 Anthropic 合作。通过 "URL Elicitation" 标准化了 MCP server 的 OAuth 2.0 认证流程。

**产品**：首个也是唯一的 MCP runtime。同时提供 MCP Gateway + 内置 OAuth 的安全 MCP 工具构建框架。

> Sources: [Arcade.dev $12M](https://www.businesswire.com/news/home/20250318815130/en/) | [MCP SEP 贡献](https://www.businesswire.com/news/home/20251125080912/en/) | [TechCrunch](https://techcrunch.com/2025/03/18/arcade-raises-12m-from-perplexity-co-founders-new-fund-to-make-ai-agents-less-awful/)

---

### c) Manufact / mcp-use (YC S25)

| 详情 | 数据 |
|------|------|
| 融资 | **$6.3M** (2025) |
| 采用 | 5M+ SDK 下载，9,000 GitHub stars。用户包括 NASA, NVIDIA, SAP |

**做什么**：开源全栈 MCP 框架 — SDK + 云基础设施，用于构建/部署 MCP server。基于角色的访问控制、安全配置文件、集中化配置管理。

**定位**："AI 的 USB-C" — 标准化 agent 与工具通信的连接层。

> Sources: [VentureBeat](https://venturebeat.com/infrastructure/manufact-raises-usd6-3m-as-mcp-becomes-the-usb-c-for-ai-powering-chatgpt-and/) | [YC Page](https://www.ycombinator.com/companies/manufact)

---

### d) Klavis AI (YC X25)

| 详情 | 数据 |
|------|------|
| 创始人 | 前 Google DeepMind 和前 Lyft 工程师 |

**差异化**：托管式、多租户 MCP server。企业不需要自己运行 MCP server，Klavis 提供生产就绪的托管 server + 内置认证。

**核心产品**："Strata" — 一个 MCP server 通过渐进式智能工具选择处理数千个工具（不是一次加载全部）。

**集成**：GitHub, GitLab, Slack, Discord, Gmail, Salesforce, HubSpot, Notion, Google Drive, Linear, Jira。在 AWS Marketplace 上可用。

> Sources: [Klavis AI](https://www.klavis.ai/) | [YC Page](https://www.ycombinator.com/companies/klavis-ai)

---

### e) Nia / Nozomio (YC S25)

| 详情 | 数据 |
|------|------|
| 融资 | **$6.2M seed** |
| 投资人 | CRV, BoxGroup, LocalGlobe。天使：**Paul Graham**, Thomas Wolf |

**问题**：Context — 而非生成 — 是 coding agent 的瓶颈。模型不知道你的实际代码仓库、内部 wiki 或确切的 SDK 版本。

**方案**：索引整个代码库和文档站点的 MCP server，执行深度研究，让 Cursor/Continue/Cline 等 agent "直接知道" 正确答案。

**效果**：索引外部文档后，内部评估中 Cursor 性能提升 27%。

> Sources: [HN Launch](https://news.ycombinator.com/item?id=46194828) | [YC Launch](https://www.ycombinator.com/launches/NyY-nia-10x-the-context-of-your-coding-agent)

---

### f) Golf (YC X25) — Agent 安全与治理

**核心洞察**：在 MCP 层而非 LLM 层运作 — agent 与各自的 LLM 通信，而 Golf 治理它们连接到你数据的方式。

**3 大能力**：(1) 看到每个 AI agent、MCP server 和数据连接，包括 shadow AI；(2) 监控使用、数据访问和操作；(3) 按工具、团队和数据源的细粒度策略。

> Sources: [YC Page](https://www.ycombinator.com/companies/golf) | [Golf.dev](https://www.golf.dev/)

---

### g) 其他值得关注的 YC Agent 基础设施公司

| 公司 | 做什么 | 融资 | 亮点 |
|------|--------|------|------|
| **Dedalus Labs** (S25) | "Agent 的 Vercel" — 3 次点击部署 MCP server | $11M seed | Demo Day 最受追捧 |
| **Blaxel** (X25) | 持久化沙箱，25ms 恢复，零冷启动 | $7.3M seed (First Round) | 16 个全球区域，百万级请求/天 |
| **Autumn** (S25) | "AI 的 Stripe" 计费基础设施 | YC only | 为 40+ 家 YC 创业公司处理支付 |
| **Alter** (S25) | Agent 的 Zero-trust 身份认证 (RBAC/ABAC) | YC only | 支持 MCP，A2A 即将支持 |
| **Observee** (S25) | 集 OAuth + 可观测性于一体的 MCP SDK | YC only | 1,000+ 预集成工具 |

**另有**：Browser Use, CopyCat, Cua, Cyberdesk, Notte（浏览器/计算机控制工具）；Mastra, Truffle, Cactus（agent 框架）；Capacitive, Lumari, Odapt, Okibi, Sim Studio（低代码 agent 构建器）。

---

## 3. Agent Marketplace / 经济生态

### 纯 Agent Marketplace

**值得注意的是：没有一家占主导地位的 YC 投资的纯 agent marketplace。** 这是一个显著的 gap。

| 公司 | 类型 | 状态 |
|------|------|------|
| CrewAI Enterprise Marketplace | 模板市场 + "计划中" 的分成 | 本质上是框架公司 |
| Relevance AI | 1,000+ 免费 agent | 本质上是平台公司 |
| SkillsMP | 社区驱动，66,500+ Agent Skills | 独立项目，不是公司 |
| MindStudio | 构建、部署、变现 agent | 15-30% marketplace 费。非 YC |

### Agent 计费/支付基础设施

| 公司 | 融资 | 做什么 |
|------|------|--------|
| **Autumn** (YC S25) | YC only | AI 应用计费基础设施。开源。40+ 家 YC 客户 |
| **Nevermined** | $4M | "AI 商业的 PayPal"。Agent-to-agent 支付。支持 MCP, A2A, x402 |
| **t54 Labs** | $5M | Agent 金融的信任层。Ripple + Franklin Templeton 投资 |

### Agent Discovery / Trust / Identity

- **Non-Human Identity Governance**：2025 年仅此类别融资 $400M+
- **Defakto**：$30.75M Series B — 机器身份生命周期管理
- **Golf** (YC X25)：Shadow AI 发现与治理
- **Alter** (YC S25)：Agent 身份与访问控制

---

## 4. CrewAI — 深度研究

| 详情 | 数据 |
|------|------|
| 融资 | **$18M**（Insight Partners，2024 年 10 月） |
| 开源 | 40,000 GitHub stars，1.8M+ 月下载 |
| 企业 | 60%+ Fortune 500。150+ 企业客户：IBM, Microsoft, P&G, Walmart, SAP, Adobe, PayPal |
| 规模 | $3.2M 收入，100K+ agent 执行/天，14 亿次总执行 |
| Marketplace | 模板市场。分成 "计划中" 但未公开发布 |

**多 Agent 概念**：角色扮演的自主 agent "Crews"，具备自我迭代、性能评估、持久记忆和协作结构。

**Gap**：分成细节不透明。Marketplace 聚焦模板，不是完整的 agent 经济。

> Sources: [Insight Partners](https://www.insightpartners.com/ideas/crewai-scaleup-ai-story/) | [SiliconANGLE](https://siliconangle.com/2024/10/22/agentic-ai-startup-crewai-closes-18m-funding-round/)

---

## 5. Relevance AI — 深度研究

| 详情 | 数据 |
|------|------|
| 融资 | **$37M 总计**（$24M Series B，Bessemer，2025 年 5 月） |
| 规模 | 2025 年 1 月单月注册 40,000 个 AI agent |
| Marketplace | 1,000+ 免费 agent，面向销售、营销、客服、运营 |
| 创作者计划 | 联盟计划（推荐佣金），不是 agent 使用的分成 |

**Gap**：尽管有 1,000+ agent，"marketplace" 本质是模板库，不是双边市场。对创作者没有结构化的打款模式。

> Sources: [TechCrunch Series B](https://techcrunch.com/2025/05/06/relevance-ai-raises-24m-series-b-to-help-anyone-build-teams-of-ai-agents/)

---

## 6. 竞争格局矩阵

| 公司 | 类型 | 目标 | 开放/封闭 | 融资 |
|------|------|------|-----------|------|
| Composio | Skill/学习层 | 开发者 | 开放 SDK + 云 | $29M |
| Arcade.dev | 认证/runtime | 开发者 | 开放 + 托管 | $12M |
| Manufact | MCP 框架 | 开发团队 | 开源 + 云 | $6.3M |
| Klavis AI | 托管 MCP | 企业 | API/托管 | YC |
| Nia/Nozomio | Context | 开发者 | MCP server | $6.2M |
| Golf | 安全 | 企业 | 封闭 | YC |
| Alter | 身份/访问 | 企业 | 平台 | YC |
| Dedalus Labs | 部署 | 开发者 | 平台 | $11M |
| Blaxel | 沙箱/计算 | 开发者 | 平台 | $7.3M |
| Autumn | 计费 | AI 创业公司 | 开源 | YC |
| CrewAI | 框架 + Marketplace | 企业 | OSS + 企业版 | $18M |
| Relevance AI | 平台 + Marketplace | GTM 团队 | 封闭 | $37M |
| Nevermined | 支付 | 开发者 | 协议 | $4M |

### 资金流向何处？

- 2025 H1 agentic AI 创业公司总融资：**$2.8B**，全年预计 $6.7B
- 基础设施层 2x YoY 增长（$9.2B → $18B）
- 纯 agent 工具集中在 $5M-$30M seed/A 轮
- 大部分资金仍在基础模型 API（$12.5B）

---

## 7. 白空间

### 明显缺失的部分

1. **真正的双边 agent marketplace** — 没有人在一个平台上同时提供 discovery + 评分 + 信任分 + 创作者变现。CrewAI = 模板。Relevance AI = 库。都不支持有意义的创作者经济。

2. **Agent-to-agent 支付 rail** — Nevermined ($4M) 是唯一认真做这个的。Stripe, Visa, Mastercard, PayPal 都在布局但没有创业公司占领。

3. **Agent 声誉/信任评分** — t54 Labs 针对金融领域。没有通用的 "agent 信用评分" 或声誉系统。

4. **Skill 创作者变现基础设施** — 最大的单一 gap。Anthropic 发布了 Agent Skills 规范 (SKILL.md, 2025 年 12 月)，OpenAI 采用相同格式。SkillsMP 聚合了 66,500+ skills 但只是目录。没有人在做 agent skill 构建者的创作者经济工具。

5. **Agent 评估/测试规模化** — 被认为是企业部署 "最大的未解决瓶颈" 之一。

6. **跨平台 agent 互操作** — MCP 用于工具，但 agent-to-agent (A2A) 仍处于萌芽。没有 YC 公司占领。

---

## 8. 启示

### YC 的押注告诉我们什么

1. **当前的正确玩法是基础设施。** YC 在 picks-and-shovels 上的投入远多于应用层 agent。市场观点：应用层太早选赢家，但基础设施无论如何都需要。

2. **MCP 是胜出的标准。** YC MCP 公司的数量（Manufact, Klavis, Observee, Dedalus, Golf, Alter, Metorial + 外部的 Arcade）验证了 MCP 作为事实标准的地位。这是 agent 的 HTTP。

3. **安全/治理是企业解锁的关键。** Golf, Alter 和 $400M+ 的 non-human identity governance 融资表明，没有安全/合规/审计，企业不会规模化部署 agent。

4. **垂直 agent 将胜过水平。** 垂直 AI agent 62.7% CAGR vs. 整体市场 46.3%（MarketsandMarkets）。

### Skill 创作者变现的机会

这是格局中最大的单一 gap：

- **Anthropic 发布了 SKILL.md 规范（2025 年 12 月）**，OpenAI 采用相同格式 → 标准已有，但没有变现层
- **SkillsMP**：66,500+ skills，仅作目录
- **MindStudio**：支持变现，15-30% 费率，封闭平台
- **CrewAI**：分成 "计划中" 但未发布
- **Composio**：受益的是 agent 构建者，不是 skill 创作者
- **Nevermined**：有支付 rail 但无 discovery/marketplace

**机会**：为 SKILL.md 标准构建缺失的变现 + 分发层 — "Agent skills 的 Spotify"，创作者从使用中赚取收入，有透明的分析、自动计费和内置的信任信号。位于 MCP 标准化 + agent 经济 + 创作者经济的交汇处。目前没有任何资金充裕的公司在做。

---

## 融资汇总

| 公司 | 融资 | 阶段 | 年份 |
|------|------|------|------|
| Relevance AI | $37M | Series B | 2025 |
| Composio | $29M | Series A | 2025 |
| CrewAI | $18M | Series A | 2024 |
| Arcade.dev | $12M | Seed | 2025 |
| Dedalus Labs | $11M | Seed | 2025 |
| Blaxel | $7.3M | Seed | 2025 |
| Manufact/mcp-use | $6.3M | Seed | 2025 |
| Nia/Nozomio | $6.2M | Seed | 2025 |
| t54 Labs | $5M | Seed | 2025 |
| Nevermined | $4M | Seed | 2025 |

---

## Sources

- [YC S25 Demo Day (TechCrunch)](https://techcrunch.com/2025/09/15/the-9-most-sought-after-startups-from-yc-demo-day/)
- [YC S25 Batch 分析 (Catalaize)](https://catalaize.substack.com/p/y-combinator-s25-batch-profile-and)
- [YC S25 Full Batch (New Economies)](https://www.neweconomies.co/p/ycstartups2025)
- [解读 YC S25 (Alumni Ventures)](https://www.av.vc/blog/decoding-ycs-s25-demo-day-trends-takeaways)
- [YC 2025 Agentic 格局 (Medium)](https://artemerritt.medium.com/yc-2025-agentic-landscape-de5af758bd19)
- [Agentic AI 融资 H1 2025](https://aiagentsdirectory.com/blog/agentic-ai-venture-funding-explodes-dollar28-billion-invested-in-h1-2025-as-autonomous-workplace-agents-reshape-industries)
- [YC Agent 经济 (EntrepreneurLoop)](https://entrepreneurloop.com/y-combinator-agent-economy-startup-innovation/)
- [AI Agent 预测 2026 (CB Insights)](https://www.cbinsights.com/research/ai-agent-predictions-2026/)
- [Crunchbase AI 融资 2025](https://news.crunchbase.com/ai/big-funding-trends-charts-eoy-2025/)
- [Menlo Ventures GenAI 现状 2025](https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/)
