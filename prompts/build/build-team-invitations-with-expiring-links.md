---
title: "Build team invitations with expiring invite links"
slug: build-team-invitations-with-expiring-links
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-team-invitations-with-expiring-links
---
# Build team invitations with expiring invite links

Build a Supabase invitation schema and acceptance flow with hashed tokens, expiry, email checks, role controls, and revocation.

Variables: schema_definition, access_rules, invitation_requirements

## Prompt

You are a senior Supabase engineer designing secure workspace invitations.

Context:
- Existing schema, functions, and policies: {{schema_definition}}
- Workspace roles and authorization rules: {{access_rules}}
- Invitation and email delivery requirements: {{invitation_requirements}}

Your task is to design the invitation schema, SQL, and flow from issuance to acceptance.

Steps:
1. Define invitations with workspace, normalized email, granted role, unique token hash, inviter, expiry, and acceptance and revocation timestamps. Add foreign keys, CHECK constraints, indexes, and membership uniqueness.
2. Generate tokens with at least 32 random bytes using pgcrypto or a secure server generator. Store only a SHA-256 hash. Explain expiry, email delivery, and keeping raw tokens out of logs, analytics, and browser referrers.
3. Write issuance, re-invite, and revoke operations. Check workspace authority and allowed role grants. Rotate tokens on re-invite and serialize changes with acceptance so old tokens cannot succeed after revocation commits.
4. Write an atomic acceptance RPC using auth.uid(), a row lock, and server time. Match the invite email against the current confirmed email in auth.users, never a client argument or editable metadata. Validate token, expiry, role, and unused status; insert membership and consume the invite in one transaction.
5. Add RLS and least privilege grants. Pin SECURITY DEFINER search_path and qualify objects; restrict EXECUTE. Handle concurrent acceptance, replay, expired or revoked tokens, email mismatch or changes, existing members without role escalation, deleted workspaces, and failed delivery. Give SQL checks and expected outcomes.
6. Flag unverifiable behavior and missing inputs. List assumptions and next steps for migrations, authorization tests, and delivery checks.

Constraints:
- Do not invent project facts; label assumptions.
- Deny direct client invite writes and token hash reads.
- Do not consume invites on GET requests or link previews.
- Keep membership creation and invite consumption atomic; roll back both on failure.

Output format, in Markdown: Assumptions first, then Schema and SQL in sql code blocks, Flow, Checks as a table with columns case, action, expected result, then Unverified items and next steps.

## Tips

Paste your workspace and membership schema, existing policies, and allowed roles. Include how users verify emails and how invitation emails are sent.
