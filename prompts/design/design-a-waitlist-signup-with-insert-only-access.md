---
title: "Design a waitlist signup with insert-only access"
slug: design-a-waitlist-signup-with-insert-only-access
stage: Design
category: "Landing Page & Marketing"
grade: A
score: 88
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-waitlist-signup-with-insert-only-access
---
# Design a waitlist signup with insert-only access

Build a public waitlist signup with insert only access, policy based email checks, private owner access, and spam controls.

Variables: project_stack, existing_schema, signup_requirements

## Prompt

You are a database security engineer building a public waitlist signup.

Context:
- Stack, database version, and form code: {{project_stack}}
- Existing schema, policies, and grants: {{existing_schema}}
- Signup requirements and owner authentication: {{signup_requirements}}

Your task is to design an insert only waitlist with email validation, safe duplicate handling, spam controls, and a private owner view.

Steps:
1. Map the form, API, and database roles. For PostgreSQL, define an id, email, and server assigned created_at. Mark stack assumptions before proposing SQL.
2. Enable RLS. Revoke public SELECT, UPDATE, and DELETE. Grant INSERT only on email to the submitting role. Check inherited grants and existing policies. Add a FOR INSERT WITH CHECK policy using char_length and a bounded email regex; reject nulls, whitespace, and emails over 254 characters. Add matching CHECK constraints for paths that bypass RLS.
3. Define normalization and enforce uniqueness with a unique index on lower(btrim(email)), noting case handling tradeoffs. Handle conflicts without granting read access. Verify privileges needed by ON CONFLICT DO NOTHING. Avoid RETURNING and client calls that fetch inserted rows.
4. Return the same status and message for new and duplicate emails. Keep raw database errors private. Explain how direct database API access can expose uniqueness errors and bypass endpoint controls; close that route if using a protected endpoint.
5. Add server verified CAPTCHA, request size limits, and rate limits before insertion. Do not treat RLS as spam protection. Keep privileged keys off the client and validate requests even when using a role that bypasses RLS.
6. Create an owner only view with explicit grants and owner SELECT policy. Use security_invoker where supported; otherwise explain view owner RLS behavior. Supply checks for valid and invalid inserts, duplicates, blocked reads and mutations, unauthorized view access, and owner access.

Constraints:
- Do not invent project facts. List assumptions and version dependencies.
- Never grant visitors read access to resolve duplicates.
- Provide SQL and integration code, labeling placeholders and checks not run.

Output format, in Markdown: Assumptions, SQL migration, Form and endpoint code, Spam controls, and a Verification table with action and expected result.

## Tips

Paste your database provider, form code, schema, and current grants if available. State how the owner signs in and whether a server endpoint is available.
