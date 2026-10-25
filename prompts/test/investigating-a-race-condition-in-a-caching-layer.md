---
title: "Investigating a Race Condition in a Caching Layer"
slug: investigating-a-race-condition-in-a-caching-layer
stage: Test
category: "Critical Bugs"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/investigating-a-race-condition-in-a-caching-layer
---
# Investigating a Race Condition in a Caching Layer

Get a technical document on cache stampedes under heavy load, with a sequence diagram, global locking tradeoffs, and a proposed solution.

Variables: service_name, language

## Prompt

Our high-traffic web service, {{service_name}}, uses a caching layer (e.g., Redis) to reduce database load. The logic is simple: check for data in the cache; if it's a miss, fetch it from the database, and then write it to the cache for future requests. However, under heavy load, we're seeing a "cache stampede" or "dog-piling" effect. Multiple concurrent requests for the same missing key are all hitting the database simultaneously, overwhelming it.

This is a classic race condition. As a senior engineer, you need to write a technical document explaining the problem and proposing a robust, production-ready solution.

1.  **Analyzing the Race Condition:**
    *   Provide a clear, step-by-step description of the race condition. Use a sequence diagram involving at least two concurrent requests and the cache/database to illustrate how both requests end up going to the database for the same key.
    *   Explain the negative consequences of this race condition: database overload, increased latency, and potential cascading failures.

2.  **Initial (but flawed) Solution: Simple Locking:**
    *   A junior developer might suggest a simple lock. They propose: "When a request gets a cache miss, it acquires a global lock, fetches from the DB, writes to the cache, and then releases the lock. Other requests wait on the lock."
    *   Explain why this solution is problematic. What are the performance and scalability issues with a single, global lock in a high-concurrency environment?

3.  **Proposed Solution: Lock-free Cache Population (Promise-based):**
    *   Propose a more sophisticated, lock-free solution suitable for a modern, asynchronous application (e.g., in Node.js, Python with asyncio, or Java with CompletableFuture).
    *   The idea is that the *first* request to miss the cache creates a *promise* (or future) for the database query and stores this promise in the cache (or a local in-memory map). Subsequent requests for the same key get the promise and wait for it to resolve, rather than starting their own database query.
    *   Provide a detailed pseudocode or code example in {{language}} that implements this logic. Your code should handle:
        *   Storing the promise/future.
        *   Handling successful database query resolution (caching the result and fulfilling the promise).
        *   Handling database query failures (removing the promise and propagating the error).

4.  **Alternative Solution: Using a Distributed Lock with Timeouts:**
    *   In some architectures, a distributed lock is a more suitable approach. Describe how to implement a more robust locking mechanism using a distributed cache like Redis.
    *   Explain how to use a Redis command like 'SET key value NX PX timeout' to acquire a lock with a timeout. This is a "spin lock."
    *   Provide pseudocode for the locking logic. It should include:
        *   Attempting to acquire the lock.
        *   If the lock is acquired: fetch from DB, write to cache, release the lock.
        *   If the lock is *not* acquired: wait (spin) for a short period and then retry by checking the cache again (as the lock holder may have populated it).
    *   Discuss the importance of the lock timeout to prevent deadlocks if a process crashes while holding the lock.

5.  **Comparing the Solutions and Best Practices:**
    *   Create a table comparing the promise-based solution and the distributed lock solution. Compare them on criteria like: performance, complexity, fault tolerance, and language/framework suitability.
    *   Provide a concluding recommendation on which solution to use for our {{service_name}} and why.

Your response should be a detailed technical document of at least 600 words.
