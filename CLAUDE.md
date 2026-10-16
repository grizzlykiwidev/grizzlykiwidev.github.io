# CLAUDE.md

<!-- Template for Claude Code. Replace <...>. If you also keep AGENTS.md, you can make this file just one line: @AGENTS.md  (Claude Code imports the referenced file) and add Claude-specific notes below it. -->

## Project
<What it is, in one sentence.> Stack: <...>.

## Commands
- Build: `<...>`  Typecheck: `<...>`  Lint: `<...>`
- Test one file: `<...>` (prefer single-file runs over the full suite)

## Workflow
1. For non-trivial work: explore the relevant files, then propose a plan before editing.
2. Make the smallest change that works; follow existing patterns.
3. Verify: typecheck, lint, run affected tests. Report what you ran and the result.
4. Commit only when asked. Use conventional commits (`feat:`, `fix:`, `chore:`).

## Code style
- <TypeScript strict, named exports, early returns...>
- IMPORTANT: never use `any`, `@ts-ignore`, or skip/delete tests to make checks pass.

## Ask before
- Deleting files, schema/migration changes, adding dependencies, touching auth/payments/CI.

## Gotchas
- <Project-specific traps.>
