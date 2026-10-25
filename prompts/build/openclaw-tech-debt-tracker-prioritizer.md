---
title: "OpenClaw: Tech Debt Tracker & Prioritizer"
slug: openclaw-tech-debt-tracker-prioritizer
stage: Build
category: "OpenClaw"
grade: C
score: 66
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-tech-debt-tracker-prioritizer
---
# OpenClaw: Tech Debt Tracker & Prioritizer

Get a technical debt inventory and weighted scoring framework to classify backlog items by impact, frequency, risk, and effort.

## Prompt

# Tech Debt Tracker & Prioritizer

## Debt Classification
| Type | Description | Examples |
|------|-------------|---------|
| **Deliberate** | Conscious shortcuts for speed | "Ship now, refactor later" |
| **Accidental** | Discovered after implementation | Unforeseen scaling issues |
| **Bit rot** | Code aging without maintenance | Outdated dependencies, deprecated APIs |
| **Design** | Architectural limitations | Monolith needing decomposition |
| **Testing** | Insufficient test coverage | No integration tests, flaky tests |
| **Documentation** | Missing or outdated docs | Tribal knowledge, no runbooks |

## Debt Inventory Template
| ID | Title | Type | Location | Age | Impact | Effort | Score |
|----|-------|------|----------|-----|--------|--------|-------|
| TD-001 | Migrate auth to OAuth2 | Design | auth/ | 6 mo | High | L | 8.5 |
| TD-002 | Add retry logic to payments | Deliberate | billing/ | 3 mo | Critical | M | 9.2 |
| TD-003 | Remove deprecated jQuery | Bit rot | frontend/ | 2 yr | Low | XL | 3.1 |

## Prioritization Formula
Score = (Impact × 0.4) + (Frequency × 0.2) + (Risk × 0.2) + (Effort_inverse × 0.2)

| Factor | 1 | 2 | 3 | 4 | 5 |
|--------|---|---|---|---|---|
| Impact | Cosmetic | Minor friction | Slows team | Blocks features | Causes outages |
| Frequency | Yearly | Monthly | Weekly | Daily | Every change |
| Risk | None | Unlikely | Possible | Likely | Certain |
| Effort | XL (months) | L (weeks) | M (days) | S (hours) | XS (minutes) |

## Payoff Strategy
- **20% Rule:** Dedicate 20% of each sprint to debt reduction
- **Boy Scout Rule:** Leave code better than you found it
- **Debt Sprints:** Quarterly dedicated debt-reduction sprint
- **Coupling:** Attach debt items to feature work when areas overlap

## Reporting
Monthly debt report:
- New debt added (with justification)
- Debt retired
- Top 5 riskiest items
- Trend: is debt growing or shrinking?

## Tips

Classifies, inventories, and prioritizes technical debt with a scoring formula. Includes payoff strategies and monthly reporting templates.
