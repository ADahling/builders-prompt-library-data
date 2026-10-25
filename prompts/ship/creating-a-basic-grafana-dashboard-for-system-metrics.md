---
title: "Creating a Basic Grafana Dashboard for System Metrics"
slug: creating-a-basic-grafana-dashboard-for-system-metrics
stage: Ship
category: "Monitoring & Observability"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-basic-grafana-dashboard-for-system-metrics
---
# Creating a Basic Grafana Dashboard for System Metrics

Generate a JSON-formatted Grafana dashboard configuration to visualize system performance metrics using Prometheus data sources and alerts.

Variables: cpu_metric, memory_metric, disk_io_metric

## Prompt

You are tasked with creating a Grafana dashboard for monitoring basic system metrics such as CPU usage, memory consumption, and disk I/O. Use Grafana's built-in Prometheus data source to visualize these metrics. Ensure the dashboard includes the following panels: CPU usage over time, memory usage percentage, and disk read/write rates. Provide clear labels for each graph and set appropriate thresholds for alerts. Include a brief description for each panel explaining the metric and its importance. Use the following variables: {{cpu_metric}}, {{memory_metric}}, {{disk_io_metric}}. Output format: a JSON configuration for Grafana that includes all panels and settings.

## Tips

This prompt is suitable for developers new to Grafana and system monitoring.
