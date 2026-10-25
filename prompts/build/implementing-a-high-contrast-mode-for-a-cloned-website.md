---
title: "Implementing a High-Contrast Mode for a Cloned Website"
slug: implementing-a-high-contrast-mode-for-a-cloned-website
stage: Build
category: "Website Cloning"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-a-high-contrast-mode-for-a-cloned-website
---
# Implementing a High-Contrast Mode for a Cloned Website

Implement a toggleable, accessible high-contrast mode with a specialized stylesheet and persistent local storage to improve readability.

Variables: website_to_add_high_contrast_url

## Prompt

You are a front-end developer focused on accessibility. Your task is to add a high-contrast mode to a cloned website to improve its readability for users with low vision. The high-contrast mode should be easily toggled by the user.

Context:
- The cloned website is {{website_to_add_high_contrast_url}}.
- You will need to create an alternative stylesheet for the high-contrast mode that uses a limited color palette with high contrast ratios.
- The user's preference for high-contrast mode should be saved in local storage.

Provide:
1. The CSS for the high-contrast mode.
2. The JavaScript for the theme switcher that enables and disables high-contrast mode.

If you cannot open {{website_to_add_high_contrast_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

A practical way to improve the accessibility of a website for a specific user group.
