---
title: "Generate Code with Type Hints from a Database Schema"
slug: generate-code-with-type-hints-from-a-database-schema
stage: Build
category: "AI Coding Assistants"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-code-with-type-hints-from-a-database-schema
---
# Generate Code with Type Hints from a Database Schema

Get a prompt for generating Python dataclasses from a SQL schema, with classes matching database tables and type hints based on SQL data types.

Variables: sql_schema

## Prompt

You have a database schema defined in a SQL file. You want to generate Python data classes with type hints that correspond to the tables in your database.

Provide the SQL schema (`{{sql_schema}}`) to an AI assistant and ask it to generate the Python code. The prompt should specify that the generated classes should use Python's `dataclasses` module and include type hints based on the SQL data types.

## Tips

A practical prompt for bridging the gap between database and application code.
