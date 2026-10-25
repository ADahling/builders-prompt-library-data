---
title: "Design a RESTful API for a Domain Application"
slug: design-a-restful-api-for-a-domain-application
stage: Build
category: "API Design"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-restful-api-for-a-domain-application
---
# Design a RESTful API for a Domain Application

Get a Markdown API design for your application's resources, including attributes, HTTP methods, URI patterns, and resource relationships.

Variables: domain, resource_1, resource_2, resource_3, attribute_1, attribute_2, attribute_3

## Prompt

I am building a {{domain}} application and I need to design a RESTful API for it. The application will have the following resources: {{resource_1}}, {{resource_2}}, and {{resource_3}}.

Your task is to design the API endpoints for these resources.

**Instructions:**
1.  **Resource Modeling:** Identify the attributes for each resource. For example, a '{{resource_1}}' resource might have attributes like '{{attribute_1}}', '{{attribute_2}}', and '{{attribute_3}}'.
2.  **Endpoint Design:** Define the HTTP methods (GET, POST, PUT, DELETE) and URI patterns for each resource. For example, what would be the endpoint to get all '{{resource_1}}'s by a specific user?
3.  **Relationships:** Show how to represent relationships between resources. For example, how would you fetch all '{{resource_2}}'s for a specific '{{resource_1}}'?

**Output Format:**
Provide the output as a Markdown document. For each resource, list the attributes and the corresponding API endpoints with their HTTP methods and URI patterns.
