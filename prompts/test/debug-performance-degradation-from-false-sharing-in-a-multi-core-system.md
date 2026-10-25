---
title: "Debug Performance Degradation from False Sharing in a Multi-Core System"
slug: debug-performance-degradation-from-false-sharing-in-a-multi-core-system
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-performance-degradation-from-false-sharing-in-a-multi-core-system
---
# Debug Performance Degradation from False Sharing in a Multi-Core System

Identify and resolve multi-threaded performance bottlenecks by refactoring C++ code to eliminate cache line contention using alignas.

## Prompt

You are a high-performance computing developer. You have a multi-threaded C++ application that is not scaling as expected on a multi-core processor. You have identified that the problem is ‘false sharing’. Two threads are accessing two different variables that happen to be located on the same cache line. Even though the threads are not sharing data, the cache coherency protocol is causing the cache line to be bounced back and forth between the cores, dramatically slowing down performance.

Context:
- The application has an array of counters, and each thread updates its own counter in the array.
- The counters are small (e.g., 64-bit integers), and multiple counters fit onto a single 64-byte cache line.
- Profiling tools show a high number of cache misses and memory bus traffic.

Provide:
1. A detailed explanation of what a cache line is and what false sharing is.
2. A C++ code snippet that is vulnerable to false sharing.
3. The corrected code that avoids false sharing. The solution is to pad the data structure with extra bytes so that the variables accessed by different threads are on different cache lines. This can be done using C++11’s `alignas` keyword to align the variables to the cache line size.

## Tips

A very subtle and deep performance issue that requires a good understanding of modern CPU architecture.
