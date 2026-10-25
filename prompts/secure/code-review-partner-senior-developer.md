---
title: "Code Review Partner (Senior Developer)"
slug: code-review-partner-senior-developer
stage: Secure
category: "Security Review"
grade: B
score: 73
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/code-review-partner-senior-developer
---
# Code Review Partner (Senior Developer)

Get a senior-level review of code or a diff for bugs, security, performance, maintainability, and edge cases, with severity, locations, and fixes.

## Prompt

Review this code as a senior developer:

[Paste your code or diff]

Check for:
1. Bugs: Logic errors, off-by-one, null handling, race conditions
2. Security: Injection risks, auth issues, data exposure
3. Performance: N+1 queries, unnecessary loops, memory leaks
4. Maintainability: Naming, complexity, duplication
5. Edge cases: What inputs would break this?

For each issue:
- Severity: Critical / High / Medium / Low
- Line number or section
- What's wrong
- How to fix it

Be harsh. I'd rather fix issues now than in production.

## Tips

The 'Be harsh' instruction is key — without it, AI reviews are too gentle. Source: medium.com/data-science-collective
