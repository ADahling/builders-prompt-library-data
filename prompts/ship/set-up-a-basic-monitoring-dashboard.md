---
title: "Set Up a Basic Monitoring Dashboard"
slug: set-up-a-basic-monitoring-dashboard
stage: Ship
category: "Deployment & Launch"
grade: B
score: 71
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-a-basic-monitoring-dashboard
---
# Set Up a Basic Monitoring Dashboard

Configure a monitoring dashboard in a specific tool to visualize core system performance metrics and high-percentile request latency.

Variables: monitoring_tool

## Prompt

You are a site reliability engineer (SRE). Your task is to set up a basic monitoring dashboard for a web service using {{monitoring_tool}}. The service exposes metrics for CPU usage, memory usage, and request latency.

Instructions:
1. Create a new dashboard in {{monitoring_tool}}.
2. Add widgets to visualize CPU and memory usage over time.
3. Create a chart to display the P95 request latency.
4. Set the dashboard to auto-refresh every 5 minutes.

## Tips

An introductory prompt for those new to monitoring and observability.
