---
title: "Create Contribution Guidelines for an Open-Source Project"
slug: create-contribution-guidelines-for-an-open-source-project
stage: Design
category: "Documentation"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-contribution-guidelines-for-an-open-source-project
---
# Create Contribution Guidelines for an Open-Source Project

Generate a comprehensive CONTRIBUTING.md file to streamline community onboarding and standardize the pull request process for GitHub projects.

Variables: project_name, issue_tracker_url, code_of_conduct_url

## Prompt

You are the maintainer of a popular open-source project, {{project_name}}. To encourage community contributions and streamline the process of accepting them, you need to create a clear and comprehensive set of contribution guidelines.

Your task is to generate a CONTRIBUTING.md file that provides potential contributors with all the information they need to get started. The file should include the following sections:

*   **Code of Conduct:** A link to the project's code of conduct.
*   **How to Contribute:** A guide on how to find issues to work on, how to report bugs, and how to suggest new features.
*   **Development Setup:** Step-by-step instructions on how to set up a local development environment.
*   **Pull Request Process:** A detailed explanation of the process for submitting a pull request, including requirements for branch naming, commit messages, and code review.
*   **Style Guides:** Links to the project's coding style guides.
*   **Testing:** Instructions on how to run the project's tests.

Here is some information about the project:

*   **Project Name:** {{project_name}}
*   **Issue Tracker:** {{issue_tracker_url}}
*   **Code of Conduct:** {{code_of_conduct_url}}

Generate the complete CONTRIBUTING.md file. The tone should be welcoming and encouraging to new contributors.
