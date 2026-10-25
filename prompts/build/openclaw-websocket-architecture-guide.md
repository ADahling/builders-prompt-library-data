---
title: "OpenClaw: WebSocket Architecture Guide"
slug: openclaw-websocket-architecture-guide
stage: Build
category: "OpenClaw"
grade: B
score: 72
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-websocket-architecture-guide
---
# OpenClaw: WebSocket Architecture Guide

Get WebSocket architecture guidance for real-time apps, covering authentication, message formats, scaling, backpressure, and reliability.

## Prompt

# WebSocket Architecture Guide

## Connection Lifecycle

### Handshake
```
Client → Server: HTTP Upgrade request with auth token
Server → Client: 101 Switching Protocols (or 401/403)
```

### Authentication Strategy
- Token passed as query param or first message after connect
- Validate JWT on handshake, reject before upgrade
- Refresh token mechanism: client sends refresh before expiry
- Never trust client-sent user IDs — derive from token

### Message Protocol
```json
{
  "type": "event|request|response|error|ping",
  "id": "uuid-for-request-response-correlation",
  "channel": "optional-topic",
  "payload": { ... },
  "timestamp": "ISO-8601"
}
```

## Scaling Considerations

### Extracting from Single Server
| Challenge | Solution |
|-----------|----------|
| Sticky sessions | Use Redis pub/sub for cross-server messaging |
| Connection state | Store in Redis, not in-memory |
| Reconnection | Client stores last event ID, server replays missed events |
| Load balancing | Layer 4 (TCP) LB, not Layer 7 (HTTP) |

### Backpressure Handling
- Server: buffer messages per client, drop oldest if buffer full
- Client: acknowledge processing, server pauses if unacked > threshold
- Rate limit inbound messages per connection (e.g. 100/sec)

### Reliability Checklist
- [ ] Heartbeat/ping-pong every 30s (detect dead connections)
- [ ] Exponential backoff reconnection on client (max 30s)
- [ ] Graceful shutdown: server sends close frame before terminating
- [ ] Message ordering guaranteed per channel
- [ ] Deduplication via message IDs on client
- [ ] Connection count monitoring and alerting
- [ ] Max connections per user to prevent abuse
- [ ] Binary protocol (MessagePack/Protobuf) for high-throughput use cases

## Tips

Architecture guide for WebSocket systems covering connection lifecycle, authentication, message protocol, scaling, and reliability.
