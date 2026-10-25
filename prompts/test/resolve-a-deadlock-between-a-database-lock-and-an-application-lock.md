---
title: "Resolve a Deadlock between a Database Lock and an Application Lock"
slug: resolve-a-deadlock-between-a-database-lock-and-an-application-lock
stage: Test
category: "Critical Bugs"
grade: C
score: 68
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-deadlock-between-a-database-lock-and-an-application-lock
---
# Resolve a Deadlock between a Database Lock and an Application Lock

Analyze and resolve cross-system deadlocks by synchronizing lock acquisition order between application threads and database transactions.

## Prompt

You are a senior developer. Your application is experiencing a complex deadlock that involves both a database lock and an application-level lock. Your task is to analyze and resolve this tricky situation.

Context:
- A thread in your Java application acquires an application-level lock (a `ReentrantLock`).
- It then starts a database transaction and issues a query that acquires a row-level lock in the database.
- Meanwhile, another database transaction (from a different thread or process) holds a lock on a different row that the first thread needs, and it is waiting for the first transaction to commit. To do this, it makes a call back to the application, which then tries to acquire the same application-level lock that the first thread is holding.

Provide:
1. A sequence diagram that illustrates this complex deadlock scenario.
2. An explanation of why this is so difficult to debug (the deadlock involves two different locking systems).
3. A solution that involves refactoring the code to never make a call from the database (e.g., from a trigger or stored procedure) back into the application while holding a database lock. Alternatively, ensure that locks are always acquired in a consistent order (e.g., always acquire the application lock before starting a database transaction).

## Tips

A very challenging deadlock scenario that spans multiple systems.
