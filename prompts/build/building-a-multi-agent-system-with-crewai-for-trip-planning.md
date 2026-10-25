---
title: "Building a Multi-Agent System with CrewAI for Trip Planning"
slug: building-a-multi-agent-system-with-crewai-for-trip-planning
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-multi-agent-system-with-crewai-for-trip-planning
---
# Building a Multi-Agent System with CrewAI for Trip Planning

Build a hierarchical CrewAI crew with travel, culture, and logistics agents to plan a seven-day trip around interests and a budget.

Variables: destination, interests, budget

## Prompt

Create a multi-agent crew using CrewAI to plan a detailed travel itinerary. This showcases CrewAI's strength in orchestrating specialized agents for a collaborative goal.

**The Crew:**

1.  **Travel Agent:**
    *   **Role:** "Expert Travel Planner"
    *   **Goal:** "Create a 7-day travel itinerary for {{destination}}, considering the user's interests in {{interests}}."
    *   **Backstory:** "You are a world-class travel agent known for creating unique and memorable travel experiences."
2.  **Local Culture Expert:**
    *   **Role:** "Local Culture and Food Guide"
    *   **Goal:** "Find the best local restaurants and cultural attractions in {{destination}}."
    *   **Backstory:** "You are a local resident of {{destination}} with a passion for sharing your city's hidden gems."
3.  **Logistics Coordinator:**
    *   **Role:** "Logistics and Booking Manager"
    *   **Goal:** "Find flight and hotel options that fit a budget of {{budget}}."
    *   **Backstory:** "You are a meticulous planner who excels at finding the best deals on travel and accommodation."

**Your Task:**

1.  Define the three agents with their detailed personas.
2.  Define tasks for each agent that contribute to the overall plan.
3.  Create a `Crew` and set the process to `hierarchical
