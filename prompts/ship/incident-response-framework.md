---
title: "Incident Response Framework"
slug: incident-response-framework
stage: Ship
category: "Deployment & Launch"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/incident-response-framework
---
# Incident Response Framework

Incident Response Framework Create a comprehensive incident response plan for my application: describe app, tech stack, data handled, user count .

Variables: brief-name, feature, time, N, Service, Impact, investigating/mitigating/resolved, name

## Prompt

# Incident Response Framework

Create a comprehensive incident response plan for my application: [describe app, tech stack, data handled, user count].

## 1. Severity Classification
| Level | Impact | Response Time | Example |
|-------|--------|--------------|---------|
| SEV-1 | Full outage, data loss | 15 min | Database down, auth bypass, data corruption |
| SEV-2 | Major feature broken | 30 min | Payments failing, auth broken, API unreachable |
| SEV-3 | Degraded performance | 2 hours | Slow responses, partial feature loss |
| SEV-4 | Minor issue | Next business day | UI glitch, non-critical bug, cosmetic |

## 2. Incident Response Lifecycle
```
Detect → Triage → Respond → Mitigate → Resolve → Review
  ↓        ↓        ↓          ↓          ↓         ↓
 Alert   Severity  Incident   Stop the   Fix root   Blameless
 fired   assigned  Commander  bleeding   cause      postmortem
```

## 3. Roles (Scale to Team Size)
| Role | Responsibility |
|------|---------------|
| Incident Commander (IC) | Coordinates response, makes decisions, owns comms |
| Technical Lead | Drives investigation, implements fix |
| Communications Lead | Updates stakeholders, status page |
| Scribe | Documents timeline and decisions in real-time |

For solo devs: you wear all hats — but follow the same structured process.

## 4. Trigger & Detection
Activate on keywords: "down", "outage", "500 errors", "can't login", "data loss".
- Monitoring alerts (error rates, latency spikes, health checks)
- User reports (support tickets, social media)
- Deployment failures or unexpected rollbacks
- Security scan findings

## 5. Immediate Actions (First 5 Minutes)
1. Create incident timeline: incidents/YYYY-MM-DD-HH-MM-{{brief-name}}.md
2. Capture current state: error rates, affected endpoints, user impact scope
3. Check recent deployments (last 24 hours) for potential causes
4. Identify affected services and their dependency chain

## 6. Investigation Framework
### Root Cause Hypotheses — Generate 3-5 ranked by likelihood:
- What changed recently? (deploys, config, dependency updates)
- What's the blast radius? (single endpoint vs entire service)
- Is this a known failure mode? (check past incidents)
- External dependency status? (third-party API outages)

### Data Collection
- Error logs (last 30 min), deployment history (last 24h)
- Infrastructure metrics (CPU, memory, connections, disk)
- Database: slow queries, connection pool, locks
- External dependency status pages

## 7. Containment Playbooks
### Data Breach
- Revoke compromised tokens/sessions, disable affected accounts
- Preserve logs before any cleanup, rotate secrets
- Assess exposure scope and notify affected users

### DDoS / Abuse
- Enable/escalate rate limiting, activate CDN protection
- Block abusive IPs or accounts, scale if needed

### Code Vulnerability
- Deploy hotfix or revert to last known good version
- Assess exposure window, patch and verify

### Compromised Credentials
- Rotate ALL affected secrets immediately
- Audit access logs for unauthorized actions
- Force password resets if user credentials exposed

## 8. Rollback Procedure
Step-by-step to revert: code (Git revert/reset), database migrations (backward-compatible only), environment variables, feature flags.

## 9. Communication Templates
### Status Page (External)
"We are aware of issues affecting {{feature}}. Our team is actively working on a resolution. Started: {{time}}. Next update in {{N}} minutes."

### Internal Updates (Every 15 min during active incident)
"[SEV-{{N}}] {{Service}} — {{Impact}}. Status: {{investigating/mitigating/resolved}}. IC: {{name}}. Next update: {{time}}."

## 10. Post-Incident
- Generate postmortem within 48 hours (use Incident Postmortem Template)
- Update runbooks with new learnings
- Track action items to completion

Include specific commands, code snippets, and runbook entries for your stack.

## Tips

Every app needs an incident response plan BEFORE an incident. Consolidates severity levels, roles, investigation framework, containment playbooks, rollback procedures, and communication templates into one comprehensive framework.
