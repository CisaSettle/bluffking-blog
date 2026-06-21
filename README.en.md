[中文](./README.md) · [English](./README.en.md)

# BluffKing Blog

> Engineering "build notes" from a poker app built almost entirely with AI coding agents.

This repository (`CisaSettle/bluffking-blog`) is the **public source repo** for BluffKing's bilingual (中文 / English) engineering "build notes" blog: a set of self-contained bilingual HTML posts, zero build, no framework.

[BluffKing](https://bluffking.ai) is a browser No-Limit Texas Hold'em app built almost entirely **with AI coding agents** (Claude Code + OpenAI Codex). This blog documents that build: agent orchestration, Rust, and deterministic poker. We open-source the notes because getting an agent team to actually do the work is worth writing down — and worth reusing.

## Live blog

The canonical live blog lives on the marketing site; this repo's content is mirrored there for rendering:

- 中文: <https://bluffking.ai/zh/blog/>
- English: <https://bluffking.ai/en/blog/>
- First post: <https://bluffking.ai/zh/blog/why-worktrees/> · <https://bluffking.ai/en/blog/why-worktrees/>

This repo is also served via a GitHub Pages mirror at <https://cisasettle.github.io/bluffking-blog/>. That mirror sets `rel=canonical` to `bluffking.ai/zh/blog/` — i.e. it **defers** to the canonical site rather than competing with it.

## What's in here

Every post is a **self-contained HTML file**: no build step, no framework, both languages inline.

| File | Purpose |
| --- | --- |
| `index.html` | Static landing page listing the posts, with a 中文/English toggle (persisted via `localStorage`, default 中文). |
| `<slug>.html` | One self-contained HTML file per post (e.g. `why-worktrees.html`). Both languages inline, in-page 中文/English toggle, default 中文, green brand palette. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is, without Jekyll processing. |
| `README.md` / `README.en.md` | This bilingual README. |

### How a post is structured

- **Self-contained bilingual HTML**: both 中文 and English live in the same file.
- **In-page toggle**: switch between the two languages via the 中文/English toggle, **default 中文**.
- **Never inline-mixed**: one language shows at a time; the two are never displayed side by side.
- **Zero dependencies**: no external dependencies, no build, no framework — just open it in a browser.

## Posts so far

| Date | Slug | Title | Tags |
| --- | --- | --- | --- |
| 2026-06-20 | `why-worktrees` | Why every AI coding agent needs its own git worktree | git worktree · Claude Code · Codex · agent orchestration |

## Add a post

1. Copy an existing `<slug>.html` as your template.
2. Write **both 中文 and English** inside it behind the toggle (default 中文, **never inline-mixed**).
3. Add a card to `index.html`.
4. Commit.

The same post also gets mirrored into the marketing site (`website/content/posts/<slug>/{zh,en}.html`) — that mirror is what powers the canonical `bluffking.ai` blog.

## About BluffKing

BluffKing is a browser No-Limit Texas Hold'em app built almost entirely with AI coding agents (Claude Code + OpenAI Codex). This blog documents that build: agent orchestration, Rust, and deterministic poker.

---

Main site [bluffking.ai](https://bluffking.ai) · X / Twitter [@PokerCoachAI](https://x.com/PokerCoachAI)
