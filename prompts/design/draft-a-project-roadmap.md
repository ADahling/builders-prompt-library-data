---
title: "Draft a Project Roadmap"
slug: draft-a-project-roadmap
stage: Design
category: "Documentation"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/draft-a-project-roadmap
---
# Draft a Project Roadmap

Draft a public Markdown roadmap for an open-source project's next two quarters, with themes, initiatives, issue links, and expected user impact.

Variables: project_name, current_quarter, next_quarter

## Prompt

To provide transparency and a clear direction for our open-source project, `{{project_name}}`, I need to create a public project roadmap.

Generate a roadmap in Markdown format that can be published as a GitHub Issue, a project board, or a `ROADMAP.md` file in the repository. The roadmap should outline our plans for the next two quarters.

The roadmap should be structured as follows:

1.  **Introduction**: A brief statement about the project's vision and the purpose of the roadmap. Emphasize that the roadmap is a living document and subject to change based on community feedback.

2.  **Current Quarter: {{current_quarter}}** (e.g., Q3 2026)
    *   **Theme**: Define a high-level theme for the quarter (e.g., "Performance and Stability", "New User Experience").
    *   **Key Initiatives**: List 3-4 major features or initiatives planned for this quarter. For each initiative:
        *   Provide a brief description of the goal.
        *   Link to the main GitHub issue or epic for tracking (use placeholder issue numbers, e.g., `#123`).
        *   Mention the expected impact for users.

3.  **Next Quarter: {{next_quarter}}** (e.g., Q4 2026)
    *   **Theme**: Define the theme for the next quarter (e.g., "Extensibility and Integrations").
    *   **Key Initiatives**: List 3-4 planned initiatives, similar to the current quarter. Acknowledge that these plans are more tentative.

4.  **Future / Backlog**: A section for ideas and larger goals that are not yet scheduled. This shows the long-term vision and invites community discussion.
    *   List a few potential future features.
    *   Encourage the community to open issues and contribute to the discussion for these future items.

5.  **How to Contribute**: A call to action for the community to get involved in shaping the roadmap by participating in discussions, opening feature requests, and contributing to the planned initiatives.

Your output should be a complete, well-structured Markdown document.

Constraint Checklist & Confidence Score:
1.  Is the roadmap structured by quarters with clear themes? Yes.
2.  Are the initiatives for each quarter specific and linked to trackable items? Yes.
3.  Does it include a section for future ideas to encourage discussion? Yes.
4.  Is there a clear call to action for community involvement? Yes.
5.  Is the tone transparent and collaborative? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the project roadmap document.

## Tips

A public roadmap is a powerful tool for aligning the community and maintainers on the project's priorities and future direction.
