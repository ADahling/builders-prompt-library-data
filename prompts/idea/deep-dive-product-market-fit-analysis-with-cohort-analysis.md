---
title: "Deep Dive Product-Market Fit Analysis with Cohort Analysis"
slug: deep-dive-product-market-fit-analysis-with-cohort-analysis
stage: Idea
category: "Business & Strategy"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/deep-dive-product-market-fit-analysis-with-cohort-analysis
---
# Deep Dive Product-Market Fit Analysis with Cohort Analysis

Execute a rigorous cohort analysis to quantify product-market fit through retention curves, engagement metrics, and AH-HA moment discovery.

Variables: product_name, months_live

## Prompt

As a data-driven Head of Product for {{product_name}}, a B2C mobile app, I need to move beyond simple surveys and conduct a rigorous, quantitative analysis of our product-market fit. We have been live for {{months_live}} months and have access to user-level data, including sign-up date, daily activity, and subscription status.

Act as a senior data scientist specializing in growth analytics. Your task is to guide me through a cohort analysis to assess product-market fit by measuring user retention and engagement over time.

The process should be:

1.  **Cohort Definition:**
    *   Explain how to group users into monthly cohorts based on their sign-up date.
2.  **Retention Curve Analysis:**
    *   Instruct me on how to calculate and plot a classic retention curve for each cohort, showing the percentage of users who are still active 'N' days after signing up.
    *   Explain what a "flattening" retention curve indicates about long-term user retention and product value.
3.  **Engagement Analysis:**
    *   Recommend key engagement metrics to track for our app (e.g., daily active users, session duration, key feature adoption).
    *   Guide me on how to analyze the engagement levels of retained users. Are they becoming more or less engaged over time?
4.  **Identifying the 'Aha!' Moment:**
    *   Describe a methodology for identifying the "aha!" moment – the specific action or set of actions that correlates with long-term retention. For example, "users who invite 3 friends in their first week have a 50% higher retention rate."
5.  **Reporting and Interpretation:**
    *   Structure a report that synthesizes the findings from the cohort analysis. The report should clearly state whether the data indicates we have achieved product-market fit and provide evidence-based recommendations for the product roadmap.

**Output Format:**

Please provide a detailed, step-by-step guide in Markdown. Include examples of SQL queries (or pseudo-code) for calculating cohort retention. Describe the ideal visualizations (e.g., line charts for retention curves) to present the data.

**Constraints:**

*   The methodology must be rigorous and based on standard data science practices.
*   The explanation should be clear enough for a product manager with a basic understanding of data analysis to follow.
*   The focus should be on generating actionable insights, not just theoretical concepts.

## Tips

This prompt is for product leaders who want to use data science techniques to get a definitive answer on product-market fit.
