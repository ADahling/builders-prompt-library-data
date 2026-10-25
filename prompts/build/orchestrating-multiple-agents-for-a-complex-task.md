---
title: "Orchestrating Multiple Agents for a Complex Task"
slug: orchestrating-multiple-agents-for-a-complex-task
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/orchestrating-multiple-agents-for-a-complex-task
---
# Orchestrating Multiple Agents for a Complex Task

Get a Python script simulating travel-planning agents that coordinate flight searches, hotel bookings, and activities into a single itinerary.

Variables: destination, budget

## Prompt

Design a system where multiple AI agents collaborate to plan a travel itinerary. This task requires orchestrating the agents to work together, with each agent specializing in a different part of the planning process.

**Agent Team:**

1.  **Trip Planner Agent:** The main coordinator. It takes the user's high-level request (e.g., "Plan a 5-day trip to {{destination}} for a budget of {{budget}}") and breaks it down into sub-tasks for the other agents.
2.  **Flight Search Agent:** Specializes in finding flights. It has a tool to search a flight API (you can mock this) for the best deals.
3.  **Hotel Booking Agent:** Specializes in finding accommodation. It has a tool to search a hotel booking API.
4.  **Activity Suggester Agent:** Finds interesting activities and attractions at the destination.

**Orchestration Logic:**

*   The Trip Planner agent is the entry point.
*   It first calls the Flight Search Agent to find suitable flights.
*   Once flights are found, it calls the Hotel Booking Agent to find a hotel for the selected dates.
*   While the hotel is being booked, it can concurrently call the Activity Suggester Agent.
*   Finally, the Trip Planner agent consolidates all the information (flight details, hotel booking confirmation, and a list of suggested activities) into a single, coherent itinerary.

**Your Task:**

Write a Python script that simulates this orchestration. You don't need to connect to real APIs, but you should:

*   Define each agent, its specialization, and its tools (as mock functions).
*   Implement the orchestration logic that controls the flow of information between the agents.
*   Consider using a framework like LangGraph or CrewAI to manage the state and flow, or implement the logic manually.

**Output:**

A final travel itinerary in Markdown format, which is the result of the agents' collaboration.
