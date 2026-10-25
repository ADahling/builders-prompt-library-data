---
title: "Resolve Incorrect Time Input from a User's Local Time"
slug: resolve-incorrect-time-input-from-a-user-s-local-time
stage: Test
category: "Functional Bugs"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-incorrect-time-input-from-a-user-s-local-time
---
# Resolve Incorrect Time Input from a User's Local Time

Correct timezone synchronization by capturing user offsets on the frontend and converting them to UTC on the backend for accurate storage.

Variables: project_name, tech_stack, backend_framework

## Prompt

You are a developer for {{project_name}}, a booking application. A user selects "3:00 PM" from a time picker on the frontend. The user is in the "America/New_York" timezone (EDT, UTC-4). The frontend sends this time to the backend as a string, "15:00:00". The backend, running in UTC, combines this time with today's date and saves it, assuming it's a UTC time. This results in the appointment being saved for 3:00 PM UTC, which is 11:00 AM in the user's local time—four hours earlier than intended.

Your task is to fix the communication between the client and server to ensure the user's local time is interpreted correctly.

**Context:**
- **Frontend:** {{tech_stack}} application with a time picker input.
- **Backend:** {{backend_framework}} API.

**Instructions:**

1.  **Identify the Ambiguity:** Explain why sending just a time string like "15:00:00" is ambiguous and leads to incorrect data storage.
2.  **Frontend Fix: Send Timezone Information:** Modify the frontend logic. When the user picks a time, the frontend must also send the user's IANA timezone name (e.g., "America/New_York") along with the date and time to the backend. You can get this from the browser using `Intl.DateTimeFormat().resolvedOptions().timeZone`.
3.  **Backend Fix: Interpret Time with Timezone:** Modify the backend endpoint. It should now expect the date, time, and timezone as input. Use a server-side date library (like `date-fns-tz` for Node.js, `pytz` or `zoneinfo` for Python) to combine these three pieces of information into a correct UTC timestamp for storage in the database.

**Output Format:**

- **Ambiguity Analysis:** A clear explanation of the problem.
- **Frontend Code Snippet:** The frontend code showing how to get the user's timezone and include it in the API request payload.
- **Backend Code Snippet:** The backend code showing how to parse the local time with the provided timezone and convert it to UTC.

## Tips

Focuses on the critical step of capturing the user's timezone during input to resolve ambiguity.
