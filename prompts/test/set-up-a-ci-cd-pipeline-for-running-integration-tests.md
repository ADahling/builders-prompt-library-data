---
title: "Set Up a CI/CD Pipeline for Running Integration Tests"
slug: set-up-a-ci-cd-pipeline-for-running-integration-tests
stage: Test
category: "Testing & QA"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-a-ci-cd-pipeline-for-running-integration-tests
---
# Set Up a CI/CD Pipeline for Running Integration Tests

Get a commented CI/CD config to run integration tests on main branch pushes, set up dependencies and services, and report results.

Variables: ci_cd_platform, test_command

## Prompt

Our development team wants to automate the process of running integration tests. We use `{{ci_cd_platform}}` (e.g., Jenkins, GitLab CI, GitHub Actions) for our CI/CD pipelines. I need a configuration file that sets up a pipeline to run our integration tests automatically.

**Instructions:**
1.  **Test Command:** The command to run the integration tests is `{{test_command}}`.
2.  **Pipeline Configuration:**
    *   **Trigger:** The pipeline should be triggered on every push to the `main` branch.
    *   **Environment:** The pipeline should set up the necessary environment, including installing dependencies and starting any required services (e.g., a database).
    *   **Test Stage:** The pipeline should have a dedicated stage for running the integration tests.
    *   **Reporting:** The pipeline should be configured to display the test results in the CI/CD platform's UI.
3.  **Output Format:** Provide the complete CI/CD pipeline configuration file (e.g., `Jenkinsfile`, `.gitlab-ci.yml`, `main.yml`). The file should be well-commented to explain each step of the pipeline.
