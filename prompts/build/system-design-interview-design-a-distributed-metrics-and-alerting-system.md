---
title: "System Design Interview: Design a Distributed Metrics and Alerting System"
slug: system-design-interview-design-a-distributed-metrics-and-alerting-system
stage: Build
category: "System Architecture"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/system-design-interview-design-a-distributed-metrics-and-alerting-system
---
# System Design Interview: Design a Distributed Metrics and Alerting System

Architect a scalable, pull-based monitoring infrastructure with time-series storage and alerting logic for high-availability systems.

## Prompt

You are in a system design interview. The interviewer asks you to "Design a distributed metrics and alerting system like Prometheus."

**Your Task:**
Provide a design for a system that can collect, store, and query time-series metrics and send alerts.

**Instructions & Constraints:**
1.  **Architecture:**
    *   **Metrics Collection:** A pull-based model where the system scrapes metrics from applications.
    *   **Time-Series Database (TSDB):** A database optimized for storing and querying time-series data.
    *   **Query Engine:** A powerful query language to analyze the data.
    *   **Alerting Manager:** A component to manage and send alerts.

2.  **Scaling the System:**
    *   Discuss how to scale the storage and query layers.

**Output Format:**
Generate a design document in Markdown:
1.  **Designing a Prometheus-like Metrics and Alerting System**
2.  **A Pull-Based Architecture for Metrics Collection**
3.  **The Time-Series Database and Query Engine**
4.  **The Alerting Pipeline**
