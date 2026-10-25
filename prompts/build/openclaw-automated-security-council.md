---
title: "OpenClaw: Automated Security Council"
slug: openclaw-automated-security-council
stage: Build
category: "OpenClaw"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-automated-security-council
---
# OpenClaw: Automated Security Council

Audit a codebase nightly from offensive, defensive, privacy, and operational perspectives to produce a security report with prioritized findings.

Variables: Date

## Prompt

# Security Council — OpenClaw Nightly Automation

## Schedule
Cron: Every night at 3:30 AM

## Process
AI reads the entire codebase from 4 security perspectives simultaneously:

### 1. Offensive Perspective (Red Team)
"How would I exploit this codebase?"
- Authentication bypass vectors
- Injection points (SQL, XSS, command injection)
- Privilege escalation paths
- Data exfiltration opportunities
- API abuse vectors (rate limiting, IDOR)

### 2. Defensive Perspective (Blue Team)
"What protections are missing?"
- Input validation gaps
- Missing authentication on endpoints
- CORS misconfiguration
- Missing rate limiting
- Logging blind spots (actions not audited)

### 3. Data Privacy Perspective
"How could user data be exposed?"
- PII in logs or error messages
- Data retention policy violations
- Third-party data sharing without consent
- Backup encryption status
- Access control on sensitive tables

### 4. Operational Realism
"What would actually happen in a breach?"
- Incident detection capability
- Backup and recovery readiness
- Secret rotation procedures
- Dependency vulnerability exposure
- Bus factor for security-critical code

## Output
```
🛡️ SECURITY COUNCIL REPORT — {{Date}}

🔴 CRITICAL (alert immediately):
- [Offensive] Unauthenticated endpoint: /api/admin/users — full user list exposed

🟡 HIGH (fix this sprint):
- [Defensive] Rate limiting missing on /api/auth/login — brute force possible
- [Privacy] User email appears in CloudWatch logs on error

🟢 MEDIUM (add to backlog):
- [Operational] No runbook for secret rotation — manual process only
- [Offensive] IDOR on /api/orders/:id — no ownership check

Reply with finding number for detailed exploit scenario and fix.
```

## Tips

Nightly automated security review from 4 perspectives. Critical findings alert immediately. From mberman84's gist.
