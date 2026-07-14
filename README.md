<div align="center">

<img src="assets/banner.png" alt="Plaiful - AI Agent Directory" width="100%" />

<h1>Plaiful - AI Agent Directory</h1>

<p><b>A full-stack SaaS platform for discovering and comparing AI agents - built as a heavy customization of the open-source OpenAlternative codebase for the banking &amp; credit-union sector.</b></p>

<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React%2019-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React 19" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white" alt="Prisma" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white" alt="Turborepo" />
  <img src="https://img.shields.io/badge/License-GPL--3.0-blue?style=flat-square" alt="License GPL-3.0" />
</p>

</div>

---

## Overview

**Plaiful** is a directory platform where users can discover, browse, and compare AI agents. It was delivered for a client as a dedicated space for the banking and credit-union sector, with advanced filtering, search, and a modern, intuitive interface.

The project is built on top of the open-source [OpenAlternative](https://openalternative.co/) codebase, which I significantly customized and extended - reworking it from a general software directory into a focused, production AI-agent directory.

> **Attribution:** This project uses source code from the open-source [OpenAlternative](https://openalternative.co/) and is released under the same **GPL-3.0** license.

## What I Worked On

- Reworked the OpenAlternative software directory into a **dedicated AI-agent directory** for the banking / credit-union niche
- Advanced **filtering and search** for discovering and comparing agents
- A modern, intuitive **listing and detail UI**
- Integration and configuration across the full monorepo stack below

## Tech Stack

| Area | Tech |
| --- | --- |
| Monorepo | Turborepo + Bun workspaces |
| Framework | Next.js (App Router) + React 19 |
| Language | TypeScript |
| Database | Prisma ORM + PostgreSQL |
| Auth | Auth.js (NextAuth v5) |
| AI | Vercel AI SDK (OpenAI + Anthropic), Firecrawl for enrichment |
| Payments | Stripe |
| Email | Resend + React Email |
| Background jobs | Inngest |
| Caching / limits | Upstash Redis + Ratelimit |
| Storage | AWS S3 |
| UI | Radix UI, Tailwind CSS, Tiptap editor, TanStack Table |
| Analytics | PostHog |

## Project Structure

```
apps/
  web/          # Next.js application (frontend + server actions + API)
packages/
  db/           # Prisma schema, client, migrations, and seeds
  github/       # GitHub data integration
```

## Getting Started

### Prerequisites

- [Bun](https://bun.sh/) `1.1.40+`
- A PostgreSQL database
- API keys for the integrations you plan to use (OpenAI/Anthropic, Stripe, Resend, Upstash, S3, etc.)

### Setup

```bash
git clone https://github.com/yuto-kazuma/plai.git
cd plai
bun install

# configure environment (see apps/web and packages/db for required vars)
cp apps/web/.env.example apps/web/.env

# generate the Prisma client & run migrations
bun run db:generate
bun run db:migrate

# start the dev server
bun run dev
```

### Useful scripts

```bash
bun run build        # build all apps/packages via Turborepo
bun run typecheck    # type-check the monorepo
bun run db:studio    # open Prisma Studio
bun run db:seed      # seed the database
```

## License

Released under the **GPL-3.0** license, inherited from [OpenAlternative](https://openalternative.co/). See the [LICENSE](LICENSE) file.

---

<div align="center">
  <sub>Customized &amp; delivered by <a href="https://github.com/yuto-kazuma">Yuto Kazuma</a> · <a href="https://yuto-kazuma.vercel.app/">Portfolio</a></sub>
</div>
