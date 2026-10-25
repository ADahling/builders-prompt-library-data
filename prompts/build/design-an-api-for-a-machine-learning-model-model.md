---
title: "Design an API for a Machine Learning Model"
slug: design-an-api-for-a-machine-learning-model-model
stage: Build
category: "API Design"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-machine-learning-model-model
---
# Design an API for a Machine Learning Model

Get a RESTful prediction API design for serving a trained model, with JSON input and output formats and an asynchronous prediction approach.

Variables: machine_learning_model

## Prompt

I have trained a {{machine_learning_model}} model and I want to deploy it as a web service so that other applications can use it for predictions.

Your task is to design a RESTful API for this machine learning model.

**Instructions:**
1.  **Prediction Endpoint:** Design a `POST /predict` endpoint that takes the input data for the model as a JSON payload and returns the model's prediction.
2.  **Input and Output Format:** Define the JSON format for the input data and the prediction response.
3.  **Asynchronous Prediction:** For models that take a long time to make a prediction, it might be better to use an asynchronous approach. Describe how you would modify your API design to support asynchronous predictions.

**Output Format:**
Provide the output as a Markdown document. Describe the design of the prediction endpoint, including the request and response formats. Also, describe your approach for handling asynchronous predictions.
