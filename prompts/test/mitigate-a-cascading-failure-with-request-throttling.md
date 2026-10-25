---
title: "Mitigate a Cascading Failure with Request Throttling"
slug: mitigate-a-cascading-failure-with-request-throttling
stage: Test
category: "Critical Bugs"
grade: C
score: 67
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/mitigate-a-cascading-failure-with-request-throttling
---
# Mitigate a Cascading Failure with Request Throttling

Implement an NGINX or API gateway rate limiter using token bucket algorithms to stop traffic spikes and prevent cascading microservice failure.

## Prompt

You are an SRE. A sudden spike in traffic from a single misbehaving client is overwhelming one of your key microservices. This is causing it to slow down, which in turn is causing failures in other services that depend on it. Your task is to implement request throttling to protect the service.

Context:
- The service is a public-facing API.
- The traffic spike is from a single IP address making thousands of requests per second.
- You need a way to limit the number of requests a single client can make in a given time period.

Provide:
1. An explanation of what request throttling (or rate limiting) is and how it can prevent cascading failures.
2. A design for implementing a rate limiter. You can describe an algorithm like the token bucket or leaky bucket algorithm.
3. An example of how to implement this using a reverse proxy like NGINX or an API gateway, which can enforce rate limits before the requests even hit your service.

## Tips

Focuses on a crucial operational pattern for protecting services from overload.
