---
title: "Design a Content Negotiation Strategy for a RESTful API"
slug: design-a-content-negotiation-strategy-for-a-restful-api
stage: Build
category: "API Design"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-content-negotiation-strategy-for-a-restful-api
---
# Design a Content Negotiation Strategy for a RESTful API

Design an Accept-header strategy for a multi-format REST API, with unsupported-format handling and server-side pseudocode.

## Prompt

I want my RESTful API to support multiple response formats (e.g., JSON, XML). I need to implement content negotiation to allow the client to choose the format they want to receive.

Your task is to design a content negotiation strategy using the `Accept` header.

**Instructions:**
1.  **Content Negotiation with `Accept` header:** Explain how to use the `Accept` HTTP request header for content negotiation. Describe how to handle cases where the client requests a format that the server does not support.
2.  **Server Implementation:** Provide a pseudo-code example of how to implement content negotiation on the server-side in a language of your choice (e.g., Python with Flask, Node.js with Express).

**Output Format:**
Provide the output as a Markdown document. First, explain the concept of content negotiation with the `Accept` header. Then, provide the pseudo-code example for the server-side implementation.
