---
title: "Incorrect Date Displayed Due to Naive Timezone Handling"
slug: incorrect-date-displayed-due-to-naive-timezone-handling
stage: Test
category: "Functional Bugs"
grade: A+
score: 90
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/incorrect-date-displayed-due-to-naive-timezone-handling
---
# Incorrect Date Displayed Due to Naive Timezone Handling

Refactor a full-stack event scheduling workflow to handle timezone conversions by storing UTC in the database and rendering local times.

Variables: project_name, backend_framework, database_type, frontend_framework

## Prompt

You are a developer for {{project_name}}, a global event scheduling application. A user in London (UTC+1, during BST) creates an event for "July 15, 2024, 10:00 AM". A user in New York (UTC-4, during EDT) views the event, but the time is incorrectly displayed as "July 15, 2024, 10:00 AM" instead of the correct, converted time of "July 15, 2024, 5:00 AM".

This is because the backend is storing the date and time as a naive string (e.g., "2024-07-15 10:00:00") without any timezone information, and the frontend is displaying it directly.

Your task is to fix this entire workflow to be timezone-aware.

**Context:**
- **Backend:** {{backend_framework}} API with a {{database_type}} database.
- **Frontend:** {{frontend_framework}} application.

**Instructions:**

1.  **Explain the Core Problem:** Describe why storing and transmitting naive datetimes is a critical bug for a global application.
2.  **Propose a Backend Solution:** Your primary recommendation should be to store all datetimes in the database as UTC. Show how to modify the backend code that saves the event to ensure the incoming local time from the user is converted to and stored as UTC. The user's timezone should be sent with the request.
3.  **Propose a Frontend Solution:** On the frontend, when displaying the event time, you must convert the UTC time received from the API into the viewing user's local timezone. Show how to do this using a library like `date-fns-tz

## Tips

The most fundamental timezone bug. This prompt establishes the best practice of 'Store in UTC, display in local time'.
