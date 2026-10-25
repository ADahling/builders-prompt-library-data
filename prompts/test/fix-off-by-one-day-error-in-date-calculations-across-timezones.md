---
title: "Fix Off-by-One-Day Error in Date Calculations Across Timezones"
slug: fix-off-by-one-day-error-in-date-calculations-across-timezones
stage: Test
category: "Functional Bugs"
grade: A+
score: 99
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-off-by-one-day-error-in-date-calculations-across-timezones
---
# Fix Off-by-One-Day Error in Date Calculations Across Timezones

Debug and resolve off-by-one-day timezone errors by calculating precise UTC range boundaries for user-specific date reporting.

Variables: project_name, backend_language, database_name

## Prompt

You are a developer working on a reporting feature for {{project_name}}. A report is generated for "yesterday's sales". A user in San Francisco (UTC-7) runs the report on April 16th at 10:00 AM. They expect to see sales data for April 15th. However, the report is showing data for April 14th. 

This is happening because the server, which operates in UTC, calculates "yesterday" based on its own clock. At the time the report is run (April 16th, 5:00 PM UTC), "yesterday" on the server is April 15th. But the query to the database is using a simple date comparison that gets misinterpreted by timezone differences.

**Context:**
- **Backend:** {{backend_language}} script that generates the report.
- **Database:** {{database_name}}

**Buggy Report Generation Logic:**

```javascript
// Node.js example
const getYesterdaySales = (userTimezone) => {
  // This is the BUG. `new Date()` is the server's current time in UTC.
  const today = new Date();
  const yesterday = new Date(today);
  yesterday.setDate(today.getDate() - 1);

  // The date part is extracted, but the timezone context is lost or assumed.
  const yesterdayString = yesterday.toISOString().split('T')[0]; // e.g., "2024-04-15"

  // This query might be interpreted as "from the start of the day in the DB's timezone"
  const query = `SELECT * FROM sales WHERE DATE(sale_timestamp) = '${yesterdayString}';`;
  // ... run query ...
};
```

**Instructions:**

1.  **Analyze the Timezone Mismatch:** Explain step-by-step how the server's UTC date calculation combined with a naive date query leads to the off-by-one-day error for a user in a western timezone.
2.  **Implement a Timezone-Aware Date Calculation:** Rewrite the logic to correctly determine the start and end of "yesterday" *in the user's timezone*. You must use a robust date library like `date-fns-tz` or `luxon` to handle this. The output should be two UTC ISO 8601 strings representing the exact start and end of the user's "yesterday".
3.  **Correct the Database Query:** Modify the database query to use a `BETWEEN` clause with the two UTC timestamps you generated. This ensures the query is precise and not subject to implicit timezone conversions by the database.

**Output Format:**

- **Mismatch Analysis:** A detailed breakdown of the off-by-one-day bug.
- **Corrected Date Calculation Logic:** The new code that correctly calculates the UTC start and end times for the user's "yesterday".
- **Corrected Database Query:** The updated, timezone-safe SQL query.

## Tips

A very common and tricky bug related to date-based reporting across different timezones.
