---
title: "Design a System for Zero-Downtime Schema Migrations"
slug: design-a-system-for-zero-downtime-schema-migrations
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-system-for-zero-downtime-schema-migrations
---
# Design a System for Zero-Downtime Schema Migrations

Get a schema migration plan for keeping an app online, with backward-compatible steps, tools, staging tests, code coordination, and monitoring.

Variables: database_type

## Prompt

We need to be able to make changes to our database schema without taking our application offline. I need to design a system for zero-downtime schema migrations for our {{database_type}} database.

Your task is to design a system for zero-downtime schema migrations. The design should include:

1.  **Migration Strategy:** A strategy for performing schema migrations in a way that is backward-compatible. This should involve breaking down schema changes into a series of small, incremental steps.
2.  **Tooling:** A recommendation for a database migration tool that supports zero-downtime migrations (e.g., gh-ost, pt-online-schema-change).
3.  **Process:** A step-by-step process for performing a zero-downtime schema migration. This should include creating the migration script, testing it in a staging environment, and running it in production.
4.  **Code Changes:** A plan for how to coordinate the database schema changes with the corresponding changes in the application code.
5.  **Monitoring:** A plan for how to monitor the migration process to ensure that it is running smoothly and to detect any problems.

## Tips

This prompt is a critical practice for any application that needs to be highly available.
