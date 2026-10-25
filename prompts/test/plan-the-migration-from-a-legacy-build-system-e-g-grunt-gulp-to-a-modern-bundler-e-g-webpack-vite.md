---
title: "Plan the Migration from a Legacy Build System (e.g., Grunt/Gulp) to a Modern Bundler (e.g., Webpack/Vite)"
slug: plan-the-migration-from-a-legacy-build-system-e-g-grunt-gulp-to-a-modern-bundler-e-g-webpack-vite
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 73
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/plan-the-migration-from-a-legacy-build-system-e-g-grunt-gulp-to-a-modern-bundler-e-g-webpack-vite
---
# Plan the Migration from a Legacy Build System (e.g., Grunt/Gulp) to a Modern Bundler (e.g., Webpack/Vite)

Get a migration plan from a legacy frontend task runner to a modern bundler, including migration rationale and a feature comparison table.

Variables: legacy_build_tool, modern_build_tool

## Prompt

My project is still using an old task runner, `{{legacy_build_tool}}` (e.g., Grunt, Gulp), for its frontend build process. The build is slow, the configuration is complex, and it doesn't support modern features like tree-shaking and Hot Module Replacement (HMR).

I want to migrate our build process to a modern bundler, `{{modern_build_tool}}` (e.g., Webpack, Vite).

Your task is to create a detailed migration plan.

1.  **Why Migrate?** Start by making the case for the migration. Create a table comparing the features of `{{legacy_build_tool}}` and `{{modern_build_tool}}

## Tips

Migrating a build system is a complex and often-dreaded task. A detailed plan is crucial for success.
