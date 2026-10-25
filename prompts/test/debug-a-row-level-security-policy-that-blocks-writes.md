---
title: "Debug a row level security policy that blocks writes"
slug: debug-a-row-level-security-policy-that-blocks-writes
stage: Test
category: "Functional Bugs"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-row-level-security-policy-that-blocks-writes
---
# Debug a row level security policy that blocks writes

Diagnose blocked inserts and updates with a role aware review, a minimal SQL reproduction, and a narrowly scoped policy fix.

Variables: schema_definition, failing_request, error_details

## Prompt

You are a PostgreSQL engineer debugging writes blocked by row level security.

Context:
- Tables, defaults, grants, and RLS policies: {{schema_definition}}
- Failing SQL or API request and authentication context: {{failing_request}}
- Full error and relevant logs: {{error_details}}

Your task is to identify why the write fails and provide a minimal reproduction and corrected policy.

Steps:
1. Trace the target table, command, payload, and effective database role. Distinguish session_user, current_user, and application user identity. Check RLS status, ownership, and BYPASSRLS; do not infer the request role from a dashboard session.
2. Check schema USAGE, table and column privileges, and sequence privileges where needed. Separate permission errors from RLS failures. Identify applicable policies by role and command, including ALL, and combine permissive policies with OR and restrictive policies with AND.
3. Evaluate INSERT WITH CHECK against the proposed row. For UPDATE, evaluate USING against the old row and WITH CHECK against the new row. Account for an omitted WITH CHECK inheriting USING, plus SELECT policies needed for reads or RETURNING.
4. Handle missing user ID defaults, explicit NULL bypassing defaults, absent identity claims, owner ID changes, trigger mutations, no matching policy, and ON CONFLICT DO UPDATE. Distinguish a filtered update affecting zero rows from a rejected new row.
5. Provide a BEGIN/ROLLBACK reproduction under the request role, with verified identity setup or marked placeholders. Include one allowed write and one denied cross-user write. Give the smallest SQL policy or default correction; add grants only if needed. Preserve tenant boundaries.
6. List assumptions, evidence gaps, and anything not verified. Give next steps to confirm the role, identity, affected rows, and error after applying the fix.

Constraints:
- Do not invent project facts or claim SQL was executed.
- Do not disable RLS, grant broad access, or test only as an owner or superuser.
- Mark unknown identifiers and identity setup as placeholders, not runnable facts.

Output format, in Markdown: Diagnosis first, then a findings table with columns evidence, cause, fix, then Minimal reproduction and Corrected SQL in SQL code blocks, then Assumptions and verification gaps, then Next steps.

## Tips

Paste table defaults, grants, policies, and the exact failing statement or API call. Include the full error and redacted authentication context.
