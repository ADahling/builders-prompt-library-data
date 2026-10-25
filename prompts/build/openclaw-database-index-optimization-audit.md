---
title: "OpenClaw: Database Index Optimization Audit"
slug: openclaw-database-index-optimization-audit
stage: Build
category: "OpenClaw"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-database-index-optimization-audit
---
# OpenClaw: Database Index Optimization Audit

Audit PostgreSQL slow queries, execution plans, and index usage to identify missing, duplicate, unused, or oversized indexes.

## Prompt

# Database Index Optimization Audit

## Query Analysis

### Step 1: Identify Slow Queries
```sql
-- PostgreSQL: queries taking > 100ms
SELECT query, calls, mean_exec_time, total_exec_time
FROM pg_stat_statements
WHERE mean_exec_time > 100
ORDER BY total_exec_time DESC
LIMIT 20;
```

### Step 2: Analyze Query Plans
For each slow query, run EXPLAIN (ANALYZE, BUFFERS, FORMAT TEXT):
- Look for: Seq Scan on large tables (> 10k rows)
- Look for: Nested Loop with high row estimates
- Look for: Sort operations without index support
- Look for: Hash Join where Merge Join would be better

### Index Review Checklist
- [ ] Every foreign key column has an index
- [ ] Composite indexes match query WHERE + ORDER BY column order
- [ ] Covering indexes used for frequent read-only queries
- [ ] Partial indexes for filtered queries (WHERE status = 'active')
- [ ] No duplicate indexes (A, B) and (A) — the composite covers single-column
- [ ] Unused indexes identified and dropped
- [ ] GIN/GiST indexes for JSONB, array, and full-text search columns

### Index Health Metrics
```sql
-- Find unused indexes
SELECT schemaname, relname, indexrelname, idx_scan
FROM pg_stat_user_indexes
WHERE idx_scan = 0
AND indexrelname NOT LIKE '%_pkey'
ORDER BY pg_relation_size(indexrelid) DESC;

-- Find bloated indexes
SELECT indexrelname, pg_size_pretty(pg_relation_size(indexrelid)) as index_size,
       idx_scan, idx_tup_read
FROM pg_stat_user_indexes
ORDER BY pg_relation_size(indexrelid) DESC
LIMIT 10;
```

### Optimization Patterns
| Pattern | When to Use |
|---------|-------------|
| B-tree (default) | Equality and range queries |
| Hash | Equality-only queries (rare) |
| GIN | JSONB, arrays, full-text |
| GiST | Geometric, range types |
| BRIN | Large tables with natural ordering (timestamps) |
| Partial | Queries always filter on same condition |
| Covering (INCLUDE) | Avoid heap lookups for SELECT columns |

## Tips

Database index optimization audit with slow query identification, EXPLAIN analysis, index health metrics, and optimization patterns for PostgreSQL.
