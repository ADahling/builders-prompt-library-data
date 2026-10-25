---
title: "Clone Pricing Page with Stripe Integration"
slug: clone-pricing-page-with-stripe-integration
stage: Build
category: "Website Cloning"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-pricing-page-with-stripe-integration
---
# Clone Pricing Page with Stripe Integration

Replicate a professional SaaS pricing page and end-to-end Stripe subscription workflow including webhooks, database sync, and billing portal.

Variables: target_url

## Prompt

You are a full-stack developer specializing in SaaS billing. Reproduce the pricing page and payment flow from the target website.

Target URL: {{target_url}}

## Frontend
1. **Pricing Table**: Exact layout (columns, feature comparison, highlighted plan, toggle for monthly/annual).
2. **Plan Cards**: Styling, feature lists with check/x icons, CTA buttons, "Most Popular" badge.
3. **Billing Toggle**: Monthly/Annual switch with discount percentage display and price animation.
4. **Feature Comparison**: Full comparison table with tooltips explaining each feature.
5. **FAQ Section**: Common billing questions with accordion behavior.

## Backend (Stripe + Supabase)
1. **Stripe Products & Prices**: Create products matching each plan, with monthly and annual price variants.
2. **Checkout Flow**: Stripe Checkout Session creation with success/cancel URLs.
3. **Webhook Handler**: Process checkout.session.completed, invoice.paid, customer.subscription.updated, customer.subscription.deleted.
4. **Subscription Management**: Upgrade, downgrade, cancel, reactivate flows.
5. **Usage Tracking**: If usage-based pricing, implement metered billing.
6. **Customer Portal**: Stripe Customer Portal for self-service billing management.

## Database
- subscriptions table (user_id, stripe_customer_id, stripe_subscription_id, plan, status, current_period_end)
- RLS policies for subscription access
- Helper function: get_user_plan(user_id)

Output complete code for:
- PricingPage component with all variants
- Stripe Edge Functions (create-checkout, webhook-handler, create-portal)
- Database migrations
- Subscription context provider for frontend

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Complete SaaS pricing page with Stripe billing integration. Handles subscriptions, webhooks, and customer portal.
