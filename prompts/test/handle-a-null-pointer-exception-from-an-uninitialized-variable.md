---
title: "Handle a Null Pointer Exception from an Uninitialized Variable"
slug: handle-a-null-pointer-exception-from-an-uninitialized-variable
stage: Test
category: "Critical Bugs"
grade: C
score: 68
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/handle-a-null-pointer-exception-from-an-uninitialized-variable
---
# Handle a Null Pointer Exception from an Uninitialized Variable

Identify and resolve Java NullPointerExceptions by properly initializing class fields within constructors to ensure stable object references.

## Prompt

You are a Java beginner. Your program is crashing with a `NullPointerException`. You have a field in your class that is an object, but you have forgotten to initialize it before using it. Your task is to find and fix this bug.

Context:
- You have a class `Car` that has a field `Engine engine`.
- In the `Car`’s constructor, you do not create an instance of the `Engine` class for the `engine` field.
- Later, in a method of the `Car` class, you try to call a method on the `engine` field, which is `null`.

Provide:
1. The Java code for the `Car` class that shows the uninitialized `engine` field.
2. An explanation of why instance fields in Java are initialized to `null` by default if they are objects, and why this leads to a `NullPointerException` if you don’t explicitly initialize them.
3. The corrected `Car` constructor that properly initializes the `engine` field by creating a new `Engine` object (e.g., `this.engine = new Engine();`).

## Tips

A fundamental initialization error that many Java beginners encounter.
