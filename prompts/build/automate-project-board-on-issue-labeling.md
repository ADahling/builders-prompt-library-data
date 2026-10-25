---
title: "Automate Project Board on Issue Labeling"
slug: automate-project-board-on-issue-labeling
stage: Build
category: "DevOps & IaC"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/automate-project-board-on-issue-labeling
---
# Automate Project Board on Issue Labeling

Get GitHub Actions YAML that adds new issues to a project's Triage column and moves labeled issues to Bugs, Features, or Up for Grabs.

Variables: project_board_url

## Prompt

I want to automate the management of my project's GitHub Project board. Specifically, I need a GitHub Actions workflow that automatically adds new issues to the project board and moves them to the correct column based on their labels.

Generate a GitHub Actions workflow file named `.github/workflows/project-automation.yml` that does the following:

**Trigger**: The workflow should run whenever an issue is opened or labeled.

**Jobs**:
1.  **`add-to-project`**: 
    *   This job should trigger when a new issue is opened.
    *   It should use the `actions/add-to-project@v0.4.0` action.
    *   It needs to add the newly created issue to the project board with the URL `{{project_board_url}}`.
    *   The issue should be placed in the `Triage` column.

2.  **`move-issue`**: 
    *   This job should trigger when a label is added to an issue.
    *   It should use a script or an action to check the label and move the issue to the corresponding column.
    *   **If the label is `bug`**: Move the issue to the `Bugs` column.
    *   **If the label is `enhancement`**: Move the issue to the `Features` column.
    *   **If the label is `good first issue`**: Move the issue to the `Up for Grabs` column.

Provide the complete and valid YAML for the workflow file. Ensure you use the correct syntax for accessing the event payload (e.g., `github.event.issue.node_id`) and secrets (e.g., `secrets.GH_PAT`). Assume a personal access token with project permissions is stored in a secret named `GH_PAT`.

Constraint Checklist & Confidence Score:
1.  Is the workflow triggered by the correct events (issues opened, labeled)? Yes.
2.  Does it correctly add new issues to the specified project board and column? Yes.
3.  Does it correctly move issues to different columns based on their labels? Yes.
4.  Is the YAML syntax correct and well-structured? Yes.
5.  Does it correctly reference the necessary secrets and event data? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the complete GitHub Actions workflow YAML file for project automation.

## Tips

Automating project boards saves maintainers significant time and keeps the project status transparent.
