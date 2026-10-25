---
title: "Design a Multi-Tenant SaaS Architecture"
slug: design-a-multi-tenant-saas-architecture
stage: Build
category: "System Architecture"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-multi-tenant-saas-architecture
---
# Design a Multi-Tenant SaaS Architecture

Design a multi-tenant SaaS architecture with isolation, auth, billing, onboarding, scaling, SQL migrations, and critical-path code.

## Prompt

Design a multi-tenant SaaS architecture for [describe app]:

1. Tenant Isolation: Shared database with tenant_id column vs schema-per-tenant. Recommend and justify.
2. Data Model: How tenant_id propagates through every table. RLS policies per table.
3. Auth: How users belong to tenants. Invite flow. Role hierarchy within a tenant.
4. Billing: Per-tenant usage tracking. How to meter and limit.
5. Onboarding: Tenant creation flow. Default data seeding.
6. Admin: Super-admin vs tenant-admin capabilities.
7. Scaling: What changes at 10 tenants vs 1,000 vs 100,000.

Provide SQL migrations and code for critical paths.

## Tips

Essential for B2B SaaS. Get the tenant model right from day one.
