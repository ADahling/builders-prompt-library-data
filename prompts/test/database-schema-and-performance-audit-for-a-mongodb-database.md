---
title: "Database Schema and Performance Audit for a MongoDB Database"
slug: database-schema-and-performance-audit-for-a-mongodb-database
stage: Test
category: "Quality Audits"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/database-schema-and-performance-audit-for-a-mongodb-database
---
# Database Schema and Performance Audit for a MongoDB Database

Analyze MongoDB schema, indexing, and query performance to generate a comprehensive audit report with prioritized optimization strategies.

Variables: project_name, project_description

## Prompt

As a database administrator, I need you to perform a thorough audit of the MongoDB database for our application, `{{project_name}}`. This application is a {{project_description}}. We are experiencing performance issues and are concerned about the long-term scalability and maintainability of our database.

Your audit should focus on the following areas:

1.  **Schema Design and Data Modeling:**
    *   Review the database schema for adherence to MongoDB data modeling best practices.
    *   Identify any issues with document structure, embedding, and linking.
    *   Assess the appropriateness of data types used for each field.
    *   Check for consistent and clear naming conventions for collections and fields.

2.  **Indexing Strategy:**
    *   Analyze the existing indexes and their effectiveness.
    *   Identify any missing indexes that could improve query performance.
    *   Find and recommend the removal of any unused or redundant indexes.

3.  **Query Performance:**
    *   Identify the top 5 most expensive queries in terms of execution time and resource consumption.
    *   For each expensive query, analyze its execution plan and provide specific recommendations for optimization (e.g., rewriting the query, adding indexes).

4.  **Security:**
    *   Review user privileges and roles to ensure the principle of least privilege is being followed.
    *   Check for any potential security vulnerabilities.
    *   Assess the database configuration for any security misconfigurations.

5.  **Backup and Recovery:**
    *   Review the current backup and recovery strategy to ensure it meets our business continuity requirements.
    *   Verify that backups are being performed regularly and that they can be successfully restored.

**Output Format:**

Please provide a database audit report in a Markdown file with the following sections:

*   **Database Health Summary:** A high-level overview of the database's health, including a summary of the most critical issues found.
*   **Audit Findings:** A detailed list of all identified issues, categorized by the areas mentioned above. For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **Severity:** (High, Medium, Low)
    *   **Description:** A clear explanation of the issue.
    *   **Recommendation:** Specific and actionable steps to fix the issue.
*   **Database Optimization Plan:** A prioritized list of recommendations for improving the database's performance, security, and maintainability.

Your report should be a comprehensive guide that our team can use to improve the health and performance of our database.
