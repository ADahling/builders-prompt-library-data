---
title: "Review a pull request for risk, not style"
slug: review-a-pull-request-for-risk-not-style
stage: Test
category: "Code Review"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/review-a-pull-request-for-risk-not-style
---
# Review a pull request for risk, not style

Focus review on correctness, blast radius, and rollback rather than formatting a linter already handles.

Variables: diff_content, service_context

## Prompt

You are a senior engineer reviewing a pull request where review time is scarce.

Context:
- The diff: {{diff_content}}
- What the service does and who depends on it: {{service_context}}

Your task is to produce a review that concentrates entirely on what could break, not on what a tool can fix.

Steps:
1. Summarise what the change does in two sentences, based only on the diff.
2. Identify the risk surface: data writes, external calls, auth checks, concurrency, and error paths.
3. For each risky area, state the failure mode and whether the diff handles it. Cite the file and line.
4. Check the tests: do they exercise the failure modes you listed, or only the happy path? Name the missing cases.
5. Check reversibility: can this be rolled back cleanly, and does it contain a migration or a format change that prevents that?
6. Rank comments as blocking, should-fix, or optional, and state the single change that would most reduce risk.

Constraints:
- Do not comment on formatting, naming, or import order.
- Every blocking comment must name the failure it prevents.
- If the diff is too large to review safely, say so and propose a split.

Output format, in Markdown: **Summary**, then a comments table with columns severity, file:line, issue, suggested change, ordered by severity, then **Missing tests** and **Rollback assessment**.

## Tips

If a linter or formatter can catch it, do not spend review attention on it. Spend it on what breaks in production.
