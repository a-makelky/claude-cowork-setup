# claude-cowork-setup

**Start here:** [GET-STARTED.md](./GET-STARTED.md) — universal onboarding for a personal **agent chief of staff** workspace (Cursor, Codex, Claude Code, or Claude Cowork).

| Guide | What it covers |
| --- | --- |
| **[GET-STARTED.md](./GET-STARTED.md)** | Full workspace pattern: `context/`, `AGENTS.md`, optional `vault/daily/today.md`, setup interview, connectors, daily habit |
| **[SETUP.md](./SETUP.md)** | **Cowork only** — original guided interview that generates `context/*.md` for Claude Cowork Global Instructions |

---

## Cowork quick path (context files only)

Paste the prompt from `SETUP.md` into a new Claude conversation at claude.ai, answer the questions, and Claude produces ready-to-use context files in about 10 minutes.

### What you get (SETUP.md)

```
claude-cowork-workspace/
└── context/
    ├── about-me.md
    ├── working-preferences.md
    ├── voice-and-tone.md        # work/both only
    ├── my-context.md
    └── global-instructions.md
```

### How to use SETUP.md

1. Open `SETUP.md`
2. Copy the prompt inside the code block
3. Paste into a new Claude conversation at claude.ai
4. Answer the interview questions
5. Save the generated files to a local `claude-cowork-workspace/context/` folder
6. Paste `global-instructions.md` into Cowork → Settings → Global Instructions

For Cursor, Codex, or Claude Code — use **GET-STARTED.md** instead (same interview, plus `AGENTS.md` and optional daily notes).

## Version control

Each generated file includes a version header and changelog. Bump the version and update the changelog any time you edit a file.

## Contributing

If you improve the interview flow or discover file structures that work well, open a PR.
