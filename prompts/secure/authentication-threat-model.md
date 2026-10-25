---
title: "Design a secure authentication flow"
slug: authentication-threat-model
stage: Secure
category: "Security Review"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: true
url: https://buildersprompt.com/prompts/authentication-threat-model
---
# Design a secure authentication flow

Get ranked threats and concrete remediations for an application's authentication flow, covering OAuth, sessions, MFA, recovery, and privileged actions.

## Prompt

Act as an application security engineer. Threat-model the authentication flow for {{application}}. Review credential handling, OAuth and PKCE, session creation, fixation, rotation, logout, recovery, MFA, CSRF, redirect validation, device trust, rate limiting, audit events, and privileged re-authentication. Return ranked findings and concrete remediations.
