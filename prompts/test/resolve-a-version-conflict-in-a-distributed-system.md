---
title: "Resolve a Version Conflict in a Distributed System"
slug: resolve-a-version-conflict-in-a-distributed-system
stage: Test
category: "Critical Bugs"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-version-conflict-in-a-distributed-system
---
# Resolve a Version Conflict in a Distributed System

Implement optimistic concurrency control to handle distributed version conflicts through retry strategies and strategic locking choices.

## Prompt

You are a backend engineer. In a distributed key-value store that uses optimistic concurrency control, two clients are trying to update the same record at the same time, leading to a version conflict. Your task is to handle this conflict gracefully.

Context:
- The system uses a version number (or an ETag) to detect conflicts.
- Client A reads a record with version 1. Client B reads the same record with version 1.
- Client B updates the record successfully, incrementing the version to 2. Client A then tries to update the record using version 1, which is now stale.

Provide:
1. An explanation of optimistic concurrency control and how it leads to version conflicts.
2. A client-side strategy for handling a version conflict error, which typically involves re-reading the latest version of the record, re-applying the changes, and retrying the update.
3. A discussion of when to use optimistic vs. pessimistic locking.

## Tips

Tests understanding of concurrency control in distributed data stores.
