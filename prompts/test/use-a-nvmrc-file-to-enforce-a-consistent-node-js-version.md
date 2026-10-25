---
title: "Use a `.nvmrc` File to Enforce a Consistent Node.js Version"
slug: use-a-nvmrc-file-to-enforce-a-consistent-node-js-version
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 76
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/use-a-nvmrc-file-to-enforce-a-consistent-node-js-version
---
# Use a `.nvmrc` File to Enforce a Consistent Node.js Version

Get a guide to aligning team Node.js versions with an .nvmrc file, the nvm workflow, and a package.json preinstall check.

## Prompt

My team's Node.js project sometimes has bugs that are hard to reproduce because different developers are using different versions of Node.js on their machines. I want to enforce that every developer uses the same version.

I have heard that `nvm` (Node Version Manager) can help with this.

Your task is to explain how to use a `.nvmrc` file to solve this problem.

1.  **What is `nvm`?** Briefly explain that `nvm` is a tool to manage multiple versions of Node.js on a single machine.
2.  **The `.nvmrc` File:** Explain that a `.nvmrc` file is a simple text file that you place in the root of your project, and it contains just the version number of Node.js that the project requires (e.g., `18.17.1`).
3.  **The Workflow:** Explain the simple workflow for developers:
    *   When a developer clones the project and `cd`s into the directory, they just have to run the command `nvm use`.
    *   `nvm` will automatically read the `.nvmrc` file and switch to the correct Node.js version. If they don't have that version installed, `nvm` will prompt them to install it.
4.  **Package Manager Enforcement:** Show how to add a check to the `package.json` `preinstall` script to ensure that the correct version of Node.js is being used before `npm install` is run. This will warn developers who are not using the correct version.

Output should be a simple guide for improving team consistency.

## Tips

A very simple and effective way to eliminate 'works on my machine' bugs related to Node.js versions.
