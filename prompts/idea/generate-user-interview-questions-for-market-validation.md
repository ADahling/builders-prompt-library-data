---
title: "Generate User Interview Questions for Market Validation"
slug: generate-user-interview-questions-for-market-validation
stage: Idea
category: "Business & Strategy"
grade: A+
score: 98
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-user-interview-questions-for-market-validation
---
# Generate User Interview Questions for Market Validation

Generate unbiased user interview scripts based on The Mom Test to validate market needs and workflows before building a product.

Variables: product_idea, target_audience

## Prompt

I am an entrepreneur in the very early stages of exploring a new business idea. The idea is a {{product_idea}} for {{target_audience}}. Before I write a single line of code, I want to validate the problem and the potential solution by conducting user interviews.

Act as a seasoned user researcher and startup mentor. Your task is to generate a set of user interview questions designed to validate the market need without biasing the interviewee.

The interview script should be structured in three parts:

1.  **Warm-up & Context:**
    *   Questions to build rapport and understand the user's current role and context.

2.  **Problem Discovery (The Most Important Part):**
    *   A set of open-ended questions to explore the user's current workflow, challenges, and pain points related to the problem space. These questions should NOT mention my solution idea.
    *   The goal is to understand how they are solving the problem today, what they have tried, and what the consequences of the problem are.
    *   Follow the principles of 'The Mom Test' by Rob Fitzpatrick - focus on their life, not my idea.

3.  **Solution Exploration (Optional & To Be Used with Caution):**
    *   Only after deeply understanding the problem, I might briefly introduce my proposed solution.
    *   Provide questions to gauge their reaction to the concept, but in a way that still avoids simple validation. For example, instead of "Would you use this?", ask "What would you expect this to do?" or "How would this fit into your current workflow?"

**Output Format:**

Please generate a complete user interview script in Markdown. The script should include an introduction, the questions for each section, and some best-practice tips for conducting the interviews (e.g., "listen more than you talk").

**Constraints:**

*   The questions must be open-ended and non-leading.
*   The script must be designed to uncover genuine problems and needs.
*   The tone should be curious, empathetic, and neutral.

## Tips

Crucial for any entrepreneur. This prompt helps avoid the cardinal sin of startups: building something nobody wants.
