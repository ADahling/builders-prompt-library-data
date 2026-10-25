---
title: "Zero-Downtime Database Migration Strategy for a Production PostgreSQL Database"
slug: zero-downtime-database-migration-strategy-for-a-production-postgresql-database
stage: Ship
category: "Deployment & Launch"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/zero-downtime-database-migration-strategy-for-a-production-postgresql-database
---
# Zero-Downtime Database Migration Strategy for a Production PostgreSQL Database

Plan a production PostgreSQL schema migration targeting zero downtime, with phased steps to limit table locking and online migration tool examples.

Variables: postgres_version, app_stack, migration_type, table_size

## Prompt

I need to perform a schema migration on a production PostgreSQL database with zero downtime. The application is a high-traffic web service and cannot afford any service interruption.

**Migration Details:**
- **Database:** PostgreSQL version `{{postgres_version}}`.
- **Application Stack:** `{{app_stack}}`.
- **Migration Type:** `{{migration_type}}` (e.g., adding a new table, adding a column with a default value, changing a column type).
- **Current Table Size:** The table to be migrated has approximately `{{table_size}}` rows.

**Requirements for the Migration Strategy:**
1.  **Phased Approach:** Outline a step-by-step, phased approach to perform the migration without locking the tables for an extended period. This should include steps for preparing the database, applying the changes, and verifying the migration.
2.  **Tooling:** Recommend and provide examples of using a database migration tool that supports online schema changes for PostgreSQL (e.g., `pg_repack

## Tips

This is an advanced prompt for developers and database administrators who need to perform complex database migrations on a live production system.
