---
title: "What is a Threat Model?"
slug: what-is-a-threat-model
stage: Secure
category: "Security Checklist"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/what-is-a-threat-model
---
# What is a Threat Model?

Generate a STRIDE-based threat model, data flow diagram, and mitigation strategy to secure a custom software architecture during design.

Variables: service_type, service_function

## Prompt

You are a software architect who is designing a new online service. You want to identify potential security threats to your service early in the design phase. You have decided to create a threat model for your service. Your task is to create a simple threat model.

Context:
- The service is a `{{service_type}}` that allows users to `{{service_function}}`.
- You will use the STRIDE methodology for your threat model.

Provide:
1. A simple data flow diagram (DFD) for your service, showing the main components and the data flows between them.
2. A list of potential threats to your service, categorized using the STRIDE framework (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege).
3. For each identified threat, a potential mitigation that you could implement in your design.

## Tips

A practical and important security practice, presented as a hands-on design task.
