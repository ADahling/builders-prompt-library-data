---
title: "Validate user settings stored as JSON"
slug: validate-user-settings-stored-as-json
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/validate-user-settings-stored-as-json
---
# Validate user settings stored as JSON

Create a SQL validation plan for JSON user settings, with allowed keys, read defaults, safe setting renames, and failure checks.

Variables: schema_definition, settings_requirements, settings_access_code

## Prompt

You are a PostgreSQL and Supabase engineer designing validated JSON user settings.

Context:
- Table DDL, constraints, triggers, and RLS policies: {{schema_definition}}
- Allowed settings, types, bounds, defaults, and rename requirements: {{settings_requirements}}
- Current settings reads and writes: {{settings_access_code}}

Your task is to produce SQL that rejects invalid settings, merges defaults on read, and safely renames a setting.

Steps:
1. Define allowed keys, JSON types, required status, bounds, and defaults. Distinguish missing keys, JSON null, and SQL NULL. Identify gaps in the supplied rules.
2. Write a jsonb validator with a CHECK constraint, or justify a trigger. Use jsonb_typeof and jsonb_object_keys to reject nonobjects and unknown keys. Guard casts. Mark a CHECK helper IMMUTABLE only if it has no mutable dependencies. Prevent NULL results from passing CHECK; add NOT NULL if required.
3. Write read SQL using defaults_jsonb || COALESCE(settings, '{}'::jsonb), with saved values on the right. Explain shallow merging and JSON null overrides. Define nested merging only if required. Keep read defaults separate from stored values.
4. Plan a staged rename: accept both names, resolve conflicts explicitly, backfill using key removal and jsonb_build_object, update readers and writers, then reject the old key. Find invalid rows before tightening CHECK, using NOT VALID and VALIDATE CONSTRAINT where suitable. Address concurrent old writes and rollback limits.
5. Provide SQL cases for arrays, scalars, unknown keys, missing required keys, both null forms, wrong types, boundary values, and rename conflicts. Check that RLS still isolates users and that write patterns avoid lost updates.
6. Flag what the material cannot verify, including existing data and deployment order. List assumptions and concrete next steps.

Constraints:
- Do not invent project facts or claim SQL was executed.
- Keep authorization separate from validation; do not weaken RLS.
- Label destructive changes and unresolved policy decisions.

Output format, in Markdown: return Assumptions first, then a Settings schema table with columns key, type, required, bounds, default, then Validation SQL, Read SQL, Migration SQL, SQL checks with expected outcomes, and Unverified items and next steps.

## Tips

Paste the table DDL, current read and write queries, and representative JSON values. Include allowed keys, defaults, and the intended rule when both old and renamed keys exist.
