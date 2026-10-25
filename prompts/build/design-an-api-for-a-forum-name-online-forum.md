---
title: "Design an API for an Online Forum"
slug: design-an-api-for-a-forum-name-online-forum
stage: Build
category: "API Design"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-forum-name-online-forum
---
# Design an API for an Online Forum

Get a REST API design for an online forum, with methods, URIs, and data formats for browsing, threads, replies, private messages, profiles, and settings.

Variables: forum_name

## Prompt

I am building an online forum called {{forum_name}}. I need to design the API for it.

Your task is to design the core API for the online forum.

**Instructions:**
1.  **Core Resources:** Identify the core resources of the forum (e.g., users, forums, threads, posts, private messages).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   Browsing forums and threads.
    *   Creating new threads and posting replies.
    *   Sending and receiving private messages.
    *   User profiles and settings.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoints, including the HTTP methods, URIs, and request/response formats.
