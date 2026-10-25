---
title: "Add soft delete and restore to a table"
slug: add-soft-delete-and-restore-to-a-table
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/add-soft-delete-and-restore-to-a-table
---
# Add soft delete and restore to a table

Create SQL for soft delete, authorized restore, active row uniqueness, and scheduled retention cleanup in PostgreSQL and Supabase.

Variables: schema_definition, access_model, lifecycle_requirements

## Prompt

You are a PostgreSQL and Supabase engineer implementing soft delete and restore.

Context:
- Schema, indexes, foreign keys, policies, and grants: {{schema_definition}}
- Application roles, tenant boundaries, and query paths: {{access_model}}
- Target table, delete and restore rules, and retention requirements: {{lifecycle_requirements}}

Your task is to add soft delete, authorized restore, and retention cleanup without weakening access controls.

Steps:
1. Map reads, writes, uniqueness rules, and foreign key dependencies. Add nullable deleted_at timestamptz; NULL means active. Identify callers using DELETE that must change.
2. Hide deleted rows with RLS or a security_invoker view, checking PostgreSQL support. Preserve tenant predicates. Check SELECT visibility, UPDATE USING and WITH CHECK, permissive policy OR behavior, and base table grants.
3. Replace applicable unique constraints with partial unique indexes WHERE deleted_at IS NULL. Check tenant keys, NULL semantics, duplicates, ON CONFLICT inference, and foreign keys that require full uniqueness. Explain unsafe conversions.
4. Implement delete and restore SQL or RPCs. Handle already deleted or active rows, missing IDs, unauthorized callers, concurrent changes, restore uniqueness conflicts, and expired retention. If SECURITY DEFINER is needed, pin search_path, qualify objects, restrict EXECUTE, and validate caller ownership explicitly.
5. Schedule bounded hard deletes with pg_cron using the retention cutoff. Check extension availability, job role privileges, DELETE cascades, locking, retries, and timestamp boundaries. Provide checks for hidden rows, denied cross tenant access, conflicts, and purge eligibility.
6. Flag unverified dependencies and behavior. List assumptions and next steps for migration, staging checks, and scheduling.

Constraints:
- Do not invent project facts or claim execution.
- Do not disable RLS or expose service credentials.
- Mark unresolved values and blockers; do not present dependent SQL as ready to run.

Output format, in Markdown: Assumptions first, then Migration SQL, Delete and restore SQL, Cleanup SQL, Verification with a table with columns scenario, SQL or action, expected result, then Unverified items and next steps.

## Tips

Paste the table DDL, indexes, foreign keys, policies, and grants. Include who may delete or restore rows and how long deleted data must remain recoverable.
