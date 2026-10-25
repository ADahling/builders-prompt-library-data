---
title: "System Design Interview: Design a Distributed Message Queue from Scratch"
slug: system-design-interview-design-a-distributed-message-queue-from-scratch
stage: Build
category: "System Architecture"
grade: B
score: 78
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/system-design-interview-design-a-distributed-message-queue-from-scratch
---
# System Design Interview: Design a Distributed Message Queue from Scratch

Architect a scalable, fault-tolerant message queue by defining storage protocols, replication strategies, and delivery guarantees.

## Prompt

You are in a system design interview for a staff engineer role. The interviewer asks you to "Design a distributed message queue like RabbitMQ or SQS from first principles."

**Your Task:**
Provide a detailed, first-principles design for a distributed message queue.

**Instructions & Constraints:**
1.  **Core Concepts:**
    *   Define the basic concepts: producer, consumer, queue.

2.  **Storage Layer:**
    *   Discuss how you would store the messages. You need a durable, append-only log for each queue.

3.  **Distribution and High Availability:**
    *   Explain how you would distribute the queues across multiple servers and replicate them for high availability.

4.  **Producer and Consumer Interaction:**
    *   Describe the protocol for producers to send messages and for consumers to receive them.

5.  **Reliability:**
    *   Discuss how to ensure at-least-once delivery of messages.

**Output Format:**
Generate a design document in Markdown:
1.  **Designing a Distributed Message Queue from First Principles**
2.  **The Storage Layer: A Durable, Replicated Log**
3.  **The Producer and Consumer Protocol**
4.  **Ensuring Reliability and At-Least-Once Delivery**
