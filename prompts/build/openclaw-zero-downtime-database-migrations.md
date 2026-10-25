---
title: "OpenClaw: Zero-Downtime Database Migrations"
slug: openclaw-zero-downtime-database-migrations
stage: Build
category: "OpenClaw"
grade: C
score: 60
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-zero-downtime-database-migrations
---
# OpenClaw: Zero-Downtime Database Migrations

Plan database schema changes with phased migration patterns, concurrent indexes, and batched backfills for running production systems.

## Prompt

# Zero-Downtime Database Migrations

## Golden Rules
1. Never lock tables for more than a few seconds
2. Always backward-compatible with current running code
3. Deploy in phases: schema first, code second, cleanup third
4. Test migrations against production-sized data

## Safe Migration Patterns

### Add Column
```sql
-- ✅ Safe: nullable column, no default rewrite
ALTER TABLE orders ADD COLUMN discount_pct DECIMAL(5,2);

-- ⚠️ Unsafe in older Postgres: non-null default rewrites table
-- ✅ Safe in Postgres 11+: non-null with default is metadata-only
ALTER TABLE orders ADD COLUMN status TEXT NOT NULL DEFAULT 'pending';
```

### Rename Column (Expand-Contract)
1. Add new column
2. Dual-write to both columns in application
3. Backfill old rows
4. Switch reads to new column
5. Stop writing to old column
6. Drop old column

### Add Index
```sql
-- ✅ CONCURRENTLY avoids table lock
CREATE INDEX CONCURRENTLY idx_orders_status ON orders(status);

-- ⚠️ Without CONCURRENTLY: locks entire table during build
```

### Change Column Type
1. Add new column with target type
2. Dual-write with type conversion
3. Backfill with batched UPDATE (1000 rows/batch, sleep between)
4. Swap reads, drop old column

## Large Table Backfills
```sql
-- Batch update to avoid long-running transactions
DO $$
DECLARE batch_size INT := 5000;
DECLARE rows_updated INT;
BEGIN
  LOOP
    UPDATE orders SET new_col = compute(old_col)
    WHERE new_col IS NULL AND id IN (
      SELECT id FROM orders WHERE new_col IS NULL LIMIT batch_size
    );
    GET DIAGNOSTICS rows_updated = ROW_COUNT;
    EXIT WHEN rows_updated = 0;
    PERFORM pg_sleep(0.1);
    COMMIT;
  END LOOP;
END $$;
```

## Rollback Strategy
- Every migration has a corresponding reverse migration
- Test rollback before deploying forward migration
- Keep old columns/tables for 1-2 release cycles

## Anti-Patterns
- ❌ DROP COLUMN in same deploy as code change
- ❌ ALTER TYPE on large tables without expand-contract
- ❌ Running migrations during peak traffic
- ❌ No migration testing against production-scale data

## Tips

Zero-downtime database migration patterns including expand-contract, concurrent indexing, batched backfills, and rollback strategies.
