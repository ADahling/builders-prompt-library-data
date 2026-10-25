---
title: "Production Outage from a Bad Database Migration"
slug: production-outage-from-a-bad-database-migration
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-outage-from-a-bad-database-migration
---
# Production Outage from a Bad Database Migration

Formulate a critical recovery plan and long-term prevention strategy for production database failures caused by destructive migrations.

## Prompt

You are a backend developer. You have just deployed a new version of your application, which included a database migration. The migration script had a bug, and it has corrupted a critical table in the production database, causing the application to fail. Your task is to handle this emergency.

Context:
- The migration was supposed to add a new column to the `users` table but instead dropped it.
- The application is now throwing errors whenever it tries to access the missing column.
- You have database backups, but restoring the entire database would cause significant data loss from recent transactions.

Provide:
1. An immediate action plan, including putting the application into maintenance mode and communicating the issue.
2. A strategy to recover from the bad migration. This might involve restoring only the affected table from a recent backup and then re-applying any transactions that occurred since the backup (using binary logs if available).
3. A proposal for a safer database migration process, including mandatory code reviews for migration scripts, running migrations in a staging environment first, and using tools that support reversible migrations.

## Tips

A stressful but common scenario that tests both technical and process-oriented skills.
