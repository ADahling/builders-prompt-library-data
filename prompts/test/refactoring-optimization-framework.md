---
title: "Refactoring & Optimization Framework"
slug: refactoring-optimization-framework
stage: Test
category: "Performance & Code"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactoring-optimization-framework
---
# Refactoring & Optimization Framework

Get refactored function code with explanations, trade-offs, and edge cases tailored to your readability or performance issues and constraints.

## Prompt

I have a [language] function in a [framework] project that needs refactoring.

Current code:
[paste code]

Issues I'd like to address:
[specific issue, e.g., low readability, high cyclomatic complexity]
[specific issue, e.g., non-optimal O(n^2) time complexity]

What I've considered:
[any approaches you've thought about, e.g., using a Map instead of an array filter]

Constraints:
[e.g., must remain backward compatible, no new dependencies, must be a pure function]

Please suggest refactored code with explanations for your changes, including trade-offs and any potential edge cases I should be aware of.

## Tips

This turns the AI into a dedicated refactoring assistant that understands your constraints. Source: medium.com/@onix_react/ultimate-prompts-for-every-developer
