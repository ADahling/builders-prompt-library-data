---
title: "Securing an Agent with Restricted Tool Access"
slug: securing-an-agent-with-restricted-tool-access
stage: Build
category: "AI Agent Development"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/securing-an-agent-with-restricted-tool-access
---
# Securing an Agent with Restricted Tool Access

Get a Python script that configures agent tools by user role and demonstrates that admin tools are unavailable to regular users.

## Prompt

Design a security-conscious agent system where the agent's access to tools is restricted based on the user's permissions or the context of the task.

**The Problem:**

You don't want every user to be able to use every tool. For example, a regular user shouldn't be able to call an `admin_delete_user` tool.

**Implementation Strategy:**

1.  **Define User Roles:** Create a simple role system (e.g., 'admin', 'user').
2.  **Tool Permissions:** Create a mapping that defines which roles have access to which tools.
    ```python
    tool_permissions = {
        'search': ['user', 'admin'],
        'admin_delete_user': ['admin']
    }
    ```
3.  **Dynamic Tool Loading:**
    *   When a request comes in, identify the user's role.
    *   Before initializing the agent, create the list of available tools *dynamically* based on the user's role and the `tool_permissions` mapping.
4.  **Agent Initialization:**
    *   Initialize the agent with only the subset of tools that the user is allowed to access.

**Your Task:**

Write a Python script that simulates this. It should have a function `get_agent_for_user(user_role)` that returns an agent configured with the correct tools. Then, show that an 'admin' user can access the admin tool, while a 'user' cannot.

**Output:**

A Python script that demonstrates this dynamic, role-based tool loading for enhanced security.
