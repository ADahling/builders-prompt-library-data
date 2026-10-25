---
title: "OpenClaw: Investor Updates & Runway Monitor"
slug: openclaw-investor-updates-runway-monitor
stage: Build
category: "OpenClaw"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-investor-updates-runway-monitor
---
# OpenClaw: Investor Updates & Runway Monitor

Set up monthly investor updates with metrics, highlights, and asks, plus weekly cash runway checks and threshold alerts for founders.

Variables: Company, Month Year, amount, %, target, count, +/-, change, Auto-generated from team digest, Asana milestones, Flagged items from advisory council, risk assessor, Carried forward from previous unresolved asks, months, date range, Date, If runway < alert threshold:, X

## Prompt

# Investor Updates & Runway Monitor — OpenClaw Founder Automation

## Monthly Investor Update (1st of each month)
Auto-compile from data sources:

```markdown
# {{Company}} — Investor Update — {{Month Year}}

## Key Metrics
| Metric | This Month | Last Month | MoM Change | Target |
|--------|-----------|------------|------------|--------|
| MRR | ${{amount}} | ${{amount}} | {{%}} | ${{target}} |
| Customers | {{count}} | {{count}} | {{+/-}} | {{target}} |
| Churn | {{%}} | {{%}} | {{change}} | <{{target}}% |
| CAC | ${{amount}} | ${{amount}} | {{change}} | <${{target}} |
| Burn | ${{amount}} | ${{amount}} | {{change}} | — |

## Highlights
- {{Auto-generated from team digest, Asana milestones}}

## Challenges
- {{Flagged items from advisory council, risk assessor}}

## Asks
- {{Carried forward from previous unresolved asks}}

## Runway
**Current runway: {{months}} months** (at current burn rate)
Runway at 50% growth: {{months}} months
Next fundraise window: {{date range}}
```

## Runway Monitor (Weekly)
```
💰 RUNWAY CHECK — {{Date}}
Cash: ${{amount}}
Monthly burn: ${{amount}} (30-day rolling avg)
Runway: {{months}} months
⚠️ Alert threshold: {{months}} months

{{If runway < alert threshold:}}
🔴 RUNWAY WARNING: Less than {{X}} months remaining.
Consider: 1) Revenue acceleration 2) Cost reduction 3) Begin fundraise process
```

## Tips

For founders: auto-compiles investor updates from multiple data sources. Weekly runway monitoring with alerts. From Rezvani's 25 automation prompts.
