---
title: "Set Up Prisma with Postgres (Step-by-Step)"
slug: set-up-prisma-with-postgres-step-by-step
stage: Build
category: "Modern Data Stack"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-prisma-with-postgres-step-by-step
---
# Set Up Prisma with Postgres (Step-by-Step)

Get a Prisma setup for TypeScript and PostgreSQL, with schemas, migrations, a database client, Studio, and CRUD and transaction examples.

## Prompt

Set up Prisma in my TypeScript project with PostgreSQL. Include:

1. Install dependencies:
```bash
npm install prisma @prisma/client
npx prisma init
```

2. Define schema (prisma/schema.prisma) for these tables: [DESCRIBE YOUR TABLES]
   - Include: @id, @default, @unique, @relation, @map
   - Add @@index for frequently queried columns
   - Use proper types (String, Int, Boolean, DateTime, Json)

3. Configure datasource:
```prisma
datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

generator client {
  provider = "prisma-client-js"
}
```

4. Generate client and run migration:
```bash
npx prisma generate
npx prisma migrate dev --name init
```

5. Create db client (src/lib/prisma.ts):
```typescript
import { PrismaClient } from '@prisma/client';

const globalForPrisma = globalThis as unknown as { prisma: PrismaClient };
export const prisma = globalForPrisma.prisma || new PrismaClient();
if (process.env.NODE_ENV !== 'production') globalForPrisma.prisma = prisma;
```

6. Launch Prisma Studio:
```bash
npx prisma studio
```

7. Example CRUD operations:
   - findMany with include and where
   - create with nested relations
   - update and upsert patterns
   - Transaction example

## Tips

Prisma's DX remains excellent. The schema.prisma DSL is opinionated but productive. Re-run 'prisma generate' after every schema change.
