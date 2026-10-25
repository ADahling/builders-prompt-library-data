---
title: "Handle a Null Reference from a Weak Reference that has been Collected"
slug: handle-a-null-reference-from-a-weak-reference-that-has-been-collected
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/handle-a-null-reference-from-a-weak-reference-that-has-been-collected
---
# Handle a Null Reference from a Weak Reference that has been Collected

Safely retrieve and null-check objects from a C# WeakReference to prevent NullReferenceExceptions during garbage collection.

## Prompt

You are a C# developer. You are using a `WeakReference` to hold a reference to an object without preventing it from being garbage collected. Your code is trying to get the target of the `WeakReference`, but the object has already been garbage collected. This results in a `null` reference, and your code is not handling it, leading to a `NullReferenceException`.

Context:
- You are using a `WeakReference` to implement a cache of large objects.
- When memory pressure is high, the garbage collector can reclaim the objects in the cache.
- Your code gets the `WeakReference` object from the cache and tries to access its `Target` property without checking if it is `null`.

Provide:
1. A C# code snippet that demonstrates the problem.
2. An explanation of what weak references are and when they are useful.
3. The corrected code that safely gets the target of the `WeakReference`. The correct pattern is to get the target into a local variable, check if that local variable is `null`, and only if it is not `null`, use it. This is important because the target could be collected in between the null check and the usage if you don’t hold a strong reference to it in a local variable.

## Tips

A good prompt for testing the understanding of garbage collection and advanced reference types.
