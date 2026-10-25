---
title: "Generate a CI/CD Pipeline Configuration for a Node.js Web App"
slug: generate-a-ci-cd-pipeline-configuration-for-a-node-js-web-app
stage: Ship
category: "Deployment & Launch"
grade: A+
score: 94
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-ci-cd-pipeline-configuration-for-a-node-js-web-app
---
# Generate a CI/CD Pipeline Configuration for a Node.js Web App

Get commented GitHub Actions YAML to install, test, build, and deploy a Node.js app over SSH on pushes to main, with step explanations.

Variables: server_host, server_user, ssh_private_key, project_name

## Prompt

I need to create a basic CI/CD pipeline for my Node.js web application. The application is hosted on GitHub and I want to deploy it to a server using SSH.

Please generate a complete CI/CD pipeline configuration file for GitHub Actions.

The pipeline should be triggered on every push to the `main` branch.

Here are the steps I want to include in the pipeline:
1.  **Checkout Code:** Check out the latest code from the repository.
2.  **Install Dependencies:** Install the Node.js dependencies using `npm install`.
3.  **Run Tests:** Run the unit tests for the application using `npm test`.
4.  **Build Application:** Build the application for production using `npm run build`.
5.  **Deploy to Server:** Deploy the built application to the production server using `scp` and `ssh`.

Here are the details for the deployment step:
-   **Server Host:** `{{server_host}}`
-   **Server User:** `{{server_user}}`
-   **SSH Private Key:** `{{ssh_private_key}}`
-   **Source Directory:** `./build`
-   **Destination Directory:** `/var/www/{{project_name}}`

Please provide the complete YAML configuration file for the GitHub Actions workflow. The configuration should be well-commented and easy to understand. Also, provide a brief explanation of each step in the pipeline.

## Tips

This prompt is for beginners who are new to CI/CD and want to set up a simple pipeline for their Node.js application.
