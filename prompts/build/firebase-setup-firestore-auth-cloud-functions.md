---
title: "Firebase Setup: Firestore + Auth + Cloud Functions"
slug: firebase-setup-firestore-auth-cloud-functions
stage: Build
category: "Modern Data Stack"
grade: C
score: 61
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/firebase-setup-firestore-auth-cloud-functions
---
# Firebase Setup: Firestore + Auth + Cloud Functions

Set up a Firebase project for PROJECT DESCRIPTION with Firestore, Authentication, and Cloud Functions.

## Prompt

Set up a Firebase project for [PROJECT DESCRIPTION] with Firestore, Authentication, and Cloud Functions.

## 1. Project Setup
```bash
npm install firebase firebase-admin
npm install -g firebase-tools
firebase login
firebase init
```
Select: Firestore, Functions, Authentication, Hosting

## 2. Client SDK Setup (src/lib/firebase.ts)
```typescript
import { initializeApp } from 'firebase/app';
import { getFirestore } from 'firebase/firestore';
import { getAuth } from 'firebase/auth';

const firebaseConfig = {
  apiKey: import.meta.env.VITE_FIREBASE_API_KEY,
  authDomain: import.meta.env.VITE_FIREBASE_AUTH_DOMAIN,
  projectId: import.meta.env.VITE_FIREBASE_PROJECT_ID,
  // ... rest of config
};

export const app = initializeApp(firebaseConfig);
export const db = getFirestore(app);
export const auth = getAuth(app);
```

## 3. Firestore Data Model
Design collections and documents for: [DESCRIBE YOUR DATA]
- Use subcollections for 1:many relationships
- Denormalize data for read performance
- Plan Security Rules from day 1

## 4. Security Rules (firestore.rules)
Write rules for: [DESCRIBE ACCESS PATTERNS]
- Authenticated users can read/write own data
- Public data readable by all
- Admin-only collections

## 5. Cloud Functions (2nd gen)
Create functions for: [DESCRIBE SERVER-SIDE LOGIC]
- onDocumentCreated / onDocumentUpdated triggers
- HTTPS callable functions
- Scheduled functions

## 6. Authentication
Set up auth providers: [EMAIL / GOOGLE / APPLE / PHONE]
- Auth state listener pattern
- Protected routes
- Token management

## Tips

Firebase remains the go-to for mobile-first and real-time apps. Firestore's offline-first sync is unmatched.
