---
title: "Creating a Meeting Summarization Agent"
slug: creating-a-meeting-summarization-agent
stage: Build
category: "AI Agent Development"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-meeting-summarization-agent
---
# Creating a Meeting Summarization Agent

Build a meeting transcript summarization prompt for JSON output covering the meeting summary, key decisions, and action items with named owners.

Variables: transcript

## Prompt

Build an AI agent that can take the transcript of a meeting and produce a concise summary, including key decisions and action items.

**Agent's Task:**

Given a long meeting transcript (`{{transcript}}`), the agent should extract:
1.  A brief, one-paragraph summary of the meeting's purpose and outcome.
2.  A bulleted list of key decisions made.
3.  A bulleted list of action items, with the assigned person for each (if mentioned).

**Implementation:**

This is a prompt engineering task that requires a structured output.

*   **The Prompt:**
    *   **Role:** "You are an expert executive assistant who excels at summarizing meetings."
    *   **Task:** "Analyze the following meeting transcript and extract the summary, key decisions, and action items."
    *   **Input:** Provide the `{{transcript}}`.
    *   **Output Format:** "Your output must be a JSON object with three keys: `summary
