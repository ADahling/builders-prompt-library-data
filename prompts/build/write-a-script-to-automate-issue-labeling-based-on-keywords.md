---
title: "Write a Script to Automate Issue Labeling Based on Keywords"
slug: write-a-script-to-automate-issue-labeling-based-on-keywords
stage: Build
category: "DevOps & IaC"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-script-to-automate-issue-labeling-based-on-keywords
---
# Write a Script to Automate Issue Labeling Based on Keywords

Get GitHub Actions workflow and labeler configuration files for keyword-based labeling of newly opened or edited project issues.

Variables: project_name

## Prompt

To help with triaging issues in my project, `{{project_name}}`, I want to create a GitHub Action that automatically adds labels to new issues based on keywords in their title and body.

Generate a GitHub Actions workflow file named `.github/workflows/auto-labeler.yml`.

The workflow should:

1.  **Trigger**: Run whenever an issue is opened or edited.

2.  **Action**: Use a marketplace action like `flydiver/auto-labeler-action@v1` or the built-in `actions/labeler` action (which requires a separate config file).

For this prompt, generate the solution using the `actions/labeler` action.

**Part 1: The Labeler Configuration File**

First, create the content for the configuration file named `.github/labeler.yml`. This file defines the mapping between keywords and labels.

*   If the issue title or body contains "documentation", "docs", or "tutorial", add the `documentation` label.
*   If the issue title or body contains "bug", "error", "fails", or "traceback", add the `bug` label.
*   If the issue title or body contains "feature", "idea", or "suggestion", add the `enhancement` label.
*   If the issue title or body contains "test", "pytest", or "coverage", add the `testing` label.

**Part 2: The GitHub Actions Workflow**

Next, create the `.github/workflows/auto-labeler.yml` file. This workflow will use the configuration file to apply the labels.

*   **Name**: "Auto Label Issues".
*   **Trigger**: On `issues: opened, edited`.
*   **Job**: Define a job named `label-issues`.
*   **Steps**: The job should use the `actions/labeler@v4` action and provide it with the necessary `GITHUB_TOKEN`.

Your output should include the complete YAML content for both files.

Constraint Checklist & Confidence Score:
1.  Does the `labeler.yml` file correctly map keywords to labels? Yes.
2.  Does the workflow file trigger on the correct issue events? Yes.
3.  Does the workflow use the official `actions/labeler` action? Yes.
4.  Are both YAML files syntactically correct and well-structured? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the configuration and workflow for the auto-labeler.

## Tips

Automating issue labeling is a huge time-saver for maintainers, allowing them to quickly filter and prioritize incoming issues.
