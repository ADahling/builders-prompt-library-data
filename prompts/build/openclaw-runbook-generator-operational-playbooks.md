---
title: "OpenClaw: Runbook Generator \u2014 Operational Playbooks"
slug: openclaw-runbook-generator-operational-playbooks
stage: Build
category: "OpenClaw"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-runbook-generator-operational-playbooks
---
# OpenClaw: Runbook Generator — Operational Playbooks

Get an incident runbook for a service alert, with quick assessment steps, diagnostic commands, and remediation options by risk and downtime.

Variables: service, scenario, env, team, escalation_path, db

## Prompt

# Runbook Generator — Operational Playbooks

## Input
- Service name: {{service}}
- Alert/scenario: {{scenario}} (e.g., "high CPU", "database connection pool exhausted", "deployment failed")
- Environment: {{env}} (production / staging / development)

## Runbook Template

### 🔔 Alert: {{scenario}}
**Severity:** SEV-1 / SEV-2 / SEV-3
**On-call team:** {{team}}
**Escalation:** {{escalation_path}}

### 📋 Quick Assessment (< 2 min)
1. Check dashboard: [link to monitoring dashboard]
2. Verify: Is this affecting users? (check error rates, latency)
3. Check: Is this a known issue? (search recent incidents)
4. Determine: Is immediate action needed?

### 🔍 Diagnosis Steps
Step-by-step commands with expected output:
```bash
# Check service health
curl -s https://{{service}}/health | jq .

# Check recent logs
kubectl logs -l app={{service}} --tail=100 --since=5m

# Check resource usage
kubectl top pods -l app={{service}}

# Check database connections
SELECT count(*) FROM pg_stat_activity WHERE datname = '{{db}}';
```

### 🛠️ Remediation Options
| Option | Risk | Downtime | When to Use |
|--------|------|----------|-------------|
| Restart service | Low | ~30s | Transient issues |
| Scale up | Low | None | Load-related |
| Rollback deploy | Medium | ~2 min | Post-deploy regression |
| Failover to secondary | Medium | ~1 min | Primary failure |
| Manual DB intervention | High | Varies | Data corruption |

### ✅ Verification
- [ ] Error rate returned to baseline
- [ ] Latency within SLO
- [ ] No user-facing impact
- [ ] Monitoring alerts cleared

### 📝 Post-Incident
- [ ] Update incident channel with resolution
- [ ] Create follow-up ticket if needed
- [ ] Schedule postmortem if SEV-1/SEV-2

## Tips

Generates operational runbooks from alert scenarios. Includes quick assessment, diagnosis commands, remediation options, and verification steps.
