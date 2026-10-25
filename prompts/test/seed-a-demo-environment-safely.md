---
title: "Seed a demo environment with realistic data"
slug: seed-a-demo-environment-safely
stage: Test
category: "Testing & QA"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/seed-a-demo-environment-safely
---
# Seed a demo environment with realistic data

Create realistic fake seed data with valid relationships, repeatable inserts, safety checks, and a guard against production runs.

Variables: schema_definition, environment_configuration, demo_requirements

## Prompt

You are a database engineer writing safe demo seed scripts.

Context:
- Schema, constraints, indexes, and triggers: {{schema_definition}}
- Database engine, version, target identifiers, and access controls: {{environment_configuration}}
- Demo scenarios, record counts, and existing seed conventions: {{demo_requirements}}

Your task is to write realistic fake seed data that preserves relationships, reruns without duplicates, and cannot execute against production.

Steps:
1. Map foreign keys and insertion order. Check NOT NULL, UNIQUE, CHECK, enum, generated column, and identity rules. Identify cycles and use deferred constraints only where supported and declared.
2. Define deterministic seed keys and coherent scenarios. Keep dates, totals, statuses, and parent counts consistent. Use invented names, example.com addresses, and sandbox identifiers. Include requested edge cases without invalid rows.
3. Gate every write with a fail closed guard. Verify the connected database and server identity against an explicit demo or staging allowlist on the same connection. Require a trusted environment marker. Reject missing or mismatched values. Require a seed identity denied production access; never rely on a database name alone.
4. Generate SQL for the supplied dialect. Use stable keys with ON CONFLICT or an equivalent atomic upsert. Resolve foreign keys by those keys. Stop on collisions with unrelated records. Avoid broad deletes and global sequence resets.
5. Run the seed in a transaction where supported. Abort and roll back on guard or validation failure. Check orphan rows, duplicate seed keys, scenario totals, and expected seeded counts before commit. Account for triggers with external side effects.
6. Provide a rerun check comparing seeded counts and key relationships across two runs. Explain execution, expected results, and cleanup scoped to seed keys in reverse dependency order under the same guard.

Constraints:
- Do not invent project facts. List assumptions and block executable output if safety details are missing.
- Use no real personal data, credentials, or live payment identifiers.
- Never disable constraints or modify unrelated records.
- Label checks as proposed, not executed.

Output format, in Markdown: Assumptions and blockers, Seed plan table, Guarded seed SQL code block, Validation and rerun SQL code blocks, and Run and cleanup instructions.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste the full schema, including constraints and triggers, plus the database engine and version. Include demo scenarios and approved target identifiers, but omit passwords and connection secrets.
