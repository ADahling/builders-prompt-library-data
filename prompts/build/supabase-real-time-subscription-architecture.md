---
title: "Supabase Real-Time Subscription Architecture"
slug: supabase-real-time-subscription-architecture
stage: Build
category: "Database & Supabase"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/supabase-real-time-subscription-architecture
---
# Supabase Real-Time Subscription Architecture

Architect a scalable Supabase real-time system with robust channel structuring, RLS-secure subscriptions, and resilient state management.

Variables: feature_name, application_name, realtime_requirement_1, realtime_requirement_2, concurrent_users

## Prompt

You are a Supabase real-time expert. Design a real-time subscription architecture for {{feature_name}} in {{application_name}}.

Requirements:
- {{realtime_requirement_1}}
- {{realtime_requirement_2}}
- Expected concurrent users: {{concurrent_users}}

Provide:
1. **Channel Design**: How to structure channels (per-user, per-room, broadcast vs presence vs postgres_changes)
2. **Subscription Code**: React hooks for subscribing with proper cleanup
3. **Optimistic Updates**: How to update UI immediately while waiting for server confirmation
4. **Conflict Resolution**: How to handle simultaneous edits
5. **Reconnection Strategy**: How to handle disconnects and catch up on missed events
6. **Performance**: How to minimize subscription count and payload size
7. **Security**: RLS policies that work with real-time (common gotchas)
8. **Testing**: How to test real-time features in development

## Tips

Supabase Realtime is powerful but has gotchas around RLS and channel limits. This prompt covers them all.
