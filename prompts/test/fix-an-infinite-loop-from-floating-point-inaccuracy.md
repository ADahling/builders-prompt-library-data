---
title: "Fix an Infinite Loop from Floating Point Inaccuracy"
slug: fix-an-infinite-loop-from-floating-point-inaccuracy
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-an-infinite-loop-from-floating-point-inaccuracy
---
# Fix an Infinite Loop from Floating Point Inaccuracy

Correct infinite loops caused by floating-point imprecision using epsilon-based comparisons in C++ code.

## Prompt

You are a game developer. You have written a loop that is supposed to terminate when a floating-point variable reaches a specific value. However, the loop is running forever. You realize this is due to the imprecision of floating-point arithmetic.

Context:
- The code is in C++ and uses a `for` loop that increments a `float` variable by `0.1` in each iteration.
- The loop condition is `f != 1.0`.
- Due to how floating-point numbers are represented in binary, the variable may never be exactly `1.0`. It might be `0.9999999` or `1.0000001`.

Provide:
1. The C++ code snippet that demonstrates the infinite loop.
2. An explanation of why comparing floating-point numbers for exact equality is dangerous.
3. The corrected loop condition that checks if the variable is within a small tolerance (epsilon) of the target value (e.g., `abs(f - 1.0) < 0.0001`).

## Tips

A classic pitfall in programming that deals with floating-point numbers.
