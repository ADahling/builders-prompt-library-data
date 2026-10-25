---
title: "Stale Data Displayed Due to Aggressive Browser Caching"
slug: stale-data-displayed-due-to-aggressive-browser-caching
stage: Test
category: "Functional Bugs"
grade: B
score: 77
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/stale-data-displayed-due-to-aggressive-browser-caching
---
# Stale Data Displayed Due to Aggressive Browser Caching

Resolve stale content issues by implementing cache-busting strategies and Cache-Control headers in a full-stack web application.

Variables: project_name, frontend_framework, backend_framework

## Prompt

You are a full-stack developer working on {{project_name}}, a content management system. A user has reported that when they update a news article, they are not seeing the changes reflected immediately. When they refresh the page, the old content is still displayed. Only after a hard refresh (Ctrl+Shift+R) does the new content appear.

This indicates that the browser is aggressively caching the API response for the article. Your task is to implement a cache-busting strategy to prevent this.

**Context:**
- **Frontend:** A {{frontend_framework}} SPA.
- **Backend:** A REST API built with {{backend_framework}}.
- **Problematic API Endpoint:** `GET /api/articles/:id`

**Instructions:**

1.  **Explain Browser Caching:** Briefly explain how browser caching works for API requests and why it can lead to stale data being served.
2.  **Propose a Cache-Busting Strategy:** Choose one of the following common cache-busting techniques and explain why it is effective:
    *   **Cache-Control Headers:** Configure the backend to send appropriate `Cache-Control` headers (e.g., `no-cache

## Tips

A very common issue that is fundamental to building reliable web applications.
