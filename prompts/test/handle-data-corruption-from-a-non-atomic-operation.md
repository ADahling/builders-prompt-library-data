---
title: "Handle Data Corruption from a Non-Atomic Operation"
slug: handle-data-corruption-from-a-non-atomic-operation
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/handle-data-corruption-from-a-non-atomic-operation
---
# Handle Data Corruption from a Non-Atomic Operation

Eliminate race conditions in user balance updates by implementing atomic SQL operations to ensure data integrity during concurrent requests.

## Prompt

You are a backend developer. You have a service that manages user balances in an online game. You have discovered that balances are sometimes incorrect due to a non-atomic read-modify-write operation. Your task is to fix this data corruption bug.

Context:
- The service reads the current balance from the database, adds the winnings in the application code, and then writes the new balance back to the database.
- If two requests for the same user are processed at the same time, one of the updates can be lost.
- The database is a relational database like PostgreSQL or MySQL.

Provide:
1. A step-by-step example of the race condition, showing how two concurrent requests can lead to an incorrect final balance.
2. A solution that performs the update atomically in the database using a single SQL `UPDATE` statement (e.g., `UPDATE users SET balance = balance + ? WHERE id = ?`).
3. A discussion of why performing the read and write as separate operations is not safe in a concurrent environment and how atomic database operations solve this.

## Tips

A critical concept in application development that interacts with a database.
