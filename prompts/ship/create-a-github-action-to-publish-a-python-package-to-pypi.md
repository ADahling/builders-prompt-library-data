---
title: "Create a GitHub Action to Publish a Python Package to PyPI"
slug: create-a-github-action-to-publish-a-python-package-to-pypi
stage: Ship
category: "Deployment & Launch"
grade: A+
score: 95
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-github-action-to-publish-a-python-package-to-pypi
---
# Create a GitHub Action to Publish a Python Package to PyPI

Automate the secure building and publishing of Python packages to PyPI via GitHub Actions using OIDC-based trusted publishing.

Variables: package_name

## Prompt

I am ready to publish my open-source Python package, `{{package_name}}`, to the Python Package Index (PyPI). I want to automate this process using GitHub Actions.

Generate a GitHub Actions workflow file named `.github/workflows/publish.yml` that automatically builds and publishes the package to PyPI whenever a new release is created on GitHub.

The workflow must:

1.  **Trigger**: The workflow should only run when a new release is created.

2.  **Job**: Define a single job named `publish` that runs on `ubuntu-latest`.

3.  **Permissions**: The job needs permissions to write to the repository (to create the release) and to manage identity (for trusted publishing). Configure the `permissions` block accordingly.

4.  **Steps**: The job should perform the following sequence of steps:
    *   Check out the repository code.
    *   Set up a specific Python version.
    *   Install the necessary build dependencies (e.g., `build`).
    *   Build the source and wheel distributions using `python -m build`.
    *   Use the official `pypa/gh-action-pypi-publish@release/v1` action to publish the distributions to PyPI.

5.  **Trusted Publishing**: Configure the publishing step to use PyPI's trusted publishing mechanism (OIDC). This is a modern, secure method that avoids the need to store long-lived API tokens as GitHub secrets.
    *   The `pypi-publish` action should be configured to use this method by default when no password is provided.

Your output should be the complete, valid, and well-commented YAML for the `publish.yml` workflow file. Also, briefly explain the necessary setup on the PyPI side (i.e., setting up the project as a "pending publisher").

Constraint Checklist & Confidence Score:
1.  Does the workflow trigger only on release creation? Yes.
2.  Does it correctly build the Python package? Yes.
3.  Does it use the official PyPA action for publishing? Yes.
4.  Is it configured for modern, secure trusted publishing (OIDC)? Yes.
5.  Is the YAML syntax correct and well-commented? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the GitHub Actions workflow for publishing to PyPI.

## Tips

Automating your release process with trusted publishing is the current best practice for securely and reliably distributing Python packages.
