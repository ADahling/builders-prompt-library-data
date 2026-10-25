---
title: "Generate RLS Policies for All Tables"
slug: generate-rls-policies-for-all-tables
stage: Build
category: "Database & Supabase"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-rls-policies-for-all-tables
---
# Generate RLS Policies for All Tables

Get commented SQL for Supabase RLS across your tables, with user-owned row access, admin overrides, and public reads where appropriate.

## Prompt

Here are my Supabase tables: [list table names and columns, especially user_id]. Generate RLS policies for every table:

1. Enable RLS statement.
2. SELECT: Users read only their own rows (user_id = auth.uid()).
3. INSERT: Users insert only with their own user_id.
4. UPDATE: Users update only their own rows.
5. DELETE: Users delete only their own rows (or soft delete).
6. Admin override: Admins read/write all rows.
7. Public tables: Public SELECT where appropriate.

Write complete SQL with comments. Paste into Supabase SQL editor.

## Tips

Single most important security step.
