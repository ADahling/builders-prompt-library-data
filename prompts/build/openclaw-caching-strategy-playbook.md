---
title: "OpenClaw: Caching Strategy Playbook"
slug: openclaw-caching-strategy-playbook
stage: Build
category: "OpenClaw"
grade: B
score: 72
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-caching-strategy-playbook
---
# OpenClaw: Caching Strategy Playbook

Plan app caching with cache-level comparisons, read and write patterns, and a TypeScript Redis cache-aside implementation.

## Prompt

# Caching Strategy Playbook

## Cache Levels
| Level | Latency | Capacity | Use Case |
|-------|---------|----------|----------|
| L1: In-process | < 1ms | MBs | Hot config, parsed templates |
| L2: Distributed (Redis) | 1-5ms | GBs | Session data, API responses |
| L3: CDN/Edge | 5-50ms | TBs | Static assets, public API responses |
| L4: Browser | 0ms | MBs | Assets, API responses |

## Cache Patterns
| Pattern | Description | Use Case |
|---------|-------------|----------|
| Cache-Aside | App checks cache, fills on miss | General purpose, most common |
| Read-Through | Cache fetches from DB on miss | Transparent to application |
| Write-Through | Write to cache and DB synchronously | Strong consistency needed |
| Write-Behind | Write to cache, async write to DB | High write throughput |
| Refresh-Ahead | Proactively refresh before expiry | Predictable access patterns |

## Cache-Aside Implementation
```typescript
async function getUser(userId: string): Promise<User> {
  const cacheKey = `user:${userId}`;
  
  // Check cache
  const cached = await redis.get(cacheKey);
  if (cached) return JSON.parse(cached);
  
  // Cache miss: fetch from DB
  const user = await db.users.findById(userId);
  if (!user) throw new NotFoundError();
  
  // Populate cache with TTL
  await redis.set(cacheKey, JSON.stringify(user), 'EX', 3600);
  
  return user;
}

// Invalidate on update
async function updateUser(userId: string, data: Partial<User>) {
  await db.users.update(userId, data);
  await redis.del(`user:${userId}`);
}
```

## TTL Strategy
| Data Type | TTL | Rationale |
|-----------|-----|-----------|
| User session | 24h | Balance security vs convenience |
| Product catalog | 5-15min | Changes infrequently |
| Search results | 1-5min | Freshness matters |
| Static config | 1h | Rarely changes |
| Real-time data | 10-30s | Short cache for rate limiting |

## Cache Invalidation Strategies
| Strategy | Consistency | Complexity |
|----------|------------|-----------|
| TTL expiry | Eventual (within TTL) | Simple |
| Event-driven | Near real-time | Medium |
| Version tags | Immediate on deploy | Medium |
| Pub/Sub broadcast | Real-time across instances | Complex |

## Thundering Herd Prevention
- **Locking**: Only one request fetches on miss, others wait
- **Stale-while-revalidate**: Serve stale, refresh in background
- **Probabilistic early expiry**: Random early refresh to spread load
- **Request coalescing**: Batch concurrent identical requests

## Monitoring
| Metric | Healthy | Alert |
|--------|---------|-------|
| Hit rate | > 90% | < 70% |
| Miss rate | < 10% | > 30% |
| Eviction rate | Low | Sudden spike |
| Memory usage | < 80% | > 90% |
| Latency (p99) | < 5ms | > 20ms |

## Anti-Patterns
- ❌ Caching everything (cache only hot data)
- ❌ No TTL (stale data forever)
- ❌ Cache invalidation without event system (manual, error-prone)
- ❌ Same TTL for all data types
- ❌ No cache warming strategy (cold start = slow)

## Tips

Caching strategy playbook covering cache levels, patterns, TTL design, invalidation strategies, thundering herd prevention, and monitoring.
