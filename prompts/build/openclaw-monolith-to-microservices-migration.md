---
title: "OpenClaw: Monolith to Microservices Migration"
slug: openclaw-monolith-to-microservices-migration
stage: Build
category: "OpenClaw"
grade: C
score: 66
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-monolith-to-microservices-migration
---
# OpenClaw: Monolith to Microservices Migration

Plan a monolith migration with module assessments, strangler fig extraction steps, and data ownership rules for moving to microservices.

Variables: module, capability, data, frequency, team, 1-10

## Prompt

# Monolith to Microservices Migration Plan

## Assessment Phase

### Decomposition Analysis
For each candidate module, evaluate:
| Module | Business Capability | Data Ownership | Change Frequency | Team Ownership | Coupling Score |
|--------|-------------------|----------------|------------------|----------------|---------------|
| {{module}} | {{capability}} | {{data}} | {{frequency}} | {{team}} | {{1-10}} |

### Strangler Fig Pattern Steps
1. **Identify** — Pick the module with lowest coupling score and highest change frequency
2. **Proxy** — Route traffic through an API gateway / reverse proxy
3. **Extract** — Build new service replicating module functionality
4. **Verify** — Shadow traffic comparison (old vs new responses)
5. **Redirect** — Switch traffic to new service
6. **Retire** — Remove old code path from monolith

### Data Decomposition Strategy
- [ ] Identify shared tables — which services read/write?
- [ ] Define data ownership — one service owns each table
- [ ] Create API contracts for cross-service data access
- [ ] Plan data migration with zero-downtime strategy
- [ ] Implement eventual consistency where appropriate
- [ ] Set up change data capture (CDC) for transition period

### Anti-Patterns to Avoid
- ❌ Distributed monolith (microservices that must deploy together)
- ❌ Shared database between services
- ❌ Synchronous chains of 4+ services
- ❌ "Nano-services" that are too small to justify overhead
- ❌ Big bang migration (extract everything at once)

### Migration Checklist Per Service
- [ ] Service has its own database/schema
- [ ] Health check and readiness endpoints
- [ ] Centralized logging with correlation IDs
- [ ] Circuit breakers for all outbound calls
- [ ] Contract tests (consumer-driven)
- [ ] Independent CI/CD pipeline
- [ ] Runbook for on-call engineers
- [ ] Load tested at 2x expected traffic

## Tips

Step-by-step migration plan from monolith to microservices using the Strangler Fig pattern with assessment, data decomposition, and per-service checklist.
