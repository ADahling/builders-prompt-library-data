---
title: "Generate a Complete Database Schema"
slug: generate-a-complete-database-schema
stage: Build
category: "Database & Supabase"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-complete-database-schema
---
# Generate a Complete Database Schema

Turn a PRD into a Supabase SQL migration with tables, relationships, indexes, RLS policies, timestamps, and appropriate soft deletes.

## Prompt

Based on this PRD: [paste PRD or summary]. Design a complete Supabase (PostgreSQL) schema:

1. Tables: Every table with name, all columns (type, PK, NOT NULL, defaults).
2. Relationships: Foreign keys. One-to-one, one-to-many, many-to-many with junction tables.
3. Indexes: For frequently queried/filtered columns.
4. RLS Policies: For each table, SELECT/INSERT/UPDATE/DELETE policies referencing auth.uid(). Write actual SQL.
5. Enums or Lookup Tables: Fixed value sets.
6. Timestamps: created_at and updated_at on every table.
7. Soft Delete: deleted_at column where appropriate.

Provide the complete SQL migration file for Supabase.

## Tips

Run this SQL in Supabase SQL editor.
