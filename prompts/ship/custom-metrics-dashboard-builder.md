---
title: "Custom Metrics Dashboard Builder"
slug: custom-metrics-dashboard-builder
stage: Ship
category: "Monitoring & Observability"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/custom-metrics-dashboard-builder
---
# Custom Metrics Dashboard Builder

Generate a comprehensive, production-ready monitoring dashboard configuration with optimized queries and alert rules for specific services.

Variables: service_name, dashboard_tool, metric_1, metric_2, metric_3

## Prompt

You are a data visualization engineer. Design a monitoring dashboard for {{service_name}} using {{dashboard_tool}}.

Key metrics to display:
- {{metric_1}}
- {{metric_2}}
- {{metric_3}}

Dashboard design:
1. **Layout**: Golden signal panels at top (latency, traffic, errors, saturation)
2. **Time Series Graphs**: Request rate, error rate, latency percentiles (p50, p95, p99)
3. **Heatmaps**: Request latency distribution over time
4. **Tables**: Top 10 slowest endpoints, most frequent errors
5. **Single Stats**: Current values with trend arrows
6. **Annotations**: Deployment markers, incident markers
7. **Variables**: Environment, service, time range selectors
8. **Alerts**: Visual alert indicators on each panel

Provide:
- Dashboard JSON/config for import
- PromQL/query for each panel
- Recommended refresh interval
- Alert rules for each critical metric

## Tips

A good dashboard tells a story at a glance. If you need to click around to understand system health, it needs redesign.
