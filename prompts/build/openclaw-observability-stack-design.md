---
title: "OpenClaw: Observability Stack Design"
slug: openclaw-observability-stack-design
stage: Build
category: "OpenClaw"
grade: C
score: 60
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-observability-stack-design
---
# OpenClaw: Observability Stack Design

Design service observability with structured logging rules, RED and USE metrics, and OpenTelemetry tracing with log correlation.

## Prompt

# Observability Stack Design

## Three Pillars + Context

### Logging
```json
{
  "timestamp": "ISO-8601",
  "level": "info|warn|error",
  "service": "order-service",
  "traceId": "abc123",
  "spanId": "def456",
  "message": "Order created",
  "context": {
    "userId": "uuid",
    "orderId": "uuid",
    "amount": 99.99
  }
}
```

**Rules:**
- Structured JSON, never unstructured text
- Include traceId and spanId in every log line
- Log at boundaries: incoming request, outgoing call, errors
- Don't log PII (mask email, redact tokens)
- Log levels: DEBUG (dev only), INFO (business events), WARN (recoverable), ERROR (action needed)

### Metrics (RED + USE)
| Method | Metrics |
|--------|---------|
| RED (services) | Rate, Errors, Duration |
| USE (resources) | Utilization, Saturation, Errors |

**Key Metrics:**
- request_duration_seconds (histogram, by endpoint, status)
- request_total (counter, by endpoint, method, status)
- error_total (counter, by type)
- queue_depth (gauge)
- connection_pool_size (gauge, active/idle)
- db_query_duration_seconds (histogram)

### Tracing
- [ ] OpenTelemetry SDK integrated in all services
- [ ] Context propagation via W3C Trace Context headers
- [ ] Span naming: `<verb> <resource>` (e.g. "GET /api/orders")
- [ ] Custom attributes on spans for business context
- [ ] Sampling: 100% for errors, 10% for success in production
- [ ] Trace-to-log correlation via traceId

### Dashboards
1. **Service Overview** — RED metrics per service, error rate trend
2. **Infrastructure** — CPU, memory, disk, network per node
3. **Business KPIs** — Orders/min, revenue, conversion funnel
4. **Dependencies** — External API latency and error rates
5. **On-Call** — Active alerts, incident timeline, error budget burn

### Alerting Rules
- Error rate > 1% for 5 minutes → page on-call
- p99 latency > 2x baseline for 10 minutes → page
- Error budget burn rate > 10x for 1 hour → page
- Disk usage > 80% → warn; > 90% → page
- Zero traffic for 5 minutes → page (possible outage)

## Tips

Designs a complete observability stack with structured logging, RED/USE metrics, distributed tracing, dashboards, and alerting rules.
