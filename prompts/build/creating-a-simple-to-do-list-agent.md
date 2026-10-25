---
title: "Creating a Simple 'To-Do List' Agent"
slug: creating-a-simple-to-do-list-agent
stage: Build
category: "AI Agent Development"
grade: B
score: 72
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-simple-to-do-list-agent
---
# Creating a Simple 'To-Do List' Agent

Get a Python ReAct agent script and interaction transcript for managing an in-memory to-do list with add, list, and remove tools.

## Prompt

Build a simple, stateful agent that can manage a to-do list. The agent should be able to add items, list items, and mark items as complete.

**Agent's State:**

The agent's state will be a simple list of strings representing the to-do items.

**Agent's Tools:**

1.  `add_item(item: str)`: Adds a new item to the list.
2.  `list_items()`: Returns the current list of items.
3.  `remove_item(item: str)`: Removes an item from the list.

**Implementation:**

*   You can implement this with a custom Python class that holds the list in memory.
*   Create a ReAct agent and provide it with the three tools.
*   The tool functions will modify the list held by your class.

**Example Interaction:**

*   User: "Add 'buy milk' to my list."
*   User: "Add 'walk the dog'."
*   User: "What's on my list?"
*   Agent: "Your to-do list: ['buy milk', 'walk the dog']"
*   User: "I finished walking the dog."
*   Agent: (Calls `remove_item('walk the dog')`)

**Your Task:**

Write a Python script that defines the to-do list class, the tools, and the agent. The script should then run through a series of interactions to demonstrate the agent's functionality.

**Output:**

A Python script and a transcript of the interaction.
