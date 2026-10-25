---
title: "Production Outage from an Exhausted Connection Pool"
slug: production-outage-from-an-exhausted-connection-pool
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-outage-from-an-exhausted-connection-pool
---
# Production Outage from an Exhausted Connection Pool

Identify and fix Java database connection leaks by implementing try-with-resources to resolve connection pool exhaustion and outages.

## Prompt

You are a backend developer. Your application is unable to connect to the database and is throwing exceptions about the connection pool being exhausted. This has caused a complete outage. Your task is to find the cause of the connection leak.

Context:
- The application is a Java application using a HikariCP connection pool to connect to a PostgreSQL database.
- The application code is supposed to borrow a connection from the pool, use it, and then return it to the pool.
- A bug in the code is causing some connections to not be returned to the pool, eventually exhausting all available connections.

Provide:
1. An explanation of how a database connection pool works and why it is important to always close connections.
2. A Java code snippet that demonstrates a connection leak. This usually happens when an exception is thrown, and the `connection.close()` call in the `finally` block is missing or is not being reached.
3. The corrected code that uses a `try-with-resources` statement, which guarantees that the connection is closed and returned to the pool, even if an exception occurs.

## Tips

A very common and critical bug in any application that uses a database connection pool.
