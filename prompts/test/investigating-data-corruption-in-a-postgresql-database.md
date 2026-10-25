---
title: "Investigating Data Corruption in a PostgreSQL Database"
slug: investigating-data-corruption-in-a-postgresql-database
stage: Test
category: "Critical Bugs"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/investigating-data-corruption-in-a-postgresql-database
---
# Investigating Data Corruption in a PostgreSQL Database

Get a PostgreSQL data corruption investigation plan covering scope queries, containment, backups, recovery, and application code review.

Variables: app_name, table_name

## Prompt

We have detected data corruption in our PostgreSQL database for our {{app_name}} application. Specifically, we are seeing records in the {{table_name}} table with inconsistent or invalid data that should not be possible according to our application logic. This is a critical issue that is affecting the integrity of our data and the functionality of our application.

As a database specialist, you are tasked with investigating the root cause of this data corruption. Your response should be a detailed investigation plan that our team can follow. The plan should cover the following areas:

1.  **Initial Assessment and Containment:** What are the very first steps you would take to assess the extent of the corruption and prevent it from spreading? This should include:
    *   **Identifying the Scope:** How would you write queries to identify all the corrupted records?
    *   **Backups and Recovery:** What is the immediate plan for backing up the current data and potentially recovering from a previous backup?
    *   **Disabling Problematic Code:** Should we disable any parts of the application that might be causing the corruption?

2.  **Identifying the Source of Corruption:** Outline a systematic approach to find the source of the data corruption. This should include investigating:
    *   **Application Code:** How would you review the application code to find bugs that could lead to data corruption? What specific patterns would you look for (e.g., race conditions, incorrect data validation, SQL injection vulnerabilities)?
    *   **Database Triggers and Stored Procedures:** How would you review our database triggers and stored procedures for any logic that could be causing the issue?
    *   **External Systems:** Are there any external systems or batch jobs that interact with our database? How would you investigate them?
    *   **Hardware Issues:** While less likely, how would you rule out hardware issues (e.g., faulty memory, disk corruption) as a potential cause?

3.  **Using PostgreSQL Tools for Investigation:** What PostgreSQL tools and features can we use to help with the investigation? This should include:
    *   **Logging:** How can we increase the logging level in PostgreSQL (e.g., 'log_statement = 'all'') to capture all queries being executed?
    *   **Auditing:** How can we use tools like 'pgaudit' to create an audit trail of all changes to the {{table_name}} table?
    *   **Page-Level Inspection:** How can we use tools like 'pageinspect' to look at the low-level storage of the corrupted rows?

4.  **Data Recovery and Repair:** Once the root cause is identified and fixed, what is the plan for repairing the corrupted data? This should include:
    *   **Writing a Data-Fixing Script:** Provide a template for a SQL script that would identify and fix the corrupted records.
    *   **Testing the Script:** How would you test the script in a staging environment before running it on production?

5.  **Post-Mortem and Prevention:** What are the key lessons learned from this incident? What changes should we make to our development and deployment processes to prevent data corruption in the future?

Your response should be at least 500 words and provide a thorough and practical investigation plan.
