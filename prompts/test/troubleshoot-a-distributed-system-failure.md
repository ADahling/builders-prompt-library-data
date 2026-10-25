---
title: "Troubleshoot a Distributed System Failure"
slug: troubleshoot-a-distributed-system-failure
stage: Test
category: "Critical Bugs"
grade: C
score: 67
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/troubleshoot-a-distributed-system-failure
---
# Troubleshoot a Distributed System Failure

Diagnose and resolve silent failures in Kafka-based Scala microservices while implementing long-term observability improvements.

## Prompt

You are a distributed systems engineer. A complex distributed system responsible for real-time data processing has failed. The system is composed of multiple services that communicate via a message queue. Your task is to troubleshoot the failure and bring the system back online.

Context:
- The system uses Kafka as a message broker and services are written in Scala.
- Monitoring shows that some services have stopped processing messages from the queue.
- There are no obvious errors in the logs of the failed services.

Provide:
1. A systematic approach to troubleshooting the distributed system, starting from the message queue.
2. A list of potential root causes for this type of failure, such as network partitions or broker failures.
3. A plan for improving the observability of the system to make future troubleshooting easier.

## Tips

This prompt requires a holistic understanding of distributed systems.
