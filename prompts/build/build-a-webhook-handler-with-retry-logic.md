---
title: "Build a Webhook Handler with Retry Logic"
slug: build-a-webhook-handler-with-retry-logic
stage: Build
category: "API Design"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-webhook-handler-with-retry-logic
---
# Build a Webhook Handler with Retry Logic

Build an Edge Function webhook handler for your service with signature checks, duplicate tracking, error handling, logging, and mock test payloads.

## Prompt

Build a production webhook handler for [service: Stripe, GitHub, Twilio]:

1. Signature Verification: Validate webhook signature using the service's signing secret.
2. Idempotency: Handle duplicate deliveries using event ID tracking.
3. Event Processing: Switch on event type, process each with specific handlers.
4. Error Handling: Distinguish retryable vs permanent failures. Return appropriate HTTP codes.
5. Logging: Structured logs for every event with correlation ID.
6. Dead Letter Queue: How to handle events that fail after max retries.
7. Testing: Mock webhook payloads for local development.

Complete Edge Function code with all error cases handled.

## Tips

Webhooks are the backbone of integrations. Get reliability right.
