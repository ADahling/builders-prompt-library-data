---
title: "Use TDD to Implement a Caching Mechanism"
slug: use-tdd-to-implement-a-caching-mechanism
stage: Test
category: "Testing & QA"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/use-tdd-to-implement-a-caching-mechanism
---
# Use TDD to Implement a Caching Mechanism

Implement a high-performance caching layer using Test-Driven Development and benchmarks to optimize slow operations and verify latency gains.

Variables: cache_type

## Prompt

You are a software engineer focused on performance. Your task is to use Test-Driven Development (TDD) to implement a caching mechanism for a function that performs a slow operation, such as a database query or an API call.

Context:
- The goal is to improve the performance of the function by caching its results.
- You will use an in-memory cache or a distributed cache like {{cache_type}}.

Provide:
1. A set of failing tests that define the behavior of the caching mechanism (e.g., cache hit, cache miss, cache expiration).
2. The implementation of the caching mechanism that makes the tests pass.
3. A benchmark to measure the performance improvement after implementing the cache.

## Tips

A prompt for engineers who want to practice TDD to implement a common performance optimization technique.
