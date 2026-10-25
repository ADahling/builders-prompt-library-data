---
title: "Handle a Cascading Failure Caused by a Service Dependency"
slug: handle-a-cascading-failure-caused-by-a-service-dependency
stage: Test
category: "Critical Bugs"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/handle-a-cascading-failure-caused-by-a-service-dependency
---
# Handle a Cascading Failure Caused by a Service Dependency

Implement resilience patterns like timeouts and exponential backoff to prevent service timeouts from triggering cascading system failures.

## Prompt

You are a microservices developer. A seemingly minor service in your architecture has failed, but it has caused a chain reaction of failures in upstream services that depend on it. Your task is to implement a solution to make the system more resilient.

Context:
- Service A calls Service B, and Service B calls Service C. Service C has failed.
- Service B does not handle the failure of Service C gracefully and starts timing out, which in turn causes Service A to time out.
- The system lacks proper timeouts and retry mechanisms.

Provide:
1. An explanation of how the lack of timeouts and retries contributes to the cascading failure.
2. A code example of implementing a timeout and a retry mechanism with exponential backoff for the call from Service B to Service C.
3. A discussion on the importance of setting appropriate timeouts and the dangers of immediate, repeated retries (retry storms).

## Tips

Focuses on fundamental patterns for building resilient microservices.
