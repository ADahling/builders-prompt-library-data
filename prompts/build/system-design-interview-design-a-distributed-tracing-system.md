---
title: "System Design Interview: Design a Distributed Tracing System"
slug: system-design-interview-design-a-distributed-tracing-system
stage: Build
category: "System Architecture"
grade: B
score: 78
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/system-design-interview-design-a-distributed-tracing-system
---
# System Design Interview: Design a Distributed Tracing System

Architect a scalable distributed tracing infrastructure featuring instrumentation, context propagation, and efficient sampling strategies.

## Prompt

You are in a system design interview. The interviewer asks you to "Design a distributed tracing system like Jaeger or Zipkin."

**Your Task:**
Provide a design for a system that can trace requests as they flow through a microservices architecture.

**Instructions & Constraints:**
1.  **Core Concepts:**
    *   Explain the concepts of traces, spans, and context propagation.

2.  **Architecture:**
    *   **Instrumentation:** Client libraries to instrument the application code.
    *   **Collector:** A service to receive the trace data.
    *   **Storage:** A database to store the trace data.
    *   **UI:** A web interface to visualize the traces.

3.  **Sampling:**
    *   Discuss the need for sampling to reduce the volume of trace data.

**Output Format:**
Generate a design document in Markdown:
1.  **Designing a Distributed Tracing System**
2.  **Core Concepts: Traces, Spans, and Context Propagation**
3.  **High-Level Architecture**
4.  **The Importance of Sampling**
