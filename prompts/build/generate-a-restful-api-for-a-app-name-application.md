---
title: "Generate a RESTful API for an Application"
slug: generate-a-restful-api-for-a-app-name-application
stage: Build
category: "API Design"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-restful-api-for-a-app-name-application
---
# Generate a RESTful API for an Application

Design a RESTful API for your application's core resources with data models, CRUD endpoints, resource relationships, and consistent error responses.

Variables: app_name, resource_1, resource_2, resource_3, user_type, user_action, attribute_1, attribute_2, attribute_3, resource_plural, resource_2_plural

## Prompt

I am building a {{app_name}} application and need a well-structured RESTful API. The core resources are {{resource_1}}, {{resource_2}}, and {{resource_3}}. The application will be used by {{user_type}} to {{user_action}}.

Your task is to generate a complete RESTful API design for this application.

**Instructions:**
1.  **Resource Modeling:** For each resource ({{resource_1}}, {{resource_2}}, {{resource_3}}), define the data model with relevant attributes. For example, for {{resource_1}}, you might have attributes like {{attribute_1}}, {{attribute_2}}, and {{attribute_3}}.
2.  **Endpoint Design:** Define the full set of RESTful endpoints for each resource, including:
    *   `GET /{{resource_plural}}` (List)
    *   `POST /{{resource_plural}}` (Create)
    *   `GET /{{resource_plural}}/{id}` (Retrieve)
    *   `PUT /{{resource_plural}}/{id}` (Update)
    *   `DELETE /{{resource_plural}}/{id}` (Delete)
3.  **Relationships:** Define how to represent and query relationships between the resources. For example, how would a user retrieve all {{resource_2_plural}} associated with a specific {{resource_1}}?
4.  **Error Handling:** Specify a consistent error response format, including error codes and messages for common issues like invalid input or resource not found.

**Output Format:**
Provide the output as a Markdown document. For each resource, provide the data model and the full list of API endpoints with their HTTP methods, URI patterns, and a brief description. Include a section on the error handling strategy with example error responses.
