---
title: "Set up user roles with a secure role check"
slug: set-up-user-roles-with-a-has-role-check
stage: Secure
category: "Security Review"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-user-roles-with-a-has-role-check
---
# Set up user roles with a secure role check

Create a secure role system with separate role storage, a hardened role check, access policies, and a safe first admin setup.

Variables: schema_definition, auth_setup, role_requirements

## Prompt

You are a PostgreSQL security engineer designing secure user roles.

Context:
- Schema, grants, functions, and policies: {{schema_definition}}
- Authentication, database roles, and migration access: {{auth_setup}}
- Admin and editor permissions: {{role_requirements}}

Your task is to add separate role storage, a hardened role check, access policies, and safe first admin provisioning.

Steps:
1. Map the trusted caller identity and required permissions. Explain why roles must never live on the profile table: editable profile fields can turn profile updates into privilege escalation.
2. Define user_roles with a user foreign key, a CHECK restricting roles to admin or editor, and UNIQUE(user_id, role). Enable RLS. Restrict grants and role mutations; deny self promotion and editor role assignment.
3. Write a boolean has_role function using EXISTS and SECURITY DEFINER. Resolve identity from the trusted authentication mechanism, not a caller supplied user ID. Pin search_path to pg_catalog and fully qualify application objects. Use a narrowly privileged, nonlogin owner able to read user_roles without recursive RLS. Revoke EXECUTE from PUBLIC and grant it only to required roles.
4. Write policies calling has_role for each required operation. Separate USING from WITH CHECK. Review existing permissive policies for OR based bypasses, table grants, and owner or BYPASSRLS access. Keep client roles from replacing the function or writing role records directly.
5. Handle null identities, unknown roles, duplicate grants, deleted users, recursive policies, unauthorized role changes, and last admin removal. Provide allow and deny SQL checks. Bootstrap the first admin through a trusted migration transaction targeting a verified user, never a public signup path; address concurrent attempts.
6. List assumptions, anything not verifiable from the inputs, and next steps for deployment and validation.

Constraints:
- Do not invent project facts or authentication helpers.
- Do not put roles on profiles or trust client role claims.
- Mark unresolved SQL placeholders; do not claim checks ran.

Output format, in Markdown: Design and assumptions first, then Migration SQL in a sql code block, Bootstrap procedure, a Checks table with columns actor, operation, expected result, SQL, then Unverified items and next steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

Migration and authorization acceptance requirements:
- Translate the supplied role requirements into an actor-by-operation allow and deny matrix before writing SQL; include unauthenticated, roleless, editor, and admin callers, and enforce every stated row and workflow restriction.
- If writes must go through approved functions, do not add direct table-write access for admins or editors that bypasses those functions; test both permitted function calls and rejected direct SQL.
- Do not copy existing profile roles into trusted role storage unless the supplied requirements explicitly authorize and verify that migration; treat existing profile values as untrusted.
- Order the migration by dependencies: establish required owners and grants, create referenced objects and functions before policies that call them, and replace policies depending on profile role columns before removing those columns.
- Show the exact privileges and RLS behavior that let the nonlogin has_role owner read user_roles without recursion; SECURITY DEFINER alone does not establish that access, and client roles must not inherit or assume the owner role.
- Reconcile the final grants, all permissive policies, function execution permissions, and existing policies against the matrix; roleless users must not inherit access reserved for a role.
- Include rollback-based allow and deny checks for actual caller identities, direct writes, function-only workflows, and any draft or published-row restrictions in the inputs; label unresolved dependencies instead of presenting a migration as executable or verified.


## Tips

Paste existing tables, grants, policies, and how database requests identify the signed in user. Include what admins and editors may read or change.
