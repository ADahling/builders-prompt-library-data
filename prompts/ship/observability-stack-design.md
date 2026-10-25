---
title: "Observability Stack Design"
slug: observability-stack-design
stage: Ship
category: "Monitoring & Observability"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/observability-stack-design
---
# Observability Stack Design

Architect a full-lifecycle observability strategy covering telemetry, alerting, and SLOs tailored to specific scale and budget constraints.

Variables: application_name, architecture_type, scale_description, monthly_budget, current_tools

## Prompt

You are an observability architect. Design a comprehensive observability stack for {{application_name}}.

System details:
- Architecture: {{architecture_type}}
- Scale: {{scale_description}}
- Budget: {{monthly_budget}}
- Current tools: {{current_tools}}

Design:
1. **Metrics**: What to measure (RED method: Rate, Errors, Duration), Prometheus/Datadog setup
2. **Logging**: Structured logging format, log levels, aggregation (ELK/Loki)
3. **Tracing**: Distributed tracing setup (OpenTelemetry), trace sampling strategy
4. **Dashboards**: Key dashboards (system health, business metrics, SLO tracking)
5. **Alerting**: Alert hierarchy (P1-P4), routing, escalation, on-call rotation
6. **SLO/SLI Definition**: Service Level Objectives and Indicators for each service
7. **Error Tracking**: Sentry/Bugsnag setup, error grouping, assignment
8. **Synthetic Monitoring**: Uptime checks, user journey monitoring
9. **Cost Optimization**: How to manage observability costs at scale
10. **Runbooks**: Automated runbooks linked to alerts

## Tips

You can't improve what you can't measure. Observability is the foundation of reliability engineering.
