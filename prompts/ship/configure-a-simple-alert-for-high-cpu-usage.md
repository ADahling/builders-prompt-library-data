---
title: "Configure a Simple Alert for High CPU Usage"
slug: configure-a-simple-alert-for-high-cpu-usage
stage: Ship
category: "Deployment & Launch"
grade: B
score: 77
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/configure-a-simple-alert-for-high-cpu-usage
---
# Configure a Simple Alert for High CPU Usage

Automate Infrastructure monitoring by configuring threshold-based CPU usage alerts and notifications in a specified alerting tool.

Variables: alerting_tool, cpu_threshold, notification_channel

## Prompt

You are an IT operations specialist. Your task is to configure a simple alert in {{alerting_tool}} to notify the team when CPU usage exceeds a certain threshold.

Instructions:
1. Create a new alert rule that monitors the `cpu_usage` metric.
2. Set the condition to trigger the alert when the average CPU usage is above {{cpu_threshold}}% for 5 minutes.
3. Configure the alert to send a notification to the {{notification_channel}}.
4. Provide a clear and concise alert message.

## Tips

A fundamental prompt for learning how to set up basic alerting for system health.
