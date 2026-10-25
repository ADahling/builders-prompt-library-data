---
title: "OpenClaw: Technical Interview Question Generator"
slug: openclaw-technical-interview-question-generator
stage: Build
category: "OpenClaw"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-technical-interview-question-generator
---
# OpenClaw: Technical Interview Question Generator

Get role-specific technical interview questions with coding examples, follow-ups, system design topics, and evaluation rubrics for hiring.

Variables: role, level, areas, stage

## Prompt

# Technical Interview Question Generator

## Input
- Role: {{role}} (e.g., Senior Frontend Engineer, Staff Backend Engineer)
- Level: {{level}} (Junior / Mid / Senior / Staff / Principal)
- Focus areas: {{areas}} (e.g., React, system design, algorithms)
- Interview stage: {{stage}} (phone screen / technical / system design / behavioral)

## Question Categories

### Coding (30 min)
Generate 2-3 problems scaled to level:
- Junior: Array manipulation, string parsing, basic data structures
- Mid: Hash maps, trees, dynamic programming (simple)
- Senior: Graph algorithms, optimization, concurrent data structures
- Staff+: Design a data structure for specific use case

Each problem includes:
- Problem statement (clear, no ambiguity)
- Example input/output
- Follow-up questions (optimize, handle edge cases, scale)
- Evaluation rubric (approach, code quality, testing, communication)

### System Design (45 min)
- Junior: Design a URL shortener, design a todo app
- Mid: Design a chat system, design a rate limiter
- Senior: Design a notification system, design a search engine
- Staff+: Design a multi-region deployment strategy, design a ML pipeline

### Behavioral (STAR format)
Generate 3-5 questions targeting:
- Conflict resolution
- Technical decision making
- Mentorship and leadership
- Handling ambiguity
- Failure and learning

## Evaluation Rubric
| Signal | Strong | Acceptable | Weak |
|--------|--------|------------|------|
| Problem solving | Identifies approach quickly | Needs hints | Cannot progress |
| Code quality | Clean, idiomatic | Functional | Messy, bugs |
| Communication | Explains thinking | Answers questions | Silent coding |
| Testing | Proactively tests | Tests when asked | No testing |

## Tips

Generates role-appropriate technical interview questions with evaluation rubrics. Covers coding, system design, and behavioral rounds.
