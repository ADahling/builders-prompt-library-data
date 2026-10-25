---
title: "Mitigate a Cascading Failure with Adaptive Throttling"
slug: mitigate-a-cascading-failure-with-adaptive-throttling
stage: Test
category: "Critical Bugs"
grade: C
score: 63
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/mitigate-a-cascading-failure-with-adaptive-throttling
---
# Mitigate a Cascading Failure with Adaptive Throttling

Design an adaptive throttling system that dynamically adjusts request rates based on downstream service health to prevent cascading failures.

## Prompt

You are a principal engineer at a large-scale web service. You have implemented basic rate limiting, but you find that it is not effective enough. A downstream service can still become overloaded and fail, and your static rate limits are either too permissive or too restrictive. Your task is to design an adaptive throttling system.

Context:
- Your service (Service A) calls a downstream service (Service B).
- You want to throttle requests from Service A to Service B based on the health of Service B.
- The health of Service B can be measured by its latency or error rate.

Provide:
1. An explanation of the limitations of static rate limiting.
2. A design for an adaptive throttling system. This could involve a client-side component in Service A that monitors the success rate and latency of calls to Service B. If the latency increases or the error rate crosses a threshold, the client should automatically reduce the rate at which it sends requests.
3. A discussion of how this system could be implemented using a token bucket algorithm where the rate of token replenishment is adjusted based on the health signals from the downstream service.

## Tips

A sophisticated, next-level approach to building resilient systems, as practiced by companies like Netflix and Amazon.
