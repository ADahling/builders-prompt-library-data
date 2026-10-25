---
title: "Optimize a Slow-Running API Endpoint"
slug: optimize-a-slow-running-api-endpoint
stage: Test
category: "Critical Bugs"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-a-slow-running-api-endpoint
---
# Optimize a Slow-Running API Endpoint

Identify N+1 query bottlenecks in a Rails API and implement eager loading, caching, and serialization optimizations to reduce response times.

## Prompt

You are a backend developer. A specific API endpoint is unacceptably slow, taking several seconds to respond and causing timeouts for clients. Your task is to diagnose the performance issue and optimize the endpoint.

Context:
- The endpoint is part of a Ruby on Rails application and aggregates data from multiple database tables.
- The slowness is caused by an N+1 query problem, where one initial query leads to N subsequent queries.
- The data is being serialized into a complex JSON object.

Provide:
1. An explanation of the N+1 query problem and how to detect it using tools like the Rails logger or a performance monitoring tool.
2. A corrected version of the Rails controller code that uses eager loading (`includes`) to fix the N+1 query problem.
3. Other potential optimization strategies for this endpoint, such as caching the response or optimizing the JSON serialization.

## Tips

A common performance problem in ORM-based applications.
