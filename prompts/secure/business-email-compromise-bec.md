---
title: "Business Email Compromise (BEC)"
slug: business-email-compromise-bec
stage: Secure
category: "Security Checklist"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/business-email-compromise-bec
---
# Business Email Compromise (BEC)

Analyze a BEC incident to document attacker techniques, identify red flags, and recommend technical and procedural security controls.

Variables: amount_of_money, email_provider

## Prompt

You are a fraud investigator who is analyzing a Business Email Compromise (BEC) incident. The attacker impersonated the CEO of the company and sent an email to the CFO, requesting an urgent wire transfer to a fraudulent bank account. Your task is to write a report on the incident and provide recommendations to prevent it from happening again.

Context:
- The company lost `{{amount_of_money}}` in the incident.
- The company's email system is `{{email_provider}}`.

Provide:
1. A summary of the BEC incident, including the timeline of events and the techniques used by the attacker.
2. A list of the red flags in the attacker's email that could have been spotted.
3. A set of recommendations for the company to prevent future BEC attacks. This should include both technical controls (e.t., email filtering, DMARC) and procedural controls (e.g., out-of-band verification for financial transactions).

## Tips

A practical prompt that deals with a very common and costly type of cybercrime.
