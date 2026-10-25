---
title: "Implement Idempotency for API Write Operations to Prevent Duplicate Resource Creation"
slug: implement-idempotency-for-api-write-operations-to-prevent-duplicate-resource-creation
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 77
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-idempotency-for-api-write-operations-to-prevent-duplicate-resource-creation
---
# Implement Idempotency for API Write Operations to Prevent Duplicate Resource Creation

Design API middleware using an Idempotency-Key header and cached responses for a POST endpoint where client retries create duplicate items.

Variables: framework

## Prompt

My API has a `POST /items` endpoint for creating a new item. I have a problem where clients sometimes experience a network error and retry the request, which results in duplicate items being created.

I want to make this endpoint idempotent, meaning that if the client sends the same request multiple times, it will have the same effect as sending it once.

Your task is to design a system for this using an `Idempotency-Key` header.

1.  **Idempotency Explained:** Explain what idempotency is and why it's important for robust APIs.
2.  **The `Idempotency-Key` Header:** Explain the standard pattern: 
    *   The client generates a unique key (e.g., a UUID) for each request they want to make idempotent.
    *   The client sends this key in an `Idempotency-Key` HTTP header.
3.  **Server-Side Implementation:** Describe how the server should handle this key. This should be implemented as a middleware in our `{{framework}}` application.
    *   When a request with an `Idempotency-Key` comes in, the server checks if it has seen this key before (e.g., by looking it up in a Redis cache).
    *   **If the key is new:** The server processes the request as normal, but before sending the response, it saves the response (the status code and body) in the cache, using the idempotency key as the cache key.
    *   **If the key has been seen before:** The server does not re-process the request. It immediately returns the cached response.
4.  **Cache Considerations:** What are the important considerations for the cache? (e.g., setting a TTL on the cached responses to clear out old keys).

Output should be a detailed design for this critical API feature.

## Tips

Idempotency is a key feature of high-quality, reliable APIs, especially for payment and e-commerce systems.
