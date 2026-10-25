---
title: "Hardcoded UI Strings Preventing Translation"
slug: hardcoded-ui-strings-preventing-translation
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/hardcoded-ui-strings-preventing-translation
---
# Hardcoded UI Strings Preventing Translation

Refactor hardcoded strings into an i18n framework to enable multi-language support through translation keys and structured JSON files.

Variables: project_name, tech_stack, library_name

## Prompt

You are an internationalization (i18n) engineer working on {{project_name}}, a web application that is being prepared for a global launch. The application is built with {{tech_stack}}, but many components contain hardcoded English strings directly in the JSX/HTML, making it impossible to translate the UI for different locales.

Your task is to refactor a component to remove hardcoded strings and replace them with a translation function provided by an i18n library like {{library_name}} (e.g., react-i18next, vue-i18n).

**Context:**
- **Library:** {{library_name}}
- **Problem:** Hardcoded text in the UI.

**Component with Hardcoded Strings:**

```javascript
const UserProfile = ({ user }) => {
  return (
    <div>
      <h1>User Profile</h1>
      <p>Name: {user.name}</p>
      <button>Edit Profile</button>
      <a href="/settings">Go to Settings</a>
    </div>
  );
};
```

**Instructions:**

1.  **Explain the Problem:** Describe why hardcoding text is a major blocker for internationalization and how i18n libraries solve this problem using translation keys and JSON files.
2.  **Create a Translation File:** Create a sample JSON translation file (e.g., `en.json`) that contains the key-value pairs for the strings in the `UserProfile` component (e.g., `"userProfileTitle": "User Profile"`).
3.  **Refactor the Component:** Rewrite the `UserProfile` component to use the `t()` translation function from {{library_name}}. Replace every hardcoded string with a call to `t("yourTranslationKey")`.

**Output Format:**

- **Problem Explanation:** A summary of the issue with hardcoded strings.
- **Sample `en.json`:** The JSON object for the English translations.
- **Refactored `UserProfile` Component:** The complete, internationalized component code.

## Tips

The most common and fundamental i18n task. A perfect starting point for any developer new to localization.
