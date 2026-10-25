---
title: "Create a Database Migration Guide"
slug: create-a-database-migration-guide
stage: Design
category: "Documentation"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-database-migration-guide
---
# Create a Database Migration Guide

Generate a comprehensive end-to-end database migration guide with technical checklists, ETL scripts, validation tests, and rollback plans.

Variables: source_database, target_database, migration_tool

## Prompt

You are a database administrator (DBA) responsible for planning and executing a migration from {{source_database}} to {{target_database}}. A detailed migration guide is crucial to ensure a smooth and successful migration with minimal downtime.

Your task is to create a comprehensive migration guide that covers the entire process from planning to post-migration validation. The guide should include the following sections:

*   **Introduction:** An overview of the migration, including the reasons for migrating and the expected benefits.
*   **Pre-Migration Checklist:** A detailed checklist of all the tasks that need to be completed before the migration begins, such as backing up the source database, analyzing the schema, and preparing the target environment.
*   **Migration Steps:** A step-by-step plan for the migration itself, including data extraction, transformation, and loading (ETL). Provide specific commands and scripts where applicable.
*   **Post-Migration Validation:** A set of tests and checks to verify that the migration was successful and that the data is consistent and accurate.
*   **Rollback Plan:** A detailed plan for rolling back to the source database in case of any issues during the migration.

Here is some information about the migration:

*   **Source Database:** {{source_database}}
*   **Target Database:** {{target_database}}
*   **Migration Tool:** {{migration_tool}}

Generate the complete migration guide in Markdown format. The guide should be extremely detailed, precise, and leave no room for ambiguity.
