---
title: "Create a GitHub Action to Validate Links in Documentation"
slug: create-a-github-action-to-validate-links-in-documentation
stage: Test
category: "Testing & QA"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-github-action-to-validate-links-in-documentation
---
# Create a GitHub Action to Validate Links in Documentation

Get commented GitHub Actions YAML to check repository Markdown links when documentation changes in a pull request.

Variables: project_name

## Prompt

To ensure the quality of our project's documentation for `{{project_name}}`, I want to create a GitHub Action that automatically checks for broken links in our Markdown files.

Generate a GitHub Actions workflow file named `.github/workflows/link-checker.yml` that runs on every pull request and checks all Markdown files in the repository.

The workflow should:

1.  **Name**: "Check Markdown Links".

2.  **Trigger**: Run on every pull request that modifies Markdown files (`**.md`).

3.  **Job**: Define a single job named `markdown-link-check` that runs on `ubuntu-latest`.

4.  **Steps**: The job should perform the following steps:
    *   **Checkout**: Check out the repository code.
    *   **Run Link Checker**: Use a well-regarded marketplace action for this purpose, such as `lycheeverse/lychee-action@v1` or `gaurav-nelson/github-action-markdown-link-check@v1`.

5.  **Configuration**: Configure the link-checker action:
    *   If using `lychee-action`, configure it to check all Markdown files in the repository.
    *   If using `github-action-markdown-link-check`, it typically works out of the box on all `.md` files.
    *   **(Optional but recommended)** Create a configuration file for the link checker (e.g., `.lycheeignore`) to specify any links that should be ignored (e.g., `localhost` links that are expected to be broken in CI).

Your output should be the complete, valid, and well-commented YAML for the `link-checker.yml` workflow file. For this prompt, use the `gaurav-nelson/github-action-markdown-link-check@v1` action for simplicity.

Constraint Checklist & Confidence Score:
1.  Does the workflow trigger on the correct event and file paths? Yes.
2.  Does it use a standard, reliable action for link checking? Yes.
3.  Is the job configured to run on an appropriate runner? Yes.
4.  Is the YAML syntax correct and well-commented? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the GitHub Actions workflow for checking broken links.

## Tips

Broken links are a common problem in documentation and create a poor user experience. Automating this check is a simple and effective way to maintain quality.
