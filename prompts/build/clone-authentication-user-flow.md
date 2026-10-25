---
title: "Clone Authentication & User Flow"
slug: clone-authentication-user-flow
stage: Build
category: "Website Cloning"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-authentication-user-flow
---
# Clone Authentication & User Flow

Reverse-engineer and implement a full-stack authentication system using React and Supabase based on a target website's specific user flows.

Variables: target_url

## Prompt

You are a full-stack engineer specializing in authentication systems. Reproduce the complete auth flow from the target website.

Target URL: {{target_url}}

Reproduce the complete auth system:

## Frontend
1. **Sign Up Flow**: Form fields, validation rules, password requirements, email verification, onboarding steps.
2. **Sign In Flow**: Email/password, social OAuth providers (Google, GitHub, etc.), magic link, remember me.
3. **Password Reset**: Request flow, email template, reset form, success confirmation.
4. **Protected Routes**: Route guard pattern, redirect behavior, loading states during auth check.
5. **User Menu**: Avatar, dropdown with profile/settings/logout, responsive behavior.
6. **Form UX**: Inline validation, error messages, loading states, success animations.

## Backend (Supabase)
1. **Auth Configuration**:
   - Email/password settings
   - OAuth provider setup (exact providers used)
   - Email templates (verification, reset, magic link)
   - Redirect URLs

2. **Database Schema**:
   - Profiles table (linked to auth.users)
   - RLS policies for profile access
   - Trigger for auto-creating profile on signup

3. **Row Level Security**:
   - Users can read own profile
   - Users can update own profile
   - Public profiles (if applicable)

Build with:
- React + TypeScript
- Supabase Auth (@supabase/supabase-js)
- React Router (protected route component)
- Zod for form validation
- Sonner for toast notifications

Output complete code for: AuthProvider, SignUpForm, SignInForm, ResetPasswordForm, ProtectedRoute, UserMenu, and all Supabase migrations.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Complete auth system reproduction including social OAuth, email verification, and Supabase backend. Production-ready.
