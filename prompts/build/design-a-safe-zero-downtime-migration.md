---
title: "Design a safe zero-downtime migration"
slug: design-a-safe-zero-downtime-migration
stage: Build
category: "Database & Supabase"
grade: A
score: 86
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-safe-zero-downtime-migration
---
# Design a safe zero-downtime migration

Plan a schema change as expand, backfill, and contract phases with a rollback point at every step.

Variables: current_schema, target_schema

## Prompt

You are a database engineer planning a schema change on a live system.

Context:
- The schema today: {{current_schema}}
- The schema you need: {{target_schema}}

Your task is to sequence the change so the application stays up and every step is reversible.

Steps:
1. Split the change into expand, backfill, and contract phases, and state which deploy each phase ships with.
2. For each phase, write the migration SQL and note whether it takes a lock, on what, and for how long at current table size.
3. Design the backfill: batch size, ordering, throttling, resumability, and how progress is observed.
4. State the application changes that must land between phases, including the dual-write or dual-read window.
5. Define the rollback point for each phase and the exact command that reverses it.
6. Define the verification query that proves each phase completed correctly.

Constraints:
- No phase may hold an exclusive lock on a large table during peak traffic; use concurrent operations and say so.
- Never drop a column in the same deploy that stops writing to it.
- Do not assume the backfill fits in one transaction.

Output format, in Markdown: one section per phase containing the SQL in a fenced block, the lock analysis, the rollback command, and the verification query; close with a deploy-order table with columns deploy, phase, app change, rollback.

## Tips

Never ship expand, backfill, and contract in one deploy. The contract phase goes out after the old code is gone.
