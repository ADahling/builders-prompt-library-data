---
title: "OpenClaw: Technical Debt Prioritization Matrix"
slug: openclaw-technical-debt-prioritization-matrix
stage: Build
category: "OpenClaw"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-technical-debt-prioritization-matrix
---
# OpenClaw: Technical Debt Prioritization Matrix

Get a technical debt classification and impact versus effort matrix with scoring criteria to prioritize engineering maintenance work.

Variables: description, category, score, days, P0-P3, team, Q

## Prompt

# Technical Debt Prioritization Matrix

## Debt Classification

### Categories
| Category | Description | Example |
|----------|-------------|---------|
| Code Debt | Poor code quality, no tests | God classes, copy-paste code |
| Architecture Debt | Wrong patterns, tight coupling | Monolith that should be split |
| Infrastructure Debt | Manual processes, outdated infra | No IaC, manual deployments |
| Dependency Debt | Outdated/vulnerable packages | Major version behind, CVEs |
| Documentation Debt | Missing/outdated docs | No API docs, stale runbooks |
| Test Debt | Low coverage, flaky tests | No integration tests, 20% coverage |
| Process Debt | Manual steps, no automation | Manual QA checklist, no CI/CD |

## Prioritization Framework

### Impact × Effort Matrix
```
                    Low Effort    High Effort
High Impact    │  DO FIRST ★   │  PLAN NEXT    │
               │  Quick wins    │  Major project │
Low Impact     │  AUTOMATE     │  DON'T DO     │
               │  If free, do  │  Not worth it  │
```

### Scoring Rubric (1-5 each)
| Dimension | 1 (Low) | 5 (High) |
|-----------|---------|----------|
| Blast Radius | One file | Entire system |
| Developer Pain | Minor annoyance | Blocks daily work |
| Customer Impact | No user impact | Causes outages/bugs |
| Risk | No security/compliance risk | Active vulnerability |
| Growth Blocker | No effect on scaling | Prevents scaling |

**Priority Score = (Blast Radius + Dev Pain + Customer Impact + Risk + Growth Blocker) / Effort**

### Debt Inventory Template
| ID | Description | Category | Score | Effort (days) | Priority | Owner | Quarter |
|----|-------------|----------|-------|---------------|----------|-------|---------|
| TD-001 | {{description}} | {{category}} | {{score}} | {{days}} | {{P0-P3}} | {{team}} | {{Q}} |

## Integration Into Sprint Work
- Allocate 15-20% of sprint capacity to tech debt
- Every feature PR should include one small debt fix ("boy scout rule")
- Tech debt review in sprint planning (pick top 2-3 items)
- Quarterly tech debt retrospective
- Track debt-to-feature ratio in metrics dashboard

## Anti-Patterns
- ❌ "We'll fix it later" without tracking
- ❌ Dedicated "tech debt sprints" (never gets priority)
- ❌ Rewriting instead of incremental improvement
- ❌ No metrics on debt (can't improve what you don't measure)
- ❌ Gold plating disguised as debt reduction

## Tips

Technical debt prioritization matrix with classification, impact-effort scoring rubric, inventory template, sprint integration, and anti-patterns.
