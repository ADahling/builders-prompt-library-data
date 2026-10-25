---
title: "Write a Zero-Downtime Data Migration Script for a Major Schema Change"
slug: write-a-zero-downtime-data-migration-script-for-a-major-schema-change
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 71
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-zero-downtime-data-migration-script-for-a-major-schema-change
---
# Write a Zero-Downtime Data Migration Script for a Major Schema Change

Plan a major schema migration targeting zero downtime with a phased strategy, idempotent script, consistency checks, and rollback steps.

Variables: application_name, database_type, scripting_language

## Prompt

Our {{application_name}} application is undergoing a major schema change in our {{database_type}} database. We need to migrate a large amount of data from the old schema to the new one without causing any downtime for our users. The migration involves restructuring tables, renaming columns, and transforming data.

Your task is to generate a detailed, step-by-step plan and a corresponding migration script in {{scripting_language}} to perform this migration with zero downtime. The plan should include:

1.  **Phased Migration Strategy:** Propose a phased approach to the migration (e.g., the expand-and-contract pattern) that allows the application to work with both the old and new schemas simultaneously during the transition period.
2.  **Migration Script:** Write a well-documented and idempotent migration script that can be run multiple times without causing data duplication or corruption. The script should handle data transformation, validation, and error logging.
3.  **Data Consistency Checks:** Describe how to perform data consistency checks to ensure that all data has been migrated correctly and that the new schema is consistent with the old one.
4.  **Rollback Plan:** Outline a detailed rollback plan in case the migration fails or introduces critical issues. The rollback plan should specify how to revert the schema and data to their original state.
5.  **Performance Considerations:** Suggest ways to optimize the migration script for performance to minimize the impact on the production database.

## Tips

This prompt is for experienced developers tackling complex data migrations in live production environments, where uptime is critical.
