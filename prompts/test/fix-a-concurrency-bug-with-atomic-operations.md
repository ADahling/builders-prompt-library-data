---
title: "Fix a Concurrency Bug with Atomic Operations"
slug: fix-a-concurrency-bug-with-atomic-operations
stage: Test
category: "Critical Bugs"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-concurrency-bug-with-atomic-operations
---
# Fix a Concurrency Bug with Atomic Operations

Resolve race conditions in multi-threaded C++ applications by replacing non-atomic increments with thread-safe std::atomic operations.

## Prompt

You are a C++ developer. You have a multi-threaded application where multiple threads need to increment a shared counter. You are using a simple `int` for the counter and incrementing it with `counter++`. You have discovered that the final value of the counter is incorrect because this operation is not atomic.

Context:
- The `counter++` operation is actually three separate steps: read the value from memory, increment the value in a register, and write the value back to memory.
- Two threads can read the same value, both increment it, and then one will overwrite the other’s result.
- This is a classic race condition.

Provide:
1. A C++ code snippet that demonstrates this race condition with multiple threads.
2. An explanation of why `++` is not an atomic operation.
3. The corrected code that uses C++’s `std::atomic<int>` for the counter. The `fetch_add()` method of `std::atomic` provides a thread-safe, atomic increment operation, ensuring that the final count is correct.

## Tips

A fundamental concept in low-level concurrent programming.
