---
title: "Create a GitHub Action to Auto-assign Reviewers"
slug: create-a-github-action-to-auto-assign-reviewers
stage: Build
category: "DevOps & IaC"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-github-action-to-auto-assign-reviewers
---
# Create a GitHub Action to Auto-assign Reviewers

Get a GitHub Actions workflow to assign reviewers based on changed files when pull requests open or become ready for review.

Variables: project_name, default_reviewers

## Prompt

To streamline our pull request process in the `{{project_name}}` repository, I want to automatically assign reviewers based on the files that were changed.

Generate a GitHub Actions workflow file named `.github/workflows/auto-assign.yml` that assigns reviewers to new pull requests.

The assignment logic should be as follows:

1.  **Trigger**: The workflow should run whenever a pull request is opened, or when it's ready for review.

2.  **Default Reviewers**: A default set of reviewers, `{{default_reviewers}}\

## Tips

Auto-assigning reviewers based on code ownership is a best practice that ensures the right eyes are on the code, speeding up the review process.
