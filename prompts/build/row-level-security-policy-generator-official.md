---
title: "Row Level Security Policy Generator (Official)"
slug: row-level-security-policy-generator-official
stage: Build
category: "Database & Supabase"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/row-level-security-policy-generator-official
---
# Row Level Security Policy Generator (Official)

Get Supabase Postgres row level security policies for your tables and access rules, with separate operations and role-specific checks.

## Prompt

You're a Supabase Postgres expert in writing row level security policies. Generate policies with these rules:

- Only use CREATE POLICY or ALTER POLICY queries
- Always use double apostrophe in SQL strings (e.g., 'Night''s watch')
- Always use "auth.uid()" instead of "current_user"
- SELECT policies: USING only (no WITH CHECK)
- INSERT policies: WITH CHECK only (no USING)
- UPDATE policies: both USING and WITH CHECK
- DELETE policies: USING only (no WITH CHECK)
- Don't use FOR ALL — create 4 separate policies (select, insert, update, delete)
- Policy names should be short but descriptive, enclosed in double quotes
- Discourage RESTRICTIVE policies, encourage PERMISSIVE (and explain why)

Roles: 'anon' (unauthenticated), 'authenticated' (logged in). Use TO clause after FOR.

Performance tips:
- Wrap auth.uid() in a subselect: (select auth.uid()) — causes initPlan caching
- Minimize joins between source and target tables — use IN or ANY instead
- Always specify roles with TO to prevent unnecessary policy evaluation
- Add indexes on columns used in RLS policies

Example:
```sql
CREATE POLICY "Users can view own records" ON my_table
  FOR SELECT TO authenticated
  USING ((select auth.uid()) = user_id);
```

Generate policies for: [describe your tables and access rules]

## Tips

Official Supabase RLS prompt. The (select auth.uid()) subselect trick alone can 10x RLS performance. Source: supabase.com/docs
