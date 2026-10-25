---
title: "OpenClaw: Event-Driven Architecture Blueprint"
slug: openclaw-event-driven-architecture-blueprint
stage: Build
category: "OpenClaw"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-event-driven-architecture-blueprint
---
# OpenClaw: Event-Driven Architecture Blueprint

Design an event-driven architecture with naming conventions, envelope schemas, event categories, and broker choices for your volume and latency needs.

Variables: domain, current, volume, latency

## Prompt

# Event-Driven Architecture Blueprint

## System Context
- Domain: {{domain}}
- Current architecture: {{current}} (monolith / microservices / hybrid)
- Expected event volume: {{volume}} events/day
- Latency requirement: {{latency}} (real-time / near-real-time / batch)

## Event Design

### Event Naming Convention
```
<domain>.<entity>.<action>.<version>
Example: orders.order.created.v1
```

### Event Envelope Schema
```json
{
  "id": "uuid-v4",
  "type": "orders.order.created.v1",
  "source": "order-service",
  "time": "2025-01-15T10:30:00Z",
  "dataContentType": "application/json",
  "data": { ... },
  "metadata": {
    "correlationId": "uuid",
    "causationId": "uuid",
    "userId": "uuid"
  }
}
```

### Event Categories
| Category | Description | Example |
|----------|-------------|---------|
| Domain Events | Business state changes | OrderPlaced, PaymentReceived |
| Integration Events | Cross-service communication | InventoryReserved |
| System Events | Infrastructure signals | ServiceStarted, HealthCheckFailed |
| Command Events | Requests to perform action | ProcessRefund |

## Topology Decisions

### Broker Selection
| Broker | Best For |
|--------|----------|
| Apache Kafka | High throughput, event sourcing, replay |
| RabbitMQ | Complex routing, low latency, RPC patterns |
| AWS EventBridge | Serverless, AWS-native, rule-based routing |
| NATS | Lightweight, edge computing, low overhead |
| Redis Streams | Simple pub/sub, already using Redis |

### Consumer Patterns
- [ ] Competing consumers for horizontal scaling
- [ ] Fan-out for multi-consumer scenarios
- [ ] Saga/choreography for distributed transactions
- [ ] Dead letter queue for failed processing
- [ ] Idempotency keys on all consumers
- [ ] At-least-once delivery with deduplication

### Reliability Checklist
- [ ] Schema registry for event versioning (Avro/Protobuf/JSON Schema)
- [ ] Event store for audit trail and replay
- [ ] Poison pill handling (move to DLQ after N retries)
- [ ] Consumer lag monitoring and alerting
- [ ] Backpressure mechanisms for slow consumers
- [ ] Event ordering guaranteed within partition/stream
- [ ] Exactly-once semantics where required (transactional outbox)

## Tips

Blueprints an event-driven architecture with event naming, envelope schemas, broker selection, consumer patterns, and reliability checklist.
