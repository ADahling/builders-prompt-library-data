---
title: "Set Up Supabase Edge Functions"
slug: set-up-supabase-edge-functions
stage: Build
category: "Database & Supabase"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-supabase-edge-functions
---
# Set Up Supabase Edge Functions

Get TypeScript/Deno Supabase Edge Function code for sensitive app operations, with JWT auth, validation, CORS, secrets, and frontend callers.

## Prompt

I need Supabase Edge Functions for my [describe app]:

1. For each sensitive operation (payment processing, emails, external APIs with secret keys), write a complete Edge Function in TypeScript/Deno.
2. Each function: validate request, verify JWT auth, perform operation, handle errors, return proper HTTP status codes.
3. CORS headers: not wildcard, specify allowed origins.
4. Secrets: use Deno.env.get() for API keys.
5. Frontend caller: show how to call via supabase.functions.invoke().

Provide complete, deployable code for each function.

## Tips

Never put API keys in frontend code.
