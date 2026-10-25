---
title: "ECC Rule: Php Security"
slug: ecc-rule-php-security
stage: Secure
category: "Security Review"
grade: C
score: 60
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/ecc-rule-php-security
---
# ECC Rule: Php Security

PHP Security This file extends common/security.md ../common/security.md with PHP specific content.

## Prompt

# PHP Security

> This file extends [common/security.md](../common/security.md) with PHP specific content.

## Input and Output

- Validate request input at the framework boundary (`FormRequest`, Symfony Validator, or explicit DTO validation).
- Escape output in templates by default; treat raw HTML rendering as an exception that must be justified.
- Never trust query params, cookies, headers, or uploaded file metadata without validation.

## Database Safety

- Use prepared statements (`PDO`, Doctrine, Eloquent query builder) for all dynamic queries.
- Avoid string-building SQL in controllers/views.
- Scope ORM mass-assignment carefully and whitelist writable fields.

## Secrets and Dependencies

- Load secrets from environment variables or a secret manager, never from committed config files.
- Run `composer audit` in CI and review new package maintainer trust before adding dependencies.
- Pin major versions deliberately and remove abandoned packages quickly.

## Auth and Session Safety

- Use `password_hash()` / `password_verify()` for password storage.
- Regenerate session identifiers after authentication and privilege changes.
- Enforce CSRF protection on state-changing web requests.

## Reference

See skill: `laravel-security` for Laravel-specific security guidance.

## Tips

Source: Everything Claude Code (ECC) — Rule: php/security
