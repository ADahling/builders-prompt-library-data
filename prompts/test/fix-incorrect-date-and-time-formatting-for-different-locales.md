---
title: "Fix Incorrect Date and Time Formatting for Different Locales"
slug: fix-incorrect-date-and-time-formatting-for-different-locales
stage: Test
category: "Functional Bugs"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-incorrect-date-and-time-formatting-for-different-locales
---
# Fix Incorrect Date and Time Formatting for Different Locales

Refactor hardcoded date formatting into a reusable, locale-aware component using the Intl.DateTimeFormat API to improve internationalization.

Variables: project_name, tech_stack

## Prompt

You are a developer for {{project_name}}, a blog platform. The publication date of an article is being displayed as "4/16/2024". This format (MM/DD/YYYY) is common in the US but is confusing for users in Europe, who expect "16/04/2024" (DD/MM/YYYY) or another local format.

This is happening because the date is being formatted with a simple, hardcoded string manipulation instead of a locale-sensitive API.

Your task is to create a flexible date formatting component using the `Intl.DateTimeFormat` API.

**Context:**
- **Problem:** Date formats are not adapting to the user's locale.

**Instructions:**

1.  **Analyze the Date Formatting Bug:** Explain why hardcoding a date format like MM/DD/YYYY is a significant internationalization bug.
2.  **Create a `FormattedDate` Component:** Write a reusable component (e.g., for {{tech_stack}}) named `FormattedDate`. This component should accept a `Date` object as a prop.
3.  **Use `Intl.DateTimeFormat`:** Inside the component, use the `Intl.DateTimeFormat` API to format the date. You should get the user's locale (e.g., from the browser) and pass it to the formatter. Also, provide options to format the date in different styles (e.g., `short

## Tips

Another practical application of the `Intl` API, focusing on dates and component reusability.
