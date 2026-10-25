---
title: "Fix a Deadlock in a Python Application with Threading Locks"
slug: fix-a-deadlock-in-a-python-application-with-threading-locks
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-deadlock-in-a-python-application-with-threading-locks
---
# Fix a Deadlock in a Python Application with Threading Locks

Resolve Python threading deadlocks by identifying circular lock dependencies and implementing strict acquisition ordering for safe concurrency.

## Prompt

You are a Python developer. You have a multi-threaded Python application where two threads are deadlocking. Each thread is trying to acquire two locks in a different order. Your task is to identify and fix the deadlock.

Context:
- The application uses Python’s `threading.Lock` for synchronization.
- Thread 1 acquires `lock_A` and then waits to acquire `lock_B`.
- Thread 2 acquires `lock_B` and then waits to acquire `lock_A`.

Provide:
1. A simple Python script that reliably reproduces this deadlock.
2. An explanation of why this is happening and how to recognize the circular wait pattern in the code.
3. The corrected code that establishes a strict ordering for lock acquisition (e.g., always acquire `lock_A` before `lock_B`), which prevents the deadlock. You should also mention the use of `RLock` (re-entrant lock) if a thread needs to acquire the same lock multiple times.

## Tips

A fundamental concurrency issue that is important to understand for any multi-threaded programming.
