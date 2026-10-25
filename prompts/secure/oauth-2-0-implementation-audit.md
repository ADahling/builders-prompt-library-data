---
title: "OAuth 2.0 Implementation Audit"
slug: oauth-2-0-implementation-audit
stage: Secure
category: "Security Review"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/oauth-2-0-implementation-audit
---
# OAuth 2.0 Implementation Audit

Audit OAuth 2.0 implementations for security vulnerabilities to ensure robust authentication flows, secure token storage, and PKCE compliance.

Variables: application_name, oauth_provider, grant_type, token_storage, requested_scopes

## Prompt

You are an OAuth security expert. Audit the OAuth 2.0 implementation in {{application_name}}.

Implementation details:
- OAuth provider: {{oauth_provider}}
- Grant type: {{grant_type}}
- Token storage: {{token_storage}}
- Scopes: {{requested_scopes}}

Audit:
1. **Authorization Flow**: Is the correct grant type used? (PKCE for SPAs, auth code for server-side)
2. **State Parameter**: Is CSRF protection via state parameter implemented correctly?
3. **Token Storage**: Are tokens stored securely? (httpOnly cookies > localStorage)
4. **Token Refresh**: Is refresh token rotation implemented?
5. **Scope Minimization**: Are only necessary scopes requested?
6. **Redirect URI Validation**: Is the redirect URI strictly validated?
7. **Token Expiration**: Are access tokens short-lived? Are refresh tokens revocable?
8. **Error Handling**: Are OAuth errors handled without leaking information?
9. **Logout**: Is single logout implemented? Are all tokens revoked?
10. **PKCE**: Is Proof Key for Code Exchange used for public clients?

For each finding, provide the vulnerability, risk level, and exact code fix.

## Tips

OAuth misconfigurations are in the OWASP Top 10. Most SPAs get token storage wrong.
