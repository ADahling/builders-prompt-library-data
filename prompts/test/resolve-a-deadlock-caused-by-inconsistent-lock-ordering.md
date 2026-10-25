---
title: "Resolve a Deadlock Caused by Inconsistent Lock Ordering"
slug: resolve-a-deadlock-caused-by-inconsistent-lock-ordering
stage: Test
category: "Critical Bugs"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-deadlock-caused-by-inconsistent-lock-ordering
---
# Resolve a Deadlock Caused by Inconsistent Lock Ordering

Debug and prevent multithreaded deadlocks by enforcing consistent lock ordering to eliminate circular wait conditions in resource access.

## Prompt

You are a systems developer. You are writing a multi-threaded program where threads need to lock two different mutexes to perform an operation. The program is deadlocking because threads are acquiring the mutexes in different orders. Your task is to fix the deadlock.

Context:
- There are two mutexes, `mutexA` and `mutexB`.
- Thread 1 locks `mutexA` then tries to lock `mutexB`.
- Thread 2 locks `mutexB` then tries to lock `mutexA`.
- This creates a classic circular wait condition.

Provide:
1. A simple C++ or Java code example that demonstrates this deadlock scenario.
2. A clear explanation of why the inconsistent lock ordering leads to a deadlock.
3. The corrected code that enforces a strict global order for acquiring the locks (e.g., always lock `mutexA` before `mutexB`), thus preventing the circular wait and the deadlock.

## Tips

A textbook example of a deadlock, perfect for testing fundamental concurrency concepts.
