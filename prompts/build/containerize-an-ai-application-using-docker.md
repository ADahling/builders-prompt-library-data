---
title: "Containerize an AI Application using Docker"
slug: containerize-an-ai-application-using-docker
stage: Build
category: "DevOps & IaC"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/containerize-an-ai-application-using-docker
---
# Containerize an AI Application using Docker

Get a commented multi-stage Dockerfile for a Python AI app, covering dependency installation, model files, and a non-root runtime user.

Variables: app_purpose, port_number

## Prompt

I have a Python-based AI application for `{{app_purpose}}` that I need to containerize using Docker. This will make it easier for others to run the application in a consistent and reproducible environment.

The application has the following structure:
*   The main application script is `app.py`.
*   Dependencies are listed in `requirements.txt`.
*   It requires a pre-trained model file located at `models/model.p`.
*   It exposes a service on port `{{port_number}}`.

Your task is to generate a complete and optimized `Dockerfile` for this application. The Dockerfile should follow best practices for security, build speed, and image size.

Generate the `Dockerfile` content with detailed comments explaining each instruction. The Dockerfile should perform the following steps:

1.  **Use a Multi-Stage Build**: 
    *   **Build Stage**: Start from a standard Python base image (e.g., `python:3.9-slim-buster`) to install dependencies. This helps keep the final image smaller.
    *   Copy only the `requirements.txt` file first.
    *   Install the dependencies using `pip` with the `--no-cache-dir` option to reduce layer size.

2.  **Final Stage**:
    *   Start from the same clean Python base image.
    *   Copy the installed packages from the build stage into the final image.
    *   Copy the application source code (including the `app.py` and the `models` directory).
    *   Create a non-root user to run the application for better security. The user should be named `appuser`.
    *   Set the working directory to the user's home directory.
    *   Switch to the non-root user.
    *   Expose the application's port.
    *   Define the command to run the application when the container starts.

Additionally, create a `.dockerignore` file to prevent unnecessary files from being copied into the Docker context (e.g., `__pycache__`, `.git`, `.vscode`).

Your output should include the content for both the `Dockerfile` and the `.dockerignore` file.

Constraint Checklist & Confidence Score:
1.  Does the Dockerfile use a multi-stage build? Yes.
2.  Does it follow best practices like using a non-root user and caching dependency installation? Yes.
3.  Is the Dockerfile well-commented and easy to understand? Yes.
4.  Is the .dockerignore file comprehensive? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the content for the Dockerfile and .dockerignore file.

## Tips

Docker is an essential tool for packaging and distributing applications, ensuring that they run reliably in any environment.
