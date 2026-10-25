---
title: "OpenClaw: Business Advisory Council"
slug: openclaw-business-advisory-council
stage: Build
category: "OpenClaw"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-business-advisory-council
---
# OpenClaw: Business Advisory Council

Get a Telegram business digest combining eight expert assessments of revenue, growth, technology, customers, people, and risk.

Variables: Date

## Prompt

# Business Advisory Council — OpenClaw Multi-Agent Automation

## Concept
8 parallel AI expert personas analyze your business data independently, then a Synthesizer merges their findings into an actionable digest.

## Expert Personas
1. **RevenueGuardian** — Revenue trends, pricing, churn signals
2. **GrowthStrategist** — Acquisition channels, conversion funnels, market expansion
3. **SkepticalOperator** — Cost efficiency, process bottlenecks, operational risks
4. **TechArchitect** — Infrastructure decisions, build vs. buy, technical debt
5. **CustomerChampion** — User feedback patterns, NPS trends, support tickets
6. **MarketIntel** — Competitor moves, industry trends, market positioning
7. **PeopleAdvisor** — Team dynamics, hiring needs, culture signals
8. **RiskAssessor** — Regulatory changes, security posture, business continuity

## Data Sources
Each expert pulls from relevant channels:
- YouTube, Instagram, X analytics (social metrics)
- CRM data (customer relationships)
- Email and meeting summaries
- Slack conversations
- Asana/Linear task boards
- HubSpot pipeline
- Newsletter engagement metrics

## Pipeline
1. Each expert analyzes data independently (parallel execution)
2. Each produces a 3-5 bullet assessment with confidence levels
3. Synthesizer merges all findings, resolves contradictions
4. Numbered digest delivered to Telegram

## Output Format
```
🏛️ ADVISORY COUNCIL — {{Date}}

1. [RevenueGuardian] Monthly churn increased 0.8% — concentrated in
   mid-tier plan. Likely related to feature gap vs. competitor X.

2. [GrowthStrategist] LinkedIn content driving 3× more sign-ups than
   Twitter this month. Recommend shifting budget.

3. [SkepticalOperator] AWS costs up 23% with no traffic increase.
   Suspect runaway Lambda invocations.

4. [RiskAssessor] EU AI Act compliance deadline approaching. Need
   legal review of our automated decision-making features.

Reply "Tell me more about #3" for a deep dive on any item.
```

## Feedback Loop
- Track which items get "tell me more" requests
- Adjust expert focus based on engagement patterns
- Weekly calibration: are the right topics being surfaced?

## Tips

8 parallel AI expert personas analyze business data and produce a merged digest. 'Tell me more about #3' for deep dives. From mberman84's gist.
