---
title: "Design an API for a Weather App"
slug: design-an-api-for-a-weather-app-name-weather-app
stage: Build
category: "API Design"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-weather-app-name-weather-app
---
# Design an API for a Weather App

Get a RESTful API design to wrap your weather data source, with methods, URIs, and request/response formats for conditions, forecasts, and locations.

Variables: weather_app_name

## Prompt

I am building a weather app called {{weather_app_name}}. I need to design an API that provides weather data.

Your task is to design the API for the weather app.

**Instructions:**
1.  **Data Source:** Assume you have a source for weather data. Your API will act as a facade for this data source.
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   Getting the current weather for a specific location.
    *   Getting the weather forecast for the next few days for a specific location.
    *   Searching for locations.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoint, including the HTTP method, URI, and request/response format.
