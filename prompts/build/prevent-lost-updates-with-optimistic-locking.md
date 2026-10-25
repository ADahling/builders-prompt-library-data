---
title: "Prevent lost updates with optimistic locking"
slug: prevent-lost-updates-with-optimistic-locking
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/prevent-lost-updates-with-optimistic-locking
---
# Prevent lost updates with optimistic locking

Add optimistic locking with version checked writes, clear conflict messages, and a two session test plan to prevent lost edits.

Variables: schema_definition, write_path_code, edit_requirements

## Prompt

You are a backend engineer preventing lost updates with optimistic locking.

Context:
- Database engine, version, and schema: {{schema_definition}}
- Read handlers, write handlers, and edit form code: {{write_path_code}}
- Access rules and edit requirements: {{edit_requirements}}

Your task is to add version checked writes and a clear conflict flow without silently overwriting newer edits.

Steps:
1. Trace reads and every write path, including jobs and bulk updates. Identify keys, access predicates, transaction boundaries, and how the form retains the version it loaded.
2. Add an integer version column. Provide dialect appropriate SQL to backfill existing rows, set DEFAULT 1 and NOT NULL, and deploy without leaving old writers unguarded.
3. Replace read then write checks with one atomic UPDATE. Match the key, access scope, and expected version in WHERE; set edited fields and version = version + 1. Use RETURNING or the driver's matched row count to detect success. Return the new version.
4. Handle stale versions, missing rows, revoked access, invalid version tokens, and isolation errors. On a stale write, return HTTP 409 or the transport equivalent with authorized current values and their version. Preserve local edits; offer reload or explicit reconciliation. Never retry by blindly applying edits with a fresh version.
5. Write a two session race test: both read version N; A saves and commits; B saves with N and must conflict without altering A's data. Check stored values and version N+1. Test a reconciled save, deletion, and access loss. Give commands and expected results; account for locks and isolation errors.
6. Flag anything not verifiable from the supplied material. List assumptions and concrete next steps for rollout and test execution.

Constraints:
- Do not invent project facts or claim unrun tests passed.
- Keep authorization in both writes and conflict reads.
- Use the supplied stack; label any required placeholders.

Output format, in Markdown: return Assumptions, Write path review, Migration SQL in a sql block, Backend and UI changes in code blocks, Two session tests with commands and expected results, then Unverified items and next steps.

## Tips

Paste your table schema, read and update handlers, and edit form code. Include the database engine and version, access rules, and conflict behavior you need.
