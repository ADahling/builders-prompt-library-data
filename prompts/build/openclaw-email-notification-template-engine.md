---
title: "OpenClaw: Email & Notification Template Engine"
slug: openclaw-email-notification-template-engine
stage: Build
category: "OpenClaw"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-email-notification-template-engine
---
# OpenClaw: Email & Notification Template Engine

Write event-triggered messages for email, push, SMS, or in-app channels using your brand voice and structured transactional copy guidelines.

Variables: event, voice, channel, product, name, days, Product

## Prompt

# Email & Notification Template Engine

## Input
- Trigger event: {{event}} (signup, purchase, password reset, etc.)
- Brand voice: {{voice}} (professional / friendly / minimal)
- Channel: {{channel}} (email / push / SMS / in-app)

## Email Template Framework

### Transactional Emails
| Event | Subject Line | Key Content |
|-------|-------------|-------------|
| Welcome | Welcome to {{product}}, {{name}}! | Next steps, key features, support link |
| Email Verify | Verify your email address | One-click verify button, expiry note |
| Password Reset | Reset your {{product}} password | Reset button, expiry (1hr), security note |
| Purchase Receipt | Your receipt from {{product}} | Items, total, billing info, support |
| Trial Ending | Your trial ends in {{days}} days | Value recap, upgrade CTA, comparison |

### Structure (every email)
1. **Preheader:** 40-90 chars, extends subject line
2. **Header:** Logo + optional nav
3. **Hero:** One clear message + primary CTA
4. **Body:** Supporting details (keep <200 words)
5. **CTA:** One primary button (contrasting color, 44px+ height)
6. **Footer:** Unsubscribe, address, social links

### Copy Rules
- Subject: <50 chars, no ALL CAPS, no spam triggers
- Body: 2nd person ("you/your"), active voice, short paragraphs
- CTA: Action verb + benefit ("Start your free trial", not "Click here")
- Mobile: 40% of opens — single column, 16px+ body text

## Push Notifications
- Title: <50 chars
- Body: <100 chars
- Deep link to relevant screen
- Respect quiet hours (no sends 10pm-8am local)
- Batch non-urgent notifications

## SMS
- <160 chars (avoid multi-part)
- Include opt-out: "Reply STOP to unsubscribe"
- No URL shorteners (spam filters)
- Identify sender: "{{Product}}: Your code is 123456"

## Tips

Template engine for transactional emails, push notifications, and SMS. Includes copy rules, structure guidelines, and channel-specific best practices.
