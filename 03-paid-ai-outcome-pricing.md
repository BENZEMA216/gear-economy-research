# Paid.ai 与 Outcome-Based Pricing 深度研究

> 为什么传统 SaaS 定价对 AI Agent 根本不适用，以及谁在构建替代方案。

## 1. Paid.ai 公司深度研究

### 创始人与背景

**Manny Medina** — 前 **Outreach** CEO 兼联合创始人，将 Outreach 做到 **$4.4B 估值**、6,000 客户、**$250M ARR**。2025 年 3 月 25 日推出 Paid。

**联合创始人：**
- **Manoj Ganapathy** — 连续创业者，曾在 Salesforce 构建计费系统
- **Raj Dosanjh** — 早期 Palantir
- **Arnon Shimoni** — 早期 Pleo（欧洲金融科技）

| 详情 | 数据 |
|------|------|
| 成立时间 | 2025 |
| 总部 | 伦敦 |
| 团队 | 24 人 |
| 知名投资人 | Pat Grady (Sequoia Capital) |

### 融资：总计 $33.3M

| 轮次 | 金额 | 领投 |
|------|------|------|
| Pre-seed | ~$11.7M | EQT Ventures |
| Seed | $21.6M（超募） | Lightspeed Venture Partners |
| 总计 | **$33.3M** | + FUSE, EQT, Sequoia |

### Paid.ai 做什么

定位为 **"AI Agent 经济的 Stripe 或 Adyen"** — 计费基础设施，不是 marketplace。Drop-in SDK，几行代码即可集成。

**五大核心能力：**

1. **客户价值证明 ("Value Receipts")** — 品牌化门户，展示 AI agent 实际完成了什么：节省时间、降低成本、规避风险、产生收入、ROI%。超越发票，证明影响力。

2. **自定义定价配置** — 无代码设置 credits、usage-based、outcome-based 或混合定价。分钟级上线每客户定价。

3. **Outcome-Based 与混合模型** — 替代 seat-based：收入分成、成功费、按解决计费、按结果计费。

4. **成本追踪与归因** — 实时遥测追踪每个 agent action 的精确成本，按客户、模型、tool call 细分。利润可见性。

5. **AI 商业智能** — Dashboard 展示按客户/产品/agent 的收入、成本、利润。实时事件流。

**Paid.ai 自身定价：**

| 层级 | 价格 | 计费量 |
|------|------|--------|
| Free | $0/月 | 年计费 ≤$100K |
| Grow | $300/月 | ≤$200K |
| Scale | $600/月 | ≤$500K |
| Accelerate | $1,000/月 | ≤$1M |

符合 SOC 2、GDPR、HIPAA、ISO 27001 标准。

### 核心论点

> 一个 AI 每月处理 1,000 个支持工单，节省了 $50,000 的人力成本，但开发者只收 $500/月。

这就是**价值捕获差距**。Token 定价"把大量价值留在了桌上。它定价的是原材料，不是成品。"

### Paid Blog 的关键概念

- **"SaaSpocalypse"** — Seat-based SaaS 正在消亡。预计到 2030 年 50% 的劳动力将是 AI agent，按座定价将崩溃。
- **Credit-Led Growth (CLG)** — 取代 PLG 和 SLG 的新 GTM 模式，credits 作为参与和扩展的单位。
- **"Human Value Equivalents"** — 将 credits 锚定在人类劳动上（1 credit = 一个人类任务完成的价值）。
- **"Vibe Revenue"** — 批评那些 AI 顶线数字好看但对利润率、单客户成本、可持续单位经济学毫无头绪的公司。

> Sources: [TechCrunch](https://techcrunch.com/2025/03/25/outreach-founder-manny-medina-has-a-new-startup-that-helps-ai-agents-get-paid/) | [Paid Seed 公告](https://paid.ai/blog/company/paid-raises-21-6-million-seed-round) | [Sequoia Portfolio](https://sequoiacap.com/companies/paid/)

---

## 2. Lightspeed 的分析

### "$19 万亿的问题"

[原文链接](https://lsvp.com/stories/the-ai-agent-economy-has-a-19-trillion-problem-our-investment-in-paid/)

**关键数字：**
- **$19.9T** — 2030 年 Agent 经济规模（因定价基础设施缺失而面临风险）
- AI Agent 到 2030 年可贡献全球 GDP 增长的 **7%**（Goldman Sachs）
- **95% 的 AI pilot 未能推向生产** — 不是因为技术不行，而是企业无法量化 ROI
- 接入 Paid 的企业看到 **20-40% 的收入增长**（底层技术相同）

**"Gen AI 悖论"：** 惊艳的 pilot 结果无法转化为生产部署，因为**影响和成本无法用现有工具精确衡量**。

**为什么传统 SaaS 对 Agent 失效：**
- Agent **动态消耗**计算资源（不是固定 seat）
- Agent **持续运行**（24/7，不是 9-5）
- Agent 产生**高度可变的业务结果**（取决于任务复杂度）
- 一个销售 AI 可能"一周产生 $10,000 的 pipeline，下一周 $100,000"，但收取相同月费

### "AI Agent 时代的计费基础设施"

[原文链接](https://lsvp.com/stories/billing-infrastructure-in-the-age-of-co-pilots-and-ai-agents/)

> "Seat-based 模型曾经颠覆了永久授权模型，usage/performance 定价也将颠覆 SaaS。十年后，我们可能会回过头来看，订阅定价只是一个异常时期。"

**对 7 大企业系统的系统性影响：**

1. **CRM** — 必须追踪使用遥测，而非仅追踪交易阶段
2. **CPQ** — 目前改价需 3-6 个月；必须支持 per-use、tiered、credits、outcome-based（通过配置而非代码）
3. **CLM** — 向自主合同审查和动态谈判演进
4. **Procurement** — 从规则审批走向智能自主谈判
5. **Billing/Invoicing** — 从月末账单走向实时使用可见性
6. **Revenue Management** — 必须实时符合 ASC 606、IFRS 15（无法再均匀确认收入）
7. **ERP** — 遗留系统假设静态定价、简单合同、极少的中途变更

### 另：TollBit 投资

Lightspeed 还领投了 **TollBit 的 $24M Series A** — 当 AI 工具使用出版商内容时自动收取费用的基础设施。同一论点：**AI 经济中的价值交换基础设施**。

---

## 3. Outcome-Based Pricing — 深度分析

### 如何定义"结果"？

> "Resolution 是关闭的工单、满意的客户、还是留存的账户？每种定义都影响定价架构、产品开发和客户关系。" — [Sequence](https://sequencehq.com/blog/what-is-outcome-based-pricing)

**实际案例中的结果定义：**

| 公司 | 结果定义 | 价格 |
|------|----------|------|
| **Intercom Fin** | AI 完全解决客户问题（正面回应或无后续追问） | $0.99/次解决 |
| **Zendesk** | AI 无需人工介入即解决（CX 领域首家，2024 年 8 月） | $1.50/次解决 |
| **Sierra** | 分级：简单解决 vs. 复杂 L2 技术支持。转人工不收费 | 按复杂度分层 |
| **Salesforce Agentforce** | 按对话 + AI Credits 系统 | $2/次对话 |

Salesforce 数周内签下 **1,000+ 付费客户**，预计 2025 年该业务贡献 **$4B 收入**。

### 如何衡量和验证结果？

**Intercom 的验证流程：** 向量数据库搜索 → 上下文识别 → LLM 输出 → **基于业务规则的输出再验证** → 计费。"完整解决" 需要检测明确的客户确认或无后续追问。

**所需基础设施**（Metronome）：
- 通过 CRM/分析集成的实时结果追踪
- 影响验证系统
- 可变计费自动化
- 透明的结果 dashboard
- 基于表现的收入确认

### Usage-Based vs. Outcome-Based 对比

| 维度 | Usage-Based | Outcome-Based |
|------|------------|---------------|
| 计价单位 | Token、API 调用、GPU 周期 | 解决的工单、产生的线索、节省的时间 |
| 风险 | 客户承担（账单不可预测） | 供应商承担（不交付 = 零收入） |
| 价值对齐 | 弱（可以不产生价值也计费） | 强（付费 = 验证的价值） |
| 衡量难度 | 低（计数 API 调用） | 高（定义 + 验证结果） |
| 作弊风险 | 低 | 高（agent 可能关闭工单但不真正解决） |
| 每价值单位收入 | 低（定价的是商品） | 高（定价的是成品） |

### 五大挑战

**1. 归因 — "甩锅问题"**
当多个工具、agent 和人类共同贡献结果时，证明直接因果关系很难。Metronome 建议使用多指标和正式的争议解决流程。

**2. 结果定义争议**
"是预约的会议还是成功完成的会议？" 需要在合同中预先约定定义。

**3. 作弊/扭曲激励**
Agent 可能优化可衡量的指标，而非真正的结果。需要护栏和质量指标。

**4. 供应商收入不可预测**
失败的解决尝试消耗资源但不产生收入。这就是为什么**混合模型**（基础费 + 结果奖金）正在成为实际标准。

**5. 支付处理经济学**
Stripe 每笔 2.9% + $0.30 在低价位时会蚕食利润。$0.99/次解决 时，支付手续费消耗 ~60% 的收入。解决方案：月度汇总计费或预付 credits 系统。

---

## 4. 竞争格局

### Outcome-Based 计费的采用者

| 公司 | 方式 | 价位 |
|------|------|------|
| Paid.ai | 完整计费基础设施（"Agent 的 Stripe"） | 平台费 $0-1K/月 |
| Intercom (Fin) | 按解决计费 | $0.99/次解决 |
| Zendesk | CX 领域首家（2024 年 8 月） | $1.50/次解决 |
| Sierra | Outcome + 消耗混合 | 按复杂度分级 |
| Salesforce (Agentforce) | 按对话 + credits | $2/次对话 |
| Forethought | 从订阅转向 outcome-based | 仅在有表现时收费 |

### 计费基础设施竞品

| 公司 | 聚焦 | vs. Paid.ai |
|------|------|------------|
| Metronome | usage-based 计费，扩展到 outcome | 缺少 AI 特定功能（价值证明、成本追踪） |
| Sequence | AI/usage 计费 | 范围更窄 |
| Flexprice | Outcome-based 计费 | 生态更小 |
| Chargebee | 订阅/usage，增加 AI playbooks | 遗留架构 |
| Stripe Billing | 通用 | 无 agent 特定功能 |

### Agent Marketplace 分成比例

| 平台 | 创作者份额 | 平台抽成 |
|------|-----------|---------|
| Agent37 | 80% | 20% |
| OpenAI GPT Store | ~70% | ~30% |
| Anthropic Claude Agent SDK | 50% | 50% |
| Microsoft Copilot Studio | 97% | 3% 固定手续费 |

### 其他行业的 Outcome-Based 模式

并非新概念 — 有现成参照：
- **效果营销**：按点击付费、按获客付费
- **成功费**：投行（交易额的 %）、猎头（首年薪资的 %）
- **风险代理费**：法律行业（和解金额的 %）
- **收益分享**：管理咨询（节省成本的 %）
- **PayPal**：纯 outcome-based — 只在钱动了的时候收费

---

## 5. 对 Skill 创作者变现的启示

### 打包 Skills 的三种定价模型

1. **按调用 (usage-based)**：每次 skill 被调用时创作者获得收入。简单但定价的是商品，不是价值。

2. **按结果 (outcome-based)**：skill 贡献到成功结果时创作者获得收入。每单位收入更高但需要验证和归因。

3. **混合**：基础授权费 + 结果奖金。例如 $0.001/次调用 + 归因价值的 10%。

### 多 Agent 归因问题（"谁买单"）

当 Agent A（编排者）调用 Skill B（研究）和 Skill C（分析）来产生 Outcome D（赚钱的投资建议）…… **谁该获得功劳？**

这映射了数字营销中的**多触点归因问题** — 15 年以上未解决，尽管投入了数十亿。

**可能的方法：**

| 方法 | 机制 | 优点 | 缺点 |
|------|------|------|------|
| Last-touch | 最终 skill 获得报酬 | 简单 | 对上游不公平 |
| 平均分配 | 所有 skill 平分 | 看起来公平 | 忽略差异化贡献 |
| Shapley 值 | 博弈论边际贡献计算 | 理论最优 | 计算昂贵 |
| 市场定价 | Skill 自己设按调用价格 | 完全避免归因 | 无法捕获 outcome 增值 |
| 预定义合同 | 预先协商分成比例 | 近期最实际 | 不灵活 |

### Agent-to-Agent 交易需要什么

- **标准化的结果定义**：机器可读，执行前约定
- **Escrow/结算基础设施**：验证前锁定支付，验证后分发
- **归因证明**：加密或审计链证据证明哪个 agent/skill 贡献了什么
- **争议解决**：当 agent 对结果是否达成存在分歧时

这本质上是**"智能合约"问题** — Paid.ai 发表了 "Legal Contracts Built for AI Agents"（他们 HN 最热帖：72 分，45 评论）。

### 市场信号

- Seat-based 定价从 **21% 降到 15%**（12 个月内，2024-2025）
- Outcome-based 定价：比固定费方案高 **25% ROI**
- 企业 AI 采用率：**2025 年 88%**（2024 年 78%）
- 延迟变现至 ~10K MAU 的 AI marketplace 展示出 **30% 更高的长期增长率**
- 垂直特定 agent：**$2,000/月** vs. 通用工具 $20 — **100 倍溢价**

---

## Sources

- [Paid.ai](https://www.paid.ai)
- [Lightspeed: $19 万亿的问题](https://lsvp.com/stories/the-ai-agent-economy-has-a-19-trillion-problem-our-investment-in-paid/)
- [Lightspeed: AI Agent 时代的计费基础设施](https://lsvp.com/stories/billing-infrastructure-in-the-age-of-co-pilots-and-ai-agents/)
- [TechCrunch: Paid 发布](https://techcrunch.com/2025/03/25/outreach-founder-manny-medina-has-a-new-startup-that-helps-ai-agents-get-paid/)
- [Paid Seed 公告](https://paid.ai/blog/company/paid-raises-21-6-million-seed-round)
- [Sequoia Portfolio: Paid](https://sequoiacap.com/companies/paid/)
- [Sierra: Outcome-Based Pricing](https://sierra.ai/blog/outcome-based-pricing-for-ai-agents)
- [Chargebee: AI 定价 Playbook](https://blog.chargebee.com/blog/pricing-ai-agents-playbook/)
- [Metronome: Outcome-Based Pricing](https://metronome.com/blog/outcome-based-pricing)
- [Sequence: 什么是 Outcome-Based Pricing](https://sequencehq.com/blog/what-is-outcome-based-pricing)
- [Agent37: 如何为 AI Agent 定价](https://agent37.com/blog/how-to-charge-for-ai-agents-you-build)
- [Monetizely: AI Agent 收入模型](https://getmonetizely.com/articles/how-to-build-effective-revenue-models-for-ai-agent-marketplaces)
- [Sequoia Podcast: AI 时代的定价](https://podcasts.apple.com/us/podcast/get-paid-with-manny-medina/id1792748956)
- [Lightspeed: TollBit 投资](https://lsvp.com/stories/investing-in-tollbit-the-internets-ai-toll-booth/)
