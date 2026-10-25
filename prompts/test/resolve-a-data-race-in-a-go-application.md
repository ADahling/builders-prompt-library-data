---
title: "Resolve a Data Race in a Go Application"
slug: resolve-a-data-race-in-a-go-application
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-data-race-in-a-go-application
---
# Resolve a Data Race in a Go Application

Implement thread-safe map access in Go using sync.RWMutex and the race detector to prevent concurrent write crashes in multi-threaded apps.

## Prompt

You are a Go developer. You have a Go application where multiple goroutines are concurrently updating a shared map. The application is intermittently crashing with a `fatal error: concurrent map writes`. Your task is to fix this data race.

Context:
- The application uses goroutines to process incoming requests in parallel.
- Each goroutine needs to write to a global map that serves as a cache.
- Go's maps are not safe for concurrent write access.

Provide:
1. An explanation of what a data race is and why it's a problem in Go with maps.
2. A solution using a `sync.RWMutex` to protect the map. Writes should use a full lock (`Lock()`), and reads should use a read lock (`RLock()`).
3. A guide on how to use Go's race detector (`go run -race`) to automatically detect data races in your code during testing.

## Tips

A fundamental concurrency problem in Go with a standard solution.
