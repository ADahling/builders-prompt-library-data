---
title: "Create an Integration Test for a Database Migration"
slug: create-an-integration-test-for-a-database-migration
stage: Test
category: "Testing & QA"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-integration-test-for-a-database-migration
---
# Create an Integration Test for a Database Migration

Generate a comprehensive integration test plan, validation script, and rollback procedure to ensure data integrity during database migrations.

Variables: migration_purpose, source_database, target_database, scripting_language

## Prompt

You are a database administrator. Your task is to create an integration test for a database migration script that {{migration_purpose}}. The migration is from {{source_database}} to {{target_database}}.

Context:
- The migration script is written in {{scripting_language}}.
- You need to ensure that the data is migrated correctly and that there is no data loss.

Provide:
1. A test plan for the database migration.
2. An integration test that runs the migration script and verifies the data in the target database.
3. A rollback plan in case the migration fails.

## Tips

A prompt for database administrators and backend developers who need to test database migrations, which are critical and high-risk operations.
