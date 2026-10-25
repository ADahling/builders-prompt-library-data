---
title: "Back up data before a risky migration"
slug: back-up-data-before-a-risky-migration
stage: Ship
category: "Deployment & Launch"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/back-up-data-before-a-risky-migration
---
# Back up data before a risky migration

Create a PostgreSQL migration runbook with durable row backups, count and checksum checks, a transaction dry run, and exact restore SQL.

Variables: schema_definition, migration_sql, deployment_requirements

## Prompt

You are a PostgreSQL engineer planning reversible migrations.

Context:
- Schema, keys, dependencies, and grants: {{schema_definition}}
- Proposed schema and data changes: {{migration_sql}}
- PostgreSQL version, access, maintenance window, and recovery requirements: {{deployment_requirements}}

Your task is to write a backup, rehearsal, migration, and restore runbook before any change starts.

Steps:
1. Map affected rows, dependent objects, cascades, and inserted keys. Define backup predicates, stable keys, and success checks. Flag statements such as CREATE INDEX CONCURRENTLY that cannot run inside a transaction.
2. Quiesce writers through final verification. Create durable backup tables with CREATE TABLE AS SELECT in a separate committed transaction. Include cascade targets, restrict backup grants, and record sequence state and original DDL separately.
3. Verify source and backup counts and deterministic content checksums using explicit columns and stable key ordering. Supply SQL that raises an exception on mismatch. Define lock_timeout, statement_timeout, and storage checks.
4. Write restore SQL before execution. Reverse DDL as needed, delete only migration-created rows, and restore updated or deleted rows by key. Order operations around foreign keys. Restore sequence state safely. Require count and checksum checks against backups before COMMIT.
5. Rehearse with BEGIN, the migration, assertions, and ROLLBACK; then repeat with COMMIT only after checks pass. Handle NULLs, duplicate or missing keys, triggers, identity/generated columns, foreign keys, lock waits, concurrent writes, and interrupted sessions. Flag sequence changes and external effects that ROLLBACK cannot undo.
6. List assumptions, unverified behavior, and next steps, including a restore rehearsal and approval gates. Define backup retention and cleanup only after acceptance.

Constraints:
- Do not invent project facts or claim SQL was executed.
- Stop if backup scope or safe restore keys cannot be established.
- Keep committed backups outside migration rollback scope.
- Label SQL requiring missing inputs; never present it as ready to run.

Output format, in Markdown: Scope and assumptions first, then a risk table with columns object, failure mode, safeguard, then ordered SQL blocks for Backup and verification, Restore, Dry run, and Apply, then Unverified items and next steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste the full migration and definitions for affected tables, indexes, triggers, and foreign keys. Include the PostgreSQL version, maintenance window, and recovery requirements.
