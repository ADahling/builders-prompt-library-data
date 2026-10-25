---
title: "OpenClaw: Zero-Downtime Deployment Playbook"
slug: openclaw-zero-downtime-deployment-playbook
stage: Build
category: "OpenClaw"
grade: C
score: 66
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-zero-downtime-deployment-playbook
---
# OpenClaw: Zero-Downtime Deployment Playbook

Plan production rollouts with compatibility checks, phased database migrations, and blue-green, canary, or rolling deployment steps.

## Prompt

# Zero-Downtime Deployment Playbook

## Pre-Deployment

### Compatibility Checklist
- [ ] Database migrations are backward-compatible (expand-then-contract)
- [ ] API changes are additive (no field removals in this deploy)
- [ ] Feature flags wrap any behavior changes
- [ ] Config changes are backward-compatible
- [ ] No breaking changes to message/event schemas

### Database Migration Pattern (Expand-Contract)
**Phase 1: Expand** (deploy with old + new code)
- Add new column (nullable or with default)
- Add new table
- Create new index CONCURRENTLY

**Phase 2: Migrate** (backfill data)
- Backfill new columns from old columns
- Dual-write to old and new columns

**Phase 3: Contract** (after full rollout)
- Remove old column reads from code
- Deploy code that only uses new column
- Drop old column (separate deploy)

## Deployment Strategies

### Blue-Green
```
1. Deploy to Green (inactive)
2. Run smoke tests against Green
3. Switch LB to Green
4. Monitor for 15 minutes
5. If OK: decommission Blue
6. If NOT OK: switch back to Blue (instant rollback)
```

### Canary
```
1. Deploy canary (1-5% of traffic)
2. Compare metrics: canary vs baseline
3. Auto-promote if: error_rate_diff < 0.1%, latency_diff < 10%
4. Auto-rollback if: error_rate > 1% or latency > 2x
5. Progressive: 5% → 25% → 50% → 100%
```

### Rolling Update
```
1. Replace instances one-by-one
2. Wait for health check to pass before next
3. maxUnavailable: 25%, maxSurge: 25%
4. Rollback: reverse the rolling update
```

## Post-Deployment
- [ ] Smoke tests pass in production
- [ ] Key business metrics within normal range
- [ ] No increase in error rate or latency
- [ ] Deployment recorded in change log with commit SHA
- [ ] On-call notified of deployment

## Tips

Zero-downtime deployment playbook with expand-contract migration pattern, blue-green/canary/rolling strategies, and pre/post deployment checklists.
