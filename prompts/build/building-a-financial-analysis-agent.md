---
title: "Building a Financial Analysis Agent"
slug: building-a-financial-analysis-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-financial-analysis-agent
---
# Building a Financial Analysis Agent

Get a Python script for a financial analysis agent with stock, news, and metrics tools, plus an example company report with data citations.

Variables: company_ticker

## Prompt

Create an AI agent designed to perform financial analysis on a given company. The agent should be able to retrieve stock prices, read recent news, and summarize the company's financial health.

**Agent Capabilities:**

1.  **Stock Price Tool:** A tool that takes a ticker symbol (e.g., "AAPL") and returns the current stock price and daily change. You can mock this or use a free API like Yahoo Finance (yfinance).
2.  **News Tool:** A tool that searches for recent news articles about the company.
3.  **Financial Summary Tool:** A tool that retrieves basic financial metrics (e.g., P/E ratio, market cap).

**Agent Workflow:**

*   The user asks a question like: "Give me a financial overview of {{company_ticker}}."
*   The agent should use its tools to gather the necessary data.
*   It should then synthesize this data into a coherent report.

**Implementation:**

*   Use LangChain to build a ReAct agent.
*   Define the three tools described above.
*   Write a system prompt that instructs the agent to act as a professional financial analyst. The prompt should emphasize accuracy and the need to cite the data it retrieves.

**Output:**

A Python script containing the agent and tool definitions, along with an example of the agent generating a report for a specific ticker symbol.
