---
title: "OpenClaw: Overnight Mini-App Builder"
slug: openclaw-overnight-mini-app-builder
stage: Build
category: "OpenClaw"
grade: C
score: 62
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-overnight-mini-app-builder
---
# OpenClaw: Overnight Mini-App Builder

Overnight Mini-App Builder — OpenClaw Automation Concept Tell your agent your goals and ideas before bed.

Variables: minutes, name

## Prompt

# Overnight Mini-App Builder — OpenClaw Automation

## Concept
Tell your agent your goals and ideas before bed. It figures out what to build while you sleep. Morning: working mini-app in a project folder + Telegram explanation.

## How It Works
1. **Evening brain dump:** User shares goals, frustrations, or ideas in chat
2. **Agent analyzes:** Identifies a small, useful tool that addresses one of the ideas
3. **Overnight build:** Uses coding skills to build a working mini-app
4. **Morning delivery:** Telegram message with:
   - What it built and why
   - How to run it
   - What to try first
   - Known limitations
   - Time to build: {{minutes}}

## Daily Task Generation
At 8:00 AM, generate 4-5 daily tasks:
- 3 from existing goals/projects
- 1 learning task (based on knowledge gaps detected)
- 1 mini-build (the overnight app for tonight)

## Guard Rails
- Maximum complexity: single-file or small project (< 500 lines)
- Stack: User's preferred stack from USER.md
- No external deployments without approval
- No purchases or API signups
- Save to: ~/clawd/builds/YYYY-MM-DD-{{name}}/

## Example Outputs
- A CLI tool that converts CSV to formatted reports
- A local dashboard that visualizes git commit patterns
- A browser bookmarklet that extracts data from a specific site
- A notification script that monitors a URL for changes
- A data cleaning script for a recurring file format

## Uses Skills
- sessions_spawn and sessions_send for multi-step builds
- File system access for creating project folders
- Browser automation for testing web-based builds

## Tips

Tell the agent your goals before bed. Wake up to a working mini-app. From DataCamp's 9 OpenClaw Projects.
