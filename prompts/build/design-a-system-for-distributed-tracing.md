---
title: "Design a System for Distributed Tracing"
slug: design-a-system-for-distributed-tracing
stage: Build
category: "Backend & Data Integrity"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-system-for-distributed-tracing
---
# Design a System for Distributed Tracing

Get a tracing design for debugging microservice requests, with standards, instrumentation, collector options, visualization, and sampling.

## Prompt

Our microservices architecture is becoming increasingly complex, and it's difficult to trace a request as it flows through the different services. This makes it hard to debug problems and to understand the performance of our system. I need to design a system for distributed tracing.

Your task is to design a system for distributed tracing. The design should include:

1.  **Tracing Standard:** A recommendation to use an open standard for distributed tracing, such as OpenTelemetry or OpenTracing.
2.  **Instrumentation:** A plan for how to instrument our microservices to generate and propagate trace data. This should involve using an SDK for our programming language and adding instrumentation to our web framework, database clients, and other libraries.
3.  **Trace Collector:** A recommendation for a trace collector to receive the trace data from our microservices. This could be a self-hosted collector like Jaeger or Zipkin, or a cloud-based service like AWS X-Ray or Google Cloud Trace.
4.  **Trace Visualization:** A plan for how to visualize the traces to make it easy to understand the flow of a request and to identify any performance bottlenecks.
5.  **Sampling:** A discussion of different sampling strategies to reduce the volume of trace data and to minimize the performance overhead of tracing.

## Tips

This prompt is an essential tool for debugging and monitoring microservices architectures.
