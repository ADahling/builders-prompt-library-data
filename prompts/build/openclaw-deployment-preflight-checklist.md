---
title: "OpenClaw: Deployment Preflight Checklist"
slug: openclaw-deployment-preflight-checklist
stage: Build
category: "OpenClaw"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-deployment-preflight-checklist
---
# OpenClaw: Deployment Preflight Checklist

Deployment Preflight Checklist — OpenClaw Workflow Prompt Trigger Activate whenever deployment, release, push to production, or "ship it" is mentioned.

Variables: service-name, date

## Prompt

# Deployment Preflight Checklist — OpenClaw Workflow Prompt

## Trigger
Activate whenever deployment, release, push to production, or "ship it" is mentioned.

## Automated Checks

### 1. Environment Variables
- Compare .env.example against production config
- Flag any missing or mismatched variables
- Check for development-only values in production config
- Verify secret rotation dates (flag if >90 days old)

### 2. Database Migrations
- Are all pending migrations ready to run?
- Do migrations have rollback scripts?
- Will migrations lock tables? (Flag for high-traffic tables)
- Data backfill requirements estimated?

### 3. Dependencies
- Any new dependencies added since last deploy?
- Security audit results (npm audit / pip audit)
- Version pinning — are all deps pinned to exact versions?
- License compatibility check

### 4. API Changes
- Any breaking API changes? (Endpoint removals, schema changes)
- API versioning updated?
- Documentation updated for changed endpoints?
- Client SDKs need updating?

### 5. Rollback Plan
- Can this deployment be rolled back with one command?
- Is the rollback tested?
- Database migration rollback scripts available?
- Feature flags in place for gradual rollout?

### 6. Monitoring Readiness
- Error tracking configured for new code paths?
- Alerting rules updated?
- Dashboard widgets for new features?
- Log levels appropriate for production?

## Output: Go / No-Go Report
```
🚀 DEPLOYMENT PREFLIGHT — {{service-name}} — {{date}}

✅ Environment: All variables matched
⚠️ Migrations: 2 pending, 1 locks users table (~30s downtime)
✅ Dependencies: No new vulns, all pinned
🔴 API: Breaking change in /api/v2/users — clients not updated
✅ Rollback: One-command rollback tested
⚠️ Monitoring: Missing alert rule for new payment flow

VERDICT: 🔴 NO-GO — Fix API breaking change first
```

## Tips

Triggers on deployment-related keywords. Generates a structured go/no-go report. From Analytics Vidhya's 20 OpenClaw Prompts.
