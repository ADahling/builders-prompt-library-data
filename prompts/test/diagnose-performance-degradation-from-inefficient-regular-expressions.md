---
title: "Diagnose Performance Degradation from Inefficient Regular Expressions"
slug: diagnose-performance-degradation-from-inefficient-regular-expressions
stage: Test
category: "Critical Bugs"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/diagnose-performance-degradation-from-inefficient-regular-expressions
---
# Diagnose Performance Degradation from Inefficient Regular Expressions

Identify and resolve catastrophic backtracking in regular expressions to eliminate CPU spikes and optimize service response times.

## Prompt

You are a developer. A service you wrote is experiencing high CPU usage and slow response times. After profiling, you have traced the problem to a regular expression that is being used to validate user input. The regex is suffering from ‘catastrophic backtracking’.

Context:
- The service is written in a language like JavaScript, Python, or Ruby, whose regex engines are susceptible to this problem.
- The regex is something like `(a+)+$`, and it is being run against a string like `aaaaaaaaaaaaaaaaaaaaaaaa!`.
- The regex engine’s backtracking algorithm has an exponential time complexity for this combination of regex and input string.

Provide:
1. An explanation of what catastrophic backtracking is and why it happens in certain regex patterns (nested quantifiers with overlapping patterns).
2. A demonstration of the problem, showing how a seemingly simple regex can take seconds or even minutes to execute on a short string.
3. A revised version of the regex that avoids the problem. This often involves making the quantifiers possessive or atomic (e.g., `(a++)+` in Java) or rewriting the pattern to be more specific and avoid the nested quantifiers (e.g., `a+$`).

## Tips

A subtle and often surprising performance bug that can be very difficult to diagnose.
