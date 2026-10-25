---
title: "Build a Stripe Payment Integration"
slug: build-a-stripe-payment-integration
stage: Build
category: "API Design"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-stripe-payment-integration
---
# Build a Stripe Payment Integration

Get code for a Stripe payment flow with Supabase Edge Functions, Checkout, verified webhooks, subscription records, and premium access controls.

## Prompt

Set up complete Stripe payment flow for [describe what users pay for]:

1. Edge Function: Create Stripe Checkout session with correct price, redirects, metadata. Secret key in Supabase secrets.
2. Frontend: Payment button calling Edge Function, redirect to Stripe Checkout.
3. Webhook Handler: Edge Function receiving Stripe events (checkout.session.completed, invoice.payment_failed), verifying webhook signature, updating subscription in DB.
4. Database: subscription table (user_id, stripe_customer_id, stripe_subscription_id, status, current_period_end).
5. Access Control: Gate premium features in both frontend and RLS policies.
6. Test Mode: Full flow with Stripe test mode.

Complete code for every piece.

## Tips

Most common integration people get wrong.
