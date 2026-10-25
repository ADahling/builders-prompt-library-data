---
title: "CI/CD Pipeline for a Mobile App"
slug: ci-cd-pipeline-for-a-mobile-app
stage: Ship
category: "Deployment & Launch"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ci-cd-pipeline-for-a-mobile-app
---
# CI/CD Pipeline for a Mobile App

Automate cross-platform mobile builds, automated testing, code signing, and beta distribution to TestFlight and Google Play.

Variables: mobile_ci_cd_platform

## Prompt

You are a mobile developer. Your task is to set up a CI/CD pipeline for an iOS and Android app using a mobile-specific CI/CD platform like `{{mobile_ci_cd_platform}}`.

Instructions:
1. The pipeline should build the app for both iOS and Android.
2. It should run unit and UI tests on simulators or real devices.
3. It should handle code signing and provisioning profiles.
4. It should automatically upload the builds to TestFlight for iOS and Google Play Console for Android for beta testing.

## Tips

Mobile CI/CD has its own unique set of challenges and tools.
