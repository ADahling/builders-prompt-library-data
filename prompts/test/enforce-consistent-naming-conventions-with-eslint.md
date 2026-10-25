---
title: "Enforce Consistent Naming Conventions with ESLint"
slug: enforce-consistent-naming-conventions-with-eslint
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/enforce-consistent-naming-conventions-with-eslint
---
# Enforce Consistent Naming Conventions with ESLint

Get an ESLint naming configuration for variables, functions, classes, and constants, with pass/fail examples and React exceptions.

## Prompt

My team has inconsistent naming conventions for variables, functions, and classes. I want to use ESLint to enforce a consistent style. 

Our desired conventions are:
- Variables and functions: `camelCase`
- Classes: `PascalCase`
- Constants: `UPPER_CASE`

Your task is to show me how to configure ESLint to enforce these conventions. Please provide:

1.  **ESLint Rule:** The name of the ESLint rule that governs naming conventions (`@typescript-eslint/naming-convention`).
2.  **Configuration:** A complete ESLint configuration in `.eslintrc.json` that implements our desired conventions. The configuration should be well-commented to explain what each part does.
3.  **Examples:** For each convention, provide an example of code that would pass and code that would fail the lint check.
4.  **Customization:** How to customize the rule for more specific cases, for example, to allow `PascalCase` for functions that are React components.

Output should be a clear and concise guide with the necessary configuration.

## Tips

Consistent naming is a simple but powerful way to improve code readability.
