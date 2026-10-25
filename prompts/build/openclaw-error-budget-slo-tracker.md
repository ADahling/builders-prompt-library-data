---
title: "OpenClaw: Error Budget & SLO Tracker"
slug: openclaw-error-budget-slo-tracker
stage: Build
category: "OpenClaw"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-error-budget-slo-tracker
---
# OpenClaw: Error Budget & SLO Tracker

Get SLO definitions, error budget calculations, burn-rate alert thresholds, and monthly reporting for service reliability and release decisions.

## Prompt

# Error Budget & SLO Tracker

## SLO Definition Template
| Service | SLI | SLO Target | Window | Error Budget |
|---------|-----|------------|--------|-------------|
| API | Availability (2xx / total) | 99.9% | 30 days | 43.2 min downtime |
| API | Latency (p99 < 500ms) | 99.5% | 30 days | 3.6 hours slow |
| Auth | Login success rate | 99.95% | 30 days | 21.6 min failures |
| Search | Result relevance | 95% | 30 days | 36 hours poor results |

## Error Budget Calculation
Total minutes in window: 30 × 24 × 60 = 43,200
Error budget = (1 - SLO) × total minutes
Budget consumed = actual_bad_minutes / error_budget × 100%

## Alert Thresholds
| Budget Consumed | Status | Action |
|----------------|--------|--------|
| 0-50% | 🟢 Healthy | Ship features freely |
| 50-75% | 🟡 Caution | Slow releases, increase testing |
| 75-90% | 🟠 Warning | Freeze non-critical deploys |
| 90-100% | 🔴 Critical | All hands on reliability |
| >100% | 💀 Exhausted | Full feature freeze until recovered |

## Burn Rate Alerts
- Fast burn: >2% budget consumed in 1 hour → page on-call
- Slow burn: >10% budget consumed in 6 hours → ticket + Slack alert
- Trend alert: projected to exhaust budget in <7 days → notify team lead

## Monthly Report Template
1. Budget status per SLO
2. Incidents that consumed budget (with minutes)
3. Largest budget consumers (ranked)
4. Reliability vs velocity tradeoff assessment
5. Recommendations for next month

## Tips

Track SLOs, calculate error budgets, set burn-rate alerts, and generate monthly reliability reports.
