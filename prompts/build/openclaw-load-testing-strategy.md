---
title: "OpenClaw: Load Testing Strategy"
slug: openclaw-load-testing-strategy
stage: Build
category: "OpenClaw"
grade: C
score: 66
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-load-testing-strategy
---
# OpenClaw: Load Testing Strategy

Plan service load testing with test types, weighted user scenarios, performance thresholds, and a checklist for bottleneck analysis.

## Prompt

# Load Testing Strategy

## Test Types

| Type | Purpose | Duration | Load Pattern |
|------|---------|----------|-------------|
| Smoke | Verify system works under minimal load | 1-5 min | 1-5 VUs |
| Load | Validate performance at expected load | 15-30 min | Ramp to target RPS |
| Stress | Find breaking point | 30-60 min | Ramp beyond capacity |
| Soak/Endurance | Detect memory leaks, connection exhaustion | 2-8 hours | Steady at 80% capacity |
| Spike | Test sudden traffic surges | 10-15 min | 0 → 10x → 0 rapidly |
| Breakpoint | Find exact failure threshold | 30-60 min | Step increase until failure |

## Test Design

### Scenario Modeling
```yaml
scenarios:
  browse:
    weight: 60%  # 60% of traffic
    steps:
      - GET /api/products (list)
      - think_time: 2-5s
      - GET /api/products/:id (detail)
      - think_time: 3-8s
  
  purchase:
    weight: 25%
    steps:
      - POST /api/cart/add
      - GET /api/cart
      - POST /api/orders (checkout)
      - think_time: 5-15s
  
  search:
    weight: 15%
    steps:
      - GET /api/search?q=random_term
      - think_time: 1-3s
```

### Success Criteria
```yaml
thresholds:
  http_req_duration:
    p50: 200ms
    p95: 500ms
    p99: 1000ms
  http_req_failed: < 0.1%
  iterations: "> 100/s"
  checks: "> 99%"
```

## Analysis Checklist
- [ ] Identify bottleneck: CPU, memory, DB connections, or network
- [ ] Check for connection pool exhaustion
- [ ] Monitor garbage collection pauses
- [ ] Verify auto-scaling triggers at correct thresholds
- [ ] Compare results against previous baseline
- [ ] Check for graceful degradation (circuit breakers, fallbacks)

## Reporting
- Percentile distribution chart (p50, p90, p95, p99)
- Error rate over time
- Throughput (RPS) over time
- Resource utilization correlated with load
- Comparison table: current vs previous run vs SLA

## Tips

Load testing strategy covering test types, scenario modeling with weighted user flows, success criteria, analysis checklist, and reporting.
