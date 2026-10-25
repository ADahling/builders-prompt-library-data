---
title: "OpenClaw: Competitive Analysis Framework"
slug: openclaw-competitive-analysis-framework
stage: Build
category: "OpenClaw"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-competitive-analysis-framework
---
# OpenClaw: Competitive Analysis Framework

A competitive analysis framework: name your product, up to three competitors, and the focus areas you want compared.

Variables: product, competitor_1, competitor_2, competitor_3

## Prompt

# Competitive Analysis Framework

## Input
- Your product: {{product}}
- Competitors: {{competitor_1}}, {{competitor_2}}, {{competitor_3}}
- Focus areas: Features / Pricing / UX / Market position

## Analysis Dimensions

### Feature Matrix
| Feature | Your Product | Competitor 1 | Competitor 2 |
|---------|-------------|-------------|-------------|
| Feature A | ✅ Full | ⚠️ Partial | ❌ None |
| Feature B | ❌ None | ✅ Full | ✅ Full |
| Feature C | ✅ Full | ✅ Full | ⚠️ Beta |

### Pricing Comparison
| Tier | Your Product | Competitor 1 | Competitor 2 |
|------|-------------|-------------|-------------|
| Free | Limits | Limits | Limits |
| Pro | $X/mo | $Y/mo | $Z/mo |
| Enterprise | Custom | Custom | $W/mo |
| Price per unit | $X/seat | $Y/seat | Flat rate |

### Positioning Map
Plot competitors on two axes:
- X-axis: Simple ← → Full-featured
- Y-axis: Developer-focused ← → Business-focused
Identify whitespace opportunities.

### SWOT per Competitor
| | Strengths | Weaknesses |
|---|-----------|-----------|
| **Opportunities** | How to exploit their weaknesses | Gaps in their roadmap |
| **Threats** | Where they're gaining ground | Their upcoming features |

## Strategic Recommendations
1. **Double down:** Features where you lead and competitors are weak
2. **Table stakes:** Features you must match to avoid churn
3. **Differentiate:** Unique value props competitors can't easily copy
4. **Ignore:** Features that don't align with your ICP

## Monitoring Plan
- Track competitor changelogs monthly
- Monitor their job postings for strategic signals
- Set Google Alerts for competitor brand mentions
- Review quarterly: pricing changes, acquisitions, partnerships

## Tips

Structured competitive analysis with feature matrices, pricing comparisons, positioning maps, and strategic recommendations.
