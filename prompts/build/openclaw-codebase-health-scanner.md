---
title: "OpenClaw: Codebase Health Scanner"
slug: openclaw-codebase-health-scanner
stage: Build
category: "OpenClaw"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-codebase-health-scanner
---
# OpenClaw: Codebase Health Scanner

Weekly Codebase Health Scanner — OpenClaw Workflow Prompt Schedule Run every Sunday at 9 PM via cron.

Variables: date

## Prompt

# Weekly Codebase Health Scanner — OpenClaw Workflow Prompt

## Schedule
Run every Sunday at 9 PM via cron.

## Scan Targets
All repositories listed in USER.md or configured in TOOLS.md.

## Analysis Dimensions

### 1. Dead Code Detection
- Unused exports and functions
- Unreachable code blocks
- Commented-out code older than 30 days
- Unused dependencies in package.json / requirements.txt

### 2. Dependency Health
- Outdated packages (major, minor, patch)
- Known security vulnerabilities (CVE database)
- Deprecated packages with recommended replacements
- License changes in updated versions

### 3. Security Scan
- Hardcoded strings that look like secrets
- Overly permissive file permissions
- Missing input validation on API endpoints
- SQL queries without parameterization

### 4. Test Coverage
- Overall coverage percentage and trend
- Uncovered critical paths (auth, payments, data mutations)
- Test files with no assertions
- Flaky test identification (tests that pass/fail inconsistently)

### 5. Documentation Freshness
- README last updated vs. last code change
- API docs matching current endpoints
- Inline comments referencing deleted code
- Missing JSDoc/docstrings on public functions

## Output: Technical Debt Report
```
📊 CODEBASE HEALTH — Week of {{date}}

Overall Score: 7.2/10 (↑ 0.3 from last week)

🔴 Critical (fix this week):
  - 3 high-severity CVEs in dependencies
  - Hardcoded API key found in src/utils/legacy.ts:42

🟡 Important (fix this sprint):
  - Test coverage dropped to 64% (target: 80%)
  - 12 unused exports across 4 modules
  - payment.service.ts has 0% test coverage

🟢 Maintenance (backlog):
  - 8 packages have major version updates available
  - README is 45 days behind current API
  - 3 TODO comments older than 90 days

📈 Trends: Coverage ↓2%, Deps ↑1 vuln, Dead code ↓5 files
```

## Tips

Weekly automated codebase health scan. Tracks trends over time. From Analytics Vidhya's 20 OpenClaw Prompts.
