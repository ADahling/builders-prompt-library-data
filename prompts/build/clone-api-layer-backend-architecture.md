---
title: "Clone API Layer & Backend Architecture"
slug: clone-api-layer-backend-architecture
stage: Build
category: "Website Cloning"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-api-layer-backend-architecture
---
# Clone API Layer & Backend Architecture

Reverse-engineer a website’s backend to generate a complete Supabase architecture, SQL schemas, API maps, and integrated edge functions.

Variables: target_url

## Prompt

You are a backend architect. Analyze the target website's functionality and design the complete backend architecture needed to support a clone.

Target URL: {{target_url}}

Produce:

## 1. API Endpoint Map
For each user-facing feature, define:
- HTTP method and path
- Request/response schema (TypeScript interfaces)
- Authentication requirements
- Rate limiting rules
- Error response format

## 2. Database Schema
- Complete table definitions with columns, types, constraints
- Foreign key relationships (ERD)
- Indexes for query performance
- Row Level Security policies for every table
- Seed data for development

## 3. Edge Functions / Serverless
- Functions needed for business logic (payments, emails, webhooks)
- Input validation with Zod
- Error handling patterns
- Environment variables required

## 4. Third-Party Integrations
- Payment processing (Stripe): products, prices, checkout, webhooks
- Email service (Resend/SendGrid): transactional emails, templates
- File storage (S3/Supabase Storage): upload, serve, resize
- Analytics (PostHog/Mixpanel): events, funnels, user identification

## 5. Real-Time Features
- WebSocket/Supabase Realtime subscriptions
- Optimistic updates pattern
- Conflict resolution strategy

## 6. Caching Strategy
- What to cache (API responses, computed data)
- Cache invalidation triggers
- CDN configuration

Output as:
1. Complete Supabase migration files (SQL)
2. Edge Function code (TypeScript)
3. API client library for frontend consumption
4. Environment variable template (.env.example)

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Reverse-engineers the complete backend architecture from any website's frontend behavior. Covers DB, APIs, auth, and integrations.
