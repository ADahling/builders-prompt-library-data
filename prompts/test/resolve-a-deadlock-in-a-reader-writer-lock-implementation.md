---
title: "Resolve a Deadlock in a Reader-Writer Lock Implementation"
slug: resolve-a-deadlock-in-a-reader-writer-lock-implementation
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-deadlock-in-a-reader-writer-lock-implementation
---
# Resolve a Deadlock in a Reader-Writer Lock Implementation

Debug and optimize reader-writer lock logic to prevent deadlocks, eliminate writer starvation, and implement fair resource scheduling.

## Prompt

You are implementing a reader-writer lock from scratch. Your lock allows multiple readers to access a resource concurrently, but only one writer at a time. You have discovered that your implementation can lead to a deadlock or starvation. For example, a writer may be starved if readers are constantly arriving, or a deadlock can occur if a thread tries to upgrade a read lock to a write lock.

Context:
- The lock has methods like `acquireRead()`, `releaseRead()`, `acquireWrite()`, and `releaseWrite()`.
- A common problem is that a thread holding a read lock tries to acquire a write lock. If another thread is also holding a read lock, the first thread will block waiting for the second thread to release its read lock. But the second thread might also be trying to upgrade to a write lock, leading to a deadlock.

Provide:
1. A description of the state (e.g., number of readers, writer present) that your reader-writer lock needs to manage.
2. A flawed implementation of the `acquireWrite()` method that could lead to writer starvation.
3. A corrected and fair implementation. Many fair reader-writer locks give preference to waiting writers over new readers. You should also discuss why lock upgrading (from read to write) is a difficult problem and often disallowed in many reader-writer lock implementations.

## Tips

A very advanced concurrency problem that requires a deep understanding of synchronization primitives.
