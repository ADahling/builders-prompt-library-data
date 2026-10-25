---
title: "STRIDE Threat Model for New Features"
slug: stride-threat-model-for-new-features
stage: Secure
category: "Security Review"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/stride-threat-model-for-new-features
---
# STRIDE Threat Model for New Features

Perform a STRIDE threat model analysis on this feature: describe the feature, its data flows, and user interactions .

## Prompt

Perform a STRIDE threat model analysis on this feature: [describe the feature, its data flows, and user interactions].

For each STRIDE category, identify specific threats:

S — SPOOFING (Identity):
- Can someone pretend to be another user?
- Are auth tokens properly validated at every entry point?
- Can API calls be replayed with stolen tokens?

T — TAMPERING (Data Integrity):
- Can request/response data be modified in transit?
- Can users modify data they shouldn't (e.g., changing another user's ID in a request)?
- Are database writes validated server-side?

R — REPUDIATION (Accountability):
- Can users deny performing actions?
- Is there an audit log for sensitive operations?
- Are timestamps and user IDs recorded on every write?

I — INFORMATION DISCLOSURE:
- Do error messages reveal internal architecture?
- Can users access other users' data through parameter manipulation (IDOR)?
- Are API responses over-fetching (returning more data than the UI needs)?

D — DENIAL OF SERVICE:
- Are there rate limits on expensive operations?
- Can a user create unbounded data (infinite uploads, records)?
- What happens under load?

E — ELEVATION OF PRIVILEGE:
- Can a regular user access admin endpoints?
- Are role checks server-side (not just UI-hidden)?
- Can users self-assign roles?

For each threat found: severity (Critical/High/Medium/Low), attack scenario, and specific mitigation with code.

## Tips

STRIDE is the industry-standard threat modeling framework used at Microsoft and adopted across the security industry. Source: lockllm.com/blog/ai-prompts-security
