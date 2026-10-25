---
title: "Debug Recurring Event Logic Failing Across Daylight Saving Time Changes"
slug: debug-recurring-event-logic-failing-across-daylight-saving-time-changes
stage: Test
category: "Functional Bugs"
grade: A
score: 86
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-recurring-event-logic-failing-across-daylight-saving-time-changes
---
# Debug Recurring Event Logic Failing Across Daylight Saving Time Changes

Fix broken recurring event logic by implementing timezone-aware calculations that preserve consistent local times across DST transitions.

Variables: project_name

## Prompt

You are a senior engineer for {{project_name}}, a calendar application. The app has a feature for creating weekly recurring events. A user in a region that observes Daylight Saving Time (DST), such as "Europe/Berlin", creates a weekly event for every Wednesday at 9:00 AM. The event works correctly for weeks, but when DST starts or ends, the event time shifts by one hour (e.g., it suddenly appears at 8:00 AM or 10:00 AM).

This is because the application is calculating the next occurrence by simply adding exactly 7 days (in milliseconds or seconds) to the previous UTC timestamp. This does not account for the fact that the local time offset changes during a DST transition.

**Context:**
- **Feature:** Weekly recurring events.
- **Problem:** DST transitions break the local time consistency.

**Instructions:**

1.  **Analyze the DST Calculation Flaw:** Explain in detail why adding a fixed duration (like `7 * 24 * 60 * 60 * 1000` milliseconds) to a UTC timestamp fails to preserve the local time for a recurring event across a DST boundary.
2.  **Propose a Robust Recurrence Strategy:** Design a strategy that correctly calculates the next occurrence. The key is to work with the *local* date and time components in the target timezone. The process should be:
    a. Take the last event's date.
    b. Add 7 days to the local date components (year, month, day).
    c. Create the new event at the *same local time* (e.g., 9:00 AM) on that new date, within the original timezone.
    d. Convert this new local datetime back to UTC for storage.
3.  **Provide a Code Example:** Using a powerful, timezone-aware date library like `luxon` or `date-fns-tz

## Tips

A notoriously difficult bug that requires a deep understanding of how DST works and how to handle it programmatically.
