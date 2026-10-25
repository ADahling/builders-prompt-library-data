---
title: "API Rate Limiting Strategy"
slug: api-rate-limiting-strategy
stage: Build
category: "API Design"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-rate-limiting-strategy
---
# API Rate Limiting Strategy

Design an API rate limiting strategy with algorithm tradeoffs, tiers, headers, distributed enforcement, pseudocode, and middleware recommendations.

## Prompt

Design a rate limiting strategy for this API:

API type: [public / internal / partner]
Expected traffic: [requests per second]
Endpoint categories: [list endpoint groups with different limits]

Design:
1. Algorithm choice: Token bucket vs sliding window vs fixed window — justify.
2. Limit tiers: Different limits for free/paid/enterprise.
3. Headers: X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Reset, Retry-After.
4. Granularity: Per-user, per-IP, per-API-key, per-endpoint?
5. Burst handling: Allow short bursts above steady-state limit?
6. Response: What status code and body on limit exceeded?
7. Distributed: How to enforce across multiple server instances?
8. Exemptions: Health checks, webhooks, internal services?
9. Monitoring: Alerts when users consistently hit limits.

Provide implementation pseudocode and recommended middleware/library.

## Tips

Critical for any API that will face production traffic.
