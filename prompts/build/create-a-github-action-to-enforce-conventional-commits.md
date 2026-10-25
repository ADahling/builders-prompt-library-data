---
title: "Create a GitHub Action to Enforce Conventional Commits"
slug: create-a-github-action-to-enforce-conventional-commits
stage: Build
category: "DevOps & IaC"
grade: A+
score: 95
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-github-action-to-enforce-conventional-commits
---
# Create a GitHub Action to Enforce Conventional Commits

Get commented GitHub Actions YAML to check pull request titles against Conventional Commits and fail CI for titles that do not conform.

Variables: project_name

## Prompt

To maintain a clean, readable, and automated changelog-friendly Git history for our project, `{{project_name}}`, I want to enforce the Conventional Commits specification for all pull request titles.

Generate a GitHub Actions workflow file named `.github/workflows/commit-lint.yml` that checks if PR titles adhere to the Conventional Commits format.

The workflow should:

1.  **Name**: "Lint PR Title".

2.  **Trigger**: The workflow should run whenever a pull request is opened, edited, or synchronized.

3.  **Job**: Define a single job named `lint-pr-title` that runs on `ubuntu-latest`.

4.  **Action**: Use a well-regarded marketplace action for this purpose, such as `amannn/action-semantic-pull-request@v5`.

5.  **Configuration**: Configure the action:
    *   The action should check the pull request title.
    *   It should be configured to allow standard Conventional Commit types (e.g., `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`).
    *   It should also allow a scope (e.g., `feat(api): ...`).
    *   If the PR title does not conform to the spec, the action should fail the CI check, blocking the PR from being merged.
    *   The action requires the `GITHUB_TOKEN` to be passed to it.

Your output should be the complete, valid, and well-commented YAML for the `commit-lint.yml` workflow file.

**Example of a valid title**: `feat(auth): add passwordless login

## Tips

Enforcing Conventional Commits is a best practice for any serious open-source project. It makes the Git history understandable at a glance and fully automates the process of generating changelogs.
