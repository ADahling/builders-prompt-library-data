---
title: "Sync subscriptions from payment webhooks safely"
slug: sync-subscriptions-from-payment-webhooks
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/sync-subscriptions-from-payment-webhooks
---
# Sync subscriptions from payment webhooks safely

Build a safe subscription webhook flow with signature checks, idempotent writes, ordering safeguards, and client read access.

Variables: webhook_code, database_schema, integration_requirements

## Prompt

You are a backend engineer reviewing payment webhook integrity.

Context:
- Handler code and provider event examples: {{webhook_code}}
- Database schema, policies, and grants: {{database_schema}}
- Provider, API version, and subscription access rules: {{integration_requirements}}

Your task is to design safe webhook processing and app access to subscription status.

Steps:
1. Verify signatures with the provider SDK against raw request bytes before parsing. Check timestamp tolerance, secret rotation, and rejection paths. Keep secrets and payment data out of logs.
2. Design a durable inbox with a UNIQUE key scoped by provider, account, and event ID. Use INSERT ON CONFLICT or the supplied SQL dialect's equivalent. Return success only after durable acceptance; retry unfinished events, not just unseen IDs.
3. Map event types and trusted customer IDs to subscriptions. Specify status, plan, billing period, and cancellation updates. Reject client-controlled ownership mappings. Define entitlement rules from the supplied requirements.
4. Handle duplicates, concurrent workers, out-of-order events, missing mappings, invalid payloads, and crashes. Lock subscription rows with SELECT FOR UPDATE. Commit updates and the processed marker together. Do not treat event timestamps as a total order; use supported revisions or serialized authoritative reconciliation. Define retry and dead letter handling.
5. Expose status through an authenticated endpoint or owner-scoped SELECT policy. Deny client INSERT, UPDATE, and DELETE through grants and RLS where supported. Keep webhook credentials server-only. Add checks for forged signatures, duplicate delivery, reversed order, crash recovery, and unauthorized reads and writes.
6. Flag anything not verifiable from the material. List assumptions and next steps for provider checks, migrations, and reconciliation tests.

Constraints:
- Do not invent project facts or provider guarantees.
- Use the supplied SQL dialect and runtime; label missing prerequisites.
- Do not grant access from redirect parameters or client-submitted plan status.

Output format, in Markdown: Design first, then an Event mapping table with columns event, trusted key, update, ordering rule, then SQL and handler code blocks, Verification checks, and Assumptions and next steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste the handler, schema, grants, and provider event examples with secrets removed. Include the provider API version and rules for trials, failed payments, and cancellations.
