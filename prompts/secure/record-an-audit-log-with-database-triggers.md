---
title: "Record an audit log with database triggers"
slug: record-an-audit-log-with-database-triggers
stage: Secure
category: "Security Review"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/record-an-audit-log-with-database-triggers
---
# Record an audit log with database triggers

Design a trigger based audit log that records row changes and trusted actor IDs, with SQL access rules that protect history.

Variables: schema_definition, identity_flow, audit_requirements

## Prompt

You are a database security engineer designing trigger based audit logging.

Context:
- Database version, schema, roles, and grants: {{schema_definition}}
- Authentication and database identity flow: {{identity_flow}}
- Sensitive tables, redaction, readers, and retention rules: {{audit_requirements}}

Your task is to capture who changed what and when, while preventing clients from altering audit history.

Steps:
1. Map audited tables, primary keys, owners, client roles, and allowed readers. Assume PostgreSQL only if the engine is unspecified; list missing details.
2. Design a separate audit schema and table with event id, table identity, row key, operation, timestamptz, actor id, database session identity, and old/new JSONB. Define NULL behavior for INSERT and DELETE, and redact secrets before storage.
3. Trace actor identity through pooled connections. Distinguish session_user from current_user under SECURITY DEFINER. Reject client writable identity settings as proof; document missing trusted identity plumbing and service actor handling.
4. Write an AFTER INSERT OR UPDATE OR DELETE FOR EACH ROW trigger function using TG_OP, TG_TABLE_SCHEMA, TG_TABLE_NAME, OLD, and NEW. Choose and explain clock_timestamp() versus transaction_timestamp(). Fail the write if logging fails. Cover composite keys and no-op updates.
5. Use a dedicated owner and SECURITY DEFINER with a safe fixed search_path and qualified objects. Revoke client and PUBLIC mutation privileges on history, including TRUNCATE. Restrict schema CREATE and function EXECUTE; prevent clients owning audited tables or disabling triggers. Grant only required history reads; use RLS if readers need row scoping.
6. Provide SQL checks for each operation, spoofed actors, pooled identity leakage, denied history edits, TRUNCATE, and rollback. Explain transaction rollback removes audit rows and owners or superusers can bypass controls.

Constraints:
- Do not invent project facts. List assumptions and unresolved blockers.
- Return runnable PostgreSQL SQL where inputs suffice; mark blocked parts instead of fabricating identity logic.
- Do not claim tamper proof history or completed tests.

Output format, in Markdown: Assumptions and blockers, Coverage table, Migration SQL code block, Verification SQL code block with expected results, and Residual risks.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste table definitions, ownership, grants, and the code that sets database identity. Include sensitive fields that must be redacted and who may read audit history.
