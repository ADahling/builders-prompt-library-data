---
title: "OpenClaw: Load Test Scenario Builder"
slug: openclaw-load-test-scenario-builder
stage: Build
category: "OpenClaw"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-load-test-scenario-builder
---
# OpenClaw: Load Test Scenario Builder

Build load test scenarios with traffic patterns, user journeys, a k6 script template, and latency thresholds for your target service.

Variables: service_url, rps, duration, scenarios

## Prompt

# Load Test Scenario Builder

## Input
- Target service: {{service_url}}
- Expected peak traffic: {{rps}} requests/second
- Test duration: {{duration}} (default: 10 minutes)
- User scenarios: {{scenarios}} (e.g., "browse → search → add to cart → checkout")

## Scenario Design

### Traffic Patterns
| Pattern | Shape | Use Case |
|---------|-------|----------|
| Ramp-up | 0 → target over 5 min | Normal load test |
| Spike | Sudden 10× burst for 30s | Flash sale, viral event |
| Soak | Steady load for 2+ hours | Memory leak detection |
| Step | Increase by 20% every 2 min | Find breaking point |

### User Journey Modeling
Define realistic user flows with think times:
1. Homepage (think: 2-5s)
2. Search query (think: 3-8s)
3. View product (think: 5-15s)
4. Add to cart (think: 1-3s)
5. Checkout (think: 10-30s)

Distribution: 60% browse-only, 30% add-to-cart, 10% complete checkout

### k6 Script Template
```javascript
import http from 'k6/http';
import { check, sleep } from 'k6';

export const options = {
  stages: [
    { duration: '2m', target: {{rps}} },
    { duration: '5m', target: {{rps}} },
    { duration: '2m', target: 0 },
  ],
  thresholds: {
    http_req_duration: ['p(95)<500', 'p(99)<1000'],
    http_req_failed: ['rate<0.01'],
  },
};
```

## Success Criteria
| Metric | Target | Critical |
|--------|--------|----------|
| p95 latency | <500ms | <1000ms |
| p99 latency | <1000ms | <2000ms |
| Error rate | <1% | <5% |
| Throughput | Meets target RPS | >80% of target |

## Report Template
- Peak RPS achieved
- Latency distribution (p50, p90, p95, p99)
- Error rate and types
- Bottleneck identified (CPU, memory, DB, network)
- Recommendations for scaling

## Tips

Designs load test scenarios with traffic patterns, user journey modeling, k6 scripts, and success criteria. Supports ramp, spike, soak, and step patterns.
