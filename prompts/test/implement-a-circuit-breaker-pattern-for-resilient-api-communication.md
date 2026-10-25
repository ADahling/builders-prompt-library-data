---
title: "Implement a Circuit Breaker Pattern for Resilient API Communication"
slug: implement-a-circuit-breaker-pattern-for-resilient-api-communication
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-a-circuit-breaker-pattern-for-resilient-api-communication
---
# Implement a Circuit Breaker Pattern for Resilient API Communication

Get a circuit breaker guide for API calls causing cascading failures, with a library recommendation, threshold settings, fallback code, and metrics.

Variables: downstream_service_name, upstream_service_name, language

## Prompt

My microservices-based application is experiencing cascading failures. When one of my downstream services (`{{downstream_service_name}}`) becomes slow or unavailable, my upstream service (`{{upstream_service_name}}`) keeps retrying, exhausts its resources, and eventually fails as well.

I want to implement the Circuit Breaker pattern to make my application more resilient to these kinds of failures.

Your task is to provide a guide on how to implement this pattern in my `{{language}}` service.

1.  **Circuit Breaker Pattern Explained:** Explain the three states of a circuit breaker: Closed, Open, and Half-Open. Use a clear analogy (like an electrical circuit breaker).
2.  **Library Recommendation:** Recommend a well-maintained library in `{{language}}` for implementing the circuit breaker pattern (e.g., `opossum` for Node.js, `resilience4j` for Java, `polly` for .NET). 
3.  **Implementation Example:** Provide a code example showing how to wrap an API call to the `{{downstream_service_name}}` with a circuit breaker using the recommended library. The example should:
    *   Show how to configure the circuit breaker's thresholds (e.g., failure rate threshold, reset timeout).
    *   Show how to provide a "fallback" function that is executed when the circuit is open.
4.  **Monitoring:** How do we monitor the state of our circuit breakers? Explain how to emit events or metrics when the circuit changes state (e.g., on `open

## Tips

The Circuit Breaker is a fundamental pattern for building robust and fault-tolerant distributed systems.
