---
title: "Troubleshoot a Distributed System Livelock"
slug: troubleshoot-a-distributed-system-livelock
stage: Test
category: "Critical Bugs"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/troubleshoot-a-distributed-system-livelock
---
# Troubleshoot a Distributed System Livelock

Diagnose and resolve service-to-service request bouncing by implementing livelock detection, distributed tracing, and backoff strategies.

## Prompt

You are a distributed systems engineer. You have two services that are interacting in a way that is causing a livelock. They are both actively sending messages to each other, but neither is making any progress. For example, Service A receives a request, finds it is overloaded, and forwards the request to Service B. Service B, also overloaded, forwards the request back to Service A. The request bounces back and forth, consuming resources but never getting processed.

Context:
- The services are part of a request processing pipeline.
- Both services have a load shedding mechanism that forwards requests when they are busy.
- The system is burning CPU, and requests are timing out, but the services themselves have not crashed.

Provide:
1. An explanation of what a livelock is and how it differs from a deadlock.
2. A strategy to debug this livelock. This would involve distributed tracing to visualize the path of a single request and see it bouncing between the services.
3. A solution to break the livelock. This could involve introducing a random backoff before forwarding a request, or having the services drop the request instead of forwarding it if they are overloaded. Another solution is to ensure that requests can only be forwarded a certain number of times before being dropped.

## Tips

A subtle and difficult-to-debug failure mode in distributed systems.
