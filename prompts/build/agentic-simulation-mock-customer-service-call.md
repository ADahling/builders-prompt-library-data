---
title: "Agentic Simulation: Mock Customer Service Call"
slug: agentic-simulation-mock-customer-service-call
stage: Build
category: "AI Agent Development"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-simulation-mock-customer-service-call
---
# Agentic Simulation: Mock Customer Service Call

Get a Python script and conversation transcript simulating two agents handling an order status inquiry with a mock lookup tool.

Variables: order_id

## Prompt

Create a simulation of a customer service interaction between two AI agents: a "Customer" agent and a "Support" agent.

**The Scenario:**

The Customer agent wants to inquire about the status of an order.

**Agent Roles:**

1.  **Customer Agent:**
    *   **Persona:** Slightly impatient, wants a quick answer.
    *   **Goal:** To find out the shipping status of order #{{order_id}}.
    *   **Initial Message:** "Hi, I want to know where my order is."
2.  **Support Agent:**
    *   **Persona:** Polite, helpful, and follows a script.
    *   **Tools:** Has a (mock) tool called `get_order_status(order_id: str)` which can return "Shipped", "Processing", or "Delivered".
    *   **Logic:** It must first ask for the order ID before it can use its tool.

**The Simulation Loop:**

1.  Initialize both agents (they can be simple LLM chains with different system prompts).
2.  The Customer agent starts the conversation.
3.  The Support agent responds. It should ask for the order ID.
4.  The Customer agent provides the order ID.
5.  The Support agent receives the ID, calls its tool, gets the status, and provides the final answer to the customer.

**Your Task:**

Write a Python script that orchestrates this turn-by-turn conversation between the two agents.

**Output:**

A Python script and the full transcript of the simulated conversation.
