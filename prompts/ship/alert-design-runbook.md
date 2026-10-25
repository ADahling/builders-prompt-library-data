---
title: "Alert Design & Runbook"
slug: alert-design-runbook
stage: Ship
category: "Monitoring & Observability"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/alert-design-runbook
---
# Alert Design & Runbook

Design alerts and runbooks for your system with thresholds, severity, diagnostic steps, fixes, escalation paths, and automation options.

## Prompt

Design actionable alerts with runbooks for this system:

System: [describe architecture]
On-call structure: [team size, rotation]
Current alert fatigue level: [high/medium/low]

For each alert:
1. Name: Clear, specific (not "Server Error" — use "Payment Service Error Rate > 5%")
2. Condition: Exact threshold with time window (e.g., error_rate > 0.05 for 5 minutes)
3. Severity: P1 (page immediately) / P2 (page during business hours) / P3 (ticket)
4. Signal vs noise: Why this threshold? What's the normal baseline?
5. Runbook:
   a. What does this alert mean?
   b. What's the immediate impact?
   c. First 3 diagnostic steps
   d. Common root causes and fixes
   e. Escalation path if not resolved in [X] minutes
   f. Related dashboards/logs to check
6. Auto-remediation: Can any response be automated?

Goal: Zero alerts that don't require human action.

## Tips

Most teams have too many alerts, not too few. Focus on actionable ones.
