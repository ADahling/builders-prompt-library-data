---
title: "Create a Code of Conduct for an Open-Source Project"
slug: create-a-code-of-conduct-for-an-open-source-project
stage: Design
category: "Documentation"
grade: A+
score: 99
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-code-of-conduct-for-an-open-source-project
---
# Create a Code of Conduct for an Open-Source Project

Generate a Contributor Covenant-based Code of Conduct to establish professional community standards and clear enforcement guidelines.

Variables: project_name, project_domain

## Prompt

I am starting a new open-source project, `{{project_name}}`, and I need to establish a Code of Conduct (CoC) from day one to foster a safe, welcoming, and inclusive community.

Generate a complete `CODE_OF_CONDUCT.md` file for the project. The CoC should be based on the Contributor Covenant, which is the most widely adopted standard for open-source projects.

Your task is to generate the full text of the Code of Conduct in Markdown, adapted for this project. It should be based on the latest version of the Contributor Covenant (v2.1 or newer).

The generated document must include the following key sections:

1.  **Our Pledge**: A statement pledging to make participation in the project a harassment-free experience for everyone, regardless of personal characteristics.

2.  **Our Standards**: A list of examples of behavior that contributes to a positive environment, such as:
    *   Being respectful of differing viewpoints.
    *   Giving and gracefully accepting constructive feedback.
    *   Focusing on what is best for the community.
    *   Showing empathy towards other community members.

3.  **Examples of Unacceptable Behavior**: A list of examples of unacceptable behavior, such as:
    *   The use of sexualized language or imagery.
    *   Trolling, insulting, or derogatory comments.
    *   Public or private harassment.
    *   Publishing others' private information.
    *   Other conduct which could reasonably be considered inappropriate in a professional setting.

4.  **Our Responsibilities**: An explanation of the project maintainers' responsibilities to clarify and enforce the standards of acceptable behavior.

5.  **Scope**: A statement that the CoC applies to all project spaces (GitHub, Slack, etc.) and also applies when an individual is representing the project in public spaces.

6.  **Enforcement**: This is a critical section. It must clearly explain how to report a violation and what to expect.
    *   Provide a specific, private email address for reporting violations (e.g., `conduct@{{project_domain}}.com`).
    *   State that all complaints will be reviewed and investigated.
    *   Outline a range of possible consequences for violations, from a private warning to a permanent ban.

7.  **Attribution**: The document should end with an attribution line, crediting the Contributor Covenant.

Your output should be the complete, ready-to-use Markdown file.

Constraint Checklist & Confidence Score:
1.  Is the generated CoC based on the Contributor Covenant? Yes.
2.  Does it include all the key sections (Pledge, Standards, Enforcement, etc.)? Yes.
3.  Is the enforcement process clear, with a private contact method? Yes.
4.  Is the language inclusive and professional? Yes.
5.  Is the output a complete Markdown file? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the complete Code of Conduct file.

## Tips

A Code of Conduct is not optional for a modern open-source project. It is a foundational document that sets the tone for the entire community.
