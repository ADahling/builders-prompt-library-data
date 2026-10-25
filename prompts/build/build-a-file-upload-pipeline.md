---
title: "Build a File Upload Pipeline"
slug: build-a-file-upload-pipeline
stage: Build
category: "API Design"
grade: C
score: 68
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-file-upload-pipeline
---
# Build a File Upload Pipeline

Build a file upload system for photos, documents, or media with upload UI, storage rules, metadata, signed URLs, quotas, and cleanup.

## Prompt

Build a complete file upload system for [describe use case: profile photos / documents / media]:

1. Frontend: Drag-and-drop upload component with preview, progress bar, file type validation, and size limit enforcement.
2. Storage: Configure storage bucket with appropriate access rules. Private vs public bucket decision.
3. Edge Function (if processing needed): Image resizing, format conversion (WebP), virus scanning, metadata extraction.
4. Database: File metadata table (id, user_id, bucket, path, mime_type, size_bytes, created_at). RLS policies so users only access their own files.
5. Signed URLs: Generate time-limited signed URLs for private file access.
6. Cleanup: Orphaned file detection — files in storage without database records. Scheduled cleanup job.
7. Limits: Per-user storage quota. Max file size. Allowed MIME types.

Security: Never trust client-reported file types. Validate on server side.

## Tips

File uploads are deceptively complex. This covers the full pipeline.
