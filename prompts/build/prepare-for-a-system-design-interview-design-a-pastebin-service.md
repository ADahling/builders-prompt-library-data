---
title: "Prepare for a System Design Interview: Design a Pastebin Service"
slug: prepare-for-a-system-design-interview-design-a-pastebin-service
stage: Build
category: "System Architecture"
grade: B
score: 72
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/prepare-for-a-system-design-interview-design-a-pastebin-service
---
# Prepare for a System Design Interview: Design a Pastebin Service

Practice designing a scalable Pastebin-like web service by defining API endpoints, storage schemas, and high-availability architecture.

## Prompt

You are a candidate in a system design interview. The interviewer has asked you to design a service like Pastebin, where users can paste text and get a unique URL to share it.

**Your Task:**
Structure your response as if you were in the interview. This is a classic system design question that tests your ability to cover the basics.

**Instructions & Constraints:**
Follow this standard interview structure:

1.  **Requirements Clarification:**
    *   Ask clarifying questions: What is the max size of a paste? Do pastes expire? Do users need to be able to edit pastes? Do we need to support private pastes?

2.  **API Design:**
    *   Define the API endpoints for creating a new paste and retrieving an existing one (e.g., `POST /api/v1/pastes
