---
title: "Create a Database Indexing Strategy for a Read-Heavy Application"
slug: create-a-database-indexing-strategy-for-a-read-heavy-application
stage: Build
category: "Backend & Data Integrity"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-database-indexing-strategy-for-a-read-heavy-application
---
# Create a Database Indexing Strategy for a Read-Heavy Application

Design an indexing strategy for slow, read-heavy queries, with query analysis, index recommendations, maintenance, and performance measurement.

Variables: application_name, database_type

## Prompt

Our application, {{application_name}}, is experiencing performance issues due to slow database queries. The application is read-heavy, with a large number of complex queries that join multiple tables. Our database is {{database_type}}.

Your task is to create a comprehensive database indexing strategy to improve query performance. The strategy should include:

1.  **Query Analysis:** A plan for identifying the most frequent and slowest queries in our application. This should involve using the database's query logging and analysis tools.
2.  **Index Selection:** A set of guidelines for selecting the right columns to index. This should cover single-column indexes, composite indexes, and the use of different index types (e.g., B-tree, hash, full-text).
3.  **Indexing Strategy:** A detailed indexing strategy for our key tables. For each table, you should recommend specific indexes to create and justify your recommendations based on the query patterns.
4.  **Index Maintenance:** A plan for maintaining the indexes over time. This should include rebuilding or reorganizing indexes to prevent fragmentation and updating statistics to ensure the query optimizer makes good decisions.
5.  **Performance Measurement:** A process for measuring the impact of the new indexes on query performance and for monitoring the overall health of the database.

## Tips

This prompt is for developers who need to optimize the performance of a database-driven application.
