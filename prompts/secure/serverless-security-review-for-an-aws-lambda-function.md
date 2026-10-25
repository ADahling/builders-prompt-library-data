---
title: "Serverless Security Review for an AWS Lambda Function"
slug: serverless-security-review-for-an-aws-lambda-function
stage: Secure
category: "Security Review"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/serverless-security-review-for-an-aws-lambda-function
---
# Serverless Security Review for an AWS Lambda Function

Conduct a comprehensive security audit of AWS Lambda and API Gateway configurations to identify vulnerabilities and enforce least privilege.

Variables: language

## Prompt

You are a cloud security engineer reviewing a serverless application built with AWS Lambda and API Gateway. The function is written in {{language}} and processes sensitive user data. Your task is to perform a thorough security review of the serverless architecture and the function code itself.

Your review should cover:

1.  **IAM Role and Permissions:** Analyze the IAM execution role attached to the Lambda function. Ensure it follows the principle of least privilege and only has the permissions it absolutely needs.
2.  **API Gateway Configuration:** Review the API Gateway settings, including authentication and authorization mechanisms (e.g., API keys, IAM roles, or Cognito user pools). Check for any open endpoints that could be abused.
3.  **Function Code Security:** Examine the Lambda function code for vulnerabilities such as injection flaws, insecure handling of secrets, and improper error handling. Pay close attention to how the function interacts with other AWS services.
4.  **Dependency Security:** Scan the function's third-party dependencies for known vulnerabilities using a tool like Snyk or the AWS-native scanner.
5.  **Logging and Monitoring:** Verify that the function has adequate logging and is integrated with CloudWatch for monitoring and alerting on security events.

For each vulnerability or misconfiguration you find, provide a detailed explanation of the risk and a clear recommendation for how to fix it. Your output should be a structured security report in Markdown, suitable for sharing with the development team.
