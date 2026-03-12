# Contributing to Awesome Agent Skills

Thanks for helping grow this directory. Here's how to add a skill.

## What belongs here

✅ **In scope:**
- Open source AI agent skills for knowledge work (email, calendar, docs, research, meetings, content ops)
- Memory and infrastructure tools for knowledge work agents
- Curated collections of agent skills
- Benchmarks for knowledge work agent tasks
- Harness-agnostic tools and APIs that power knowledge work agents

❌ **Out of scope:**
- Pure software development tools (code review, CI/CD, linters)
- Abandoned or unmaintained repos (last commit > 12 months ago)
- Closed-source / proprietary only tools
- Framework boilerplate without actual skill content

## How to add a skill

### 1. Add to README.md

Find the right section and add a line in this format:

```markdown
- **[Skill Name](https://github.com/org/repo)** ⭐ stars (optional) — One-line description of what it does and why it's useful for knowledge work. `[harness]` `[harness]`
```

### 2. Add to docs/data/skills.js

Add an object to the `SKILLS` array:

```js
{
  id: "unique-id",                    // lowercase, hyphens
  name: "Human-readable Name",
  category: "knowledge-work",         // see categories below
  tags: ["tag1", "tag2"],             // lowercase, descriptive
  description: "2-3 sentence description...",
  repo: "https://github.com/org/repo",
  stars: "10k+",                      // or null
  harnesses: ["claude-code", "any"],  // see harnesses below
  highlight: false,                   // true for exceptional/notable skills
  actrun: true,                       // true if the skill can run on ActRun.ai
  badge: null                         // optional: "🔥 Trending" etc.
}
```

**Categories:** `knowledge-work` · `documents` · `research` · `infrastructure` · `orchestration` · `curated` · `learning`

**Harnesses:** `claude-code` · `gemini-cli` · `cursor` · `codex` · `any` · `standalone` · `api`

### 3. Open a PR

- Title: `Add: [Skill Name]`
- Include a brief note on why this skill belongs here

## Questions?

Open an issue and tag it `question`.
