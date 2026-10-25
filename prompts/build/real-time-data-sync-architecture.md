---
title: "Real-Time Data Sync Architecture"
slug: real-time-data-sync-architecture
stage: Build
category: "Modern Data Stack"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/real-time-data-sync-architecture
---
# Real-Time Data Sync Architecture

Review real-time sync patterns for your app scenario, including database change capture, broadcasts, presence, and CRDT-based sync.

Variables: scenario, latency, strategy, offline

## Prompt

# Real-Time Data Sync Architecture

## Use Case
- Scenario: {{scenario}} (collaborative editing / live dashboard / multi-device sync / multiplayer)
- Latency requirement: {{latency}} (< 100ms / < 1s / < 5s)
- Conflict resolution: {{strategy}} (last-write-wins / merge / manual)
- Offline support: {{offline}} (required / nice-to-have / not needed)

## Pattern Selection

### 1. Database-Level CDC (Change Data Capture)
```
Client ←→ API ←→ Database
                    ↓ (WAL / triggers)
              CDC Stream (Debezium / Supabase Realtime)
                    ↓
              Subscribers (WebSocket / SSE)
```
**Best for:** Dashboards, notifications, audit logs
**Supabase implementation:**
```sql
-- Enable realtime for a table
ALTER PUBLICATION supabase_realtime ADD TABLE public.messages;
```
```typescript
const channel = supabase
  .channel('messages')
  .on('postgres_changes', { event: '*', schema: 'public', table: 'messages' }, 
    (payload) => handleChange(payload))
  .subscribe();
```

### 2. Broadcast (Ephemeral Messages)
```
Client A → Supabase Channel → Client B, C, D
```
**Best for:** Cursor positions, typing indicators, live reactions
**No persistence needed — fire and forget.**

### 3. Presence (Who's Online)
```
Client joins channel → Presence state synced to all participants
```
**Best for:** "5 users viewing this document", active user lists

### 4. CRDT-Based Sync (Conflict-Free)
```
Client A (offline) ←→ CRDT Engine ←→ Server ←→ Client B (offline)
               Automatic merge on reconnect
```
**Tools:** Yjs, Automerge, Liveblocks
**Best for:** Collaborative text editing, shared whiteboards

### 5. Event Sourcing
```
Client → Append Event → Event Store → Projections → Read Models
```
**Best for:** Financial transactions, audit-heavy systems, undo/redo

## Conflict Resolution Strategies
| Strategy | Trade-off |
|----------|-----------|
| Last-Write-Wins (LWW) | Simple, may lose data |
| Operational Transform (OT) | Complex, proven (Google Docs) |
| CRDTs | Automatic merge, higher memory |
| Manual resolution | User decides, more UI work |
| Version vectors | Detect conflicts, app resolves |

## Checklist
- [ ] Reconnection with exponential backoff
- [ ] Missed event replay (last event ID or sequence number)
- [ ] Optimistic UI updates with rollback on conflict
- [ ] Connection state indicator (online/offline/reconnecting)
- [ ] Rate limiting on write operations
- [ ] Presence heartbeat with timeout (30s default)
- [ ] Graceful degradation when realtime unavailable

## Tips

Architecture patterns for real-time data sync including CDC, broadcast, presence, CRDTs, and event sourcing with Supabase implementation examples.
