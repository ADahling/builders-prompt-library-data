---
title: "Repairing Data Corruption from a Failed Database Migration"
slug: repairing-data-corruption-from-a-failed-database-migration
stage: Test
category: "Critical Bugs"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/repairing-data-corruption-from-a-failed-database-migration
---
# Repairing Data Corruption from a Failed Database Migration

Get an incident recovery plan for a partially failed database migration, covering containment, backup decisions, damage assessment, and example SQL.

Variables: app_name, table_name

## Prompt

During our last deployment for the {{app_name}} application, a database migration script failed halfway through. The script was supposed to refactor the {{table_name}} table, but it terminated unexpectedly, leaving the database in an inconsistent and partially migrated state. This has resulted in data corruption: some rows have the new schema, some have the old schema, and foreign key constraints are now violated. This is a critical incident.

As the on-call database engineer, you must lead the effort to recover from this failed migration. Your response should be a detailed incident response and recovery plan.

1.  **Immediate Incident Response (The First 15 Minutes):**
    *   What is the absolute first thing you do? (Hint: It involves preventing further data corruption).
    *   Outline the steps for immediate containment: putting the application into maintenance mode, stopping all write access to the affected tables, and communicating the status to stakeholders.
    *   What is your immediate backup and recovery strategy? Do you restore from the last backup immediately, or do you try to fix the data first? Justify your choice, considering data loss (RPO/RTO).

2.  **Assessing the Damage:**
    *   You've decided to attempt a repair before restoring from backup to avoid data loss. Outline a plan to assess the exact state of the data.
    *   Provide example SQL queries you would write to determine:
        *   Which rows were successfully migrated?
        *   Which rows were left in the old format?
        *   Are there any rows that are in a bizarre, intermediate state?
        *   Which foreign key constraints are now violated?

3.  **Developing the Rollback/Roll-Forward Plan:**
    *   Based on your assessment, you need to create a new migration script to fix the data. You have two choices: roll back (undo the partial changes) or roll forward (complete the migration for the remaining rows).
    *   Provide a set of criteria to decide whether to roll back or roll forward. (e.g., percentage of rows migrated, complexity of the rollback vs. roll-forward logic).
    *   Write a detailed pseudocode or SQL script for *both* a potential rollback and a potential roll-forward scenario. The script must be idempotent (safe to run multiple times).

4.  **Executing the Repair and Verification:**
    *   You've written the repair script. You can't just run it on production. Describe the testing and verification process.
    *   How would you create a safe, isolated environment to test your script? (e.g., restoring a snapshot of the corrupted production DB to a staging server).
    *   What verification queries would you run after executing the script to be 100% certain that the data is now consistent and correct?
    *   Describe the process of running the final, approved script on the production database during a planned maintenance window.

5.  **Post-Mortem and Improving the Migration Process:**
    *   The crisis is over. Now, you need to prevent it from ever happening again. Conduct a post-mortem.
    *   What was the root cause of the original migration script's failure? (e.g., bad error handling, unexpected data, timeout).
    *   Propose at least three concrete improvements to your team's database migration process. For example:
        *   All migrations must be wrapped in a single transaction.
        *   Migrations on large tables must be performed in smaller, non-locking batches.
        *   All migrations must be tested against a recent copy of the production database before deployment.

Your response should be a professional and thorough incident plan of at least 600 words.
