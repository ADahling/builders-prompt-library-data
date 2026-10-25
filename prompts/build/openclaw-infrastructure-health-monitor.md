---
title: "OpenClaw: Infrastructure Health Monitor"
slug: openclaw-infrastructure-health-monitor
stage: Build
category: "OpenClaw"
grade: A
score: 88
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-infrastructure-health-monitor
---
# OpenClaw: Infrastructure Health Monitor

Infrastructure Health Monitor — OpenClaw Workflow Prompt Schedule Every 30 minutes during work hours.

Variables: timestamp, 🟢 Healthy / 🟡 Warning / 🔴 Critical, %, count, ms, date, amount, If issues:

## Prompt

# Infrastructure Health Monitor — OpenClaw Workflow Prompt

## Schedule
Every 30 minutes during work hours. Every 2 hours overnight. Immediate on threshold breach.

## Monitoring Dimensions

### Compute
- CPU utilization per service (alert >80% sustained 5min)
- Memory usage per service (alert >85%)
- Container restarts (alert >3 in 1 hour)
- Pod scheduling failures

### Database
- Connection pool utilization (alert >75%)
- Slow query count (>1s, rolling 15min window)
- Replication lag (alert >5s)
- Disk usage (alert >80%)
- Active locks (alert >10 concurrent)

### Network
- Request latency P50/P95/P99
- Error rate (4xx, 5xx) by endpoint
- Bandwidth utilization
- DNS resolution time
- SSL certificate expiry (alert <14 days)

### Costs
- Daily spend vs. budget
- Per-service cost breakdown
- Anomaly detection (>20% spike from 7-day average)
- Unused resource identification (idle instances, unattached volumes)

## Health Report Format
```
🏥 INFRA HEALTH — {{timestamp}}

Overall: {{🟢 Healthy / 🟡 Warning / 🔴 Critical}}

Compute:  CPU {{%}} | Memory {{%}} | Restarts {{count}}
Database: Connections {{%}} | Slow queries {{count}} | Disk {{%}}
Network:  P95 {{ms}} | Error rate {{%}} | Certs expire {{date}}
Costs:    Today ${{amount}} / Budget ${{amount}} ({{%}})

{{If issues:}}
⚠️ ATTENTION:
- Database connection pool at 78% — approaching limit
- 3 slow queries detected on users table
- SSL cert expires in 12 days — renew now
```

## Tips

Comprehensive infrastructure monitoring with compute, database, network, and cost tracking. From Rezvani's developer automation prompts.
