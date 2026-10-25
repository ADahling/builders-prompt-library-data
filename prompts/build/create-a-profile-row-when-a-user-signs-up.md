---
title: "Create a profile row when a user signs up"
slug: create-a-profile-row-when-a-user-signs-up
stage: Build
category: "Database & Supabase"
grade: A+
score: 94
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-profile-row-when-a-user-signs-up
---
# Create a profile row when a user signs up

Create a Supabase profile migration with a signup trigger, owner only access policies, a safe backfill, and verification queries.

Variables: schema_definition, profile_requirements

## Prompt

You are a Supabase database engineer building secure signup profiles.

Context:
- Existing schema, policies, grants, and signup triggers: {{schema_definition}}
- Required profile fields and editing rules: {{profile_requirements}}

Your task is to create a profile for each auth user, restrict access to its owner, and backfill existing users.

Steps:
1. Inspect existing objects for conflicts. Define public.profiles with id uuid PRIMARY KEY REFERENCES auth.users(id) ON DELETE CASCADE. Match requested fields; explain nullable fields or defaults needed for existing users.
2. Write a trigger function returning trigger, with SECURITY DEFINER and SET search_path = ''. Qualify object names. Insert NEW.id and return NEW. Attach an AFTER INSERT FOR EACH ROW trigger to auth.users. Restrict direct function execution by PUBLIC, anon, and authenticated.
3. Treat raw_user_meta_data as untrusted. Copy only requested display fields, never roles or permissions. Handle absent or malformed values so optional metadata does not break signup. Explain that trigger errors roll back signup; do not silently swallow errors.
4. Enable RLS. Add SELECT and UPDATE policies TO authenticated using (SELECT auth.uid()) = id; also use that predicate in UPDATE WITH CHECK. Grant SELECT and UPDATE only on editable columns. Remove conflicting broad policies and grants. Deny client INSERT and DELETE; prevent id edits and anonymous access.
5. Add INSERT INTO public.profiles ... SELECT ... FROM auth.users with ON CONFLICT (id) DO NOTHING. Preserve existing profiles. Install the trigger and run the backfill in one transaction; explain concurrent signup handling and rerun behavior.
6. Supply checks for missing profiles, signup creation, owner reads and edits, cross user denial, anonymous denial, and forbidden id edits. Test RLS under client roles, not a service role or table owner. Include safe cleanup guidance.

Constraints:
- Do not invent project facts. List assumptions and unresolved requirements.
- Return runnable SQL in dependency order. Flag destructive changes before applying them.
- Never disable RLS or expose privileged credentials to clients.

Output format, in Markdown: Assumptions, Migration SQL in a sql code block, Verification with SQL and expected results, and Failure modes and cleanup.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste existing tables, policies, grants, and signup triggers, plus the profile fields you need. Use this before building profile screens or adding profile editing.
