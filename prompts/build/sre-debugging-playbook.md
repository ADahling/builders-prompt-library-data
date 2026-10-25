---
title: "SRE Debugging Playbook"
slug: sre-debugging-playbook
stage: Build
category: "DevOps & IaC"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/sre-debugging-playbook
---
# SRE Debugging Playbook

Systematically resolve system outages and performance degradations using a structured senior SRE methodology for triage and mitigation.

## Prompt

Act as a senior Site Reliability Engineer. I have an incident:

[Describe the symptoms: what's broken, when it started, what changed recently, any error messages]

Follow this debugging playbook:

1. TRIAGE (2 minutes):
   - Severity: S1 (total outage), S2 (major degradation), S3 (minor impact), S4 (cosmetic)
   - Blast radius: How many users are affected?
   - Is it getting worse?

2. QUICK CHECKS (5 minutes):
   - Recent deployments or config changes?
   - Infrastructure status (database, DNS, CDN, external APIs)
   - Error rate trends (spike vs gradual)
   - Resource utilization (CPU, memory, disk, connections)

3. ROOT CAUSE INVESTIGATION:
   - Correlate timeline: what changed when it broke?
   - Check logs: application, database, infrastructure
   - Network: DNS resolution, TLS, connectivity
   - Database: slow queries, connection pool exhaustion, lock contention

4. MITIGATION:
   - Can we rollback the last deployment?
   - Can we scale up to handle load?
   - Can we failover to a secondary?
   - Can we put up a maintenance page while we fix?

5. POST-MORTEM TEMPLATE:
   - Timeline of events
   - Root cause
   - Impact (duration, users affected, data loss)
   - Resolution
   - Action items to prevent recurrence

Walk me through this for my specific incident.

## Tips

Adapted from r/devops community and SRE best practices. Source: reddit.com/r/devops/comments/1qcu9ja
