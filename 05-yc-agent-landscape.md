# YC-Backed AI Agent Infrastructure & Marketplace Landscape (2024-2025)

> 50%+ of YC S25 batch are agentic AI startups. Infrastructure over application is the dominant bet.

## 1. YC S25 Batch Overview

**Demo Day**: September 9, 2025 — 160+ startups, 1 minute / 1 slide each.

**AI Dominance**: 141 startups (88%) classified as AI-native — highest in YC history. 50%+ are "agentic AI" startups.

**Key Themes**:
- **Vertical AI agents** over horizontal — domain-specific for insurance, mortgage, warehouse logistics
- **MCP as standard infrastructure** — multiple startups building gateways, runtimes, tools around Anthropic's MCP
- **Agent security/governance** emerging as its own category
- **Infrastructure over application** — notable shift from "build agents" to "build the plumbing"
- Garry Tan: "AI agents not as features but as the core operating system of brand-new companies"

**Most sought-after S25 startups** (per TechCrunch): Dedalus Labs (agent deployment) and Autumn (AI billing) among the 9 most in-demand.

---

## 2. Agent Infrastructure Companies — Detailed Profiles

### a) Composio — Skills Layer for AI Agents

| Detail | Data |
|--------|------|
| Funding | **$29M total** ($25M Series A led by Lightspeed, Jul 2025) |
| Founded | 2023, by IIT Bombay alumni Soham Ganatra & Karan Vaidya |
| Scale | 100K+ developers, 200+ companies, 1,000+ app integrations |
| Investors | Lightspeed, Elevation Capital, SV Angel. Angels: Guillermo Rauch (Vercel CEO), Dharmesh Shah (HubSpot CTO) |

**Core Tech**: Shared learning/skill layer for AI agents — when one agent learns an edge case (Salesforce integration, GitHub workflow, Supabase MCP), that knowledge becomes available to every other agent. Just-in-time tool calls, secure delegated auth, sandboxed environments, parallel execution.

**Strategic Position**: Moving from "integration layer" to "learning layer" — the RL component creates network effects as agents accumulate experience.

> Sources: [Composio Series A](https://composio.dev/blog/series-a) | [Lightspeed Thesis](https://lsvp.com/stories/investing-in-composio-building-the-backbone-of-ai-agent-intelligence/) | [Together Fund](https://www.together.fund/perspectives/insights/investing-in-composio-building-the-learning-layer-for-agentic-ai)

---

### b) Arcade.dev — MCP Runtime for Secure Agent Auth

| Detail | Data |
|--------|------|
| Funding | **$12M seed** (March 2025) |
| Founded | February 2024, by Alex Salazar (ex-Okta) and Sam Partee (ex-Cray/HPE/Redis) |
| Investors | Laude Ventures (Pete Sonsini, Perplexity co-founder), Flybridge (Chip Hazard — MongoDB, Firebase), Hanabi Capital (Mike Volpi — Cohere, Scale AI) |

**Core Problem**: Authentication is the #1 blocker for production AI agents. No standard way to handle auth when agents act on users' behalf in Gmail, Slack, Salesforce.

**Key Contribution**: Authored the SEP accepted into MCP spec, working directly with Anthropic. Standardizes OAuth 2.0 auth flow for MCP servers via "URL Elicitation."

**Product**: First and only MCP runtime. Ships MCP Gateway + secure framework for building custom MCP tools with OAuth built-in.

> Sources: [Arcade.dev $12M](https://www.businesswire.com/news/home/20250318815130/en/) | [MCP SEP Contribution](https://www.businesswire.com/news/home/20251125080912/en/) | [TechCrunch](https://techcrunch.com/2025/03/18/arcade-raises-12m-from-perplexity-co-founders-new-fund-to-make-ai-agents-less-awful/)

---

### c) Manufact / mcp-use (YC S25)

| Detail | Data |
|--------|------|
| Funding | **$6.3M** (2025) |
| Adoption | 5M+ SDK downloads, 9,000 GitHub stars. Used by NASA, NVIDIA, SAP |

**What they build**: Open-source fullstack MCP framework — SDK + cloud infrastructure for building/deploying MCP servers. Role-based access controls, security profiles, centralized config management.

**Positioning**: "USB-C for AI" — the connector layer standardizing how agents talk to tools.

> Sources: [VentureBeat](https://venturebeat.com/infrastructure/manufact-raises-usd6-3m-as-mcp-becomes-the-usb-c-for-ai-powering-chatgpt-and/) | [YC Page](https://www.ycombinator.com/companies/manufact)

---

### d) Klavis AI (YC X25)

| Detail | Data |
|--------|------|
| Founded by | Ex-Google DeepMind and ex-Lyft engineers |

**What they do differently**: Hosted, multi-tenant MCP servers at scale. Instead of every company running their own MCP servers, Klavis provides production-ready hosted servers with built-in auth.

**Key product**: "Strata" — one MCP server handling thousands of tools via progressive smart tool selection (rather than loading everything).

**Integrations**: GitHub, GitLab, Slack, Discord, Gmail, Salesforce, HubSpot, Notion, Google Drive, Linear, Jira. Available on AWS Marketplace.

> Sources: [Klavis AI](https://www.klavis.ai/) | [YC Page](https://www.ycombinator.com/companies/klavis-ai)

---

### e) Nia / Nozomio (YC S25)

| Detail | Data |
|--------|------|
| Funding | **$6.2M seed** |
| Investors | CRV, BoxGroup, LocalGlobe. Angels: **Paul Graham**, Thomas Wolf |

**Problem**: Context — not generation — is the bottleneck for coding agents. Models don't know your actual repo, wiki, or SDK versions.

**Solution**: MCP server that indexes entire codebases and doc sites, performs deep research, so agents like Cursor/Continue/Cline "just know" the right answer.

**Results**: 27% improvement in Cursor's performance in internal evals after indexing external docs.

> Sources: [HN Launch](https://news.ycombinator.com/item?id=46194828) | [YC Launch](https://www.ycombinator.com/launches/NyY-nia-10x-the-context-of-your-coding-agent)

---

### f) Golf (YC X25) — Agent Security & Governance

**Core insight**: Operates at the MCP layer, not the LLM layer — agents talk to their own LLMs, while Golf governs where they connect to your data.

**3 capabilities**: (1) See every AI agent, MCP server, and data connection including shadow AI; (2) Monitor usage, data access, and actions; (3) Granular policies per tool, team, and data source.

> Sources: [YC Page](https://www.ycombinator.com/companies/golf) | [Golf.dev](https://www.golf.dev/)

---

### g) Other Notable YC Agent Infrastructure

| Company | What | Funding | Notable |
|---------|------|---------|---------|
| **Dedalus Labs** (S25) | "Vercel for AI agents" — deploy MCP servers in 3 clicks | $11M seed | Most sought-after at Demo Day |
| **Blaxel** (X25) | Persistent sandbox, 25ms resume, zero cold starts | $7.3M seed (First Round) | 16 global regions, millions of requests/day |
| **Autumn** (S25) | "Stripe for AI" billing infrastructure | YC only | Processing payments for 40+ YC startups |
| **Alter** (S25) | Zero-trust identity for agents (RBAC/ABAC) | YC only | Supports MCP, A2A coming |
| **Observee** (S25) | All-in-one MCP SDK with OAuth + observability | YC only | 1,000+ pre-integrated tools |

**Also**: Browser Use, CopyCat, Cua, Cyberdesk, Notte (browser/computer-use tools); Mastra, Truffle, Cactus (agent frameworks); Capacitive, Lumari, Odapt, Okibi, Sim Studio (low-code agent builders).

---

## 3. Agent Marketplace / Economy Companies

### Pure Agent Marketplaces

**Conspicuously, there is NO dominant YC-backed pure agent marketplace.** This is a notable gap.

| Company | Type | Status |
|---------|------|--------|
| CrewAI Enterprise Marketplace | Template marketplace with "planned" revenue share | Primarily a framework company |
| Relevance AI | 1,000+ free agents | Primarily a platform company |
| SkillsMP | Community-driven, 66,500+ Agent Skills | Independent project, not a company |
| MindStudio | Build, deploy, monetize agents | 15-30% marketplace fee. Not YC-backed |

### Agent Billing / Payment Infrastructure

| Company | Funding | What |
|---------|---------|------|
| **Autumn** (YC S25) | YC only | Billing infra for AI apps. Open-source. 40+ YC customers |
| **Nevermined** | $4M | "PayPal for AI-Commerce." Agent-to-agent payments. Supports MCP, A2A, x402 |
| **t54 Labs** | $5M | Trust layer for agentic finance. Backed by Ripple + Franklin Templeton |

### Agent Discovery / Trust / Identity

- **Non-Human Identity Governance**: $400M+ raised in 2025 alone as a category
- **Defakto**: $30.75M Series B — machine identity lifecycle management
- **Golf** (YC X25): Shadow AI discovery and governance
- **Alter** (YC S25): Agent identity and access control

---

## 4. CrewAI — Deep Dive

| Detail | Data |
|--------|------|
| Funding | **$18M** (Insight Partners, Oct 2024) |
| Open Source | 40,000 GitHub stars, 1.8M+ monthly downloads |
| Enterprise | 60%+ Fortune 500. 150+ enterprise customers: IBM, Microsoft, P&G, Walmart, SAP, Adobe, PayPal |
| Scale | $3.2M revenue, 100K+ agent executions/day, 1.4B total executions |
| Marketplace | Templates marketplace. Revenue share "planned" but not publicly launched |

**Multi-agent concept**: "Crews" of role-playing autonomous agents with self-iteration, performance evaluation, persistent memory, and collaboration structures.

**Gap**: Revenue share details opaque. Marketplace is template-focused, not a full agent economy.

> Sources: [Insight Partners](https://www.insightpartners.com/ideas/crewai-scaleup-ai-story/) | [SiliconANGLE](https://siliconangle.com/2024/10/22/agentic-ai-startup-crewai-closes-18m-funding-round/)

---

## 5. Relevance AI — Deep Dive

| Detail | Data |
|--------|------|
| Funding | **$37M total** ($24M Series B, Bessemer, May 2025) |
| Scale | 40,000 AI agents registered in Jan 2025 alone |
| Marketplace | 1,000+ free agents for sales, marketing, support, ops |
| Creator Program | Affiliate program (referral commissions), NOT revenue share on agent usage |

**Gap**: Despite 1,000+ agents, the "marketplace" is a template library, not a two-sided marketplace. No structured payout for creators.

> Sources: [TechCrunch Series B](https://techcrunch.com/2025/05/06/relevance-ai-raises-24m-series-b-to-help-anyone-build-teams-of-ai-agents/)

---

## 6. Competitive Landscape Matrix

| Company | Type | Target | Open/Closed | Funding |
|---------|------|--------|-------------|---------|
| Composio | Skill/learning layer | Developers | Open SDK + cloud | $29M |
| Arcade.dev | Auth/runtime | Developers | Open + hosted | $12M |
| Manufact | MCP framework | Dev teams | Open source + cloud | $6.3M |
| Klavis AI | Hosted MCP | Companies | API/hosted | YC |
| Nia/Nozomio | Context | Developers | MCP server | $6.2M |
| Golf | Security | Enterprise | Closed | YC |
| Alter | Identity/access | Enterprise | Platform | YC |
| Dedalus Labs | Deployment | Developers | Platform | $11M |
| Blaxel | Sandbox/compute | Developers | Platform | $7.3M |
| Autumn | Billing | AI startups | Open source | YC |
| CrewAI | Framework + Marketplace | Enterprise | OSS + enterprise | $18M |
| Relevance AI | Platform + Marketplace | GTM teams | Closed | $37M |
| Nevermined | Payments | Developers | Protocol | $4M |

### Where Is Funding Going?

- Total agentic AI startup funding H1 2025: **$2.8B**, projected $6.7B by year-end
- Infrastructure layer growing 2x YoY ($9.2B → $18B)
- Pure agent tooling clustered in $5M-$30M seed/A rounds
- Most money still in foundation model APIs ($12.5B)

---

## 7. The White Spaces

### What's Conspicuously Absent

1. **A true two-sided agent marketplace** — nobody has discovery + ratings + trust scores + creator monetization in one platform. CrewAI = templates. Relevance AI = library. Neither enables meaningful creator economics.

2. **Agent-to-agent payment rails** — Nevermined ($4M) is the only player. Stripe, Visa, Mastercard, PayPal building but no startup has owned this.

3. **Agent reputation/trust scoring** — t54 Labs addresses finance specifically. No general-purpose "agent credit score" or reputation system.

4. **Skill creator monetization infrastructure** — The single biggest gap. Anthropic released Agent Skills spec (SKILL.md) Dec 2025, OpenAI adopted same format. SkillsMP aggregates 66,500+ skills but is a directory. Nobody is building creator economy tooling for agent skill builders.

5. **Agent evaluation/testing at scale** — "One of the biggest unsolved bottlenecks" for enterprise deployment.

6. **Cross-platform agent interoperability** — MCP for tools, but agent-to-agent (A2A) is nascent. No YC company owns this.

---

## 8. Implications

### What the YC Bet Tells Us

1. **Infrastructure is the play right now.** YC is funding picks-and-shovels much more aggressively than application-layer agents. Market view: application layer too early to pick winners, but infrastructure needed regardless.

2. **MCP is the winning standard.** The sheer number of YC MCP companies (Manufact, Klavis, Observee, Dedalus, Golf, Alter, Metorial + Arcade externally) validates MCP as de facto standard. This is the HTTP of agents.

3. **Security/governance is the enterprise unlock.** Golf, Alter, and $400M+ in non-human identity governance signal enterprises won't deploy at scale without security/compliance/audit.

4. **Vertical agents outperform horizontal.** 62.7% CAGR for vertical vs. 46.3% overall (MarketsandMarkets).

### The Skill Creator Monetization Opportunity

This is the single biggest gap in the landscape:

- **Anthropic released SKILL.md spec (Dec 2025)**, OpenAI adopted same format → standard exists but NO monetization layer
- **SkillsMP**: 66,500+ skills, directory only
- **MindStudio**: Allows monetization, 15-30% fee, closed platform
- **CrewAI**: Revenue share "planned" but not launched
- **Composio**: Benefits agent builders, not skill creators
- **Nevermined**: Has payment rails but no discovery/marketplace

**The opportunity**: Build the missing monetization + distribution layer for SKILL.md — the "Spotify for agent skills" where creators earn from usage, with transparent analytics, automated billing, and built-in trust signals. Sits at the intersection of MCP standardization + agent economy + creator economy. Not addressed by any well-funded company.

---

## Funding Summary

| Company | Funding | Stage | Year |
|---------|---------|-------|------|
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
- [YC S25 Batch Analysis (Catalaize)](https://catalaize.substack.com/p/y-combinator-s25-batch-profile-and)
- [YC S25 Full Batch (New Economies)](https://www.neweconomies.co/p/ycstartups2025)
- [Decoding YC S25 (Alumni Ventures)](https://www.av.vc/blog/decoding-ycs-s25-demo-day-trends-takeaways)
- [YC 2025 Agentic Landscape (Medium)](https://artemerritt.medium.com/yc-2025-agentic-landscape-de5af758bd19)
- [Agentic AI Funding H1 2025](https://aiagentsdirectory.com/blog/agentic-ai-venture-funding-explodes-dollar28-billion-invested-in-h1-2025-as-autonomous-workplace-agents-reshape-industries)
- [YC Agent Economy (EntrepreneurLoop)](https://entrepreneurloop.com/y-combinator-agent-economy-startup-innovation/)
- [AI Agent Predictions 2026 (CB Insights)](https://www.cbinsights.com/research/ai-agent-predictions-2026/)
- [Crunchbase AI Funding 2025](https://news.crunchbase.com/ai/big-funding-trends-charts-eoy-2025/)
- [Menlo Ventures State of GenAI 2025](https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/)
