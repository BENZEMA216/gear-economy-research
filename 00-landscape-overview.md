# Gear Economy: Competitive Landscape Overview

> How skill creators can monetize in the AI agent economy.

## Core Thesis

Real-world skills should be abstracted into agent-consumable services. Creators package expertise into agents, expose them via A2A (Agent-to-Agent), and other agents pay to call them. The creator gets compensated.

**Model**: Creator → Agent with Skills → A2A service → Other agents call + pay → Creator earns

## The 5-Layer Stack

| Layer | What | Key Players | Creator Revenue? |
|-------|------|-------------|-----------------|
| **MCP Directories** | Discovery | Smithery (3,300+), mcp.so, Glama (4,700+) | No |
| **Tool Platforms** | Packaged integrations | Composio ($29M), Toolhouse, Arcade ($12M) | No (platform builds) |
| **Agent Marketplaces** | Whole agents as products | Enso ($6M), CrewAI ($18M), MindStudio, Relevance AI ($37M) | Yes, but sells agents not skills |
| **Monetization Infra** | Billing + payments | MCPize (85% share), Apify (80%), Paid.ai ($33M) | Yes — this is where the action is |
| **Payment Protocols** | Machine-to-machine rails | x402 (Coinbase), A2A (Google→Linux Foundation), ACP (Stripe+OpenAI) | Bottom layer, enables everything |

## Key Findings

### 1. The unit of commerce is the agent, not the skill
Every successful monetization example sells complete agents/workflows, not individual skills. Single skills are too thin — easily copied, hard to price, low switching costs.

### 2. Apify proves skill + data + compute = monetizable
$25M ARR on $3M raised. 80% creator share. Top creators earn $10K+/mo. The moat is infrastructure (proxies, anti-bot, maintenance), not code.

### 3. Outcome-based pricing is the future, but hard
Paid.ai raised $33M on the thesis that token pricing "leaves mountains of value on the table." Intercom charges $0.99/resolution, Zendesk $1.50. But attribution in multi-agent chains remains unsolved.

### 4. Payment rails are commoditizing fast
Google (A2A), Stripe+OpenAI (ACP), Coinbase (x402) all competing. Value moves UP to discovery + trust + packaging.

### 5. The biggest gap: skill creator monetization infrastructure
- Anthropic released SKILL.md spec (Dec 2025), OpenAI adopted same format
- SkillsMP has 66,500+ skills but no monetization
- No well-funded company is building end-to-end creator economy tooling
- The "Spotify for agent skills" opportunity is wide open

### 6. Timing risk is real
A2A is very new (v1.0 just released 2026-03-12). Real agent-to-agent demand is still nascent. Most usage is still "human calls agent."

## Pricing Model Analysis

| Model | Best For | Risk |
|-------|----------|------|
| Token passthrough + margin | Simple, transparent | Race to bottom |
| Per-call / per-task | Easy to understand | Value variance across tasks |
| Outcome-based | Highest value alignment | Attribution, verification, disputes |
| Subscription + quota | Stable cash flow | High purchase decision barrier |
| **Hybrid (per-call + value tier)** | **Recommended starting point** | Complexity |

Likely evolution: **per-call + margin → per-task + value tiers → outcome-based** as infrastructure matures.

## The White Space

Nobody is building the "Shopify for Agent Skills" that combines:
- Skill packaging (help creators wrap expertise into agent services)
- Discovery + trust (ratings, reviews, security audit)
- Billing infrastructure (metering, payment splitting, value receipts)
- A2A distribution (make the agent discoverable by other agents)
- Creator dashboard (analytics, earnings, customer insights)

## Two Strategic Paths

**Path A: Skill→Agent Packaging Platform** ("Shopify for Agent Skills")
- Help creators package raw expertise into sellable agent services
- Handle packaging + billing + distribution
- Bigger vision, heavier execution

**Path B: Monetization Infrastructure Layer**
- Don't build the marketplace, build the infra for marketplaces
- Metering, billing split, usage tracking, creator dashboard
- Lighter, but risk of being absorbed by Stripe ACP

## Next Steps

1. Customer discovery: talk to potential creators and consumers
2. Choose first vertical (where is skill most irreplaceable + highest value?)
3. Deep dive specific protocol integration (A2A + x402 recommended stack)
4. Prototype: MVP of skill packaging + A2A exposure + billing

---

## Research Documents

| # | Topic | Key Insight |
|---|-------|-------------|
| [01](01-a2a-protocol-ecosystem.md) | A2A Protocol Ecosystem | A2A v1.0 just launched (2026-03-12), 200+ partners. x402 most mature payment protocol. Recommended stack: A2A + x402 |
| [02](02-apify-creator-economics.md) | Apify Creator Economics | $25M ARR on $3M raised. 80/20 split. Top creators $10K+/mo. Vision: "AirBnB for software" |
| [03](03-paid-ai-outcome-pricing.md) | Paid.ai & Outcome Pricing | $33M raised. "95% of AI pilots fail because companies can't quantify ROI." Value receipts + cost tracking |
| [04](04-indie-mcp-monetization.md) | Indie MCP Monetization | Only 1 verified success (21st.dev ~£400/mo). Market is pre-PMF. Infrastructure ahead of actual monetization |
| [05](05-yc-agent-landscape.md) | YC Agent Landscape | 88% of S25 is AI. Biggest gap: no true two-sided agent marketplace with creator monetization |
