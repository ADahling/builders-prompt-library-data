---
title: "Create a Global State Management Solution with Jotai for a Themed Application"
slug: create-a-global-state-management-solution-with-jotai-for-a-themed-application
stage: Build
category: "Frontend & Styling"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-global-state-management-solution-with-jotai-for-a-themed-application
---
# Create a Global State Management Solution with Jotai for a Themed Application

Get a single-file TypeScript example using Jotai for persistent theme state, derived styles, and a React theme switcher for a dashboard.

Variables: app_name

## Prompt

We are building a highly customizable dashboard application, {{app_name}}, that allows users to switch between different themes (e.g., 'light', 'dark', 'high-contrast'). We have chosen Jotai for our state management because of its atomic and minimalistic approach.

Create a global state management solution using Jotai to handle the application's theme. The solution should:
1.  Define a Jotai atom to hold the current theme state (e.g., 'themeAtom').
2.  Create a derived atom that provides the theme configuration (e.g., colors, fonts) based on the current theme. This derived atom should read from the 'themeAtom'.
3.  Implement a mechanism to persist the selected theme to 'localStorage' so that it is remembered across browser sessions. You can use Jotai's built-in persistence utilities for this.
4.  Create a React component that acts as a theme switcher, allowing the user to cycle through the available themes.
5.  Demonstrate how another component can consume the theme configuration from the derived atom to style itself dynamically.

Provide a complete, self-contained example in a single TypeScript file. The example should include the atom definitions, the theme switcher component, and a styled component that reacts to theme changes.
