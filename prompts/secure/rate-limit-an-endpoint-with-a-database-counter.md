---
title: "Rate limit an endpoint with a database counter"
slug: rate-limit-an-endpoint-with-a-database-counter
stage: Secure
category: "Security Checklist"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/rate-limit-an-endpoint-with-a-database-counter
---
# Rate limit an endpoint with a database counter

Build a Postgres backed endpoint rate limiter with atomic counters, private storage, retry responses, cleanup SQL, and security checks.

Variables: schema_definition, endpoint_code, rate_limit_requirements

## Prompt

You are a security engineer implementing Postgres endpoint rate limits.

Context:
- Schema, functions, and database grants: {{schema_definition}}
- Endpoint code and deployment details: {{endpoint_code}}
- Limits, identity rules, and outage requirements: {{rate_limit_requirements}}

Your task is to protect the public endpoint with a private database counter and clear retry responses.

Steps:
1. Select a fixed or sliding window from the requirements. Define scope, duration, limit, and boundary behavior. Explain fixed window bursts or sliding window approximation.
2. Derive keys from verified user IDs or server keyed IP hashes. Trust forwarded IPs only from configured proxies. Define endpoint scope, IPv6 normalization, and shared IP tradeoffs.
3. Write migration SQL and an atomic upsert function using INSERT ... ON CONFLICT DO UPDATE ... RETURNING. Add a unique key for scope, identity, and window. Use database time and qualify names. For sliding windows, serialize competing updates per key and explain correctness. Return allowed, remaining, and retry seconds without a read then write race.
4. Deny client table access with REVOKE and RLS without client policies. Revoke function EXECUTE from PUBLIC and client roles; grant only the trusted server role. If SECURITY DEFINER is needed, pin search_path and use a restricted owner. Call before protected work; return HTTP 429 with Retry-After seconds and a clear body.
5. Handle concurrent requests, exact boundaries, spoofed keys, hot rows, retries, clock shifts, and database outages. State fail open or fail closed behavior. Provide concurrency checks and indexed, bounded cleanup SQL that retains all windows needed for decisions.
6. Flag what cannot be verified from the inputs. List assumptions, expected check results, and next steps for deployment and scheduling cleanup.

Constraints:
- Do not invent project facts or claim checks ran.
- Keep credentials and hash secrets server side.
- Supply runnable SQL and integration code; label missing configuration.
- Never expose counter mutation directly to public clients.

Output format, in Markdown: Design and assumptions, SQL code blocks, Endpoint code, Checks table with columns case, procedure, expected result, then Unverified items and next steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste the endpoint handler, database roles and grants, and any existing counter schema. Include allowed request rates, identity sources, and outage behavior.
