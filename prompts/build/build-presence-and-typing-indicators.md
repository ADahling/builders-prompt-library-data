---
title: "Build presence and typing indicators"
slug: build-presence-and-typing-indicators
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-presence-and-typing-indicators
---
# Build presence and typing indicators

Build room scoped online and typing indicators with Supabase Realtime, membership checks, event throttling, and cleanup.

Variables: app_code, schema_and_policies, room_requirements

## Prompt

You are a Supabase engineer building secure presence and typing indicators.

Context:
- Client setup, dependencies, and room UI code: {{app_code}}
- Room schema, membership rules, grants, and RLS policies: {{schema_and_policies}}
- Access rules and online and typing behavior: {{room_requirements}}

Your task is to implement room scoped presence and typing with authorized Realtime channels.

Steps:
1. Define a canonical room topic and payload shapes. Use private channels with presence and broadcast. Derive identity from the authenticated session, not editable profile fields.
2. Add SQL policies on realtime.messages using auth.uid(), realtime.topic(), and membership EXISTS checks. Cover SELECT and INSERT for required presence and broadcast extensions. Check grants, existing permissive policies, and public channel access. Do not treat channel names or client checks as authorization.
3. Track presence after SUBSCRIBED. Reconcile presenceState() on sync; use join and leave for updates. Deduplicate users across tabs without dropping other active sessions. Render an empty room state.
4. Send throttled typing broadcasts with bounded payloads. Clear typing after an idle timeout, send, or blur. Expire remote typing locally if a stop event is lost. Clear timers, untrack, and remove channels on room change or unmount.
5. Handle abrupt disconnects, reconnects, duplicate listeners, stale events, token expiry, rejected subscriptions, and membership revocation. Explain revocation limits for open channels and sender spoofing risks. Add checks for two users, two tabs, room switching, and unauthorized joins.
6. List assumptions and anything not verifiable from the inputs. Give next steps for migrations, authorization checks, and client validation; distinguish proposed checks from executed checks.

Constraints:
- Do not invent project facts or claim unrun tests passed.
- Keep transient typing out of database rows. Never expose a service role key.
- Match supplied APIs and schema; mark missing details instead of guessing identifiers.

Output format, in Markdown: Design and assumptions first, then SQL migration and Client changes in code blocks, then Checks as a table with columns scenario, action, expected result, then Unverified items and next steps.

## Tips

Paste your Supabase client setup, room component, membership schema, and existing policies. Include expected behavior for multiple tabs and membership removal.
