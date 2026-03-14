# Gear Economy：竞争格局总览

> Skill 创作者如何在 AI Agent 经济中获利？

## 核心论点

现实世界的 skills 应该被抽象成 Agent 可消费的服务。创作者把专业知识封装进 Agent，通过 A2A（Agent-to-Agent）暴露给其他 Agent 调用，其他 Agent 付费使用，创作者获得收入。

**模型**：创作者 → Agent + Skills → A2A 服务 → 其他 Agent 调用 + 付费 → 创作者收入

## 5 层竞争格局

| 层级 | 功能 | 关键玩家 | 创作者能赚钱吗？ |
|------|------|----------|------------------|
| **MCP 目录** | 发现 | Smithery (3,300+), mcp.so, Glama (4,700+) | 不能 |
| **Tool 平台** | 打包集成 | Composio ($29M), Toolhouse, Arcade ($12M) | 不能（平台自建） |
| **Agent 市场** | 整个 Agent 作为产品 | Enso ($6M), CrewAI ($18M), MindStudio, Relevance AI ($37M) | 能，但卖的是 Agent 不是 skill |
| **变现基础设施** | 计费 + 支付 | MCPize (85%分成), Apify (80%), Paid.ai ($33M) | **能 — 目前最活跃的方向** |
| **支付协议** | 机器对机器支付 rail | x402 (Coinbase), A2A (Google→Linux Foundation), ACP (Stripe+OpenAI) | 底层，赋能上层 |

## 关键发现

### 1. 交易单位是 Agent，不是 skill
所有成功变现的案例卖的都是完整的 agent/workflow，不是单个 skill。单个 skill 太薄 —— 容易复制、难定价、低 switching cost。

### 2. Apify 证明：skill + 数据 + 计算 = 可变现
$25M ARR，仅融资 $3M。80% 创作者分成。Top 创作者月入 $10K+。护城河是基础设施（代理、反爬、运维），不是代码。

### 3. Outcome-based pricing 是未来，但很难
Paid.ai 拿了 $33M 融资，核心论点是 token 定价"把大量价值留在桌上"。Intercom 按 $0.99/次解决收费，Zendesk $1.50。但多 Agent 链中的归因问题仍未解决。

### 4. 支付 rail 正在 commodity 化
Google (A2A)、Stripe+OpenAI (ACP)、Coinbase (x402) 三家在抢。**价值正在向上移动到 discovery + trust + packaging 层。**

### 5. 最大的 gap：skill 创作者变现基础设施
- Anthropic 发布了 SKILL.md 规范（2025 年 12 月），OpenAI 采用了相同格式
- SkillsMP 有 66,500+ skills 但没有变现层
- 没有任何资金充裕的公司在做端到端的创作者经济工具
- "Agent skills 的 Spotify" 机会大开

### 6. Timing risk 真实存在
A2A 非常新（v1.0 刚于 2026-03-12 发布）。真正的 agent-to-agent 需求仍处于萌芽阶段。目前主流用法仍然是"人调用 agent"。

## 定价模型分析

| 模型 | 适用场景 | 风险 |
|------|----------|------|
| Token 透传 + 加价 | 简单透明 | Race to bottom |
| 按调用 / 按任务 | 容易理解 | 不同任务价值差异大 |
| Outcome-based | 价值对齐度最高 | 归因、验证、争议 |
| 订阅 + 配额 | 现金流稳定 | 购买决策门槛高 |
| **混合（按调用 + 价值分层）** | **推荐起步方案** | 复杂度 |

可能的演进路径：**按调用 + 加价 → 按任务 + 价值分层 → outcome-based**，随基础设施成熟逐步迁移。

## 白空间

没有人在做 "Agent Skills 的 Shopify"，即同时提供：
- Skill 打包（帮创作者把专业知识封装成 Agent 服务）
- Discovery + 信任（评分、评价、安全审计）
- 计费基础设施（metering、分账、价值证明）
- A2A 分发（让 Agent 可被其他 Agent 发现）
- 创作者 Dashboard（分析、收入、客户洞察）

## 两条战略路径

**路径 A：Skill→Agent 打包平台**（"Agent Skills 的 Shopify"）
- 帮创作者把原始专业知识打包成可售卖的 Agent 服务
- 平台负责打包 + 计费 + 分发
- 想象空间更大，但执行更重

**路径 B：变现基础设施层**
- 不做 marketplace 本身，做 marketplace 的 infra
- Metering、分账、使用量追踪、创作者 Dashboard
- 更轻，但可能被 Stripe ACP 吞掉

## 下一步

1. Customer discovery：跟潜在创作者和消费者聊
2. 选第一个垂直切口（哪里的 skill 最不可替代 + 价值最高？）
3. 深入具体协议集成（推荐 A2A + x402 技术栈）
4. 原型：Skill 打包 + A2A 暴露 + 计费的 MVP

---

## 研究文档

| # | 主题 | 核心洞察 |
|---|------|----------|
| [01](01-a2a-protocol-ecosystem.md) | A2A 协议生态 | A2A v1.0 刚发布 (2026-03-12)，200+ partners。x402 是最成熟的支付协议。推荐栈：A2A + x402 |
| [02](02-apify-creator-economics.md) | Apify 创作者经济 | $25M ARR，仅融 $3M。80/20 分成。Top 创作者 $10K+/月。愿景："软件界的 AirBnB" |
| [03](03-paid-ai-outcome-pricing.md) | Paid.ai 与 Outcome 定价 | $33M 融资。"95% 的 AI pilot 失败是因为企业无法量化 ROI"。价值证明 + 成本追踪 |
| [04](04-indie-mcp-monetization.md) | Indie MCP 变现 | 仅 1 个验证成功案例 (21st.dev ~£400/月)。市场处于 pre-PMF。基础设施建设领先于实际变现 |
| [05](05-yc-agent-landscape.md) | YC Agent 全景 | S25 的 88% 是 AI。最大 gap：没有真正的双边 agent marketplace + 创作者变现 |
