---
title: "Optimize Slow Pagination on a Large Dataset with Missing Index"
slug: optimize-slow-pagination-on-a-large-dataset-with-missing-index
stage: Test
category: "Functional Bugs"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-slow-pagination-on-a-large-dataset-with-missing-index
---
# Optimize Slow Pagination on a Large Dataset with Missing Index

Optimize large-dataset pagination by replacing slow OFFSET queries with keyset pagination and strategic indexing to eliminate timeouts.

Variables: project_name, database_name

## Prompt

You are a database administrator and backend engineer for {{project_name}}. The application has a table with millions of records. Users are reporting that as they navigate to higher page numbers (e.g., page 5,000), the API requests become extremely slow, sometimes timing out.

This is because the database has to scan a huge number of rows to satisfy the `OFFSET` clause in the pagination query, and the columns used for sorting are not indexed.

**Context:**
- **Database:** {{database_name}} with a very large table (e.g., `events`).
- **Slow Query:** `SELECT * FROM events ORDER BY event_date DESC LIMIT 10 OFFSET 50000;`

**Instructions:**

1.  **Analyze the Performance Bottleneck:** Explain in detail why `OFFSET` becomes progressively slower on large datasets. Describe how the database engine processes a query with a large offset and why it cannot simply "jump" to the 50,000th row.
2.  **Propose an Indexing Strategy:** Identify the column used in the `ORDER BY` clause (`event_date`). Explain that this column must have a database index. Provide the SQL command to create an index on this column.
3.  **Propose a Query Refactoring (Seek Method):** Even with an index, large offsets can be slow. Introduce a more performant query pattern known as the "seek method" or keyset pagination, which is a variation of cursor-based pagination. Instead of `OFFSET

## Tips

A critical performance optimization for applications with large datasets. This bridges the gap between development and database administration.
