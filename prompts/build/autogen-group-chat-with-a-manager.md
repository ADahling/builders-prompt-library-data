---
title: "AutoGen: Group Chat with a Manager"
slug: autogen-group-chat-with-a-manager
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/autogen-group-chat-with-a-manager
---
# AutoGen: Group Chat with a Manager

Set up an AutoGen group chat where a manager coordinates blogger, researcher, and critic agents to draft and review a blog post on a chosen topic.

Variables: topic

## Prompt

Set up a group chat simulation using AutoGen where multiple agents collaborate on a task under the supervision of a manager. This is a powerful pattern for solving complex, multi-step problems.

**Scenario:**

A team of agents needs to write a blog post about a given topic, `{{topic}}`.

**Agent Roles:**

1.  **Blogger Agent:** Specializes in writing blog posts. Knows how to structure a post with an introduction, body, and conclusion.
2.  **Researcher Agent:** Specializes in finding facts and data. Can use a (mock) search tool.
3.  **Critic Agent:** Reviews the blog post for quality, clarity, and factual accuracy.

**Group Chat Setup:**

*   **Manager:** Use `autogen.GroupChatManager` to orchestrate the conversation.
*   **Group Chat:** Create a `autogen.GroupChat` and add all the agents (Blogger, Researcher, Critic) to it.
*   **Initiator:** The user (via a `UserProxyAgent`) will kick off the chat by asking the manager to "Write a blog post about {{topic}}."

**Workflow:**

1.  The manager receives the request and starts the group chat.
2.  The Blogger might start with a draft or an outline.
3.  The Researcher would then be called upon (or chime in) to provide facts and sources.
4.  The Blogger incorporates the research into the post.
5.  The Critic reviews the draft and provides feedback.
6.  The conversation continues until the manager determines that the task is complete (e.g., the Critic is satisfied).

**Your Task:**

Write a Python script using AutoGen to set up and run this group chat. You will need to:

*   Define each `AssistantAgent` with its specific role and instructions.
*   Create the `GroupChat` and `GroupChatManager`.
*   Initiate the chat with the user's request.

**Output:**

The Python script and the full conversation transcript from the group chat, showing how the agents collaborated.
