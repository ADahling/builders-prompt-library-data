---
title: "Multi-Persona Security Review"
slug: multi-persona-security-review
stage: Secure
category: "Security Review"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/multi-persona-security-review
---
# Multi-Persona Security Review

Review code from attacker, compliance auditor, and SRE perspectives to get severity-rated findings, concrete attack scenarios, and code fixes.

## Prompt

Review this code from THREE security perspectives simultaneously:

## Perspective 1: The Attacker
Think like a malicious actor. For each endpoint, form, and data flow:
- How would I exploit this? What's the easiest attack vector?
- Can I access other users' data? Can I escalate privileges?
- Can I inject malicious content that other users will see?
- Can I cause denial of service?
- What would I do with the data I could access?

## Perspective 2: The Compliance Auditor
Check against security standards:
- OWASP Top 10: Does this code have any of the top 10 vulnerabilities?
- Data protection: Is PII handled correctly? Is it encrypted at rest and in transit?
- Authentication: Are industry best practices followed?
- Logging: Is there an audit trail for sensitive operations?
- Access control: Is least privilege enforced?

## Perspective 3: The SRE (Reliability)
Consider operational security:
- What happens when this service is under load?
- Are there resource exhaustion vectors?
- What happens when dependencies fail?
- Are secrets properly managed? What if they leak?
- Can this service recover gracefully from failures?

For each finding across all three perspectives:
- Severity: Critical / High / Medium / Low
- Attack scenario (concrete, not theoretical)
- Specific code fix with before/after

Code to review: [paste code or describe feature]

## Tips

Three perspectives catch what one misses. The Attacker perspective is especially powerful — it forces you to think about HOW your code can be exploited. Source: medium.com/data-science-collective
