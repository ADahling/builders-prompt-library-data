---
title: "Resolve a Race Condition in a Caching System"
slug: resolve-a-race-condition-in-a-caching-system
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-race-condition-in-a-caching-system
---
# Resolve a Race Condition in a Caching System

Implement distributed locking and probabilistic cache invalidation strategies to prevent database overload during concurrent cache stampedes.

## Prompt

You are a backend architect. You have designed a caching layer to reduce load on your database. However, under heavy load, you are experiencing a race condition known as a cache stampede (or dog-piling). When a popular cached item expires, multiple concurrent requests all miss the cache and rush to the database to regenerate the value, overwhelming the database.

Context:
- The cache is a distributed cache like Redis or Memcached.
- The items have a short TTL (Time To Live).
- The application code’s logic is: if cache miss, then fetch from DB and write to cache.

Provide:
1. A detailed explanation of the cache stampede race condition.
2. A solution that uses a lock (either a local mutex or a distributed lock in Redis) to ensure that only one process/thread can regenerate the cache item at a time. Other processes/threads should wait for the first one to finish and then pull the new value from the cache.
3. A discussion of an alternative, probabilistic solution called ‘early expiration’ or ‘stale-while-revalidate’, where a stale value can be served while a new value is being generated in the background.

## Tips

A classic, advanced problem in designing high-performance caching systems.
