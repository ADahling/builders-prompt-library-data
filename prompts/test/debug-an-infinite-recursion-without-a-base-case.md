---
title: "Debug an Infinite Recursion without a Base Case"
slug: debug-an-infinite-recursion-without-a-base-case
stage: Test
category: "Critical Bugs"
grade: B
score: 72
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-an-infinite-recursion-without-a-base-case
---
# Debug an Infinite Recursion without a Base Case

Identify and fix infinite recursion in a JavaScript factorial function by implementing a terminating base case to prevent stack overflows.

## Prompt

You are a student learning about recursion. You have written a function to compute the factorial of a number, but it's causing a stack overflow for any positive input. Your task is to debug the function and make it work correctly.

Context:
- The function is written in JavaScript.
- The function calls itself with `n-1` but never stops.
- The factorial of 0 is 1, which should be the base case.

Provide:
1. The flawed recursive function that is causing the stack overflow.
2. An explanation of why a base case is essential for any recursive function.
3. The corrected version of the factorial function with the proper base case to terminate the recursion.

## Tips

A classic introductory problem to teach the concept of a base case in recursion.
