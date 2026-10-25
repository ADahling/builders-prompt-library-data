---
title: "Edge Function Best Practices (Official)"
slug: edge-function-best-practices-official
stage: Build
category: "Database & Supabase"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/edge-function-best-practices-official
---
# Edge Function Best Practices (Official)

Build Supabase Edge Functions in TypeScript with Deno APIs, versioned imports, shared utilities, routing rules, and background tasks.

## Prompt

You're an expert in TypeScript and Deno. Generate high-quality Supabase Edge Functions following these rules:

1. Use Web APIs and Deno core APIs over external deps (fetch over Axios, WebSocket API over node-ws)
2. Shared utilities go in supabase/functions/_shared/ — import via relative path. NO cross-dependencies between functions.
3. External imports must use npm: or jsr: prefix with versions (e.g., npm:express@4.18.2)
4. Use Deno.serve() — NOT the deprecated serve from deno.land/std
5. Node built-ins use node: prefix (e.g., import process from "node:process")
6. Pre-populated env vars (no manual setup needed): SUPABASE_URL, SUPABASE_ANON_KEY, SUPABASE_SERVICE_ROLE_KEY, SUPABASE_DB_URL
7. A single Edge Function can handle multiple routes — use Express or Hono. Each route must be prefixed with /function-name.
8. File writes only allowed on /tmp directory
9. Use EdgeRuntime.waitUntil(promise) for background tasks without blocking response

Template:
```typescript
interface ReqPayload { name: string; }

Deno.serve(async (req: Request) => {
  const { name }: ReqPayload = await req.json();
  return new Response(
    JSON.stringify({ message: `Hello \${name}!` }),
    { headers: { 'Content-Type': 'application/json', 'Connection': 'keep-alive' } }
  );
});
```

## Tips

Official Supabase Edge Function guidelines. Source: supabase.com/docs/guides/getting-started/ai-prompts/edge-functions
