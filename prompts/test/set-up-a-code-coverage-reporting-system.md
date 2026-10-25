---
title: "Set up a Code Coverage Reporting System"
slug: set-up-a-code-coverage-reporting-system
stage: Test
category: "Testing & QA"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-a-code-coverage-reporting-system
---
# Set up a Code Coverage Reporting System

Get a GitHub Actions workflow for a Python project that runs pytest coverage, uploads XML reports to Codecov, and supports PR coverage comments.

Variables: project_name, python_version, project_slug, secrets.CODECOV_TOKEN, target_coverage

## Prompt

To improve the quality and reliability of my open-source Python project, `{{project_name}}`, I want to set up a system to measure and report code coverage for our test suite.

I need a GitHub Actions workflow that does the following:
1.  Runs the test suite and collects coverage data.
2.  Uploads the coverage report to a third-party service like Codecov or Coveralls.
3.  Posts a comment on pull requests showing how the PR affects code coverage.

Generate a complete GitHub Actions workflow file named `.github/workflows/coverage.yml` that integrates with Codecov.

The workflow should include these steps:

1.  **Trigger**: Run on every push and pull request to the `main` branch.

2.  **Job Steps**:
    *   Check out the code.
    *   Set up a specific Python version (e.g., `{{python_version}}\
    *   Install dependencies, including `pytest` and `pytest-cov`.
    *   Run the test suite using `pytest` and generate a coverage report in XML format. The command should be: `pytest --cov={{project_slug}} --cov-report=xml`.
    *   Upload the generated `coverage.xml` report to Codecov using the official `codecov/codecov-action`.

3.  **Configuration for Codecov Action**:
    *   Use the latest version of `codecov/codecov-action`.
    *   The action needs a `CODECOV_TOKEN` to upload reports for private repositories, but it's often not needed for public ones. For this prompt, assume it's a public repo, but include a commented-out line showing how to use the token if needed: `token: {{ secrets.CODECOV_TOKEN }}`.

Additionally, provide the necessary configuration for Codecov in a file named `.codecov.yml` at the root of the repository. This file should configure:

*   **Target Coverage**: Set a target overall project coverage of `{{target_coverage}}%` (e.g., 80%).
*   **Threshold for a Patch**: Set a threshold for individual PRs. For example, a PR should not decrease the overall coverage.
*   **Status Checks**: Configure the status check posted on GitHub to be informative.

Your output should include the complete YAML for both `.github/workflows/coverage.yml` and `.codecov.yml`.

Constraint Checklist & Confidence Score:
1.  Does the workflow correctly run tests and generate an XML coverage report? Yes.
2.  Does it use the official Codecov action to upload the report? Yes.
3.  Is the Codecov configuration file (\.codecov.yml) correctly set up with targets and thresholds? Yes.
4.  Are both YAML files well-structured and commented? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the workflow and configuration for code coverage reporting.

## Tips

Code coverage is a valuable metric for understanding the quality of your test suite. Integrating it into your CI/CD pipeline provides immediate feedback on every pull request.
