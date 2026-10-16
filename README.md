# Agent Rules Starter: free Cursor rules, AGENTS.md and CLAUDE.md templates

Drop-in rules and prompts that make AI coding agents (Cursor, Claude Code, Codex, Windsurf, Copilot) write code for your stack **as it is today**: current APIs, your conventions, fewer repeated mistakes. Made by [Grizzly Kiwi Dev](https://grizzlykiwidev.github.io/).

## What's inside
| File | What it does | Works with |
|---|---|---|
| [`.cursor/rules/00-general.mdc`](.cursor/rules/00-general.mdc) | Core working agreement: read first, small changes, verify, never fake a fix. Always on. | Cursor |
| [`.cursor/rules/nextjs-supabase.mdc`](.cursor/rules/nextjs-supabase.mdc) | Next.js App Router + Supabase: server/client split, async `params`, `@supabase/ssr`, `getUser()`, RLS. | Cursor |
| [`.cursor/rules/godot4-gdscript.mdc`](.cursor/rules/godot4-gdscript.mdc) | Godot 4 GDScript with a Godot 3 → 4 syntax table, static typing, "call down, signal up". | Cursor |
| [`AGENTS.md`](AGENTS.md) | Fill-in project instructions template. | Cursor, Codex, Copilot, Windsurf, most agents |
| [`CLAUDE.md`](CLAUDE.md) | Fill-in template for Claude Code. | Claude Code |
| [`prompts/vibe-coding-prompts.md`](prompts/vibe-coding-prompts.md) | 10 reusable prompts: debug, refactor, tests, review, security, deploy check. | Any agent |

Checked 16 Oct 2026 against Cursor's `.mdc` rules format, Next.js 15–16, `@supabase/ssr` and Godot 4.x.

## Install
1. Copy `.cursor/rules/` into your project root. Keep only the stack files you use.
2. Copy `AGENTS.md` (and/or `CLAUDE.md`) to your project root and replace every `<...>`. Fill in the commands section first.
3. Using both Cursor and Claude Code? Put `@AGENTS.md` at the top of `CLAUDE.md` so you only maintain one file.

```bash
npx degit grizzlykiwidev/grizzlykiwidev.github.io my-rules && cp -r my-rules/.cursor my-rules/AGENTS.md ./
```

## Get it as a download
- Free zip (same files): https://grizzlykiwi.gumroad.com/l/rdubay
- **Starter Pack (early bird US$19):** 12 rules across 9 stacks (Next.js, Supabase, FastAPI, React/Vite, Express 5, Tailwind v4, Godot 4, Unity 6, Unreal Engine 5), 30 prompts, stack-specific AGENTS.md templates and workflow guides: https://grizzlykiwi.gumroad.com/l/xgdajx

## Licence
Free for personal and commercial use in your own projects. Please don't resell or redistribute the files as-is; link to this repo or the download page instead. Provided as-is, with no warranty. Always review what your agent writes.
