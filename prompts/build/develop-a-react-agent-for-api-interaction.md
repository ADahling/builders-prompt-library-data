---
title: "Develop a ReAct Agent for API Interaction"
slug: develop-a-react-agent-for-api-interaction
stage: Build
category: "AI Agent Development"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/develop-a-react-agent-for-api-interaction
---
# Develop a ReAct Agent for API Interaction

Create a Python-based AI agent that uses the ReAct Reasoning and Acting framework to interact with a public API.

Variables: city

## Prompt

Create a Python-based AI agent that uses the ReAct (Reasoning and Acting) framework to interact with a public API. The agent should be able to understand a user's request, choose the correct API endpoint to call, and process the response to answer the user's query.

**Scenario:**

The agent will act as a weather information assistant. It will use the OpenWeatherMap API to fetch weather data.

**Agent Requirements:**

1.  **Framework:** Use LangChain to build the ReAct agent.
2.  **Tools:** Define two tools for the agent:
    *   `get_current_weather`: Takes a city name as input and returns the current weather conditions (temperature, humidity, description).
    *   `get_weather_forecast`: Takes a city name and a number of days (1-5) as input and returns the weather forecast for that period.
3.  **Agent Logic:** The agent needs to parse the user's natural language request to determine:
    *   The desired city.
    *   Whether the user wants the current weather or a forecast.
    *   If a forecast, for how many days.
4.  **Output:** The agent should provide a clear, human-readable summary of the weather information.

**Input:**

*   A natural language query, such as:
    *   "What's the weather like in {{city}} right now?"
    *   "Can I get a 3-day forecast for {{city}}?"

**Constraints:**

*   You will need an API key from OpenWeatherMap.
*   The agent should handle cases where the city is not found or the API call fails.
*   The code should be modular, with clear separation between the agent definition, tool implementations, and the main execution logic.
