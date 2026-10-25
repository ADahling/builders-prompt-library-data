---
title: "Search Term with Special Characters Breaking the Query"
slug: search-term-with-special-characters-breaking-the-query
stage: Test
category: "Functional Bugs"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/search-term-with-special-characters-breaking-the-query
---
# Search Term with Special Characters Breaking the Query

Prevent SQL syntax errors and unintended data leakage by implementing a sanitization function to escape special characters in search queries.

Variables: project_name, backend_framework, backend_language

## Prompt

You are a developer for {{project_name}}. The site-wide search is breaking when a user includes special characters, such as a percentage sign (`%`) or an underscore (`_`), in their search query. For example, searching for "100%" results in a syntax error or returns every item in the database.

This is because these characters have special meaning in a SQL `LIKE` clause and are not being properly escaped before being included in the query.

**Context:**
- **Backend:** {{backend_framework}} API.
- **Problem:** Unescaped special characters in a `LIKE` query.

**Instructions:**

1.  **Explain the Special Character Vulnerability:** Describe which characters are special in a SQL `LIKE` clause (`%` and `_`) and what they do. Explain how a malicious user could potentially exploit this (e.g., a simple SQL injection if not using parameterized queries) or how an innocent user can get unexpected results.
2.  **Implement an Escaping Function:** Write a function in your backend language ({{backend_language}}) that takes a raw search query string and properly escapes the special `LIKE` characters. For example, `%` should be replaced with `\%` and `_` with `_`. You must also specify the `ESCAPE` character in the SQL query itself.
3.  **Provide the Secure Backend Code:** Show the complete backend endpoint code that takes a search query, passes it through your escaping function, and then uses it in a parameterized SQL query to perform the search safely.

**Output Format:**

- **Vulnerability Analysis:** A clear explanation of the problem.
- **Escaping Function:** The code for the function that escapes the special characters.
- **Secure Backend Endpoint Code:** The complete, secure code for the search endpoint.

## Tips

A subtle but important security and functionality bug in search implementations.
