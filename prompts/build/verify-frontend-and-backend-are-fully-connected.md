---
title: "Verify Frontend and Backend Are Fully Connected"
slug: verify-frontend-and-backend-are-fully-connected
stage: Build
category: "System Architecture"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/verify-frontend-and-backend-are-fully-connected
---
# Verify Frontend and Backend Are Fully Connected

Audit app data flows, endpoints, UI states, and database paths for disconnections, with specific file references and fix instructions.

## Prompt

Audit my [describe app] to verify every frontend action has a backend handler and every backend endpoint has a frontend caller:

1. For every button, form, and user action in the UI, trace data flow to backend. Flag any that fire into nothing.
2. For every API endpoint or Edge Function, verify it's actually called from frontend. Flag orphaned endpoints.
3. For every database table, verify read and write paths from UI. Flag tables written but never displayed, or displayed but never written.
4. For every state variable in frontend, verify it's populated from real data (not hardcoded placeholders from prototyping).
5. For every error state in backend, verify frontend handles it with appropriate UI.
6. For every loading state, verify UI shows spinner or skeleton.

List every disconnection with specific file references and fix instructions.

## Tips

Run before launch to catch dead connections.
