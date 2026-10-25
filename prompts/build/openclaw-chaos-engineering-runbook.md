---
title: "OpenClaw: Chaos Engineering Runbook"
slug: openclaw-chaos-engineering-runbook
stage: Build
category: "OpenClaw"
grade: C
score: 66
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-chaos-engineering-runbook
---
# OpenClaw: Chaos Engineering Runbook

Design, execute, and automate systematic failure injection experiments to validate system resilience and minimize production blast radius.

## Prompt

# Chaos Engineering Runbook

## Principles
1. Build a hypothesis about steady-state behavior
2. Introduce real-world failure events
3. Run experiments in production (start small)
4. Automate experiments for continuous verification
5. Minimize blast radius

## Experiment Design Template
| Field | Description |
|-------|-------------|
| Hypothesis | "The system maintains < 200ms p95 latency when service X is down" |
| Steady State | Define normal metrics (latency, error rate, throughput) |
| Injection | What failure to introduce |
| Blast Radius | Which users/services affected |
| Abort Conditions | When to stop (error rate > 5%, latency > 2s) |
| Duration | How long to run |
| Rollback | How to reverse the failure |

## Failure Injection Catalog
| Category | Experiment | Tool |
|----------|-----------|------|
| Network | Latency injection (100-500ms) | tc netem, Toxiproxy |
| Network | Packet loss (1-10%) | tc netem |
| Network | DNS failure | CoreDNS manipulation |
| Compute | CPU stress (80-100%) | stress-ng |
| Compute | Memory pressure | stress-ng --vm |
| Compute | Process kill | kill -9, Chaos Monkey |
| Storage | Disk full | fallocate |
| Storage | I/O latency | dm-delay |
| Application | Exception injection | Code-level fault injection |
| Application | Dependency timeout | Toxiproxy |

## Progressive Rollout
```
Level 1: Dev/staging environment
Level 2: Production, single instance, off-peak
Level 3: Production, single AZ, business hours
Level 4: Production, region-level, game days
Level 5: Automated continuous chaos
```

## Game Day Checklist
- [ ] All participants briefed on experiment
- [ ] Monitoring dashboards open
- [ ] Communication channel established
- [ ] Abort procedure documented and tested
- [ ] Customer support notified
- [ ] Rollback verified in staging

## Post-Experiment
- Document findings (expected vs actual)
- File tickets for weaknesses discovered
- Update runbooks with new failure modes
- Share learnings in engineering all-hands

## Anti-Patterns
- ❌ Chaos without observability (can't learn from what you can't see)
- ❌ Starting in production without staging validation
- ❌ No abort conditions (uncontrolled experiments)
- ❌ Running chaos without stakeholder buy-in

## Tips

Chaos engineering runbook with experiment design, failure catalog, progressive rollout levels, game day checklist, and post-experiment practices.
