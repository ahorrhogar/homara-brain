---
name: brain-autofetch
description: Use when the user asks whether the brain is up to date, how the auto-pull works, why a recent edit isn't showing, or wants to disable/modify the auto-fetch behavior in this repo.
---

# Homara Brain auto-fetch

This repo has a `UserPromptSubmit` hook configured in `.claude/settings.json` that runs before every user message:

    git -C "$CLAUDE_PROJECT_DIR" pull --ff-only --quiet origin main 2>/dev/null || true

## What it does
- Pulls the latest commits from `origin/main` before each prompt is processed.
- Fast-forward only — if local commits or uncommitted edits would conflict, the pull is a silent no-op and the working tree is unchanged.
- Failures (no network, no upstream, non-FF state) are swallowed; the hook never blocks the prompt.

## Common questions
- **"Is Claude seeing my latest push?"** — Yes, as of the most recent prompt. If unsure, run `git -C /Users/martiwarda/Projects/homara/homara-brain log -1 --oneline` to compare with `origin/main`.
- **"Why didn't a remote change land?"** — Probably non-FF: there's an unpushed local commit or a dirty working tree. Run `git status` then `git pull` manually to resolve.
- **"How do I disable it?"** — Remove the `UserPromptSubmit` block from `homara-brain/.claude/settings.json` (or comment out the command).
- **"Can I make it run less often?"** — Move the hook from `UserPromptSubmit` to `SessionStart` (runs once per Claude Code session instead of per prompt).
- **"Why is `origin main` hard-coded?"** — So the hook works even on machines where `main` has no upstream tracking set. If you ever rename the default branch, update both `.claude/settings.json` and this file.

## Why project-scoped
Lives in `homara-brain/.claude/` so it's git-tracked and travels with the repo. User-scoped (`~/.claude`) would also try to pull this repo from other projects, which is wrong.
