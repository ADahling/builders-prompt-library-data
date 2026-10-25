---
title: "Event-Driven Architecture Design"
slug: event-driven-architecture-design
stage: Build
category: "System Architecture"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/event-driven-architecture-design
---
# Event-Driven Architecture Design

Architect a high-performance event-driven system with defined schemas, scaling strategies, and reliable data consistency mechanisms.

Variables: application_name, primary_use_case, events_per_second, max_latency, ordering_requirement

## Prompt

You are a senior systems architect. Design an event-driven architecture for {{application_name}} that handles {{primary_use_case}}.

Requirements:
- Expected throughput: {{events_per_second}} events/second
- Latency requirement: {{max_latency}}
- Must support at-least-once delivery
- Must handle event ordering for {{ordering_requirement}}

Provide:
1. **Event Schema Design**: Define the core events with their payloads (use JSON Schema)
2. **Topology Diagram**: Describe producers, consumers, topics/queues, and their relationships
3. **Technology Selection**: Recommend message broker (Kafka, RabbitMQ, SQS, etc.) with justification
4. **Error Handling**: Dead letter queues, retry policies, circuit breakers
5. **Monitoring**: Key metrics to track (lag, throughput, error rate)
6. **Scaling Strategy**: How to scale each component independently
7. **Data Consistency**: How to maintain consistency across services (saga pattern, outbox pattern, etc.)

## Tips

Use for designing microservices communication patterns. Adapt the throughput and latency requirements to your specific use case.
