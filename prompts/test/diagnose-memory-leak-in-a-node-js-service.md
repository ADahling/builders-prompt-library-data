---
title: "Diagnose Memory Leak in a Node.js Service"
slug: diagnose-memory-leak-in-a-node-js-service
stage: Test
category: "Critical Bugs"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/diagnose-memory-leak-in-a-node-js-service
---
# Diagnose Memory Leak in a Node.js Service

Identify, resolve, and monitor memory leaks in Node.js services by analyzing heap dumps and implementing optimized code patterns.

## Prompt

You are a backend developer. A Node.js microservice is showing a gradual increase in memory consumption over time, leading to eventual crashes and restarts. Your task is to diagnose and fix the memory leak.

Context:
- The service uses Express.js and interacts with a MongoDB database.
- Heap dumps have been captured but not yet analyzed.
- The issue is more prominent under heavy load.

Provide:
1. A step-by-step guide to analyze the heap dumps.
2. A code snippet that demonstrates a potential fix for a common cause of memory leaks in this stack.
3. A strategy for implementing memory usage monitoring and alerting.

## Tips

This prompt is useful for assessing a developer's debugging skills for memory-related issues.
