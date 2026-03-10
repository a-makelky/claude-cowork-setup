# claude-cowork-setup

A guided setup prompt that generates personalized Claude Cowork context files for your workspace.

Paste the prompt from `SETUP.md` into a new Claude conversation at claude.ai, answer the questions, and Claude produces ready-to-use context files in about 10 minutes.

## What you get

```
claude-cowork-workspace/
└── context/
    ├── about-me.md
    ├── working-preferences.md
    ├── voice-and-tone.md        # work/both only
    ├── my-context.md
    └── global-instructions.md
```

## How to use

1. Open `SETUP.md`
2. Copy the prompt inside the code block
3. Paste into a new Claude conversation at claude.ai
4. Answer the interview questions
5. Save the generated files to a local `claude-cowork-workspace/context/` folder
6. Paste `global-instructions.md` into Cowork → Settings → Global Instructions

## Version control

Each generated file includes a version header and changelog. Bump the version and update the changelog any time you edit a file.

## Contributing

If you improve the interview flow or discover file structures that work well, open a PR.
