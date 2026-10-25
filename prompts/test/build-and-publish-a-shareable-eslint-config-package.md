---
title: "Build and Publish a Shareable ESLint Config Package"
slug: build-and-publish-a-shareable-eslint-config-package
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-and-publish-a-shareable-eslint-config-package
---
# Build and Publish a Shareable ESLint Config Package

Get a guide to structuring, publishing, and maintaining a shared ESLint config package for consistent lint rules across multiple projects.

## Prompt

My organization has multiple projects, and we want to enforce a consistent set of ESLint rules across all of them. I want to create a shareable ESLint config package that can be easily reused. 

Your task is to provide a comprehensive guide to creating, publishing, and using a shareable ESLint config. Please cover:

1.  **Package Structure:** The recommended directory structure for a shareable ESLint config package. What files are needed? How should the main config file be structured?
2.  **Dependencies:** How to manage dependencies, including plugins and other shareable configs. Should they be `dependencies` or `peerDependencies`? Explain the difference and the best practice for this scenario.
3.  **Publishing to NPM:** A step-by-step guide to publishing the package to a private or public NPM registry. This should include versioning and publishing commands.
4.  **Usage:** How to use the shareable config in a consumer project. Show how to install the package and extend the config in the project's `.eslintrc.json` file.
5.  **Versioning and Maintenance:** How to manage updates to the shareable config. What is the recommended workflow for introducing new rules or changing existing ones without breaking consumer projects?

Output should be a detailed guide suitable for a developer with experience in Node.js and NPM.

## Tips

Essential for maintaining consistency and quality at scale in a multi-project environment.
