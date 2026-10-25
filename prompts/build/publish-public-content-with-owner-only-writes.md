---
title: "Publish public content with owner-only writes"
slug: publish-public-content-with-owner-only-writes
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/publish-public-content-with-owner-only-writes
---
# Publish public content with owner-only writes

Create Supabase SQL for public published content, owner draft previews, and owner-only writes, with clear policies and access checks.

Variables: schema_definition, content_requirements

## Prompt

You are a Supabase engineer setting up public content with owner-only writes.

Context:
- Existing or proposed schema, policies, and grants: {{schema_definition}}
- Content fields, public visibility, and owner actions: {{content_requirements}}

Your task is to write SQL that lets anyone read published rows while only their owner can create, edit, publish, or unpublish them, with private draft previews.

Steps:
1. Identify the table, primary key, and owner column. Define an owner UUID referencing auth.users(id), NOT NULL, and an is_published boolean NOT NULL DEFAULT false. For existing rows, flag any backfill needed before adding constraints.
2. Enable RLS. Inspect existing policies and grants. Replace conflicting policies explicitly: permissive policies combine with OR and can defeat restrictions. Grant schema USAGE as needed, SELECT to anon and authenticated, and INSERT and UPDATE only to authenticated. Revoke unwanted PUBLIC and anon write grants.
3. Add SELECT policies: anon may read only is_published = true; authenticated may read published rows or rows where owner_id = (SELECT auth.uid()). Adapt owner_id to the supplied schema. Explain why RLS hides rows, not private columns.
4. Add INSERT for authenticated with WITH CHECK enforcing ownership. Add UPDATE with both USING and WITH CHECK enforcing ownership. Allow both draft and published states so owners can publish and unpublish. Deny DELETE by default through revoked grants and no policy; if required, add owner-only DELETE with USING.
5. Show public listing and authenticated owner draft preview queries. Explain that updates need SELECT access and previews must use the owner's session, never a service_role key.
6. Provide checks for anon, owner, and another user: published reads, hidden drafts, forged inserts, owner edits, owner reassignment, cross-owner writes, unpublishing, and deletion. State expected results, not claimed outcomes.

Constraints:
- Do not invent project facts. List assumptions and label proposed names.
- Never disable RLS or expose service_role credentials.
- Return runnable SQL for the stated assumptions. Flag unsafe backfills before migration.

Output format, in Markdown: Assumptions, Migration SQL code block, Query examples, and Access checks table with actor, action, and expected result.

## Tips

Paste your existing table SQL, policies, and grants, or describe the table you want to create. Include which columns may be public and whether owners may delete rows.
