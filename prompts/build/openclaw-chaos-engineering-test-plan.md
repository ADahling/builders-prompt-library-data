---
title: "OpenClaw: Chaos Engineering Test Plan"
slug: openclaw-chaos-engineering-test-plan
stage: Build
category: "OpenClaw"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-chaos-engineering-test-plan
---
# OpenClaw: Chaos Engineering Test Plan

Plan resilience experiments with steady-state thresholds, infrastructure and network failure methods, and expected system behavior.

Variables: success_rate, p95_latency, error_budget

## Prompt

# Chaos Engineering Test Plan

## Steady State Hypothesis
Before running experiments, define normal:
- Request success rate: ≥ {{success_rate}}%
- p95 latency: ≤ {{p95_latency}}ms
- Error budget remaining: ≥ {{error_budget}}%
- Active users impacted: 0

## Experiment Categories

### Infrastructure Failures
| Experiment | Method | Expected Behavior |
|-----------|--------|-------------------|
| Node failure | Terminate random instance | Auto-scaling replaces, traffic rerouted |
| Zone outage | Block AZ network | Multi-AZ failover activates |
| Disk fill | Fill ephemeral storage to 95% | Alerts fire, pods evicted gracefully |
| CPU stress | Stress-ng on random pods | HPA scales up, performance degrades gracefully |
| Memory pressure | Allocate memory until OOM | OOMKill triggers, pod restarts, no cascade |

### Network Failures
| Experiment | Method | Expected Behavior |
|-----------|--------|-------------------|
| Latency injection | Add 500ms to service calls | Circuit breaker opens, fallback serves |
| Packet loss | Drop 10% of packets | Retries succeed, no user-visible error |
| DNS failure | Block DNS resolution | Cached entries used, graceful degradation |
| Partition | Block traffic between services | Queue backlog, no data loss, eventual recovery |

### Application Failures
| Experiment | Method | Expected Behavior |
|-----------|--------|-------------------|
| Dependency down | Kill database/cache | Connection pool handles, reads from replica |
| Slow dependency | Add 5s latency to DB | Timeout triggers, circuit breaker opens |
| Bad deploy | Deploy crashing version | Rollback within 2 minutes, zero downtime |
| Config error | Push invalid config | Validation rejects, last-known-good used |

## Execution Protocol
1. **Notify** stakeholders (even in non-prod)
2. **Set blast radius** — start with non-prod, then canary, then production
3. **Run experiment** with auto-abort conditions
4. **Observe** dashboards and alerts in real-time
5. **Document** findings and remediation actions
6. **Remediate** — fix gaps before next experiment round

## Auto-Abort Conditions
- Error rate exceeds 2x steady state
- p99 latency exceeds 3x steady state
- Any manual page triggered
- Customer-facing error count > threshold

## Tips

Structured chaos engineering test plan with steady state hypothesis, experiment categories, execution protocol, and auto-abort conditions.
