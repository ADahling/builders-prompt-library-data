---
title: "Production Readiness: Performance & Observability Audit"
slug: production-readiness-performance-observability-audit
stage: Test
category: "Quality Audits"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-readiness-performance-observability-audit
---
# Production Readiness: Performance & Observability Audit

Optimize application performance and reliability by identifying bottlenecks, implementing observability best practices, and applying architectural fixes.

## Prompt

Act as a Site Reliability Engineer (SRE) focused on performance and observability. Analyze my codebase:

1. Database Query Performance: Identify queries inside loops (N+1 problem). Suggest optimization into single efficient queries.
2. Heavy Computations: Find expensive operations or inefficient algorithms that block the main thread. Suggest async execution or optimization.
3. Data Loading: Find places where large data sets load into memory at once. Suggest pagination, streaming, or chunking.
4. Bundle Size: Identify large imports that could be code-split or lazy loaded. Check for unused imports.
5. Caching Opportunities: Find repeated identical API calls or computations that could be cached.
6. Structured Logging: Review current logging. Suggest structured logging with severity levels, request IDs, and user context.
7. Health Checks: Add a /health endpoint that verifies database connectivity and external service availability.
8. Metrics: Identify the 5 most important metrics to track (response time, error rate, active users, query performance, memory usage).
9. Alerting: Suggest thresholds for each metric that should trigger alerts.

Provide specific code changes for each recommendation.

## Tips

Based on Richard Seroter's SRE prompt. Makes your app observable and performant under real load.
