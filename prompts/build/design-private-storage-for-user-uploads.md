---
title: "Design private file storage for user uploads"
slug: design-private-storage-for-user-uploads
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-private-storage-for-user-uploads
---
# Design private file storage for user uploads

Design private Supabase uploads with user scoped paths, storage policies, short lived signed URLs, upload limits, and reliable cleanup.

Variables: schema_definition, storage_code, file_requirements

## Prompt

You are a Supabase engineer designing private file storage.

Context:
- Tables, relationships, grants, and RLS policies: {{schema_definition}}
- Existing storage configuration and application code: {{storage_code}}
- File access, type, size, and retention requirements: {{file_requirements}}

Your task is to plan private user uploads with enforceable access rules and reliable cleanup.

Steps:
1. Define a private bucket and paths as user UUID/object UUID.extension. Map records to bucket IDs and object keys. Set allowed_mime_types and file_size_limit from requirements; label proposed defaults.
2. Write storage.objects policies TO authenticated, scoped to bucket_id and (storage.foldername(name))[1] = (select auth.uid())::text. Cover SELECT, INSERT, UPDATE, and DELETE. Use WITH CHECK for inserts, USING for reads and deletes, and both for updates. Explain permissions needed for upserts. Check existing permissive policies for OR based access leaks.
3. Show upload and signed URL flows. Authorize access before signing, require SELECT for user scoped signing, and choose a short expiry. Treat signed URLs as bearer credentials; do not persist them as file identifiers or claim logout revokes them.
4. Handle cross user paths, anonymous requests, filename collisions, overwrite attempts, spoofed MIME types, oversized files, and expired URLs. Separate client checks from enforced bucket limits and server content inspection. Give negative access tests with expected results.
5. Plan record deletion with a transactional cleanup outbox holding object keys. Delete files through the Storage API, not SQL against storage.objects. Add retries, idempotency for missing files, and orphan reconciliation for failed uploads or database writes.
6. List assumptions, checks not verifiable from the supplied material, and concrete next steps. Separate proposed tests from observed results.

Constraints:
- Do not invent project facts.
- Keep the bucket private and service role keys server side.
- Use explicit placeholders for missing identifiers; flag SQL requiring adaptation.

Output format, in Markdown: Assumptions first, then Storage design, Policy SQL in a sql code block, Access flows, Cleanup plan, a Test cases table with columns case, action, expected result, then Unverified items and next steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste your record schema and any existing upload, download, and deletion code. Include allowed file types, size limits, retention rules, and who may access each file.
