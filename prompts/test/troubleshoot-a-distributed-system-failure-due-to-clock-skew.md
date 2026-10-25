---
title: "Troubleshoot a Distributed System Failure due to Clock Skew"
slug: troubleshoot-a-distributed-system-failure-due-to-clock-skew
stage: Test
category: "Critical Bugs"
grade: C
score: 62
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/troubleshoot-a-distributed-system-failure-due-to-clock-skew
---
# Troubleshoot a Distributed System Failure due to Clock Skew

Diagnose and resolve data consistency issues caused by clock skew using NTP verification and logical clock alternatives like vector clocks.

## Prompt

You are a distributed systems engineer. You have a distributed system that relies on timestamps to order events. You are seeing bizarre behavior, where events that happened later are being processed before events that happened earlier. You suspect that the clocks on the different servers in your system are not synchronized.

Context:
- The system uses timestamps to determine the order of operations or to implement TTLs (Time To Live) for cached data.
- A server’s clock has drifted significantly from the true time.
- This is causing data to be overwritten incorrectly or to expire prematurely.

Provide:
1. An explanation of what clock skew is and why it is a major problem in distributed systems.
2. A strategy to diagnose clock skew. This involves running the Network Time Protocol (NTP) daemon on all servers and using commands like `ntpq -p` to check if the clocks are synchronized with a reliable time source.
3. A discussion of alternative approaches to ordering events in a distributed system that do not rely on synchronized clocks, such as using Lamport timestamps or vector clocks. These logical clocks can establish a causal ordering of events without needing a global physical clock.

## Tips

A deep and challenging problem in distributed systems that highlights the difficulty of time.
