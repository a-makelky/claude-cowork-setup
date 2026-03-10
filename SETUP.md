# Claude Cowork Workspace Setup
**Version:** 1.0
**Created:** 2026-03-10
**Last Updated:** 2026-03-10
**Changelog:**
- 1.0 (2026-03-10): Initial version

---

## What this is

A guided setup prompt that generates personalized Claude Cowork context files for your workspace. Paste the prompt below into Claude (claude.ai), answer the questions, and Claude will produce ready-to-use files you can drop straight into your Cowork folder.

Takes about 10 minutes. Saves you hours of generic output later.

---

## How to use

1. Copy everything inside the code block below
2. Paste it into a new Claude conversation at claude.ai
3. Answer the questions as they come
4. Claude generates your context files at the end
5. Create a local folder called `claude-cowork-workspace/context/` and save the files there
6. Paste `global-instructions.md` into Cowork → Settings → Global Instructions

---

## The Setup Prompt

```
You are helping me set up a Claude Cowork workspace. Cowork is Anthropic's desktop tool for autonomous task execution with local file access. The quality of my outputs depends entirely on the context files I give it — your job is to interview me and then generate those files.

Here's how this works:
- Ask me questions one section at a time
- Wait for my answers before moving to the next section
- Generate all context files at the end based on what I told you
- No generic templates. Everything must reflect my actual answers.

---

SECTION 1: Workspace type

First question. Wait for my answer before continuing.

Will you be using this workspace primarily for work, personal use, or both?

- Work — you'll ask about my role, team, tools, and professional context
- Personal — you'll ask about my goals, interests, and how I spend my time
- Both — you'll build a combined workspace covering both

---

SECTION 2A: Work context (skip if Personal only)

Ask these together:

1. What is your job title and what does your role actually involve day to day? Don't just want the title — what do you spend most of your time doing?
2. What are your current priorities this quarter? What does success look like?
3. Who are you trying to reach or serve — customers, colleagues, an audience? Describe them specifically.
4. What tools and platforms do you use regularly for work? (Examples: Notion, Slack, Linear, Google Workspace, industry-specific software)
5. Where does your work output live? Where do things get documented, published, or delivered?
6. What's the biggest time sink in your work that you'd most want help with?

---

SECTION 2B: Personal context (skip if Work only)

Ask these together:

1. What are you trying to accomplish with a personal Cowork workspace? What kinds of tasks do you want help with?
2. What are your main interests, hobbies, or ongoing projects?
3. What tools do you use to manage your personal life? (Calendar apps, note-taking, task managers, etc.)
4. What would make this feel genuinely useful rather than just another thing to maintain?

---

SECTION 3: Working style

Ask these together:

1. How do you want Claude to work with you — give one answer and execute, or show options and explain tradeoffs?
2. What's your biggest frustration with AI writing tools? What makes outputs feel generic or off?
3. Do you have strong preferences about tone? Formal, casual, direct, detailed?
4. Are there things you never want in outputs — phrases, formats, approaches?
5. How do you feel about AI-sounding writing? Do you review and edit outputs before using them?

---

SECTION 4: Voice and quality bar (Work or Both only — skip for Personal)

Ask these together:

1. If you create content or write for an audience — what's your voice? How would you describe the tone you're going for?
2. Paste 1–3 examples of your best recent work. Posts, emails, documents, anything. These become voice reference samples.
3. What phrases or patterns would immediately signal to you that an output missed the mark?
4. What platform or format do you create for most? (LinkedIn, X/Twitter, email, internal docs, reports, etc.)

---

SECTION 5: Confirmation

Before generating files, summarize back to me:
- Workspace type (work / personal / both)
- Role and context (one paragraph)
- Current priorities
- Audience or stakeholders
- Key tools and platforms
- Working style preferences
- Voice and quality standards (if applicable)

Then ask: "Does this capture everything accurately? Anything to add or correct?"

Wait for confirmation before generating files.

---

FILE GENERATION

Once confirmed, generate these files. Every file must:
- Start with a version header block (Version, Created date, Last Updated date, Changelog)
- Reflect my specific answers — no generic filler
- Be written in plain, direct language
- Be immediately usable without editing (flag anything I still need to fill in)

---

File 1: context/about-me.md

Cover:
- My name (if I gave it) and role or context
- What I actually do and what I'm working on
- Current priorities
- Who I'm trying to reach or serve
- How I think about AI tools (collaborator, assistant, delegator, etc.)
- Working style preferences
- Where my work lives (tools, platforms, documentation)

---

File 2: context/working-preferences.md

Cover:
- How I want Claude to approach tasks (show plan first, ask questions, options vs. single answer)
- Output quality standards (what "ready" means to me)
- What I never want (phrases, formats, approaches)
- Research standards if applicable (citations, recency, sourcing)
- Any recurring workflows or platforms that need special handling

---

File 3: context/voice-and-tone.md (Work and Both only — skip for Personal)

Cover:
- Core tone and personality
- Phrases I use
- Phrases I never use
- Platform-specific rules
- AI writing quality standard — if I mentioned reviewing outputs, make this explicit and specific
- My voice samples, labeled clearly as reference examples

---

File 4: context/my-context.md

For Work: role context, team structure, audience, tools, platforms, domain-specific details I shared.
For Personal: goals, interests, ongoing projects, tools, what I want this workspace to actually help me do.
For Both: two clearly labeled sections — Work and Personal.

---

File 5: context/global-instructions.md

Write the Global Instructions block I'll paste into Cowork → Settings → Global Instructions. Tell Cowork to:
- Read all files in the context folder before starting any task
- Ask clarifying questions if a request is ambiguous
- Show a brief plan before executing
- Apply my voice and quality standards to all outputs
- Reference specific platforms or tools I mentioned
- Never publish, send, or delete anything without my approval

Make this specific to what I told you — not a generic template.

---

After generating all files, tell me:
1. Which files still need me to add anything (examples, placeholders I need to fill)
2. The exact folder structure to create locally
3. How to point Cowork at these files using the Global Instructions block
```

---

## After setup

- Save generated files to `claude-cowork-workspace/context/`
- Paste `global-instructions.md` into Cowork → Settings → Global Instructions
- Add 2–3 examples of your best work to `voice-and-tone.md` if applicable
- Update `about-me.md` whenever priorities shift — quarterly minimum
- Version bump any file you edit: update Last Updated and add a changelog line

---

## Folder structure reference

```
claude-cowork-workspace/
└── context/
    ├── about-me.md
    ├── working-preferences.md
    ├── voice-and-tone.md        # work/both only
    ├── my-context.md
    └── global-instructions.md
```
