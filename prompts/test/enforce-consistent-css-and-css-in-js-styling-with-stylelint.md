---
title: "Enforce Consistent CSS and CSS-in-JS Styling with Stylelint"
slug: enforce-consistent-css-and-css-in-js-styling-with-stylelint
stage: Test
category: "Cleanup & Warnings"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/enforce-consistent-css-and-css-in-js-styling-with-stylelint
---
# Enforce Consistent CSS and CSS-in-JS Styling with Stylelint

Set up Stylelint for mixed CSS, SCSS, and CSS-in-JS with installation commands, configuration, editor integration, and pre-commit hooks.

Variables: css_in_js_library, code_editor

## Prompt

My project uses a mix of plain CSS, SCSS, and CSS-in-JS (using {{css_in_js_library}}). The styling rules are inconsistent, and I want to enforce a unified style. I've heard of Stylelint, but I'm not sure how to configure it for this mixed environment.

Your task is to provide a guide on setting up Stylelint to enforce consistent styling across all these different methods. Please include:

1.  **Installation:** The necessary packages to install, including Stylelint, standard configs, and the specific processors for CSS-in-JS.
2.  **Configuration:** A comprehensive `.stylelintrc.json` configuration file. This should:
    *   Extend a standard configuration like `stylelint-config-standard`.
    *   Include the necessary overrides for SCSS syntax.
    *   Configure the processor and rules for {{css_in_js_library}}.
    *   Enforce a specific order for CSS properties (`stylelint-order`).
3.  **Automation:** How to integrate Stylelint into the development workflow, including editor integration for {{code_editor}} and a pre-commit hook.

Output should be a detailed guide with all the necessary configuration and commands.

## Tips

Stylelint is to CSS what ESLint is to JavaScript. Essential for maintaining clean and consistent styles.
