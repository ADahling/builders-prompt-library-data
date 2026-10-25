---
title: "Write a Tutorial for a Key Project Feature"
slug: write-a-tutorial-for-a-key-project-feature
stage: Design
category: "Documentation"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-tutorial-for-a-key-project-feature
---
# Write a Tutorial for a Key Project Feature

Write a Markdown feature tutorial with prerequisites, progressive code examples, and explanations for project users new to the feature.

Variables: project_name, feature_name, feature_purpose, language

## Prompt

I need to create a detailed tutorial for a key feature in my open-source project, `{{project_name}}`. The feature is `{{feature_name}}`, and it allows users to `{{feature_purpose}}`.

The tutorial should be written in Markdown and be suitable for the project's documentation website or a blog post. It should be aimed at a user who has basic knowledge of the project but is new to this specific feature.

Generate a complete tutorial that follows this structure:

1.  **Title**: A clear and descriptive title, e.g., "Getting Started with {{feature_name}} in {{project_name}}".

2.  **Introduction**:
    *   Briefly explain what the feature is and what problem it solves.
    *   State the prerequisites for the tutorial (e.g., "You should have {{project_name}} installed.").
    *   Outline what the user will learn by the end of the tutorial.

3.  **Step 1: The Basic Setup**
    *   Start with the simplest possible use case.
    *   Provide a small, self-contained code snippet.
    *   Explain each line of the code and the output it produces.

4.  **Step 2: Adding Complexity**
    *   Build on the previous step by introducing a new concept or parameter.
    *   Provide another code snippet.
    *   Explain the new elements and how they modify the behavior.

5.  **Step 3: An Advanced Use Case**
    *   Demonstrate a more advanced or practical application of the feature.
    *   This could involve combining it with other features or handling a more complex data structure.
    *   Again, provide a clear code example and explanation.

6.  **Conclusion and Next Steps**:
    *   Briefly summarize what the user has learned.
    *   Provide links to the relevant API documentation for a deeper dive.
    *   Suggest other related tutorials or features they might be interested in.

Throughout the tutorial, the code examples should be written in `{{language}}` and be easy to copy, paste, and run. The explanations should be clear, concise, and focused on the practical application.

Constraint Checklist & Confidence Score:
1.  Is the tutorial structured in a logical, step-by-step manner? Yes.
2.  Are the code examples clear, correct, and well-explained? Yes.
3.  Is the tutorial aimed at the correct audience (intermediate user)? Yes.
4.  Does it have a clear introduction and conclusion? Yes.
5.  Is the output a complete and polished Markdown document? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the detailed tutorial for the specified feature.

## Tips

Tutorials are one of the most effective ways to teach users how to use your project. A good tutorial can dramatically improve adoption of a new feature.
