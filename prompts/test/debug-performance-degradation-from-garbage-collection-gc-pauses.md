---
title: "Debug Performance Degradation from Garbage Collection (GC) Pauses"
slug: debug-performance-degradation-from-garbage-collection-gc-pauses
stage: Test
category: "Critical Bugs"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-performance-degradation-from-garbage-collection-gc-pauses
---
# Debug Performance Degradation from Garbage Collection (GC) Pauses

Optimize JVM garbage collection settings and log analysis to minimize stop-the-world pauses in latency-sensitive Java applications.

## Prompt

You are a Java performance tuning expert. A latency-sensitive application is experiencing long pauses, causing it to miss its service-level objectives (SLOs). You have identified that these pauses are caused by the Java Virtual Machine's (JVM) garbage collector. Your task is to tune the GC to reduce the pause times.

Context:
- The application is a real-time bidding service that requires response times in the low milliseconds.
- It is running on a JVM with the default G1 garbage collector.
- GC logs show long 'stop-the-world' pauses during full GC cycles.

Provide:
1. A guide on how to enable and analyze verbose GC logs to understand the frequency and duration of GC pauses.
2. A set of tuning parameters for the G1 GC to optimize for low pause times, such as setting a max pause time goal (`-XX:MaxGCPauseMillis`).
3. A discussion of alternative garbage collectors, like the Z Garbage Collector (ZGC) or Shenandoah, which are designed for ultra-low-latency applications, and the trade-offs involved in switching to them.

## Tips

A deep and challenging performance tuning problem for senior Java engineers.
