---
title: "Design a Real-Time Notifications System"
slug: design-a-real-time-notifications-system
stage: Build
category: "Database & Supabase"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-real-time-notifications-system
---
# Design a Real-Time Notifications System

Build a Supabase real-time notification system with SQL, access policies, React hooks, and a bell dropdown UI with unread counts.

## Prompt

Design and implement a real-time notification system using [Supabase]:

1. Schema: notifications table with user_id, type, title, body, read status, metadata, created_at.
2. RLS: Users only see their own notifications.
3. Real-time: Subscribe to new notifications using Supabase Realtime.
4. Types: Define notification types (system, mention, update, alert) with different UI treatments.
5. Batch Operations: Mark all as read, delete old notifications.
6. Push: Optional integration with browser push notifications.
7. UI Component: Bell icon with unread count, dropdown with notification list, mark-as-read on view.

Complete SQL, RLS policies, React hooks, and UI component code.

## Tips

Every app needs notifications eventually. Build it right from the start.
