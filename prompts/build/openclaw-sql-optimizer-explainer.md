---
title: "OpenClaw: SQL Optimizer & Explainer"
slug: openclaw-sql-optimizer-explainer
stage: Build
category: "OpenClaw"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-sql-optimizer-explainer
---
# OpenClaw: SQL Optimizer & Explainer

SQL Optimizer & Explainer — OpenClaw Workflow Prompt Trigger Activate when SQL query is pasted or when asked about database performance.

Variables: O(n), O(n log n), O(n²)

## Prompt

# SQL Optimizer & Explainer — OpenClaw Workflow Prompt

## Trigger
Activate when SQL query is pasted or when asked about database performance.

## Analysis Pipeline

### Step 1: Plain English Explanation
Translate the SQL into clear, non-technical language:
"This query finds all users who signed up in the last 30 days, joined with their orders, grouped by country, and sorted by total revenue descending."

### Step 2: Performance Risk Analysis
For tables with 100M+ rows, analyze:
- **Full table scans** — Is there a WHERE clause? Are indexed columns used?
- **Missing indexes** — Which columns in WHERE/JOIN/ORDER BY lack indexes?
- **Unnecessary joins** — Can any JOINs be eliminated or converted to subqueries?
- **SELECT *** — Are all columns needed?
- **N+1 patterns** — Is this query likely called in a loop?
- **Cartesian products** — Any unintended cross joins?

### Step 3: Bottleneck Detection
```
🔍 QUERY ANALYSIS
Estimated complexity: {{O(n), O(n log n), O(n²)}}
Potential bottlenecks:
  1. [HIGH] Full table scan on 'orders' — missing index on created_at
  2. [MED] ORDER BY on non-indexed column — will cause filesort
  3. [LOW] SELECT * fetching 42 columns — only 3 used downstream
```

### Step 4: Optimized Rewrite
Provide the rewritten query with:
- Appropriate indexes suggested (CREATE INDEX statements)
- Query restructured for better execution plan
- Comments explaining each optimization

### Step 5: Index Strategy
```sql
-- Suggested indexes for this query pattern:
CREATE INDEX idx_orders_created_at ON orders(created_at);
CREATE INDEX idx_orders_user_country ON orders(user_id, country);
-- Estimated improvement: ~95% reduction in scan rows
```

## Tips

Triggers on SQL paste. Explains in plain English, analyzes performance for large tables, rewrites with optimizations. From Analytics Vidhya's 20 OpenClaw Prompts.
