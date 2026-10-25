---
title: "Model a credits ledger with balance checks"
slug: model-a-credits-ledger-with-balance-checks
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/model-a-credits-ledger-with-balance-checks
---
# Model a credits ledger with balance checks

Build an append only credits ledger with atomic spending, balance views, safe refunds, and reconciliation SQL for concurrent usage.

Variables: schema_definition, credit_requirements, database_environment

## Prompt

You are a database engineer designing a credits ledger.

Context:
- Existing schema and grants: {{schema_definition}}
- Credit, refund, and access requirements: {{credit_requirements}}
- Database engine, version, and transaction settings: {{database_environment}}

Your task is to build an append-only credits ledger with atomic spending, balance views, refunds, and reconciliation SQL.

Steps:
1. Map account ownership and credit units. Define grant, spend, and refund entries, signed amounts, immutable IDs, timestamps, refund references, and scoped idempotency keys. Use integer units or exact numeric types, foreign keys, CHECK constraints, and UNIQUE constraints.
2. Write DDL and indexes. Deny client INSERT, UPDATE, DELETE, and TRUNCATE; expose authorized write functions. If using SECURITY DEFINER, pin search_path and restrict EXECUTE. Enforce tenant ownership inside functions.
3. Implement atomic spending. Lock a stable account row with SELECT FOR UPDATE, then read SUM(amount) in a fresh statement snapshot before inserting. Require every writer to take that lock. Specify supported isolation levels and retry handling for serialization failures and deadlocks; never rely on an unlocked balance check.
4. Implement grants, refunds, and idempotent retries. Handle missing accounts, empty ledgers, zero or negative requests, overflow, insufficient funds, duplicate keys with changed payloads, cross-account refunds, and concurrent partial refunds exceeding the original spend. Lock refund targets consistently.
5. Return balance views using COALESCE and reconciliation queries for negative balances, invalid refund totals, and duplicate business events. Explain which discrepancies require external usage records. Supply two-session race scripts with expected outcomes for competing spends and refunds.
6. List assumptions, unverifiable behavior, and next steps for migration, permissions review, and execution of concurrency checks.

Constraints:
- Do not invent project facts or claim checks were executed.
- Use supplied SQL dialect; label missing prerequisites.
- Keep ledger entries immutable. Correct errors with compensating entries.

Output format, in Markdown: Assumptions first, then Ledger SQL, Write Functions, Balance and Reconciliation SQL, Race Checks with SQL code blocks, then Unverified Items and Next Steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste your account schema, credit rules, and database version. Include retry behavior, tenant boundaries, and whether refunds can be partial.
