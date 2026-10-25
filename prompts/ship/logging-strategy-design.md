---
title: "Logging Strategy Design"
slug: logging-strategy-design
stage: Ship
category: "Monitoring & Observability"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/logging-strategy-design
---
# Logging Strategy Design

Design structured application logging with a JSON schema, redaction, trace IDs, retention, indexing, alerts, and example log entries.

## Prompt

Design a structured logging strategy for this application:

Stack: [your tech stack]
Environments: [dev, staging, prod]
Scale: [number of services/instances]

Define:
1. Log levels: When to use DEBUG, INFO, WARN, ERROR, FATAL — with real examples.
2. Structured format: JSON schema for log entries (timestamp, service, traceId, userId, action, duration, metadata).
3. Sensitive data: What MUST be redacted (PII, tokens, passwords)? How?
4. Correlation: How to trace a request across services (trace ID propagation)?
5. Performance: What NOT to log (high-frequency events, large payloads)?
6. Storage: Retention policy per environment (dev: 7d, staging: 30d, prod: 90d).
7. Indexing: Which fields to index for fast searching?
8. Alerting: Which log patterns should trigger alerts?

Provide example log entries for: successful request, failed auth, database error, external API timeout.

## Tips

Good logs are the difference between 5-minute and 5-hour debugging sessions.
