# AGENTS.md

<!-- Template. Replace every <...>. Delete sections you don't need. Keep it under ~150 lines: agents read all of it every time. -->

## Project
<One or two sentences: what this app does and who uses it.>

## Stack
- <e.g. Next.js 15 (App Router), TypeScript strict, Tailwind, Supabase>
- Package manager: <pnpm>. Do not use any other.

## Commands
- Install: `<pnpm install>`
- Dev: `<pnpm dev>`
- Typecheck: `<pnpm typecheck>`
- Lint: `<pnpm lint>`
- Test (single file): `<pnpm test path/to/file>`
Run typecheck, lint and relevant tests before saying a task is done.

## Layout
- `<app/>` routes and pages
- `<lib/>` shared logic; `<components/>` UI
- Canonical examples to copy: `<path/to/good-component.tsx>`, `<path/to/good-test.ts>`

## Conventions
- Small, focused changes. Follow existing patterns over personal preference.
- No new dependencies without explaining why.
- Secrets live in env vars; update `.env.example` when adding one.
- Never use `any`, `@ts-ignore` or empty `catch` to get past an error.

## Testing
- Every bug fix gets a test that fails before the fix.
- <Framework: Vitest / Pytest / GUT>. Tests live next to code as `*.test.ts`.

## Boundaries
- Ask first: deleting files, changing DB schema, CI config, auth, payments.
- Never: force-push, commit secrets, edit generated files or applied migrations.

## Gotchas
- <Things that bit you or the agent before, e.g. "params is async in Next 15".>
