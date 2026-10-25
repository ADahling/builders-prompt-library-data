---
title: "Correctly Format Time Durations and Relative Times Across Timezones"
slug: correctly-format-time-durations-and-relative-times-across-timezones
stage: Test
category: "Functional Bugs"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/correctly-format-time-durations-and-relative-times-across-timezones
---
# Correctly Format Time Durations and Relative Times Across Timezones

Implement timezone-aware relative date formatting to ensure "yesterday" and "today" labels align with the user's local midnight boundary.

Variables: project_name

## Prompt

You are a developer for {{project_name}}, a project management tool. The application displays how long ago a task was updated (e.g., "2 hours ago", "yesterday"). A bug is reported where the relative time is sometimes incorrect for users in different timezones. For example, a task is updated at 1:00 AM UTC on April 16th. A user in "America/Los_Angeles" (UTC-7) views this at 11:00 PM on April 15th their time. The UI incorrectly says "today" or "a few minutes ago" instead of "yesterday".

This is happening because the relative time calculation is naively comparing the server's current time with the timestamp, without considering the user's local timezone and their perception of "today" vs. "yesterday".

**Context:**
- **Library:** A date library like `date-fns` or `moment.js`.
- **Problem:** Relative time formatting is not timezone-aware.

**Buggy Relative Time Logic:**

```javascript
import { formatDistanceToNow } from 'date-fns';

const TaskItem = ({ task }) => {
  // task.updatedAt is a UTC timestamp string, e.g., "2024-04-16T01:00:00.000Z"
  const updatedAtDate = new Date(task.updatedAt);

  // This function compares the date to the browser's current time, but it can be misleading
  // for dates that cross the midnight boundary in the user's timezone.
  const timeAgo = formatDistanceToNow(updatedAtDate, { addSuffix: true });

  return <div>Updated {timeAgo}</div>;
};
```

**Instructions:**

1.  **Analyze the Relative Time Flaw:** Explain why simply comparing two points in time can produce a relative time string that feels wrong to the user, especially around the midnight boundary. The duration is technically correct, but the contextual day ("today", "yesterday") is wrong from the user's perspective.
2.  **Implement a Timezone-Aware Formatting Strategy:** Your solution should be to create a more intelligent formatting function. This function should:
    a. Determine the start of "today" and "yesterday" *in the user's local timezone*.
    b. Compare the task's update timestamp against these boundaries.
    c. If the update was today, use a relative format like "2 hours ago".
    d. If the update was yesterday, explicitly display "Yesterday at H:mm A".
    e. For all older dates, display the full date (e.g., "Apr 14, 2024").
3.  **Provide the Code:** Write a new React component, `TimezoneAwareTime

## Tips

A subtle UX bug that requires more than just a simple duration calculation; it requires contextual, timezone-aware formatting.
