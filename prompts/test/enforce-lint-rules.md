---
title: "Enforce Lint Rules"
slug: enforce-lint-rules
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 77
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/enforce-lint-rules
---
# Enforce Lint Rules

Review a code snippet against your specified lint rules and get a report of any violations with suggested fixes for each.

Variables: code_snippet, lint_rules

## Prompt

Given the following code snippet: {{code_snippet}}, run lint checks to enforce the following rules: {{lint_rules}}. Compile a report detailing any violations found and suggest fixes for each.

## Tips

This prompt helps maintain code quality by ensuring that specific linting rules are followed.
