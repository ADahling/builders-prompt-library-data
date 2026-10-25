---
title: "Generate a Database Seeding Script for a New Environment"
slug: generate-a-database-seeding-script-for-a-new-environment
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 75
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-database-seeding-script-for-a-new-environment
---
# Generate a Database Seeding Script for a New Environment

Get an idempotent staging database seed script with varied test data, dependency handling, volume recommendations, and an execution plan.

Variables: application_name, scripting_language

## Prompt

We are setting up a new staging environment for our {{application_name}} application, and we need to populate the database with realistic test data. The database schema is already in place, but the tables are empty. I need a script to seed the database with a variety of data to support our testing efforts.

Your task is to generate a database seeding script and a plan for using it. This should include:

1.  **Data Generation Strategy:** A strategy for generating realistic and varied test data. This should involve creating a mix of valid and invalid data to test different scenarios. You can use a library like Faker.js or a similar tool for your language.
2.  **Seeding Script:** A well-documented script in {{scripting_language}} that populates the key tables in our database. The script should be idempotent, meaning it can be run multiple times without creating duplicate data.
3.  **Handling Dependencies:** A plan for handling dependencies between tables. For example, you need to create users before you can create posts by those users.
4.  **Data Volume:** A recommendation for the volume of data to generate for each table. This should be enough to support meaningful testing but not so much that it slows down the environment.
5.  **Execution Plan:** A plan for how and when to run the seeding script. This might be as part of the environment setup process or as a manual step for testers.

## Tips

This prompt is a common task for developers when setting up new development or testing environments.
