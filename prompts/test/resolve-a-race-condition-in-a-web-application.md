---
title: "Resolve a Race Condition in a Web Application"
slug: resolve-a-race-condition-in-a-web-application
stage: Test
category: "Critical Bugs"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-race-condition-in-a-web-application
---
# Resolve a Race Condition in a Web Application

Identify and fix concurrency issues in Node.js and PostgreSQL using database transactions and distributed locking to ensure data atomicity.

## Prompt

You are a full-stack developer. A feature in your web application that allows users to claim a limited-time offer is flawed. Multiple users are able to claim the offer simultaneously, exceeding the intended limit. This is due to a race condition. Your task is to fix it.

Context:
- The backend is a Node.js application with a PostgreSQL database.
- The logic checks if the offer is available, then decrements the available count and assigns the offer to the user.
- These two steps (check and update) are not atomic.

Provide:
1. A clear explanation of how the race condition occurs between the check and the update operations.
2. A solution using a database transaction with a `SELECT FOR UPDATE` statement to lock the row, ensuring the check and update are atomic.
3. An alternative solution at the application level using a mutex or a distributed lock if the application is scaled across multiple instances.

## Tips

A classic web development race condition problem with practical solutions.
