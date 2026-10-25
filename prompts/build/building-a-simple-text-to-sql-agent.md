---
title: "Building a Simple Text-to-SQL Agent"
slug: building-a-simple-text-to-sql-agent
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-text-to-sql-agent
---
# Building a Simple Text-to-SQL Agent

Get a Python script that uses an LLM to turn a question and a CREATE TABLE schema into a raw SQL query for database querying.

Variables: question, schema

## Prompt

Create a simple AI agent that can translate a natural language question into a SQL query.

**Agent's Task:**

Given a natural language `{{question}}` and a database `{{schema}}` (provided as a CREATE TABLE statement), the agent should generate the corresponding SQL query.

**Implementation:**

This is a prompt engineering task.

*   **The Prompt:**
    *   **Role:** "You are an expert SQL developer."
    *   **Task:** "Based on the provided database schema, write a SQL query that answers the following question."
    *   **Inputs:**
        *   Schema: `{{schema}}`
        *   Question: `{{question}}`
    *   **Output Format:** "Provide only the raw SQL query, with no explanation or code block formatting."

**Example:**

*   **Schema:** `CREATE TABLE users (id INT, name TEXT, age INT);`
*   **Question:** "How many users are over the age of 30?"
*   **Expected Output:** `SELECT COUNT(*) FROM users WHERE age > 30;`

**Your Task:**

Write a Python script that takes the schema and question, uses an LLM with this prompt to generate the SQL, and prints the query.

**Output:**

A Python script for the Text-to-SQL agent.
