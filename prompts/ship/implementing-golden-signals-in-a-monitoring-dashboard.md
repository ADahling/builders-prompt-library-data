---
title: "Implementing Golden Signals in a Monitoring Dashboard"
slug: implementing-golden-signals-in-a-monitoring-dashboard
stage: Ship
category: "Monitoring & Observability"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-golden-signals-in-a-monitoring-dashboard
---
# Implementing Golden Signals in a Monitoring Dashboard

Get dashboard JSON for monitoring latency, traffic, errors, and saturation using existing telemetry, with alert thresholds and an interpretation guide.

Variables: latency_metric, traffic_metric, errors_metric, saturation_metric

## Prompt

Develop a monitoring dashboard that implements the four golden signals: latency, traffic, errors, and saturation. Use data from your existing telemetry systems such as Prometheus or Datadog. For each signal, provide a panel that visualizes relevant metrics. For example, latency could be shown as a heatmap of response times, traffic as a line graph of request rates, errors as a count of error codes, and saturation as a gauge of CPU and memory usage. Define thresholds for each metric to trigger alerts. Use variables: {{latency_metric}}, {{traffic_metric}}, {{errors_metric}}, {{saturation_metric}}. The output should be a JSON configuration for the selected dashboard tool and a brief guide on interpreting each signal.

## Tips

For developers familiar with the concept of golden signals and monitoring tools.
