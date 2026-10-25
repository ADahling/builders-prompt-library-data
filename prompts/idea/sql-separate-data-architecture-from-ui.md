---
title: "SQL \u2014 Separate Data Architecture from UI"
slug: sql-separate-data-architecture-from-ui
stage: Idea
category: "Prompt Engineering"
grade: C
score: 68
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/sql-separate-data-architecture-from-ui
---
# SQL — Separate Data Architecture from UI

Get complete migration SQL with tables, constraints, RLS policies, functions, and cascade rules for a feature before approving UI development.

## Prompt

For this feature, handle the data layer FIRST before touching any UI:

1. Write the exact SQL for all tables, columns, types, defaults, and constraints.
2. Write RLS policies for every table (SELECT, INSERT, UPDATE, DELETE) referencing auth.uid().
3. Write any database functions or triggers needed.
4. Define foreign key relationships and cascade rules.
5. Show me the complete migration SQL.

Only AFTER the data architecture is approved should you build the UI. The UI should use mock/placeholder data until we connect it.

Do NOT combine SQL and React code in the same response.

## Tips

From Reddit r/lovable — separating concerns prevents the AI from building UI around wrong data assumptions. Source: reddit.com/r/lovable/comments/1px6vpg
