---
title: "Row Level Security Policy Generator"
slug: row-level-security-policy-generator
stage: Build
category: "Database & Supabase"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/row-level-security-policy-generator
---
# Row Level Security Policy Generator

Generate production-ready PostgreSQL RLS policies for Supabase tables based on specific schema requirements and access control rules.

Variables: table_name, table_schema, access_requirement_1, access_requirement_2, access_requirement_3

## Prompt

You are a Supabase security expert. Generate comprehensive Row Level Security (RLS) policies for the {{table_name}} table in my Supabase project.

Table schema:
{{table_schema}}

Access requirements:
- {{access_requirement_1}}
- {{access_requirement_2}}
- {{access_requirement_3}}

Generate:
1. **SELECT policy**: Who can read which rows?
2. **INSERT policy**: Who can create new rows? What validation?
3. **UPDATE policy**: Who can modify which rows? Which columns?
4. **DELETE policy**: Who can delete which rows?
5. **Service role bypass**: Any operations that need service role?

For each policy provide:
- The SQL CREATE POLICY statement
- An explanation of what it does
- A test query to verify it works
- Common mistakes to avoid

Also check for:
- Policies that accidentally expose data
- Missing policies (default deny)
- Performance implications of policy expressions

## Tips

RLS is the #1 security feature in Supabase. Every table with user data MUST have RLS enabled.
