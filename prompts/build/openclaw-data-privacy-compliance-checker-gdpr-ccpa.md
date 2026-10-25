---
title: "OpenClaw: Data Privacy Compliance Checker (GDPR/CCPA)"
slug: openclaw-data-privacy-compliance-checker-gdpr-ccpa
stage: Build
category: "OpenClaw"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-data-privacy-compliance-checker-gdpr-ccpa
---
# OpenClaw: Data Privacy Compliance Checker (GDPR/CCPA)

Review personal data inventories, flows, and processors against privacy checklists for lawful basis, user rights, and technical safeguards.

## Prompt

# Data Privacy Compliance Checker

## Input
Provide:
- Data inventory: what personal data you collect, where it's stored
- Data flows: how data moves between systems
- Third-party processors: services that handle user data
- Current privacy policy URL (optional, for review)

## GDPR Compliance Checklist

### Lawful Basis
| Data Type | Basis | Documentation Required |
|-----------|-------|----------------------|
| Email (account) | Contract | Terms of Service |
| Usage analytics | Legitimate interest | LIA document |
| Marketing emails | Consent | Opt-in records |
| Cookies (non-essential) | Consent | Cookie consent banner |

### Data Subject Rights
| Right | Implementation | Response Time |
|-------|---------------|---------------|
| Access (Art. 15) | Export user data as JSON/CSV | 30 days |
| Erasure (Art. 17) | Delete account + all personal data | 30 days |
| Portability (Art. 20) | Machine-readable data export | 30 days |
| Rectification (Art. 16) | Edit profile, correct records | 30 days |
| Restriction (Art. 18) | Freeze processing | 30 days |
| Objection (Art. 21) | Opt-out of profiling/marketing | Immediately |

### Technical Measures
- [ ] Data encrypted at rest (AES-256)
- [ ] Data encrypted in transit (TLS 1.2+)
- [ ] Access logging on all personal data stores
- [ ] Retention policies implemented and automated
- [ ] Pseudonymization where possible
- [ ] Data minimization: collect only what's needed

## CCPA Additions
- "Do Not Sell My Personal Information" link
- Opt-out mechanism for data sharing
- Financial incentive disclosures
- 12-month lookback for data disclosure requests

## Output
- Compliance score per regulation
- Gap analysis with specific violations
- Remediation plan with priorities
- Privacy policy update recommendations

## Tips

Checks GDPR and CCPA compliance with data inventory analysis, rights implementation verification, and remediation planning.
