---
title: "Creating a Data Import API"
slug: creating-a-data-import-api
stage: Build
category: "API Design"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-data-import-api
---
# Creating a Data Import API

Design a bulk data import API outline with import and status endpoints, error handling, and storage considerations for large data sets.

Variables: source, data

## Prompt

Outline an API for importing bulk data into your application. Include endpoints for:
- {POST /import}: Initiating a data import process with fields {{source}}, {userId}, and {{data}}. 
- {GET /import/status}: Retrieving the status of an ongoing import.
- Discuss error handling and storage considerations for large data sets.

## Tips

This prompt will help streamline data management processes in your application.
