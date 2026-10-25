---
title: "Declarative Database Schema Management"
slug: declarative-database-schema-management
stage: Build
category: "Database & Supabase"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/declarative-database-schema-management
---
# Declarative Database Schema Management

Set up Supabase schema changes through declarative SQL files and CLI-generated migrations, following dependency, rollback, and diff caveats.

## Prompt

# Database: Declarative Schema Management (Official Supabase Pattern)

All database schema modifications must be defined within .sql files in the supabase/schemas/ directory. Do not create or modify files directly in supabase/migrations/ — migration files are generated automatically via CLI.

## Workflow:
1. For each entity (tables, views, functions), create or update a .sql file in supabase/schemas/
2. Each .sql file represents the desired FINAL state of the entity
3. Stop local Supabase before generating migrations: supabase stop
4. Generate migrations by diffing: supabase db diff -f <migration_name>
5. Schema files execute in lexicographic order — name files to manage dependencies
6. When adding columns, append to end of table definition to prevent unnecessary diffs

## Rollback:
- Update .sql files to desired state, then generate a new migration
- Review generated migration carefully to avoid unintended data loss

## Known Caveats (use versioned migrations instead):
- DML statements (insert, update, delete) are not captured by schema diff
- View ownership, security invoker, materialized views
- ALTER POLICY statements, column privileges
- Schema privileges, comments, partitions
- ALTER PUBLICATION ... ADD TABLE ...

Non-compliance with these instructions may lead to inconsistent database states.

## Tips

Official Supabase pattern for declarative schema management. Source: supabase.com/docs/guides/getting-started/ai-prompts
