---
title: "Design a RESTful API for a Task Management System"
slug: design-a-restful-api-for-a-task-management-system
stage: Build
category: "API Design"
grade: B
score: 73
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-restful-api-for-a-task-management-system
---
# Design a RESTful API for a Task Management System

Design a task management REST API with task creation, retrieval, updates, deletion, optional list filters, and success and error status codes.

Variables: status, title, description

## Prompt

Design a RESTful API for a task management system. The API should support the following endpoints: 
- `GET /tasks`: Retrieve a list of tasks with optional filtering by {{status}} and {dueDate}.
- `POST /tasks`: Create a new task with the required fields {{title}}, {{description}}, and {dueDate}.
- `GET /tasks/{taskId}`: Retrieve details of a specific task by {taskId}.
- `PUT /tasks/{taskId}`: Update a specific task identified by {taskId} with optional fields {{title}}, {{description}}, and {{status}}.
- `DELETE /tasks/{taskId}`: Delete a specific task by {taskId}. 
Include proper HTTP status codes for success and error cases.

## Tips

Use this prompt to create a structured outline for your API, taking care to define the request and response formats.
