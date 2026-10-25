---
title: "Set Up a CI/CD Pipeline with GitHub Actions"
slug: set-up-a-ci-cd-pipeline-with-github-actions
stage: Ship
category: "Deployment & Launch"
grade: B
score: 77
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-a-ci-cd-pipeline-with-github-actions
---
# Set Up a CI/CD Pipeline with GitHub Actions

Get a GitHub Actions workflow for branch-triggered app deployment, including code checkout, dependency installation, and tests.

Variables: project_name, branch_name, package_manager, deployment_environment

## Prompt

Create a GitHub Actions workflow that automates the deployment of your {{project_name}} application. The workflow should be triggered on every push to the {{branch_name}} branch. Include steps for checking out the code, installing dependencies using {{package_manager}}, running tests, and deploying to {{deployment_environment}}.

## Tips

This prompt is ideal if you want to automate deployment processes using GitHub Actions.
