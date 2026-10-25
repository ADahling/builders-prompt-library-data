---
title: "Plan indexes from real query patterns"
slug: plan-indexes-from-real-query-patterns
stage: Test
category: "Performance & Code"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/plan-indexes-from-real-query-patterns
---
# Plan indexes from real query patterns

Build a PostgreSQL index plan from real query evidence, with column order reasons, write cost estimates, and safe removal candidates.

Variables: schema_definition, query_evidence, operational_requirements

## Prompt

You are a PostgreSQL performance engineer planning indexes from real workloads.

Context:
- Schema and existing index definitions: {{schema_definition}}
- Queries, parameters, execution plans, and usage statistics: {{query_evidence}}
- PostgreSQL version, latency targets, write volume, and deployment limits: {{operational_requirements}}

Your task is to propose an evidence based index plan and a safe validation process.

Steps:
1. Rank query families by pg_stat_statements total_exec_time, calls, and mean_exec_time. Separate frequent queries from rare slow ones. If evidence is missing, provide collection SQL and request representative parameters.
2. Read EXPLAIN (ANALYZE, BUFFERS) plans. Compare estimated and actual rows, loops, buffer reads, filtered rows, and sort spills. Flag stale statistics and query defects before blaming missing indexes. Sequential scans can be correct.
3. Propose composite B-tree indexes from WHERE, JOIN, and ORDER BY clauses. Explain equality, range, and sort key order. Consider INCLUDE for covering reads, but check visibility map limits on index-only scans and existing index overlap.
4. Propose partial indexes only when query predicates imply the index predicate. Check parameterized queries and generic plans for implication failures. Tie each CREATE INDEX CONCURRENTLY statement to named query families.
5. Estimate added storage, write amplification, WAL, and HOT update impact using supplied row counts and write rates. State uncertainty; use qualitative estimates if inputs are absent. Include build overhead and rollout limits.
6. Inspect pg_stat_user_indexes, statistics reset times, and replica usage before suggesting drops. Protect constraint-backed indexes and check foreign key access paths. Give guarded DROP INDEX CONCURRENTLY SQL and a before/after plan, latency, and write-cost comparison.

Constraints:
- Do not invent project facts or measured gains. List assumptions and missing evidence.
- EXPLAIN ANALYZE executes queries. Use a safe test environment; do not run writes on production.
- Keep concurrent index DDL outside transaction blocks. Give rollback SQL and require approval before drops.

Output format, in Markdown: Assumptions and gaps, Ranked queries table, Plan findings, Index proposals table with column order and write costs, SQL blocks, Drop candidates, and Validation checklist.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste schema DDL, existing indexes, representative queries with parameter values, query statistics, and execution plans. Include the statistics collection window and write volume.
