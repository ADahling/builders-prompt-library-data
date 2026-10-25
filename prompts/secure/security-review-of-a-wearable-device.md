---
title: "Security Review of a Wearable Device"
slug: security-review-of-a-wearable-device
stage: Secure
category: "Security Review"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-review-of-a-wearable-device
---
# Security Review of a Wearable Device

Conduct a comprehensive security audit of a wearable device's firmware, Bluetooth communication, mobile application, and cloud infrastructure.

Variables: device_name, device_type

## Prompt

You are a security engineer reviewing a new wearable device, {{device_name}}. The device is a {{device_type}} that collects biometric data and syncs it with a mobile app. Your task is to identify and mitigate security vulnerabilities in the device and the mobile app.

Create a detailed security review report in Markdown. The report should cover the following areas:

1.  **Device Security:**
    *   Is the device vulnerable to physical attacks?
    *   Is the firmware signed and encrypted?
    *   Is there a secure boot process?

2.  **Bluetooth Security:**
    *   Is the Bluetooth communication between the device and the mobile app secure?
    *   Is it vulnerable to eavesdropping or man-in-the-middle attacks?

3.  **Mobile App Security:**
    *   How is the biometric data stored on the mobile app? Is it encrypted?
    *   Is the mobile app vulnerable to common mobile app vulnerabilities?

4.  **Cloud Security:**
    *   How is the biometric data stored in the cloud? Is it encrypted?
    *   Is the cloud backend secure?

For each area, provide your assessment and a list of prioritized recommendations for improvement. Your report should be a comprehensive guide for the development team to build a secure wearable device.
