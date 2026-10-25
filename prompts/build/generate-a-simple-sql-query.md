---
title: "Generate a simple SQL query"
slug: generate-a-simple-sql-query
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 90
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-simple-sql-query
---
# Generate a simple SQL query

Generate a filtered SQL SELECT statement to retrieve all columns from a specific table based on a single column value.

Variables: table_name, column_name, value

## Prompt

You are an AI coding assistant. Generate a SQL query to select all columns from a table named `{{table_name}}`. The query should also filter the results to only include rows where the `{{column_name}}` column has a value of `{{value}}`.

## Tips

A basic prompt for creating a common SQL query.
