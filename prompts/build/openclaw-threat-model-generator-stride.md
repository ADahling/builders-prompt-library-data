---
title: "OpenClaw: Threat Model Generator (STRIDE)"
slug: openclaw-threat-model-generator-stride
stage: Build
category: "OpenClaw"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-threat-model-generator-stride
---
# OpenClaw: Threat Model Generator (STRIDE)

Review system components and data flows with STRIDE to get threat descriptions, affected components, attack scenarios, and risk scores.

## Prompt

# Threat Model Generator — STRIDE Framework

## Input
Describe your system:
- Architecture diagram or component list
- Data flows (what data moves where)
- Trust boundaries (internal vs external, user vs admin)
- Authentication/authorization mechanisms

## STRIDE Analysis
For each component and data flow, evaluate:

| Threat | Question | Examples |
|--------|----------|----------|
| **S**poofing | Can someone pretend to be another user/service? | Stolen tokens, session hijacking, DNS spoofing |
| **T**ampering | Can someone modify data in transit or at rest? | Man-in-the-middle, SQL injection, file modification |
| **R**epudiation | Can someone deny performing an action? | Missing audit logs, unsigned transactions |
| **I**nformation Disclosure | Can someone access unauthorized data? | Verbose errors, unencrypted storage, logs with PII |
| **D**enial of Service | Can someone make the system unavailable? | Resource exhaustion, infinite loops, missing rate limits |
| **E**levation of Privilege | Can someone gain higher access? | IDOR, role bypass, default admin credentials |

## Risk Scoring
| Factor | Scale |
|--------|-------|
| Likelihood | 1 (rare) — 5 (almost certain) |
| Impact | 1 (negligible) — 5 (critical) |
| Risk = Likelihood × Impact | 1-5 Low, 6-14 Medium, 15-25 High |

## Output Per Threat
1. Threat description
2. Affected component(s)
3. Attack scenario (step-by-step)
4. Risk score (likelihood × impact)
5. Existing mitigations
6. Recommended countermeasures
7. Priority (P0/P1/P2)

## Summary
- Total threats identified
- Risk distribution (high/medium/low)
- Top 5 priorities
- Architecture recommendations

## Tips

Systematic threat modeling using STRIDE. Generates risk-scored threats with attack scenarios, mitigations, and prioritized countermeasures.
