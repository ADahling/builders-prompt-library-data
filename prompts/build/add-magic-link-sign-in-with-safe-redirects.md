---
title: "Add magic link sign-in with safe redirects"
slug: add-magic-link-sign-in-with-safe-redirects
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/add-magic-link-sign-in-with-safe-redirects
---
# Add magic link sign-in with safe redirects

Build Supabase magic link sign-in with request throttling, safe callback handling, redirect validation, and clear recovery states.

Variables: app_code, auth_configuration, sign_in_requirements

## Prompt

You are a Supabase authentication engineer implementing passwordless email sign-in.

Context:
- App code and dependencies: {{app_code}}
- Auth settings, email templates, and deployment URLs: {{auth_configuration}}
- Sign-in requirements and destination rules: {{sign_in_requirements}}

Your task is to implement magic link sign-in with safe redirects and recovery states.

Steps:
1. Trace the auth flow. Choose PKCE code exchange or token_hash verification from the supplied setup. Align templates and routes; make shouldCreateUser explicit.
2. Build the email form with validation, pending state, resend cooldown, and generic confirmation that does not reveal account existence. Call signInWithOtp with a trusted emailRedirectTo.
3. Enforce server-side limits per email and trusted client IP, plus Supabase Auth limits. Block direct API bypass of app limits. Use an atomic shared counter, not process memory; for PostgreSQL use INSERT ON CONFLICT with RETURNING. Handle 429 and Retry-After.
4. Configure exact Supabase redirect allowlist entries. Parse and validate return paths against the trusted origin; reject external URLs, protocol-relative URLs, backslashes, and encoded bypasses. Persist only validated destinations. Never trust Host headers; default to a safe page.
5. Implement the callback using exchangeCodeForSession or verifyOtp, not both. Persist sessions with the framework's cookie integration before redirecting. Handle expired or reused links, missing parameters, provider errors, scanner prefetch, and PKCE opened on another device. Provide resend recovery without loops.
6. Add checks for valid sign-in, hostile redirects, concurrent throttling, and each failure case. Flag unverified settings and behavior; list deployment and verification next steps.

Constraints:
- Do not invent project facts. List assumptions.
- Keep service role keys server-only. Never log tokens or callback query strings.
- Do not weaken RLS or accept a destination as proof of authorization.
- Separate proposed checks from checks actually run.

Output format, in Markdown: Assumptions first, then Implementation with file paths and code blocks, Configuration, Checks as a table with columns case, expected result, verification status, then Unverified items and next steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste the form, routes, session middleware, and Supabase client setup. Include redirect settings and email templates, but remove secrets.
