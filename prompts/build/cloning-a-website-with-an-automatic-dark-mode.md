---
title: "Cloning a Website with an Automatic Dark Mode"
slug: cloning-a-website-with-an-automatic-dark-mode
stage: Build
category: "Website Cloning"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cloning-a-website-with-an-automatic-dark-mode
---
# Cloning a Website with an Automatic Dark Mode

Implement a system-responsive dark mode with a manual override toggle for a cloned website using CSS media queries and JavaScript.

Variables: website_with_auto_dark_mode_url

## Prompt

You are a front-end developer. Your task is to clone a website that automatically switches to dark mode based on the user"s operating system preference. You will need to use the `prefers-color-scheme` media query to detect the user"s preference.

Context:
- The website to clone is {{website_with_auto_dark_mode_url}}.
- You should create a dark theme that is applied automatically when the user has dark mode enabled in their OS.
- You should also provide a manual toggle for users who want to override the system setting.

Provide:
1. The CSS for the automatic dark mode.
2. The JavaScript for the manual override toggle.

If you cannot open {{website_with_auto_dark_mode_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

A more advanced dark mode implementation that respects user preferences.
