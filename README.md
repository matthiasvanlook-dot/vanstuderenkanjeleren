# Leerplatform AI — Monorepo

Stack:
- Frontend: Next.js (App Router) + TypeScript + Tailwind + shadcn/ui
- Backend: NestJS + Prisma + PostgreSQL
- Package manager: pnpm workspaces

## Snel starten

```bash
# 1) Vereisten: Node 20+, pnpm, PostgreSQL 14+
pnpm i

# 2) .env instellen
cp apps/api/.env.example apps/api/.env
cp apps/web/.env.example apps/web/.env

# 3) Database migraties & seed
cd apps/api
pnpm prisma migrate dev --name init
pnpm ts-node prisma/seed.ts

# 4) Starten (in de root)
pnpm dev
```

Werkruimte scripts:
- `pnpm dev` start **frontend** op `http://localhost:3000` en **backend** op `http://localhost:4000`.
