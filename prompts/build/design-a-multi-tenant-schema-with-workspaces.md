---
title: "Design a multi-tenant schema with workspaces"
slug: design-a-multi-tenant-schema-with-workspaces
stage: Build
category: "Database & Supabase"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-multi-tenant-schema-with-workspaces
---
# Design a multi-tenant schema with workspaces

Design a workspace schema with membership based access, Supabase RLS policies, tenant scoped indexes, and SQL checks.

Variables: schema_definition, access_requirements, query_patterns

## Prompt

You are a PostgreSQL and Supabase architect designing workspace isolation.

Context:
- Current schema, policies, functions, and grants: {{schema_definition}}
- Workspace roles and access requirements: {{access_requirements}}
- Queries and expected data volumes: {{query_patterns}}

Your task is to design a workspace schema, membership checks, RLS policies, and tenant query indexes.

Steps:
1. Define workspaces and memberships with unique (workspace_id, user_id). Add NOT NULL workspace_id to tenant tables. Separate shared data. Use composite foreign keys to prevent cross-workspace references.
2. Plan ordered migration SQL for backfills, constraints, and RLS. Flag rows whose workspace cannot be assigned safely. Specify delete behavior and atomic workspace creation with its first owner.
3. Write a SECURITY DEFINER membership helper using auth.uid(), a fixed search_path, and qualified names. Explain its trusted owner and RLS bypass needed to avoid membership-policy recursion. Restrict EXECUTE to required roles, revoke PUBLIC access, and prevent client replacement.
4. Enable RLS on tenant and membership tables. Write command-specific policies with USING for existing rows and WITH CHECK for new rows. Check workspace membership through the helper. Gate membership writes by authorized role, prevent self-promotion, and review grants and workspace reassignment.
5. Handle anonymous users, nonmembers, revoked members, forged workspace IDs, cross-tenant references, and concurrent last-owner removal. Provide SQL access checks for each, including membership administration. Explain service_role bypass. Index membership lookups and tenant filters, joins, and sorts; propose EXPLAIN (ANALYZE, BUFFERS) checks.
6. List assumptions, unverified behavior, migration risks, and next steps. Distinguish proposed checks from checks actually run.

Constraints:
- Do not invent project facts; label assumptions.
- Never trust client-supplied membership or expose service_role keys to clients.
- Return executable SQL where supported; mark unresolved decisions instead of guessing.

Output format, in Markdown: Assumptions first, then Schema plan, ordered Migration SQL code blocks, an Access checks table with columns actor, action, expected result, check SQL, then Index rationale, then Unverified items and next steps.

## Tips

Paste your current DDL, membership roles, and representative queries. Include who can invite members, change roles, and delete a workspace.
