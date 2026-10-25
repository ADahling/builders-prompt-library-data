---
title: "Handle a Null Pointer Exception in a Chain of Method Calls"
slug: handle-a-null-pointer-exception-in-a-chain-of-method-calls
stage: Test
category: "Critical Bugs"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/handle-a-null-pointer-exception-in-a-chain-of-method-calls
---
# Handle a Null Pointer Exception in a Chain of Method Calls

Refactor fragile Java method chains into null-safe code using explicit checks and Optional to prevent NullPointerExceptions.

## Prompt

You are a Java developer. You have a line of code that chains several method calls together, like `user.getProfile().getAddress().getStreet()`. The code is throwing a `NullPointerException` because one of the intermediate objects (`getProfile()` or `getAddress()`) can return `null`. Your task is to make this code safe.

Context:
- The objects are retrieved from a database and some fields are optional.
- The current code is fragile and will crash if any part of the chain is `null`.
- You want to avoid a deeply nested series of `if (x != null)` checks.

Provide:
1. The single line of Java code that is causing the `NullPointerException`.
2. A verbose but safe way to rewrite the code using explicit `if` checks to ensure no method is called on a `null` reference.
3. A more elegant and modern solution using Java's `Optional` class to wrap the potentially null values and chain the calls safely using `flatMap`.

## Tips

A great prompt to compare the traditional way of handling nulls with the modern `Optional` approach in Java.
