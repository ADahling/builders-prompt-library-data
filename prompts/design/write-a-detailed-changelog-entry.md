---
title: "Write a Detailed Changelog Entry"
slug: write-a-detailed-changelog-entry
stage: Design
category: "Documentation"
grade: A+
score: 98
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-detailed-changelog-entry
---
# Write a Detailed Changelog Entry

Generate a standardized Markdown changelog entry that organizes new features, fixes, and improvements into a clear, user-focused summary.

Variables: version_number, new_feature, bug_description, improved_component

## Prompt

You are a software developer who has just completed a new feature for your project. Now, you need to write a clear and informative changelog entry to communicate the changes to your users.

Your task is to write a changelog entry for version {{version_number}} of your project. The changelog should follow the "Keep a Changelog" format and include the following sections:

*   **Added:** For new features.
*   **Changed:** For changes in existing functionality.
*   **Deprecated:** For soon-to-be-removed features.
*   **Removed:** For now-removed features.
*   **Fixed:** For any bug fixes.
*   **Security:** In case of vulnerabilities.

Here are the changes that were made in this version:

*   **New Feature:** Added support for {{new_feature}}.
*   **Bug Fix:** Fixed a bug where {{bug_description}}.
*   **Improvement:** Improved the performance of {{improved_component}}.

Generate the complete changelog entry in Markdown format. The language should be clear, concise, and user-focused.
