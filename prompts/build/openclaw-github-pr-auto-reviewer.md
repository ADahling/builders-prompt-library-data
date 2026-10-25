---
title: "OpenClaw: GitHub PR Auto-Reviewer"
slug: openclaw-github-pr-auto-reviewer
stage: Build
category: "OpenClaw"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-github-pr-auto-reviewer
---
# OpenClaw: GitHub PR Auto-Reviewer

GitHub PR Auto-Reviewer — OpenClaw Workflow Prompt Trigger Activate when a new PR link is shared or when asked to review a PR.

## Prompt

# GitHub PR Auto-Reviewer — OpenClaw Workflow Prompt

## Trigger
Activate when a new PR link is shared or when asked to review a PR.

## Analysis Framework
For each PR diff, analyze from these 4 perspectives:

### 1. Security Scan
- SQL injection vectors
- Hardcoded secrets or API keys
- Authentication bypass possibilities
- XSS vulnerabilities
- CSRF missing protections
- Insecure direct object references

### 2. Architecture Review
- Module coupling — does this change increase dependencies?
- SOLID principle violations
- Data migration risks — will this break existing data?
- Missing backward compatibility
- Scalability concerns for the changed components

### 3. Code Quality
- Naming clarity — can a new team member understand this?
- DRY violations — is logic duplicated elsewhere?
- Over-complex logic — can this be simplified?
- Edge cases — what inputs would break this?
- Error messages — are they helpful for debugging?

### 4. Testing Gaps
- Are existing tests updated to cover the changes?
- Missing negative test cases (what should NOT happen)
- Missing boundary condition tests
- Missing integration tests for new endpoints
- Test data — are test fixtures representative?

## Output
Generate 3-5 ready-to-paste GitHub review comments, each formatted as:
```
📍 **[file:line]** — [Severity: Critical/High/Medium/Low]
**Issue:** [Clear description]
**Risk:** [What could go wrong]
**Suggestion:**
```[code fix]```
```

Prioritize comments by severity. Always include at least one positive observation.

## Tips

Triggers on new PR links. Generates ready-to-paste review comments with severity ratings. From Analytics Vidhya's 20 OpenClaw Prompts (March 2026).
