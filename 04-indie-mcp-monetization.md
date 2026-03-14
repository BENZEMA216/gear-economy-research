# Indie MCP 变现：案例研究

> 诚实的现状：经过验证的独立 MCP 收入案例极其稀少。以下是我们掌握的情况。

## 1. 21st.dev — 标杆案例

### 做什么

最大的 AI 应用 React 组件注册表。**Magic MCP Server** 在 Cursor 和 Windsurf 等 IDE 中，通过自然语言描述生成生产就绪的 UI 组件。

| 指标 | 数值 |
|------|------|
| 总开发者 | **1.4M** |
| 月活用户 | **200K** |
| GitHub stars | **14K+** |
| Product Hunt 上线次数 | 3 |

### 商业模式

**Freemium 分层：**

| 层级 | 价格 | Credits/月 |
|------|------|-----------|
| Free | $0 | 10 |
| Pro | $16/月 | 100 |
| Pro Plus | $32/月 | 200 |
| Scale | 定制 | 500 |

**与组件发布者 50% 分成** — 打造的是 marketplace 生态，而非单一产品。

### 收入

最常被引用的数字：**~£400/月 MRR**。

> "大多数炒作帖子指向同一个案例：21st Dev 的 Magic MCP……据报道月收入约 £400+ MRR — 不算零，但谈不上淘金热。" — [MB Samuel](https://mbsamuel.substack.com/p/will-people-actually-pay-for-mcp)

这是**整个 indie MCP 变现领域中唯一被独立引用的收入数字**。

### 如何解决 "Skill 太薄" 的问题

1. **深度领域专业知识**内置于 server — 不是简单的"生成组件"，而是遵循特定设计模式、使用正确 Tailwind 类、生产就绪的组件
2. **社区贡献质量** — 50+ 位专业设计工程师发布组件
3. **网络效应** — 共享组件库随使用量累积价值
4. **Publisher 模式** 将其变成平台，而非单一工具

### Cline 的博文

[Building the MCP Economy: Lessons from 21st.dev](https://cline.bot/blog/building-the-mcp-economy-lessons-from-21st-dev-and-the-future-of-plugin-monetization)

核心结论：
- 聚焦**具体的、高价值的痛点**，而非泛泛的 "nice-to-have" 工具
- 先发窗口不会永远敞开 — 先占据质量和市场地位的人获益最大
- 5 次免费请求展示价值，然后变现

### 增长轨迹

从组件市场演进为 AI 基础设施 — 推出了 "21st Agents SDK"，定位为 "agent 互联网的基础设施和 UI 构建模块"。

---

## 2. MCPize — "唯一给创作者付钱的 Marketplace"

### 平台概览

[MCPize](https://mcpize.com/) 定位为"唯一集变现、托管和市场于一体的 MCP 平台"。不仅是目录 — 还提供部署基础设施、计费和发现。

### 85% 分成 — 已验证

MCPize 明确表示：**"MCP server 分成比例 85/15 — 创作者保留每笔交易的 85%。"**

对比：

| 平台 | 创作者份额 | 备注 |
|------|-----------|------|
| **MCPize** | **85%** | 生态最高 |
| Apify | 80%（扣除平台成本） | 实际 ~70% |
| MindStudio | 100% | 但创作者需承担 AI 模型成本 |
| Smithery | 0% | 向创作者收费 $30/月 |
| Glama | 0% | 平台保留所有订阅收入 |
| Apple App Store | 70% | 作为参考 |

月度 Stripe 打款。支持订阅、一次性购买、按使用量计费。

### "$3K-$10K/月" 的说法

MCPize 的变现指南声称："Top MCP server 创作者月入 $3,000-$10,000+"。但**无法通过独立的创作者证言或第三方数据验证**。同一指南提到"即使是 $500/月的温和收入，年化也有 $6,000"。这些看起来是营销预测而非已验证案例。

### Server 数量

**350+ 个 MCP server**，跨 20+ 个类别（从 marketplace 验证）。更广泛的生态有 11,000+ MCP servers，但**不到 5% 实现了变现**。

### MCPize 提供什么

- 托管和部署基础设施
- Gateway API（认证、限速、监控）
- Stripe 集成的计费 Dashboard
- 发现和 marketplace 上架

---

## 3. Cline MCP Marketplace

### "AI 能力的 App Store"

[Cline MCP Marketplace](https://cline.bot/mcp-marketplace) — 用户像浏览 app 一样浏览 MCP servers，一键安装。Cline 自动处理 clone、setup、配置。

### 创作者控制权

**关键差异化：创作者完全控制自己的变现方式。** Cline 不处理支付/计费 — 只提供分发和发现。创作者自己实现计费（API keys, Stripe 等）。

这更像是**带商业软件列表的 Linux 包管理器**，而非有集成计费的 App Store。

### 标准 Playbook

Nick Baumann (Cline 团队) 在 X 上：
> "1. 构建一个解决真实痛点的 MCP server。2. 给 5 次免费请求。3. 收 $20/月。"

---

## 4. Enso (RapidAPI 联合创始人)

### 公司详情

由 **Mickey Haslavsky**（RapidAPI 联合创始人）创立。2024 年 7 月脱离隐身模式。

| 详情 | 数据 |
|------|------|
| 融资 | **$6M seed**（NFX） |
| 天使投资人 | Yossi Matias (Google Research)、Shmil Levy (前 Sequoia GP) |
| Agent 数量 | 300+ |
| 定价 | $49/月无限制 或 $29-79/月按 agent |
| 目标 | 缺少技术能力的 SMB |

### 与 LangChain 合作

2025 年 2 月联合 LangChain (LangGraph) 推出。Agent 覆盖社交媒体管理、商业策略、内容创作、HR、法务、增长黑客。

### 开发者经济

平台自动化支付处理和客服。开发者获得"轻松触达数百万小企业并产生持续收入的方式"。**具体分成比例未披露。**

> Sources: [TechCrunch](https://techcrunch.com/2024/07/09/with-6m-in-seed-funding-enso-plans-to-bring-ai-agents-to-smbs/) | [SiliconANGLE](https://siliconangle.com/2025/02/18/enso-launches-ai-agent-marketplace-partnership-langchain/)

---

## 5. MindStudio

### 规模

**150K+ AI agent** 已部署。访问 **200+ AI 模型**。

### 创作者变现模式

**创作者保留 100% 收入。** 无平台费、无分成、无复杂的打款结构。平台向创作者收取基础设施使用费（AI 模型成本按供应商费率，零加价）。

### 定价指导

> "如果一个 agent 每月节省 20 小时，企业时间价值 $50/小时，你就交付了每月 $1,000 的价值。定价 $300-500，给客户留下可观的 ROI。"

有实际的 [变现大师课](https://university.mindstudio.ai/masterclass-sessions/ai-agent-monetization-masterclass)。

---

## 6. 其他变现案例

### 使用 MCP 作为分发渠道的企业公司

| 公司 | 模式 | 备注 |
|------|------|------|
| **Firecrawl** | Freemium（10 次免费爬取/分钟，之后 $16/月） | 有融资的公司，MCP 作为渠道 |
| **Bright Data** | 免费层（5K 请求/月），Pro 从 $4/CPM | 企业级，MCP 作为 GTM |

### Indie 现实

- **Browser-Use**：开源 MCP server。无直接变现。
- **未发现**有 MCP 创作者通过 Patreon/GitHub Sponsors 变现的证据。
- 有开发者"创建了 Trello MCP server，在小众论坛以 $25 出售，一周赚了 $200"（未经验证的营销引用）。

---

## 7. 新兴支付基础设施

| 平台 | 方式 |
|------|------|
| **PayMCP + Walleot** | 轻量 SDK，为现有 MCP server 添加支付，无 Stripe 最低限额 |
| **MCP-Hive** | 按请求付费的 marketplace，带质量指标（准确度、延迟） |
| **Masumi Network** | Cardano 去中心化协议，escrow 智能合约 |
| **Coinbase Payments MCP + x402** | 通过 HTTP 402 的 crypto 原生 agent 支付，仅需邮箱即可创建钱包 |
| **Moesif** | MCP tool call 的使用量计量与计费 |

---

## 8. 关键模式与教训

### 什么有效

1. **解决具体的、高价值的痛点** — 不是 "nice-to-have"。21st.dev 之所以成功，是因为手动创建生产级 UI 组件确实很痛苦。

2. **低摩擦 Freemium** — 5 次免费请求现在是默认模式。证明价值，培养习惯，然后收 $16-20/月。

3. **平台动态优于单一产品** — 21st.dev 的 50% publisher 分成创造了网络效应。单一工具可以被 commodity 化；平台不行。

4. **分发 > 构建** — 没有 Cline/MCPize/Apify，再优秀的 server 也会默默无闻。

### 赢家与输家的区别

**供给 >> 需求**：Smithery 的 2,500+ servers 中仅 8 个超过 50K 安装量。市场充斥着低质量、无差异化的 server。([Madrona](https://www.madrona.com/what-mcps-rise-really-shows-a-tale-of-two-ecosystems/))

**单位经济学问题**：标准分层（$49/$299/$999）只在 10:3:1 的客户比例下可行，但实际大多是 50:3:1。每个 Starter 客户都在亏钱。

**Commodity vs. 专业知识**：简单的 API CRUD 封装价值薄弱。赢家嵌入了**难以复制的领域专业知识**。

### 付费 Agent 工具的最小可行护城河

1. **专有数据或训练** — 无法轻易复制
2. **网络效应** — 共享资产随使用累积价值
3. **Switching cost** — 集成进工作流后，用户不想重新配置
4. **质量深度** — 不只是能力访问，而是专家级执行
5. **品牌/信任** — 在 11K+ servers 且 <5% 变现的环境中，被认知很重要

### 令人不安的真相

> MCP 变现 "淘金热" 叙事本质上指向**一个被验证的成功案例**（21st.dev ~£400/月 MRR）。大多数收入流经将 MCP 作为功能添加的企业 SaaS 公司，而非独立创作者。

> 变现的基础设施（MCPize、PayMCP、Masumi、x402）比实际变现更成熟 — 这是**市场处于 pre-PMF 阶段**的经典标志。

---

## Sources

- [Cline: 构建 MCP 经济](https://cline.bot/blog/building-the-mcp-economy-lessons-from-21st-dev-and-the-future-of-plugin-monetization)
- [人们真的会为 MCP Server 付费吗？(MB Samuel)](https://mbsamuel.substack.com/p/will-people-actually-pay-for-mcp)
- [MCP Server 变现：新兴商业格局 (Ritza)](https://ritza.co/articles/gen-articles/mcp-server-monetization-the-emerging-commercial-landscape/)
- [MCPize 开发者变现指南](https://mcpize.com/developers/monetize-mcp-servers)
- [MCP Server 变现 2026 (DEV Community)](https://dev.to/namel/mcp-server-monetization-2026-1p2j)
- [MCP Server 经济学 (Zeo)](https://zeo.org/resources/blog/mcp-server-economics-tco-analysis-business-models-roi)
- [MCP 崛起的真正含义 (Madrona)](https://www.madrona.com/what-mcps-rise-really-shows-a-tale-of-two-ecosystems/)
- [Cline MCP Marketplace](https://cline.bot/blog/introducing-the-mcp-marketplace-clines-new-app-store)
- [Nick Baumann Playbook (X)](https://x.com/nickbaumann_/status/1897825055092162775)
- [Enso Seed (TechCrunch)](https://techcrunch.com/2024/07/09/with-6m-in-seed-funding-enso-plans-to-bring-ai-agents-to-smbs/)
- [Enso + LangChain (SiliconANGLE)](https://siliconangle.com/2025/02/18/enso-launches-ai-agent-marketplace-partnership-langchain/)
- [MindStudio 创作者经济](https://www.mindstudio.ai/blog/creator-economy-ai-monetizing-agent-apps)
- [21st.dev (Product Hunt)](https://www.producthunt.com/products/21st-dev-the-npm-for-design-engineers)
- [Masumi 变现](https://www.masumi.network/blogs/monetization-of-mcp-servers)
- [Coinbase Payments MCP](https://www.coinbase.com/developer-platform/discover/launches/payments-mcp)
- [MCP-Hive](https://mcp-hive.com/)
- [Skills vs MCP Tools (LlamaIndex)](https://www.llamaindex.ai/blog/skills-vs-mcp-tools-for-agents-when-to-use-what)
