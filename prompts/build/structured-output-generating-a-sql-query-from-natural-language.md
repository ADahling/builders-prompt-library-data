---
title: "Structured Output: Generating a SQL Query from Natural Language"
slug: structured-output-generating-a-sql-query-from-natural-language
stage: Build
category: "LLM & AI Integration"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/structured-output-generating-a-sql-query-from-natural-language
---
# Structured Output: Generating a SQL Query from Natural Language

Convert natural language business questions into secure, schema-aligned PostgreSQL queries for non-technical database access.

## Prompt

You are building a business intelligence tool that allows non-technical users to query a database using plain English. You will use an LLM to translate their questions into SQL queries.

Your task is to create a robust prompt for an LLM to perform this translation.

**Scenario:**
- **Database Schema:**
  `CREATE TABLE users (id INT, name VARCHAR, signup_date DATE);
  CREATE TABLE orders (id INT, user_id INT, amount DECIMAL, order_date DATE);`
- **User Request:** "Show me the names of users who signed up this year and have placed an order with an amount over $100."

**Prompt Engineering Task:**
You are not writing code, but the prompt itself.

**Prompt Requirements:**
1.  **Role Definition:** "You are an expert SQL developer who specializes in writing complex, efficient, and secure queries."
2.  **Context (The Schema):** "Here is the database schema I am working with: [Paste the CREATE TABLE statements here]."
3.  **The Task:** "Based on the schema, convert the following user request into a single, valid SQL query for a PostgreSQL database."
4.  **User Request:** Provide the user's request text.
5.  **Security Constraint:** "IMPORTANT: Your query must be secure against SQL injection. Do not directly insert user-provided values into the query string. Assume that values will be parameterized in the application code."
6.  **Formatting Constraint:** "Your response must be a single SQL code block, with no other text or explanation. Do not use markdown formatting like `sql`."

**Desired Output (from the LLM):**
`SELECT u.name
FROM users u
JOIN orders o ON u.id = o.user_id
WHERE u.signup_date >= '2024-01-01' AND o.amount > 100;`

**Output Format:**
Provide a single block of text representing the complete, final prompt that would be sent to the LLM.
