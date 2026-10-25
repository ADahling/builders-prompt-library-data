---
title: "Autonomous Coding Agent for Bug Fixing"
slug: autonomous-coding-agent-for-bug-fixing
stage: Build
category: "AI Agent Development"
grade: B
score: 73
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/autonomous-coding-agent-for-bug-fixing
---
# Autonomous Coding Agent for Bug Fixing

Build a Python bug-fixing agent that analyzes errors, proposes patches, writes a separate corrected file, and reruns it in a verification loop.

Variables: file_path, error_message

## Prompt

Create an autonomous AI agent that can identify and fix bugs in a given Python code file. The agent should be able to read the code, understand the error, propose a fix, apply it, and verify that the fix works.

**Agent Workflow:**

1.  **Code Analysis:** The agent receives a path to a Python file (`{{file_path}}`) and the error message (`{{error_message}}`) produced when running it.
2.  **Error Understanding:** The agent must analyze the error message and the corresponding code to understand the root cause of the bug.
3.  **Fix Proposal:** Based on its analysis, the agent should generate a proposed fix. This could involve adding, removing, or modifying lines of code.
4.  **Code Patching:** The agent should apply the proposed fix to the original file. It's best to create a new, patched file to avoid overwriting the original.
5.  **Verification:** The agent must then run the patched file to see if the error is resolved. If the error persists or a new one appears, it should loop back to step 2 to re-analyze and propose a new fix.
6.  **Output:** Once the bug is fixed, the agent should output the path to the corrected file and a brief explanation of the fix.

**Tools and Techniques:**

*   **LLM:** Use a powerful coding model like `GPT-5` or `Claude Opus 4.8` for the reasoning and code generation parts.
*   **File I/O:** The agent will need tools to read and write files.
*   **Shell Access:** The agent needs to be able to execute the Python script to verify the fix. This can be done using a `subprocess` call in Python.

**Input:**

*   `{{file_path}}`: The absolute path to the buggy Python file.
*   `{{error_message}}`: The full traceback of the error.

This is a complex task that requires a robust agent design. Consider using a framework like LangChain or AutoGen to manage the agent's state and tool use.
