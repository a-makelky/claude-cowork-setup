# Get started: your agent chief of staff

**Version:** 1.0  
**Created:** 2026-05-26  
**Canonical home:** This file in [claude-cowork-setup](https://github.com/a-makelky/claude-cowork-setup) — universal guide for Cursor, Claude Code, Codex, and Claude Cowork.

**Cowork-only interview:** For the original Claude Cowork context-file prompt (no AGENTS.md / vault), use [SETUP.md](./SETUP.md) in this repo.

---

## What this is

One local workspace where your AI agent can see your context, connect to the tools you already use, and help you monitor work, draft outputs, and automate boring repeats — without jumping between a dozen apps.

Think of it as a **chief of staff folder**, not a chatbot thread.

You do not need to be technical. You need:

- A Mac (or PC with a similar agent tool)
- One coding-agent app you already like: **Cursor**, **Claude Code**, **Codex**, or **Claude Cowork**
- About 15 minutes for the setup interview below

---

## What you are building

Start small. You can grow later.

```
my-chief-of-staff/
├── README.md                 # what this folder is
├── AGENTS.md                 # main instructions (Codex / Cursor)
│   or CLAUDE.md              # if you use Claude Code
├── context/
│   ├── about-me.md           # who you are, what you are working on
│   ├── working-preferences.md # how you want the agent to behave
│   ├── my-context.md         # tools, team, priorities, links
│   └── voice-and-tone.md     # optional — if you write for an audience
└── vault/
    └── daily/
        └── today.md          # optional but useful — today's priorities
```

**Optional later:** `vault/projects/` for recurring work, connector notes, scripts, or a visual daily board. **Advanced example:** [descript-chief-of-staff](https://github.com/a-makelky/descript-chief-of-staff).

---

## Step 1: Create the folder

1. Create a folder on your machine, for example:
   - `~/Documents/my-chief-of-staff`
   - or `~/Code/my-chief-of-staff`
2. Inside it, create `context/` and (optionally) `vault/daily/`.

Do not put this in iCloud if you plan to use git — use a normal local folder or GitHub.

---

## Step 2: Pick your agent tool

| Tool | Open the folder | Where instructions live |
| --- | --- | --- |
| **Cursor** | File → Open Folder | `AGENTS.md` + `.cursor/rules/` (optional) |
| **Codex** | Open folder in Codex | `AGENTS.md` |
| **Claude Code** | `claude` in that directory | `CLAUDE.md` + `context/` |
| **Claude Cowork** | Point Cowork at the folder | `context/global-instructions.md` → Cowork Settings → Global Instructions |

All paths use the **same context files**. Only the entry-point file name changes.

---

## Step 3: Run the setup interview

Copy the prompt below into a **new conversation** in Claude, ChatGPT, Cursor, or Codex. Answer the questions. At the end, save the generated files into your folder.

Takes about 10–15 minutes. Saves hours of generic AI output later.

### Setup prompt (copy everything inside the block)

```
You are helping me set up a personal "chief of staff" workspace for an AI coding agent (Cursor, Claude Code, Codex, or Claude Cowork). The quality of my outputs depends on the context files in my workspace — your job is to interview me and generate those files.

Rules:
- Ask one section at a time
- Wait for my answers before the next section
- Generate all files at the end from my actual answers — no generic filler
- Write in plain language a non-technical colleague can maintain

---

SECTION 1: Workspace type

Will you use this primarily for work, personal life, or both?

---

SECTION 2A: Work context (skip if personal only)

Ask together:
1. Job title and what you actually do day to day
2. Current priorities this quarter — what does success look like?
3. Who you serve or work with (customers, teammates, audience)
4. Tools and platforms you use regularly (Notion, Slack, Google Calendar, email, etc.)
5. Where your work output lives (docs, tickets, calendar, Slack channels)
6. Biggest time sink you want help with

---

SECTION 2B: Personal context (skip if work only)

Ask together:
1. What you want this workspace to help you accomplish
2. Main interests, hobbies, or ongoing projects
3. Tools you use to manage personal life
4. What would make this feel useful, not like extra maintenance

---

SECTION 3: Working style

Ask together:
1. Should the agent execute after one answer, or show options first?
2. Biggest frustration with AI tools — what feels generic or wrong?
3. Tone preferences (direct, casual, formal, brief)
4. Things you never want in outputs
5. Do you edit AI writing before using it?

---

SECTION 4: Voice (work or both only)

Ask together:
1. If you create content — describe your voice
2. Paste 1–3 examples of your best recent work (optional but valuable)
3. Phrases that signal an output missed the mark
4. Main platforms or formats (email, Slack, LinkedIn, internal docs, etc.)

---

SECTION 5: Confirm

Summarize back: workspace type, role, priorities, tools, working style, voice (if any). Ask: "Does this capture everything? Anything to add?"

Wait for confirmation before generating files.

---

FILE GENERATION

Generate these files. Each must start with a version header (Version, Created, Last Updated, Changelog).

1. context/about-me.md — role, priorities, audience, how you think about AI help, where work lives
2. context/working-preferences.md — how to approach tasks, quality bar, never-do list, platform quirks
3. context/voice-and-tone.md — work/both only; tone, samples, anti-patterns
4. context/my-context.md — tools, links, team, domain details (work/personal/both sections as needed)
5. context/global-instructions.md — short block to paste into Cowork Global Instructions OR the core behavior rules for any agent
6. AGENTS.md — main agent instructions: read context/ before tasks, daily rhythm, what requires human approval, notification policy (interrupt vs handle quietly)
7. README.md — what the folder is, how to open it in the user's tool, session startup (read context + today.md if present)
8. vault/daily/today.md — starter daily note with today's date, schedule section, top 3 priorities, running task list (empty template)

Human approval rule (include in AGENTS.md and global-instructions.md):
- Agent may read and draft freely
- Agent must ask before anything public, customer-facing, spend-related, or irreversible

After generating, tell me:
1. Anything I still need to fill in manually
2. Exact folder structure
3. How to open this in Cursor, Codex, Claude Code, or Cowork
```

---

## Step 4: Wire your agent to the folder

### Cursor or Codex

1. Open the folder as your workspace.
2. Start a new agent chat.
3. First message: *"Read AGENTS.md and everything in context/, then help me set up connectors for [your tools]."*

### Claude Code

1. `cd ~/Documents/my-chief-of-staff` (or your path)
2. Run `claude`
3. It should pick up `CLAUDE.md` — if you only have `AGENTS.md`, rename or symlink per Claude Code docs.

### Claude Cowork

1. Save files to your Cowork workspace folder.
2. Paste `context/global-instructions.md` into **Cowork → Settings → Global Instructions**.
3. Cowork reads `context/` before tasks.

---

## Step 5: Connect your tools (when you are ready)

You do not need every connector on day one. Add them as they solve real problems.

| Surface | What it unlocks | Typical setup |
| --- | --- | --- |
| Google Calendar | Schedule-aware briefings | MCP or agent-native connector |
| Gmail | Inbox triage | MCP or agent-native connector |
| Notion | Docs, tasks, databases | Notion MCP |
| Slack | Channel search, intake | Slack MCP |
| Linear / Jira | Assigned work | MCP plugin |

**Safety default:** let the agent **read** and **draft**. You keep approval for anything external, expensive, or irreversible.

Aaron's connector status pattern (optional): a simple `connectors.md` note listing what is connected and what is not.

---

## Step 6: Daily habit (5 minutes)

Open `vault/daily/today.md` each morning. Keep:

- Today's schedule
- Top 3 priorities
- Running task list
- What you are waiting on

Ask your agent: *"Read today.md and context/, give me a morning brief, and tell me what is blocked."*

That is the whole operating loop.

---

## Grow when it helps

| When | Add |
| --- | --- |
| Priorities shift | Update `context/about-me.md` (quarterly minimum) |
| New tool in your stack | Add to `my-context.md` + connect MCP |
| Recurring workflow | A short note in `vault/projects/` |
| You want a visual board | A simple HTML board or FigJam — not required to start |

---

## References

- **This repo (start here):** [GET-STARTED.md](https://github.com/a-makelky/claude-cowork-setup/blob/main/GET-STARTED.md)
- **Cowork context files only:** [SETUP.md](./SETUP.md)
- **Aaron's Descript example (advanced):** https://github.com/a-makelky/descript-chief-of-staff
- **Brown Bag FigJam (interactive intro):** https://www.figma.com/board/R262Wa0GVTGB0YDW95ppmD/2026.5.27-Brownbag--Tools-for-your-agents?node-id=19-991

---

## Version history

- **1.0 (2026-05-26):** Published as GET-STARTED.md in claude-cowork-setup; universal guide for Cursor, Codex, Claude Code, and Cowork; added AGENTS.md, vault/daily pattern, connector and safety guidance.
