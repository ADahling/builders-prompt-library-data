---
title: "Create a Data Dictionary for an Existing Database"
slug: create-a-data-dictionary-for-an-existing-database
stage: Build
category: "Backend & Data Integrity"
grade: C
score: 65
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-data-dictionary-for-an-existing-database
---
# Create a Data Dictionary for an Existing Database

Get a data dictionary template and creation process for an undocumented database, with schema extraction, profiling, and maintenance guidance.

Variables: database_type

## Prompt

I have inherited a legacy database with many tables and columns, but there is no documentation. To understand the database and to help new developers get up to speed, I need to create a data dictionary.

Your task is to generate a data dictionary for our {{database_type}} database. The process should include:

1.  **Schema Extraction:** A script or a set of commands to extract the schema information from the database. This should include the table names, column names, data types, constraints, and relationships.
2.  **Data Dictionary Template:** A template for the data dictionary. The template should have a clear and consistent format for documenting each table and column.
3.  **Column Descriptions:** A process for writing clear and concise descriptions for each column. This might involve talking to business users, analyzing the application code, and querying the data to understand its meaning.
4.  **Data Profiling:** A plan for profiling the data in the database to gather additional information, such as the range of values, the number of distinct values, and the percentage of null values for each column.
5.  **Maintenance Plan:** A plan for how to keep the data dictionary up-to-date as the database schema evolves.

## Tips

This prompt is a common and important task for any developer who has to work with an existing database.
