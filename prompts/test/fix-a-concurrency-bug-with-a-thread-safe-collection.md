---
title: "Fix a Concurrency Bug with a Thread-Safe Collection"
slug: fix-a-concurrency-bug-with-a-thread-safe-collection
stage: Test
category: "Critical Bugs"
grade: B
score: 74
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-concurrency-bug-with-a-thread-safe-collection
---
# Fix a Concurrency Bug with a Thread-Safe Collection

Resolve intermittent runtime exceptions in multi-threaded C# apps by replacing non-thread-safe lists with appropriate concurrent collections.

## Prompt

You are a C# developer. You have a multi-threaded application where multiple threads are adding and removing items from a shared `List<T>`. The application is throwing random, intermittent exceptions like `IndexOutOfRangeException` or an exception about the collection being modified during enumeration. Your task is to fix this concurrency bug.

Context:
- The `List<T>` class in C# is not thread-safe. Concurrent modifications can corrupt its internal state.
- You need a collection that is designed to be used by multiple threads at the same time.

Provide:
1. A C# code example that shows how multiple threads trying to modify a `List<T>` can cause problems.
2. The corrected code that replaces the `List<T>` with one of C#’s thread-safe collections, such as `ConcurrentBag<T>` or `ConcurrentQueue<T>`.
3. A discussion of which thread-safe collection to choose based on the needs of the application (e.g., `ConcurrentQueue` for a producer-consumer scenario, `ConcurrentDictionary` for a shared cache).

## Tips

A good introduction to the concept of thread-safe collections.
