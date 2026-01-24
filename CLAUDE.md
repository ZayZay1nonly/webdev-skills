# Claude Code Skills

This repository contains skills for Claude Code and other AI coding agents.

## Installation

```bash
# Install all skills
npx add-skill augmnt/webdev-skills

# Install specific skills
npx add-skill augmnt/webdev-skills --skill using-cli-tools
```

Or manually:

```bash
cp -r skills/* ~/.claude/skills/
```

## Available Skills

### using-cli-tools
Enforces CLI tool usage over web dashboards. Triggers on GitHub, Supabase, Vercel, Netlify, Cloudflare, Prisma, Stripe, or Docker operations.

### organizing-project-files
Project structure conventions for React/Next.js. Triggers on "where should this go?" or file organization questions.

### writing-commits
Conventional Commits format. Triggers on commit messages, PR descriptions, or changelog generation.

### reviewing-code
Structured code review with prioritized feedback. Uses `allowed-tools: Read, Grep, Glob` for read-only access.

### writing-tests
Testing strategy guidance. Triggers on test writing, coverage questions, or mocking setup.

## Skill Structure

Each skill follows the [Agent Skills specification](https://agentskills.io/):

```
skill-name/
├── SKILL.md           # Required: Instructions and metadata
└── REFERENCE.md       # Optional: Detailed content loaded on-demand
```

## Contributing

1. Create a new folder under `skills/`
2. Add a `SKILL.md` with proper frontmatter
3. Keep core instructions under 500 lines
4. Use reference files for detailed content
