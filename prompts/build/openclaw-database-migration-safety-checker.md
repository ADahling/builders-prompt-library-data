---
title: "OpenClaw: Database Migration Safety Checker"
slug: openclaw-database-migration-safety-checker
stage: Build
category: "OpenClaw"
grade: C
score: 66
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-database-migration-safety-checker
---
# OpenClaw: Database Migration Safety Checker

Review database migration risks with backup and rollback checks, operation-specific mitigations, and a staged strategy for large tables.

## Prompt

# Database Migration Safety Checker

## Pre-Migration Checklist
Before running ANY migration:
- [ ] Backup verified and restorable
- [ ] Migration tested on staging with production-like data
- [ ] Rollback script written and tested
- [ ] Estimated runtime calculated
- [ ] Maintenance window scheduled (if needed)
- [ ] Team notified

## Safety Rules

### Always Safe
- Adding a nullable column
- Adding an index concurrently (CREATE INDEX CONCURRENTLY)
- Adding a new table
- Adding a column with a default (Postgres 11+)

### Requires Care
| Operation | Risk | Mitigation |
|-----------|------|------------|
| NOT NULL on existing column | Locks table | Add constraint as NOT VALID, validate separately |
| Rename column | Breaks queries | Use view aliases, dual-write period |
| Change column type | Locks + data loss risk | Add new column, backfill, swap |
| Drop column | Breaks code | Remove code references first, then drop |
| Add foreign key | Locks both tables | Add as NOT VALID, validate in background |

### Never in Production
- DROP TABLE without backup confirmation
- TRUNCATE on tables with foreign keys
- ALTER TYPE on large tables during peak traffic
- Migrations with both schema change AND data backfill

## Large Table Strategy (>1M rows)
1. Create new column (nullable)
2. Deploy code that writes to both old and new columns
3. Backfill in batches (1000-10000 rows per batch, with sleep)
4. Verify data consistency
5. Switch reads to new column
6. Remove old column writes
7. Drop old column

## Output
For each migration SQL provided:
- ✅ Safe / ⚠️ Caution / 🚫 Dangerous
- Lock type and estimated duration
- Recommended approach if unsafe
- Rollback SQL

## Tips

Validates database migrations for safety. Catches table locks, data loss risks, and provides safe alternatives for dangerous operations.
