---
title: "Design a System for Idempotent APIs"
slug: design-a-system-for-idempotent-apis
stage: Build
category: "Backend & Data Integrity"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-system-for-idempotent-apis
---
# Design a System for Idempotent APIs

Get an API idempotency design for retries that create duplicates, with key handling, response storage, middleware code, and client guidance.

Variables: programming_language

## Prompt

Our API is not idempotent, which means that if a client retries a request, it can lead to duplicate records being created. This is a problem for our customers and is causing data integrity issues. I need to design a system to make our API idempotent.

Your task is to design a system for idempotent APIs. The design should include:

1.  **Idempotency Key:** A requirement for clients to send an idempotency key in the header of each `POST` or `PUT` request. The idempotency key should be a unique value that the client generates for each request.
2.  **Server-Side Logic:** A description of the server-side logic to handle the idempotency key. The server should save the result of the first request for a given idempotency key and then return the saved result for any subsequent retries.
3.  **Storage:** A recommendation for a storage solution for the idempotency keys and the corresponding responses. The storage solution should be fast and should have a TTL to automatically clean up old keys.
4.  **Code Example:** A code example in {{programming_language}} that shows how to implement the idempotency logic as a middleware.
5.  **Client-Side Guidance:** A set of guidelines for API clients on how to generate and use the idempotency key.

## Tips

This prompt is an important feature for any API that performs state-changing operations, as it makes the API more robust and reliable.
