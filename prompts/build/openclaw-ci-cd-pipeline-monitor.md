---
title: "OpenClaw: CI/CD Pipeline Monitor"
slug: openclaw-ci-cd-pipeline-monitor
stage: Build
category: "OpenClaw"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-ci-cd-pipeline-monitor
---
# OpenClaw: CI/CD Pipeline Monitor

CI/CD Pipeline Monitor — OpenClaw Workflow Prompt Schedule Check every 15 minutes during work hours.

Variables: timestamp, name, branch, ✅ Passed / 🔴 Failed / ⚠️ Flaky, time, +/-% vs baseline, passed, total, %, If failed: Error summary and failing test names

## Prompt

# CI/CD Pipeline Monitor — OpenClaw Workflow Prompt

## Schedule
Check every 15 minutes during work hours. Immediate alerts for failures.

## Monitoring Targets
- GitHub Actions / GitLab CI / Jenkins pipelines
- Build status for all active branches
- Test suite results and timing
- Deployment status across environments

## What to Track

### Build Health
- Build success rate (rolling 24h): target >95%
- Average build time: flag if >20% increase from baseline
- Flaky builds: same commit, different results
- Queue depth: builds waiting >10 minutes

### Test Results
- New test failures (not in previous run)
- Tests that became flaky (passed last 5, failed this time)
- Coverage changes (+/- from merge base)
- Slow tests: any test >30s gets flagged

### Deployment Pipeline
- Staging deployment status
- Production deployment queue
- Rollback events in last 24 hours
- Feature flag changes

## Alert Levels

### 🟢 Include in Daily Briefing
- Build time trending up (>10% over 7 days)
- Coverage trending down
- New flaky test detected

### 🟡 Send Notification
- Build failure on main/master branch
- Coverage dropped below threshold
- Deployment to staging failed
- Build queue backed up >30 minutes

### 🔴 Immediate Alert
- Production deployment failed
- All CI pipelines failing
- Security scan found critical vulnerability
- Production rollback triggered

## Output Format
```
🔧 CI/CD STATUS — {{timestamp}}
Pipeline: {{name}} | Branch: {{branch}}
Status: {{✅ Passed / 🔴 Failed / ⚠️ Flaky}}
Duration: {{time}} ({{+/-% vs baseline}})
Tests: {{passed}}/{{total}} | Coverage: {{%}}
{{If failed: Error summary and failing test names}}
```

## Tips

Monitors CI/CD pipelines with intelligent alert levels. Tracks flaky tests, build times, and coverage trends. From Rezvani's 25 automation prompts.
