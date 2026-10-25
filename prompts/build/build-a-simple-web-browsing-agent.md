---
title: "Build a Simple Web Browsing Agent"
slug: build-a-simple-web-browsing-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-simple-web-browsing-agent
---
# Build a Simple Web Browsing Agent

Get a Python LangChain agent script that fetches webpage text and uses an LLM to answer a user's question about a specified URL.

Variables: url, question

## Prompt

Create a basic AI agent that can browse the web to answer a user's question. The agent will use a tool to fetch the content of a webpage and an LLM to extract the answer from that content.

**Agent's Goal:**

To answer a question like, "What is the main product of the company at {{url}}?"

**Core Components:**

1.  **Web Fetcher Tool:**
    *   Create a tool that takes a URL as input and returns the text content of the webpage. You can use libraries like `requests` and `BeautifulSoup` to achieve this.
    *   The tool should strip out HTML tags to get clean text.
2.  **LLM:**
    *   Use a conversational LLM (e.g., `ChatOpenAI`).
3.  **Agent Logic (Prompt):**
    *   You will create a prompt that instructs the LLM on how to use the tool.
    *   The prompt should be something like: "You have a tool to read a webpage. Use it to find the answer to the user's question. The user's question is: '{{question}}'. The URL is: '{{url}}'."
    *   You will then need to combine this with a ReAct-style prompt to guide the agent.

**Implementation Steps:**

1.  Implement the `web_fetcher` tool in Python.
2.  Define your agent using LangChain. You can use the `initialize_agent` function for simplicity.
3.  Pass the `web_fetcher` tool to the agent.
4.  Run the agent with a URL and a question.

**Output:**

A Python script that defines the tool and the agent, and then runs it to answer a question about a given URL.
