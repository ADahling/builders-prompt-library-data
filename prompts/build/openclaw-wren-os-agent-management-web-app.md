---
title: "OpenClaw: Wren OS \u2014 Agent Management Web App"
slug: openclaw-wren-os-agent-management-web-app
stage: Build
category: "OpenClaw"
grade: C
score: 64
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-wren-os-agent-management-web-app
---
# OpenClaw: Wren OS — Agent Management Web App

Wren OS — Web App to Manage an AI Agent's Work Build a web app called "Wren OS" to manage an AI agent's workflows.

## Prompt

# Wren OS — Web App to Manage an AI Agent's Work

Build a web app called "Wren OS" to manage an AI agent's workflows.

## Screens

### Dashboard (Kanban)
- Columns: todo / in progress / done
- Drag and drop between columns
- Task drawer: title, description, status, priority, dueDate, tags, project, external links, activity log

### Projects
- List page with all projects
- Detail page with tasks filtered by project

### Content Queue
- Stages: idea / draft / published
- Fields: title, platform (twitter/linkedin/blog/other), hook, status, link, tags

### Documents
- Notion links, URLs, internal notes
- Link documents to tasks

## UI Requirements
- Light, Notion-style design
- Realtime updates via subscriptions
- Optimistic UI for drag-and-drop

## Agent API (HTTP)
Base path: /api/agent/*
- POST /listTasks, /createTask, /updateTask, /moveTaskStatus
- POST /createContentIdea, /updateContentItem
- POST /createDocumentLink, /attachDocumentToTask
- POST /appendActivityEvent

Auth: Bearer token from environment variable

## Activity Feed
- Global feed (newest first)
- Per-task activity in drawer
- Deterministic, human-readable summaries
- Moving a task must: update status + write activityEvent in one atomic mutation

## Tips

Full-stack web app spec for managing AI agent workflows. Kanban board, content queue, document management with API endpoints. From Medium Codex article.
