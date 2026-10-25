---
title: "Chain-of-Thought Prompting for Complex Analysis"
slug: chain-of-thought-prompting-for-complex-analysis
stage: Idea
category: "Prompt Engineering"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/chain-of-thought-prompting-for-complex-analysis
---
# Chain-of-Thought Prompting for Complex Analysis

Generate a multi-faceted analysis and synthesis of complex topics using structured chain-of-thought reasoning to produce actionable insights.

Variables: complex_topic

## Prompt

You are a senior analyst. I need you to analyze {{complex_topic}} using chain-of-thought reasoning.

Before giving your final answer, work through the problem step by step:
1. State your initial understanding of the problem
2. Identify the key variables and constraints
3. Consider at least 3 different perspectives or approaches
4. Evaluate the trade-offs of each approach
5. Synthesize your findings into a coherent recommendation

Show your reasoning at each step. If you make an assumption, state it explicitly. If you encounter uncertainty, quantify it (high/medium/low confidence).

Format your response as:
- **Thinking Process**: Your step-by-step reasoning
- **Key Insights**: 3-5 non-obvious findings
- **Recommendation**: Your final recommendation with confidence level
- **Risks**: What could go wrong and how to mitigate

## Tips

Use this meta-prompt to get higher quality analysis from any AI model by forcing explicit reasoning.
