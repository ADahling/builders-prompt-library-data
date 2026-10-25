---
title: "OpenClaw: Platform Health Council"
slug: openclaw-platform-health-council
stage: Build
category: "OpenClaw"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-platform-health-council
---
# OpenClaw: Platform Health Council

Platform Health Council — 9-Area System Review Automated review of whether the AI system is running smoothly.

Variables: Date

## Prompt

# Platform Health Council — 9-Area System Review

Automated review of whether the AI system is running smoothly. AI reads actual codebase and analyzes 9 areas:

## Areas of Review

### 1. Cron Job Health
Are automated jobs succeeding? Check logs for failures, missed executions, and timing drift.

### 2. Code Quality
Is technical debt accumulating? Scan for code smells, TODO comments, deprecated patterns.

### 3. Test Coverage
Are there gaps? Identify untested critical paths and functions without assertions.

### 4. Prompt Quality
Are AI prompts well-written? Check for ALL-CAPS urgency markers, anti-patterns, vague instructions.

### 5. Dependencies
Outdated or vulnerable packages? Check package.json/requirements.txt against latest versions and CVE databases.

### 6. Storage
Are databases growing too large? Monitor SQLite file sizes, row counts, and growth trends.

### 7. Skill Integrity
Are all skills working correctly? Validate SKILL.md files, test scripts, check for broken dependencies.

### 8. Config Consistency
Do all config files agree with each other? Cross-check environment variables, gateway config, and skill configs.

### 9. Data Integrity
Is the contact database healthy? Check for orphaned records, duplicate entries, stale data.

## Output
Deliver findings as numbered recommendations to Telegram:
```
🏥 PLATFORM HEALTH — {{Date}}

1. [Cron] Job "daily-briefing" has failed 3 times this week. Error: timeout
2. [Deps] 4 packages have known vulnerabilities (2 high, 2 medium)
3. [Storage] CRM database grown 40% in 2 weeks — review data retention
...

Reply with number for details and suggested fix.
```

## Tips

Automated 9-area system health review: cron jobs, code quality, tests, prompts, dependencies, storage, skills, config, and data integrity. From mberman84's gist.
