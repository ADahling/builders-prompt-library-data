---
title: "Design an API for a Recipe App"
slug: design-an-api-for-a-recipe-app-name-recipe-app
stage: Build
category: "API Design"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-recipe-app-name-recipe-app
---
# Design an API for a Recipe App

Get a RESTful API design for a recipe app, with endpoints and request/response formats for creating, sharing, saving, searching, and reviewing recipes.

Variables: recipe_app_name

## Prompt

I am building a recipe app called {{recipe_app_name}}. I need to design the API for it.

Your task is to design the core API for the recipe app.

**Instructions:**
1.  **Core Resources:** Identify the core resources of the app (e.g., users, recipes, ingredients, reviews).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   Users can create, share, and save recipes.
    *   Users can search for recipes by ingredients or keywords.
    *   Users can review and rate recipes.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoints, including the HTTP methods, URIs, and request/response formats.
