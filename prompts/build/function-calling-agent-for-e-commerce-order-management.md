---
title: "Function Calling Agent for E-commerce Order Management"
slug: function-calling-agent-for-e-commerce-order-management
stage: Build
category: "AI Agent Development"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/function-calling-agent-for-e-commerce-order-management
---
# Function Calling Agent for E-commerce Order Management

Build a customer service agent that maps natural language requests to Python-based mock API functions for automated e-commerce order management.

Variables: order_id, customer_id

## Prompt

You are tasked with building an AI agent that can manage e-commerce orders through function calling. The agent will interact with a mock API that simulates an order management system.

**Core Functionality:**

The agent must be able to perform the following actions by calling predefined functions:

*   `get_order_status(order_id: str)`: Retrieves the status of a specific order.
*   `list_recent_orders(customer_id: str)`: Lists the 5 most recent orders for a customer.
*   `cancel_order(order_id: str)`: Cancels an order if it has not yet been shipped.

**Technical Stack:**

*   **Language:** Python
*   **LLM:** Use OpenAI's `GPT-5` or `GPT-5` with the function calling feature.
*   **API:** You will need to create a simple mock API using Flask or FastAPI that implements the three functions above.

**Agent's Role:**

The agent will act as a customer service chatbot. It will take natural language requests from users and translate them into the appropriate function calls.

**Example User Requests:**

*   "Where is my order #{{order_id}}?"
*   "Show me my recent orders. My customer ID is {{customer_id}}."
*   "I need to cancel order #{{order_id}}."

**Implementation Guide:**

1.  **Mock API:** Build the mock API with the specified endpoints.
2.  **Function Definitions:** Define the functions (`get_order_status
