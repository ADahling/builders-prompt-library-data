---
title: "Network I/O Trend Analysis"
slug: network-i-o-trend-analysis
stage: Ship
category: "Monitoring & Observability"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/network-i-o-trend-analysis
---
# Network I/O Trend Analysis

Get a 30-day network traffic report for your app with daily inbound and outbound averages, peak days, anomalies, and mitigation actions.

Variables: project_name, environment, monitoring_tool, average_network_io, peak_days, anomalies, mitigation_actions

## Prompt

Perform a trend analysis of network I/O for the {{project_name}} application hosted in {{environment}}. Collect data on inbound and outbound traffic over the past 30 days using {{monitoring_tool}}. The goal is to identify patterns and any anomalies in network traffic that could impact application performance. Present the findings in a report that includes:

- Daily average network I/O (inbound/outbound): {{average_network_io}}
- Peak network I/O days: {{peak_days}}
- Identified anomalies: {{anomalies}}
- Suggested actions to mitigate anomalies: {{mitigation_actions}}

Your analysis should help the team understand traffic trends and prepare for potential network capacity issues. Provide actionable insights based on the data collected.

## Tips

Useful for intermediate users performing network traffic analysis.
