---
title: "Integrate a Third-Party API Securely"
slug: integrate-a-third-party-api-securely
stage: Build
category: "API Design"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/integrate-a-third-party-api-securely
---
# Integrate a Third-Party API Securely

Get Supabase Edge Function and React code for a third-party API integration, with auth checks, secret setup, error handling, and dev testing.

## Prompt

I need to integrate [API name: Stripe, OpenAI, SendGrid, Twilio] into my Lovable/React/Supabase app:

1. Architecture: Why this must go through an Edge Function (never expose key client-side).
2. Edge Function Code: Complete function: receives request, validates auth, calls API with secret from env vars, handles response, returns data.
3. Frontend Code: React component/hook calling supabase.functions.invoke().
4. Error Handling: API errors, timeouts, rate limits, invalid responses. What user sees for each.
5. Testing: How to test in dev without production credentials.
6. Environment Setup: Step-by-step for storing API key in Supabase secrets.

Complete, production-ready code.

## Tips

Replace [API name] with your service.
