---
title: "Search Query Returning Case-Sensitive Results"
slug: search-query-returning-case-sensitive-results
stage: Test
category: "Functional Bugs"
grade: A+
score: 98
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/search-query-returning-case-sensitive-results
---
# Search Query Returning Case-Sensitive Results

Refactor SQL search queries to implement case-insensitive matching using ILIKE or LOWER for improved documentation search results.

Variables: project_name, backend_framework, database_name, search_query

## Prompt

You are a backend developer for {{project_name}}, an online documentation site. Users have reported that the search functionality is case-sensitive. For example, searching for "react" does not return documents containing the word "React". This is a poor user experience, as users expect searches to be case-insensitive.

Your task is to modify the database query to perform a case-insensitive search.

**Context:**
- **Backend:** {{backend_framework}} API.
- **Database:** {{database_name}} (e.g., PostgreSQL, MySQL).

**Buggy, Case-Sensitive Query:**

```sql
SELECT * FROM documents WHERE content LIKE '%{{search_query}}%';
```

**Instructions:**

1.  **Explain the Case-Sensitivity Problem:** Describe why the default `LIKE` operator is often case-sensitive in many SQL databases and why this is undesirable for a user-facing search.
2.  **Propose a Solution:** Your solution will depend on the specific database being used.
    *   **For PostgreSQL:** Show how to use the `ILIKE` operator, which is a drop-in replacement for `LIKE` that performs a case-insensitive match.
    *   **For MySQL/Other Databases:** Show how to use the `LOWER()` or `UPPER()` function on both the column and the search term to ensure a case-insensitive comparison (e.g., `WHERE LOWER(content) LIKE LOWER('%{{search_query}}%')`). Discuss the potential performance implications of using functions on a column.
3.  **Provide the Corrected Query:** Give the final, corrected SQL query for both PostgreSQL and a more general SQL database.

**Output Format:**

- **Problem Analysis:** A clear explanation of the case-sensitivity issue.
- **Corrected SQL Queries:** The fixed queries for both PostgreSQL (`ILIKE`) and a general solution (`LOWER()`).

## Tips

A very common and easy-to-fix search bug that significantly improves user experience.
