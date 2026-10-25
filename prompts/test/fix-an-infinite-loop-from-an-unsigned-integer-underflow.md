---
title: "Fix an Infinite Loop from an Unsigned Integer Underflow"
slug: fix-an-infinite-loop-from-an-unsigned-integer-underflow
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-an-infinite-loop-from-an-unsigned-integer-underflow
---
# Fix an Infinite Loop from an Unsigned Integer Underflow

Resolve infinite countdown loops in C caused by unsigned integer underflow by implementing proper termination conditions or signed types.

## Prompt

You are a C programmer. You have written a `for` loop that counts down from a given number to zero. You have used an `unsigned int` for the loop counter. The loop is supposed to terminate when the counter is less than zero, but because the counter is unsigned, it can never be less than zero. When it is decremented from 0, it wraps around to the maximum possible unsigned integer value, and the loop runs forever.

Context:
- The loop is `for (unsigned int i = 10; i >= 0; i--)`.
- The condition `i >= 0` is always true for an unsigned integer.
- This is a common bug when mixing signed and unsigned integers or when using unsigned integers in countdown loops.

Provide:
1. The C code snippet that demonstrates the infinite loop.
2. An explanation of unsigned integer underflow and why the loop condition is always true.
3. Two ways to fix the loop. One way is to change the loop counter to a signed `int`. Another way is to change the loop condition to `i > 0` and handle the 0 case separately, or to change the loop to a `while` loop that checks for 0 before decrementing.

## Tips

A classic C programming pitfall that highlights the importance of understanding integer types.
