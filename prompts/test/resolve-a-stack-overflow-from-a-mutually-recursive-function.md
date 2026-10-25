---
title: "Resolve a Stack Overflow from a Mutually Recursive Function"
slug: resolve-a-stack-overflow-from-a-mutually-recursive-function
stage: Test
category: "Critical Bugs"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-stack-overflow-from-a-mutually-recursive-function
---
# Resolve a Stack Overflow from a Mutually Recursive Function

Refactor mutually recursive functions into tail-recursive structures to prevent stack overflow errors during large-scale computations.

## Prompt

You are a functional programmer. You have two functions, `is_even` and `is_odd`, that are defined in terms of each other (mutual recursion). For large numbers, calling these functions results in a stack overflow error. Your task is to rewrite them to be tail-recursive to avoid this issue.

Context:
- The functions are written in a language that supports tail-call optimization (TCO), like F# or Scala.
- `is_even(n)` calls `is_odd(n-1)`, and `is_odd(n)` calls `is_even(n-1)`. The base cases are for `n=0`.
- Without TCO, each call consumes a new stack frame.

Provide:
1. The original, non-tail-recursive F# or Scala code for `is_even` and `is_odd` that causes a stack overflow.
2. An explanation of tail recursion and tail-call optimization.
3. The rewritten, tail-recursive versions of the functions that can handle large inputs without overflowing the stack. This usually involves an accumulator-passing style.

## Tips

Tests a key concept in functional programming for writing scalable recursive algorithms.
