---
title: "Resolve a Race Condition in an \u2018Upsert\u2019 Operation"
slug: resolve-a-race-condition-in-an-upsert-operation
stage: Test
category: "Critical Bugs"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-race-condition-in-an-upsert-operation
---
# Resolve a Race Condition in an ‘Upsert’ Operation

Eliminate PostgreSQL race conditions by implementing atomic upserts using ON CONFLICT or exception-handled insert-then-update logic.

## Prompt

You are a backend developer. You need to implement an ‘upsert’ logic: if a record with a certain key exists, update it; otherwise, insert it. You have implemented this as a ‘read-then-write’ operation, but you are finding that under concurrent load, it is failing with unique constraint violations. This is because two processes can both read, see that the record doesn’t exist, and then both try to insert it.

Context:
- The database is PostgreSQL, which has a unique constraint on the key.
- The application code is written in Python.
- The race condition happens when two concurrent requests try to upsert the same key for the first time.

Provide:
1. The Python code that demonstrates the race condition.
2. A solution that uses PostgreSQL’s `INSERT ... ON CONFLICT (key) DO UPDATE ...` statement. This is an atomic operation that handles the race condition at the database level.
3. An alternative solution for databases that don’t support `ON CONFLICT`. This would involve attempting the `INSERT` first, and if it fails with a unique constraint violation, then issuing an `UPDATE`. This is often better than read-then-write because the race condition is less likely to occur.

## Tips

A very common database programming pattern that needs to be handled correctly to avoid race conditions.
