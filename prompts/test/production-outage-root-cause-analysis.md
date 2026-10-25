---
title: "Production Outage Root Cause Analysis"
slug: production-outage-root-cause-analysis
stage: Test
category: "Critical Bugs"
grade: C
score: 62
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-outage-root-cause-analysis
---
# Production Outage Root Cause Analysis

Lead a rapid incident response and technical root cause analysis to restore failing Kubernetes services and implement long-term stability.

## Prompt

You are a senior SRE. A critical production service has been down for 30 minutes, impacting all users. Your task is to lead the incident response and perform a root cause analysis.

Context:
- The service is a multi-threaded Java application running on Kubernetes.
- Monitoring alerts show a sudden spike in CPU and memory usage before the crash.
- The latest deployment was 2 hours ago.

Provide:
1. An immediate action plan to restore the service.
2. A detailed post-mortem analysis to identify the root cause.
3. Long-term recommendations to prevent similar outages.

## Tips

Use this prompt to simulate a high-pressure incident response scenario.
