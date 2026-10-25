---
title: "Fix Inefficient Full-Text Search on a Large Table"
slug: fix-inefficient-full-text-search-on-a-large-table
stage: Test
category: "Functional Bugs"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-inefficient-full-text-search-on-a-large-table
---
# Fix Inefficient Full-Text Search on a Large Table

Optimize database performance by replacing slow wildcard LIKE queries with efficient, indexed full-text search implementations.

Variables: project_name, database_name

## Prompt

You are a backend engineer for {{project_name}}, a large blog platform with millions of articles. The search functionality, which uses a `LIKE '%...%'` query, is becoming unacceptably slow. The database is performing a full table scan for every search because the `LIKE` query with a leading wildcard (`%`) cannot use a standard B-tree index.

Your task is to replace the inefficient `LIKE` query with a proper full-text search (FTS) solution for your database.

**Context:**
- **Database:** {{database_name}} (e.g., PostgreSQL, MySQL, Elasticsearch).
- **Problem:** Slow performance of `LIKE` on a large dataset.

**Instructions:**

1.  **Analyze the Performance Issue:** Explain in detail why a `LIKE` query with a leading wildcard is so inefficient and why it prevents the use of standard indexes.
2.  **Implement Full-Text Search:** Your solution will depend on the database.
    *   **For PostgreSQL:** Show how to create a `tsvector` column on your `articles` table, create a GIN index on it, and use the `to_tsquery` and `@@` operator to perform a fast full-text search.
    *   **For MySQL:** Show how to create a `FULLTEXT` index on the relevant columns and use the `MATCH() ... AGAINST()` syntax.
    *   **For Elasticsearch:** Describe how you would index the document and use the Elasticsearch Query DSL to perform the search.
3.  **Provide the FTS Query:** Give the complete SQL or JSON query for performing an efficient full-text search using your chosen database technology.

**Output Format:**

- **Performance Analysis:** A detailed explanation of the `LIKE` query bottleneck.
- **FTS Implementation Steps:** The steps and DDL commands to set up full-text search for your chosen database.
- **Efficient FTS Query:** The final, performant search query.

## Tips

A crucial optimization for any application with a serious search requirement. This moves beyond basic SQL.
