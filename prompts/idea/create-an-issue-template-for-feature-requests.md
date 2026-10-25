---
title: "Create an Issue Template for Feature Requests"
slug: create-an-issue-template-for-feature-requests
stage: Idea
category: "Idea to PRD"
grade: A+
score: 99
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-issue-template-for-feature-requests
---
# Create an Issue Template for Feature Requests

Draft a GitHub feature request template with YAML metadata and sections for problems, proposed solutions, alternatives, and context.

Variables: project_name

## Prompt

Generate a feature request issue template for an open-source project named `{{project_name}}`. The template should be in Markdown format and saved as `.github/ISSUE_TEMPLATE/feature_request.md`. The purpose is to structure incoming feature ideas and gather the necessary context for evaluation.

The template should include:

1.  **Template Configuration** (YAML front matter):
    *   `name`: Feature Request
    *   `about`: Suggest an idea for this project
    *   `title`: "[FEAT] - "
    *   `labels`: ["enhancement", "needs-discussion"]
    *   `assignees`: ''

2.  **Template Body** (Markdown):
    *   **Is your feature request related to a problem? Please describe.** A clear and concise description of what the problem is. Ex. "I'm always frustrated when [...]."
    *   **Describe the solution you'd like.** A clear and concise description of what you want to happen.
    *   **Describe alternatives you've considered.** A clear and concise description of any alternative solutions or features you've considered.
    *   **Additional context.** Add any other context or mockups about the feature request here.

Your output should be the complete content for the `feature_request.md` file, including the YAML front matter.

Constraint Checklist & Confidence Score:
1.  Is the template in valid Markdown format with YAML front matter? Yes.
2.  Does it effectively capture the problem and proposed solution? Yes.
3.  Is the structure clear and user-friendly? Yes.
4.  Are the default labels and title appropriate for a feature request? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the feature request issue template file content.

## Tips

A good feature request template helps maintainers understand the value and context of new ideas from the community.
