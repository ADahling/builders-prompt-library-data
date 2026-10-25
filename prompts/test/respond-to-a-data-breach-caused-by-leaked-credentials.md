---
title: "Respond to a Data Breach Caused by Leaked Credentials"
slug: respond-to-a-data-breach-caused-by-leaked-credentials
stage: Test
category: "Critical Bugs"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/respond-to-a-data-breach-caused-by-leaked-credentials
---
# Respond to a Data Breach Caused by Leaked Credentials

Execute a multi-stage incident response plan to neutralize leaked credentials, assess data exposure, and harden your secret management.

## Prompt

You are a security operations engineer. You have detected that a developer's GitHub token has been accidentally committed to a public repository. This token has access to sensitive private repositories, and you suspect it has been used by an attacker to access source code. Your task is to manage this security incident.

Context:
- The token was found by a secret scanning service.
- The developer had access to critical infrastructure-as-code repositories.
- You need to assume that the attacker has cloned all the repositories the token had access to.

Provide:
1. A checklist of immediate actions, including revoking the leaked token, identifying all repositories it had access to, and forcing a rotation of all secrets found in those repositories.
2. A plan to investigate the extent of the breach. This includes analyzing Git logs and cloud audit logs to see what the attacker might have accessed or modified.
3. A set of preventative measures, such as implementing a pre-commit hook to scan for secrets and using a secret management system instead of hardcoding credentials.

## Tips

A very common and serious security incident that requires a swift and thorough response.
