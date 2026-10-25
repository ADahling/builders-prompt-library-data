---
title: "Map All Application Workflows"
slug: map-all-application-workflows
stage: Build
category: "System Architecture"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/map-all-application-workflows
---
# Map All Application Workflows

Map major app workflows with triggers, numbered steps, data flows, validations, decision points, error handling, and notifications.

## Prompt

For my [describe app], map every major workflow:

For each workflow provide:
1. Workflow Name (e.g., "User Onboarding", "Place an Order")
2. Trigger: What initiates it.
3. Steps: Numbered sequence: component/page, data sent where, validations, what user sees.
4. Decision Points: Conditional logic (if email not verified, redirect).
5. Error Handling: What happens at each step if something fails.
6. Success State: What user sees on completion.
7. Notifications: Emails, in-app notifications, webhooks triggered.

Cover: Registration, Login, Core feature workflow, Payment (if applicable), Admin workflow, Settings/Profile update.

## Tips

Ensures frontend and backend actually tie together.
