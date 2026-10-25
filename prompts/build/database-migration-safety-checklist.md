---
title: "Database Migration Safety Checklist"
slug: database-migration-safety-checklist
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/database-migration-safety-checklist
---
# Database Migration Safety Checklist

Generate a comprehensive database migration plan with execution guardrails, rollback scripts, and integrity checks tailored to specific schema changes.

Variables: migration_description, database_type, database_size, affected_tables, active_connections, threshold

## Prompt

You are a database reliability engineer. Create a safety checklist for running the database migration: {{migration_description}}.

Database details:
- Type: {{database_type}}
- Size: {{database_size}}
- Tables affected: {{affected_tables}}
- Active connections: {{active_connections}}

Checklist:
1. **Pre-Migration**:
   - Backup verification (can you restore from it?)
   - Migration tested on staging with production-like data
   - Rollback script prepared and tested
   - Maintenance window communicated
   - Monitoring dashboards open

2. **Migration Execution**:
   - Lock timeout configured
   - Statement timeout configured
   - Progress monitoring (for large table migrations)
   - Connection pool management

3. **Post-Migration**:
   - Data integrity verification queries
   - Application health check
   - Performance comparison (before vs after)
   - Index usage verification
   - Rollback window defined

4. **Rollback Triggers**:
   - Error rate > {{threshold}}
   - Latency > {{threshold}}
   - Data integrity check failure

Provide specific SQL commands for each step.

## Tips

Database migrations are the riskiest part of any deployment. This checklist prevents data loss.
