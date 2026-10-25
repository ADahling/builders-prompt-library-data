---
title: "Clone Email System & Transactional Templates"
slug: clone-email-system-transactional-templates
stage: Build
category: "Website Cloning"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-email-system-transactional-templates
---
# Clone Email System & Transactional Templates

Generate a complete suite of responsive, transactional HTML email templates and the corresponding backend integration logic for a web app.

Variables: target_url, user_name, action_url

## Prompt

You are an email systems engineer. Reproduce the complete email system from the target website including all transactional email templates.

Target URL: {{target_url}}

## Email Templates to Reproduce
1. **Welcome Email**: Sent after signup. Branding, onboarding CTA, feature highlights.
2. **Email Verification**: Verify link, expiration notice, support contact.
3. **Password Reset**: Reset link, security notice, expiration.
4. **Invoice/Receipt**: Payment confirmation, line items, total, download link.
5. **Subscription Change**: Upgrade/downgrade confirmation, new plan details, effective date.
6. **Notification Digest**: Weekly/daily summary of activity.

## For Each Template
- Responsive HTML email (works in Gmail, Outlook, Apple Mail)
- Inline CSS (email clients strip <style> tags)
- Dark mode support (@media (prefers-color-scheme: dark))
- Plain text fallback
- Dynamic variables ({{user_name}}, {{action_url}}, etc.)
- Unsubscribe link (CAN-SPAM compliance)

## Backend Integration
- Email service setup (Resend, SendGrid, or Supabase Auth emails)
- Trigger logic (when to send each email)
- Rate limiting (prevent email flooding)
- Bounce/complaint handling
- Email preference center (user controls which emails they receive)

Output:
- Complete HTML email templates (React Email or MJML)
- Edge Function for sending each email type
- Database table for email preferences
- Email service configuration

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Reproduces the complete transactional email system. Responsive templates that work across all email clients.
