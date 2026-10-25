---
title: "Schedule recurring jobs in Postgres"
slug: schedule-recurring-jobs-in-postgres
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/schedule-recurring-jobs-in-postgres
---
# Schedule recurring jobs in Postgres

Create a pg_cron deployment plan with idempotent job SQL, overlap protection, run logging, and alerts for failures or missed runs.

Variables: schema_definition, job_requirements, deployment_details

## Prompt

You are a Postgres engineer planning production jobs with pg_cron.

Context:
- Tables, indexes, and existing functions: {{schema_definition}}
- Cleanup, digest, and retry requirements: {{job_requirements}}
- Hosting, versions, roles, configuration, and monitoring: {{deployment_details}}

Your task is to design recurring jobs with safe execution and detectable failures.

Steps:
1. Map each requested job to its cadence, timezone, batch limit, timeout, and success signal. Check pg_cron availability, worker setup, target database, and execution role permissions.
2. Write job functions. Use bounded cleanup batches and indexed predicates. Deduplicate digests with unique keys and an outbox. Give retries an attempt cap, backoff, and terminal state. Make reruns safe with ON CONFLICT or guarded state transitions.
3. Prevent overlap with pg_try_advisory_xact_lock and stable, distinct job keys. Acquire locks before work and record lock skips. Explain transaction scope and pg_cron's same-job queuing; cover manual calls and duplicate schedules too.
4. Provide deployment SQL using cron.schedule with stable names, plus inspection and cron.unschedule SQL. Check installed-version syntax, timezone behavior, statement_timeout, and least-privilege grants.
5. Handle crashes, partial work, duplicate delivery, empty batches, lock contention, DST, and retry exhaustion. Configure cron.log_run and inspect cron.job_run_details. Log outcomes, duration, and row counts; explain rollback loss of custom failure logs. Define log retention and external alerts for failures, overdue completion, and missed starts, even if pg_cron stops.
6. Supply validation queries and rerun, concurrency, and failure checks. Flag everything not verifiable from the supplied material and list deployment and monitoring next steps.

Constraints:
- Do not invent project facts. List assumptions and mark unresolved SQL placeholders.
- Do not claim checks were executed or promise exactly-once external delivery.
- Keep work bounded and credentials out of SQL and logs.

Output format, in Markdown: Assumptions first, then a Job plan table with columns job, cadence, timezone, batch limit, timeout, success signal; SQL code blocks; a Monitoring table with columns signal, threshold, alert action; Validation checks; Unverified items and next steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste the relevant tables and functions, job timing and retention rules, and hosting details. Include your Postgres and pg_cron versions and available monitoring tools.
