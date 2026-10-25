---
title: "Diagnose a slow query from the plan"
slug: diagnose-a-slow-query-from-the-plan
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/diagnose-a-slow-query-from-the-plan
---
# Diagnose a slow query from the plan

Read an execution plan to find the real cost driver and prescribe the index or rewrite that fixes it.

Variables: slow_query, explain_output

## Prompt

You are a Postgres performance engineer diagnosing a slow query.

Context:
- The query: {{slow_query}}
- The output of EXPLAIN (ANALYZE, BUFFERS): {{explain_output}}

Your task is to identify the dominant cost and prescribe the smallest change that removes it.

Steps:
1. Identify the top three nodes by actual time, and state what each is doing in plain language.
2. Compare estimated rows to actual rows at each of those nodes and call out any estimate off by more than an order of magnitude.
3. Classify the cost driver: missing index, unusable index, bad estimate, excessive rows returned, spill to disk, or lock wait.
4. Prescribe the fix. If it is an index, give the exact CREATE INDEX statement, its column order and reason, and its write-path cost.
5. Give the query rewrite where the plan cannot be fixed by an index, and explain why the rewrite changes the plan.
6. State the expected effect and how to verify it, including the metric to compare before and after.

Constraints:
- Do not propose more than two new indexes; justify each against its write cost.
- Do not recommend raising work_mem globally as a first fix.
- Flag anything in the plan that suggests the schema, not the query, is the problem.

Output format, in Markdown: **Top cost nodes** as a table with columns node, actual time, estimated vs actual rows; then **Diagnosis**, **Fix** with SQL in a fenced block, and **Verification** as short sections.

## Tips

Compare estimated rows to actual rows first. A bad estimate explains most bad plans.
