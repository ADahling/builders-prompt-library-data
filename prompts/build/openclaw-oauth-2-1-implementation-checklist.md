---
title: "OpenClaw: OAuth 2.1 Implementation Checklist"
slug: openclaw-oauth-2-1-implementation-checklist
stage: Build
category: "OpenClaw"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-oauth-2-1-implementation-checklist
---
# OpenClaw: OAuth 2.1 Implementation Checklist

Get an OAuth implementation checklist covering PKCE, token rotation, redirect validation, and client security for app authentication.

## Prompt

# OAuth 2.1 Implementation Checklist

## Protocol Requirements (RFC 9728 / OAuth 2.1)

### Authorization Code Flow (with PKCE — mandatory)
- [ ] PKCE required for ALL clients (public AND confidential)
- [ ] code_verifier: 43-128 chars, unreserved URI characters
- [ ] code_challenge_method: S256 only (plain MUST NOT be used)
- [ ] Authorization codes are single-use, expire in ≤ 60 seconds
- [ ] Redirect URI exact-match validation (no wildcards)

### Token Security
- [ ] Access tokens are short-lived (5-15 minutes recommended)
- [ ] Refresh tokens: rotated on every use (one-time use)
- [ ] Refresh token replay detection: revoke entire grant on reuse
- [ ] Tokens bound to client (cannot be used by different client)
- [ ] Token format: opaque reference tokens or signed JWTs
- [ ] JWT tokens include: iss, sub, aud, exp, iat, jti (minimum)

### Deprecated / Removed (DO NOT implement)
- ❌ Implicit grant (removed in OAuth 2.1)
- ❌ Resource Owner Password Credentials (removed)
- ❌ Bearer tokens in URI query parameters
- ❌ Plain PKCE challenge method

### Client Security
- [ ] Client credentials stored securely (not in source code)
- [ ] Dynamic client registration validates redirect URIs
- [ ] Confidential clients authenticate via client_secret_post or private_key_jwt
- [ ] CORS restricted to registered origins

### Token Endpoint Security
- [ ] Rate limiting on token endpoint
- [ ] Brute force protection on authorization code exchange
- [ ] Token introspection endpoint requires authentication
- [ ] Token revocation endpoint supports both access and refresh tokens

### Additional Security
- [ ] State parameter: cryptographically random, bound to session
- [ ] CSRF protection via state or nonce
- [ ] Authorization server metadata discovery (RFC 8414)
- [ ] Resource indicators (RFC 8707) for multi-tenant APIs
- [ ] DPoP (RFC 9449) for sender-constrained tokens

## Tips

Complete OAuth 2.1 implementation checklist covering PKCE, token security, deprecated patterns, client security, and modern extensions.
