---
title: "Write a Test for a Machine Learning Model"
slug: write-a-test-for-a-machine-learning-model
stage: Test
category: "Testing & QA"
grade: B
score: 73
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-test-for-a-machine-learning-model
---
# Write a Test for a Machine Learning Model

Evaluate a specific machine learning model by generating a script to load data, run predictions, and produce a detailed metric report.

Variables: model_type, model_purpose, metric_1, metric_2

## Prompt

You are a machine learning engineer. Your task is to write a test for a machine learning model to evaluate its performance and ensure that it meets the quality standards. The model is a {{model_type}} that is trained to {{model_purpose}}.

Context:
- You need to test the model with a separate test dataset that was not used for training.
- You will use a set of metrics to evaluate the performance of the model, such as {{metric_1}} and {{metric_2}}.

Provide:
1. A test that loads the trained model and the test dataset.
2. A script to make predictions with the model on the test dataset.
3. A report with the performance metrics of the model and a confusion matrix.

## Tips

An advanced prompt for machine learning engineers who want to learn how to test their models and ensure their quality.
