---
title: "SLO/SLI Definition"
slug: slo-sli-definition
stage: Ship
category: "Monitoring & Observability"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/slo-sli-definition
---
# SLO/SLI Definition

Define SLOs and SLIs for critical service journeys, with measurement methods, error budget math, burn rate alerts, dashboards, and review cadence.

## Prompt

Define Service Level Objectives (SLOs) and Indicators (SLIs) for this service:

Service: [name and purpose]
Users: [who relies on this — internal teams, end users, partners]
Current pain points: [known reliability issues]

For each critical user journey:
1. SLI: What metric measures the user's experience? (availability, latency, error rate, throughput)
2. Measurement: How exactly is the SLI calculated? (server-side, client-side, synthetic?)
3. SLO target: What percentage/threshold is acceptable? (e.g., 99.9% availability, p99 < 200ms)
4. Error budget: How much downtime/degradation does the SLO allow per month?
5. Burn rate alerts: At what consumption rate should you alert? (1x, 2x, 10x burn rate)
6. Dashboard: What should the SLO dashboard show?
7. Review cadence: How often to review and adjust SLOs?

Include the math: if SLO is 99.9%, that's 43.2 minutes of allowed downtime per month.

## Tips

SRE foundation — without SLOs you're just guessing at reliability.
