---
title: "Build an Email Notification System"
slug: build-an-email-notification-system
stage: Build
category: "API Design"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-an-email-notification-system
---
# Build an Email Notification System

Get Edge Function code, email templates, a log schema, and frontend triggers for app emails with queues, tracking, and unsubscribe handling.

## Prompt

Build a complete transactional email system for [describe app]:

1. Edge Function: Receives trigger (user signup, order confirmed, password reset), renders email template, sends via [Resend / SendGrid / Postmark].
2. Email Templates: HTML email templates for each trigger — responsive, branded, tested across clients.
3. Queue Pattern: For bulk emails, implement a queue to avoid rate limits. Process in batches with delay between sends.
4. Tracking: Open tracking, click tracking, bounce handling. Store delivery status in database.
5. Unsubscribe: One-click unsubscribe link in every email. Respect unsubscribe preferences before sending.
6. Testing: Preview emails in development without sending. Use test mode / sandbox API keys.
7. Rate Limiting: Max emails per user per hour to prevent abuse.

Include complete Edge Function code, database schema for email logs, and frontend trigger examples.

## Tips

Email is the most important notification channel. Get deliverability right from the start.
