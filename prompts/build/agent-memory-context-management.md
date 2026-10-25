---
title: "Agent Memory & Context Management"
slug: agent-memory-context-management
stage: Build
category: "AI Agent Development"
grade: B
score: 77
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agent-memory-context-management
---
# Agent Memory & Context Management

Design cross-session agent memory with storage choices, retrieval methods, token budgets, prompt injection, and forgetting strategies.

## Prompt

Design a memory system for an AI agent that needs to maintain context across sessions:

## 1. MEMORY TYPES
- **Working memory**: Current conversation / task context (in-prompt)
- **Short-term memory**: Recent interactions, last N messages (vector DB or cache)
- **Long-term memory**: Persistent facts, user preferences, past decisions (database)
- **Episodic memory**: Summaries of past sessions (compressed narratives)

## 2. MEMORY ARCHITECTURE
```
User message → Retrieve relevant memories → Inject into prompt → Agent response → Store new memories
```

For each memory type, specify:
- Storage backend (in-memory, Redis, Postgres + pgvector, Pinecone)
- Retrieval method (recency, semantic similarity, importance score)
- Eviction/compression strategy (summarize old memories, TTL)
- Max tokens allocated in prompt

## 3. MEMORY INJECTION PROMPT
```
You are [agent role].

## Relevant Context (from memory)
{retrieved_memories}

## Current Conversation
{recent_messages}

## Instructions
Use the context above to inform your response. If you learn new important facts about the user or task, flag them for storage.
```

## 4. MEMORY OPERATIONS
- **Store**: After each interaction, extract key facts → embed → store
- **Retrieve**: Before each response, query top-K relevant memories
- **Forget**: Remove outdated or contradicted information
- **Summarize**: Periodically compress episodic memory

## 5. EVALUATION
- Does the agent recall facts from 5+ sessions ago?
- Does it avoid contradicting past context?
- Does memory retrieval add latency? (target: < 200ms)

Apply to: [DESCRIBE YOUR AGENT AND ITS MEMORY NEEDS]

## Tips

Memory is what separates a chatbot from a true agent. Critical for personal assistants, coding agents, and any long-running AI system.
