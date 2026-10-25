---
title: "Set Up Drizzle ORM with Postgres (Step-by-Step)"
slug: set-up-drizzle-orm-with-postgres-step-by-step
stage: Build
category: "Modern Data Stack"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-drizzle-orm-with-postgres-step-by-step
---
# Set Up Drizzle ORM with Postgres (Step-by-Step)

Get a Drizzle ORM setup for a TypeScript and PostgreSQL project, including typed schemas, a database client, migrations, Studio, and CRUD examples.

## Prompt

Set up Drizzle ORM in my TypeScript project with PostgreSQL. Include:

1. Install dependencies:
```bash
npm install drizzle-orm postgres
npm install -D drizzle-kit
```

2. Create drizzle.config.ts:
```typescript
import { defineConfig } from 'drizzle-kit';

export default defineConfig({
  schema: './src/db/schema.ts',
  out: './drizzle',
  dialect: 'postgresql',
  dbCredentials: {
    url: process.env.DATABASE_URL!,
  },
});
```

3. Define schema (src/db/schema.ts) for these tables: [DESCRIBE YOUR TABLES]
   - Include: primary keys, timestamps, foreign keys, indexes
   - Use proper column types (text, integer, boolean, timestamp, jsonb)
   - Add TypeScript inference types (InferSelectModel, InferInsertModel)

4. Create db client (src/db/index.ts):
```typescript
import { drizzle } from 'drizzle-orm/postgres-js';
import postgres from 'postgres';
import * as schema from './schema';

const client = postgres(process.env.DATABASE_URL!);
export const db = drizzle(client, { schema });
```

5. Generate and run migration:
```bash
npx drizzle-kit generate
npx drizzle-kit push
```

6. Add Drizzle Studio for visual DB browser:
```bash
npx drizzle-kit studio
```

7. Example CRUD operations using the query API

## Tips

Drizzle is the fastest-growing ORM in 2026. SQL-like API means the learning curve is near zero for anyone who knows SQL.
