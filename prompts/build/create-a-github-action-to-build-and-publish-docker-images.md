---
title: "Create a GitHub Action to Build and Publish Docker Images"
slug: create-a-github-action-to-build-and-publish-docker-images
stage: Build
category: "DevOps & IaC"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-github-action-to-build-and-publish-docker-images
---
# Create a GitHub Action to Build and Publish Docker Images

Get commented GitHub Actions YAML to build and push Docker images to GHCR on main branch pushes, with automatic tags and labels.

Variables: app_name, github_username, repo_name

## Prompt

I need a GitHub Actions workflow to automate the building and publishing of Docker images for my application, `{{app_name}}`. The images should be pushed to GitHub Container Registry (GHCR).

Generate a workflow file named `.github/workflows/docker-publish.yml` that implements a robust Docker publishing strategy.

The workflow should:

1.  **Trigger**: The workflow should run on every push to the `main` branch.

2.  **Job**: Define a single job named `build-and-push` that runs on `ubuntu-latest`.

3.  **Steps**: The job should perform the following steps:
    *   **Checkout**: Check out the repository code.
    *   **Login to GHCR**: Log in to the GitHub Container Registry using the `docker/login-action`. Use the `GITHUB_TOKEN` for authentication.
    *   **Extract Metadata**: Use the `docker/metadata-action` to automatically extract tags and labels for the Docker image. The tags should be based on the Git branch and SHA. For the `main` branch, it should generate a `latest` tag.
    *   **Build and Push**: Use the `docker/build-push-action` to build the Docker image from the `Dockerfile` in the repository root and push it to GHCR. The action should be configured with the extracted labels and tags.

4.  **Image Naming**: The image should be named after the repository, in the format `ghcr.io/{{github_username}}/{{repo_name}}`.

Your output should be the complete, valid, and well-commented YAML for the `docker-publish.yml` workflow file. Ensure you are using the latest recommended versions of the Docker actions.

Constraint Checklist & Confidence Score:
1.  Does the workflow trigger on pushes to the main branch? Yes.
2.  Does it correctly log in to GHCR? Yes.
3.  Does it use the metadata action to generate appropriate tags? Yes.
4.  Does it use the build-push action to build and publish the image? Yes.
5.  Is the YAML syntax correct and well-commented? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the GitHub Actions workflow for publishing Docker images to GHCR.

## Tips

Automating Docker image builds is a core part of modern CI/CD. This workflow provides a standard, reliable way to do it on GitHub.
