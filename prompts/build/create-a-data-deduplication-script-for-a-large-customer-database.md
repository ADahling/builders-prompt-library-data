---
title: "Create a Data Deduplication Script for a Large Customer Database"
slug: create-a-data-deduplication-script-for-a-large-customer-database
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-data-deduplication-script-for-a-large-customer-database
---
# Create a Data Deduplication Script for a Large Customer Database

Get a customer data deduplication script and execution plan with fuzzy matching, master record selection, merging rules, and backup steps.

Variables: database_type, scripting_language

## Prompt

Our customer database has grown over the years and now contains a significant number of duplicate records. This is causing issues with our marketing campaigns and analytics. I need to create a script to identify and merge these duplicate records in our {{database_type}} database.

Your task is to generate a well-structured and efficient data deduplication script and an accompanying execution plan. This should include:

1.  **Duplicate Detection Logic:** Define a set of criteria to identify potential duplicate records. This could involve matching on fields like email, phone number, and name with some tolerance for typos and variations.
2.  **Fuzzy Matching:** Recommend and show how to use a fuzzy matching library (e.g., FuzzyWuzzy for Python) to compare string fields and identify similarities.
3.  **Deduplication Script:** Write a script in {{scripting_language}} that identifies duplicate records, selects the master record to keep, and merges the data from the duplicate records into the master record. The script should also handle the deletion of the duplicate records.
4.  **Data Merging Strategy:** Define a clear strategy for merging data from duplicate records. For example, the master record might keep the oldest creation date and the most recent update date.
5.  **Execution Plan:** Provide a safe execution plan that includes backing up the database, running the script in a test environment first, and verifying the results before running it on the production database.

## Tips

This prompt helps in cleaning up and maintaining the quality of a large and important dataset.
