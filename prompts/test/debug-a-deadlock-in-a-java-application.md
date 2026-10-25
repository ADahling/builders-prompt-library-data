---
title: "Debug a Deadlock in a Java Application"
slug: debug-a-deadlock-in-a-java-application
stage: Test
category: "Critical Bugs"
grade: B
score: 71
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-deadlock-in-a-java-application
---
# Debug a Deadlock in a Java Application

Analyze thread dumps to identify circular wait conditions and eliminate Java deadlocks by enforcing consistent lock acquisition ordering.

## Prompt

You are a senior Java developer. A multi-threaded Java application has become unresponsive. A thread dump reveals that two threads are in a deadlock, each waiting for a lock held by the other. Your task is to analyze the thread dump and resolve the deadlock.

Context:
- The application involves two threads, Thread A and Thread B, and two locks, Lock 1 and Lock 2.
- Thread A acquires Lock 1 and then tries to acquire Lock 2.
- Thread B acquires Lock 2 and then tries to acquire Lock 1.

Provide:
1. A guide on how to obtain and analyze a Java thread dump (`jstack`) to identify the deadlock.
2. A detailed explanation of the circular wait condition that is causing the deadlock.
3. A corrected version of the code that ensures all threads acquire the locks in the same order, thus preventing the deadlock.

## Tips

A fundamental concurrency problem that requires deep knowledge of Java threading.
