---
title: "Stateful Agents in LangGraph"
slug: stateful-agents-in-langgraph
stage: Build
category: "AI Agent Development"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/stateful-agents-in-langgraph
---
# Stateful Agents in LangGraph

Build a LangGraph counter agent with increment and decrement tools, LLM tool selection, and a looping graph to demonstrate state across turns.

## Prompt

Illustrate the concept of a stateful agent using LangGraph. You will build a simple agent that maintains a counter in its state and can be instructed to increment or decrement it.

**State Definition:**

The state of your graph will be a simple dictionary or Pydantic model with one field: `counter: int`.

**Agent's Tools:**

1.  `increment_counter`: A tool that takes an integer `value` and adds it to the counter in the state.
2.  `decrement_counter`: A tool that takes an integer `value` and subtracts it from the counter.

**Graph Structure:**

1.  **Agent Node:** This is the main node where the agent logic resides. It takes the user's input and the current state, decides which tool to call, and executes it.
2.  **State Update:** After the tool is executed, the node should update the `counter` in the state.
3.  **Loop:** The graph should be a simple loop. After the agent node runs, it should transition back to itself, allowing for a continuous conversation where the state is preserved.

**Your Task:**

*   Define the state model.
*   Implement the two tool functions.
*   Create the agent node function that takes the state, calls the LLM to decide on a tool, and returns the updated state.
*   Build the `StatefulGraph` and add the agent node and the edge that loops back to itself.
*   Compile the graph and run it for a few turns to show that it remembers the counter's value.

**Example Interaction:**

*   User: "Increment the counter by 5." (State becomes `{'counter': 5}`)
*   User: "Add 2 more." (State becomes `{'counter': 7}`)
*   User: "Now decrement by 3." (State becomes `{'counter': 4}`)

**Output:**

A Python script that implements this stateful counter agent.
