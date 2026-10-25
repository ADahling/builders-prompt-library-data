---
title: "Broken Image Links in Sent Emails"
slug: broken-image-links-in-sent-emails
stage: Test
category: "Functional Bugs"
grade: A+
score: 93
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/broken-image-links-in-sent-emails
---
# Broken Image Links in Sent Emails

Fix broken email images by converting relative paths to absolute URLs and implementing CDN hosting for reliable asset delivery.

Variables: project_name, your_domain

## Prompt

You are a developer for {{project_name}}. The emails sent by your application are supposed to contain images (like a company logo), but users see broken image icons instead. The `<img>` tags in the email HTML are using relative paths (e.g., `<img src="/images/logo.png">`) instead of absolute URLs.

Email clients have no concept of your website's file structure, so they cannot resolve these relative paths. All assets in an email must be referenced with a full, absolute URL.

**Context:**
- **Problem:** Images in emails are broken because of relative paths.

**Instructions:**

1.  **Analyze the Relative Path Problem:** Explain why relative paths work on a website but fail completely in the context of an email that can be opened in any client (Gmail, Outlook, Apple Mail) on any device.
2.  **Fix the Email Template:** Modify the HTML email template. Find all `<img>` tags and change their `src` attributes from relative paths to absolute URLs that point to a publicly accessible server where the images are hosted (e.g., `https://cdn.{{your_domain}}.com/images/logo.png`).
3.  **Discuss Image Hosting:** Briefly discuss the best practices for hosting email images. Explain that these images should be hosted on a reliable, fast server or a Content Delivery Network (CDN) to ensure they load quickly for all users.

**Output Format:**

- **Problem Analysis:** A clear explanation of why relative paths don't work in emails.
- **Corrected HTML `<img>` Tag:** An example of the fixed `<img>` tag with an absolute URL.
- **Image Hosting Best Practices:** A short summary of how and where to host email assets.

## Tips

A simple but very common mistake for developers who are new to building HTML emails.
