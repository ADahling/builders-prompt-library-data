---
title: "Design account deletion that removes personal data"
slug: design-account-deletion-that-removes-personal-data
stage: Secure
category: "Security Checklist"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-account-deletion-that-removes-personal-data
---
# Design account deletion that removes personal data

Design a secure account deletion workflow with a data inventory, retention rules, ordered cleanup, and clear completion notices.

Variables: schema_and_storage, account_deletion_code, retention_requirements

## Prompt

You are a security engineer designing account deletion.

Context:
- Schema, storage paths, and data services: {{schema_and_storage}}
- Account, authentication, and deletion code: {{account_deletion_code}}
- Retention rules and product requirements: {{retention_requirements}}

Your task is to design server side account deletion that removes personal data and preserves only justified records.

Steps:
1. Trace account IDs and indirect joins across tables, object keys, logs, caches, backups, and vendors. Mark unknown coverage and shared ownership.
2. Assign delete, anonymize, or retain to each location. Specify fields, reason, and retention expiry. Minimize financial records; flag missing legal rules. Check that anonymized data cannot be relinked through identifiers or free text.
3. Secure the endpoint with recent authentication and server derived identity. Reject cross account requests. Check CSRF where applicable, revoke sessions, and block new writes during deletion.
4. Order operations using foreign keys, ON DELETE CASCADE, RESTRICT, and triggers. Give SQL for database changes in a transaction. Use a transactional outbox for storage and vendor cleanup, with idempotent jobs, retries, and reconciliation. Delay identity removal until required cleanup references are captured.
5. Handle duplicate requests, concurrent writes, shared files, partial failures, orphaned objects, legal holds, and backup restores. Add scoped SQL counts, storage checks, and negative authorization tests. Prevent restored backups from reviving erased data.
6. Separate acceptance from verified completion. Draft notices covering retained records and pending expiry. Keep minimal audit evidence without erased data. Flag what cannot be verified and list next steps.

Constraints:
- Do not invent project facts or legal duties. List assumptions.
- Match the supplied SQL dialect; label missing schema details.
- Never trust a client supplied account ID as authorization.
- Do not claim storage cleanup is atomic with SQL or promise instant backup erasure.

Output format, in Markdown: Assumptions first; Inventory table with columns location, linkage, action, reason, expiry; Ordered workflow with SQL and worker pseudocode blocks; Checks table with columns failure mode, check, expected result; User notices; Unverified items and next steps.

Implementation acceptance requirements:
- Derive ownership from the supplied relationships; membership alone never makes a workspace or its files private, and preserve other members' shared content.
- Show each actual foreign-key action and trigger from the supplied schema; do not assume cascades or cleanup that does not exist.
- Capture the correct account ID, storage keys, vendor IDs, and cleanup scope durably before removing their source records; cleanup jobs must remain recoverable after account deletion.
- Check legal holds before scheduling and again before destructive work; explain how concurrent hold changes and deletion are serialized, and keep held work pending rather than marking it erased.
- Specify immediate read and write denial across authenticated routes, existing sessions, and background jobs; show a locking or guarded-transaction protocol shared by deletion and concurrent writers rather than relying on a status flag alone.
- Give explicit job states, retry and abandoned-lease recovery, idempotency keys, and a finalizer that performs and verifies its remaining purge before recording completion.
- Design a minimal durable erasure ledger and restore-replay gate that survives account deletion and prevents restored data from becoming accessible before erasure is reapplied.
- For each completion claim, show the verification query or external confirmation required; pending vendor work, retained records, unverified backups, and unresolved legal rules must remain clearly labeled and must not be described as completed erasure.


## Tips

Paste your schema, bucket paths, identity provider details, and current account deletion code. Include financial retention rules and known backup or vendor limits.
