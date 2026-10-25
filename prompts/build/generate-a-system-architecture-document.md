---
title: "Generate a System Architecture Document"
slug: generate-a-system-architecture-document
stage: Build
category: "System Architecture"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-system-architecture-document
---
# Generate a System Architecture Document

Turn a PRD into a system architecture covering frontend, backend, authentication, data flows, integrations, security, and scaling for your stack.

## Prompt

Based on this PRD: [paste PRD or summary]. Generate a complete system architecture:

1. Architecture Overview: Pattern (client-server, serverless). Text diagram of frontend, backend, database, auth, external services.
2. Frontend Architecture: Framework, routing, state management, component hierarchy, data flow.
3. Backend Architecture: Edge Functions / API routes. Each endpoint: method, purpose, auth required, request/response shape.
4. Authentication Flow: Step-by-step for signup, login, logout, password reset, session refresh.
5. Data Flow: For 3 most important user actions, trace complete flow from click to DB write to UI update.
6. External Integrations: Third-party services, connection method, where keys stored.
7. Security Architecture: Where sensitive logic lives, secrets management, CORS, rate limiting.
8. Scalability: What happens at 100 vs 10,000 users. Bottlenecks.

Assume [specify stack].

## Tips

Create before building to avoid architectural mistakes.
