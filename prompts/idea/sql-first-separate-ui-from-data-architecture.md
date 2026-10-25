---
title: "SQL FIRST \u2014 Separate UI from Data Architecture"
slug: sql-first-separate-ui-from-data-architecture
stage: Idea
category: "Prompt Engineering"
grade: C
score: 69
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/sql-first-separate-ui-from-data-architecture
---
# SQL FIRST — Separate UI from Data Architecture

Get SQL for a feature's table, including fields, defaults, RLS policies, foreign keys, indexes, and needed triggers before frontend work.

## Prompt

Mock the UI for now, but write me the exact SQL for a table that handles [specific feature]. Include:
- All necessary fields with correct types and defaults
- Row Level Security policies (SELECT, INSERT, UPDATE, DELETE)
- Foreign key relationships
- Indexes for frequently queried columns
- Trigger functions if needed

Don't touch the frontend until the data layer is solid.

## Tips

Schema first, UI second. Most vibe coding bugs are data model bugs. Source: reddit.com/r/lovable
