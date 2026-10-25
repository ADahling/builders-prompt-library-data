---
title: "Database Migration Strategy: Zero-Downtime Patterns"
slug: database-migration-strategy-zero-downtime-patterns
stage: Build
category: "Modern Data Stack"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/database-migration-strategy-zero-downtime-patterns
---
# Database Migration Strategy: Zero-Downtime Patterns

Plan a database migration targeting zero downtime, with schema translation, dual writes, validation, cutover phases, and rollback steps.

## Prompt

Design a zero-downtime database migration strategy for [CURRENT DB] → [TARGET DB].

## 1. Pre-Migration Audit
- Map all tables, columns, types, constraints, indexes
- Document all foreign key relationships
- List all stored procedures, triggers, views
- Identify data volume per table
- Check for: circular references, custom types, generated columns

## 2. Schema Translation
- Map source types to target types (e.g., MySQL ENUM → Postgres ENUM or CHECK)
- Handle auto-increment → serial/identity differences
- Translate indexes (covering, partial, expression-based)
- Convert stored procedures to target syntax or edge functions

## 3. Data Migration Plan
```
Phase 1: Schema creation (empty tables in target)
Phase 2: Historical data migration (batch insert)
Phase 3: Dual-write period (write to both DBs)
Phase 4: Verification (row counts, checksums, spot checks)
Phase 5: Cutover (switch reads to target)
Phase 6: Decommission source (after confidence period)
```

## 4. Dual-Write Implementation
- Application-level: Write to both databases in transaction
- CDC-based: Use change data capture (Debezium, pg_logical)
- Proxy-based: Database proxy that mirrors writes

## 5. Rollback Plan
- Keep source database running for [X days] after cutover
- Feature flag to switch traffic back
- Data sync from target back to source if needed

## 6. Validation Queries
- Row count comparison per table
- Checksum comparison for critical tables
- Application-level smoke tests
- Performance benchmarks (query latency, throughput)

Apply this to: [DESCRIBE YOUR SPECIFIC MIGRATION]

## Tips

Never migrate a production database without a rollback plan. The dual-write pattern is your safety net.
