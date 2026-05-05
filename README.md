# Claude Code Skills — by Marcel Grau

5 skills I use every week to create content faster with AI. Each one teaches Claude Code a specific capability — hook writing, cinematic AI prompts, reel scripts, captions, and motion graphics.

Free. No setup. Installed in 30 seconds.

---

## What is a Claude Code skill?

Claude Code is Anthropic's AI assistant that runs in your terminal. A skill is a small `.md` file you add to it that gives Claude a new, specific capability. Once installed, you just type `/skill-name` and Claude executes it — no explaining, no prompting, no setup.

Think of it like installing an app, but for your AI.

---

## Requirements

- [Claude Code](https://claude.ai/download) installed (free plan works)
- A terminal (Mac/Linux: Terminal — Windows: Git Bash or WSL)

---

## Install all 5 at once

Open your terminal and paste this:

```bash
curl -o ~/.claude/skills/viral-hook-creator.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/01-viral-hook-creator.md && \
curl -o ~/.claude/skills/higgsfield-cinematic.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/02-higgsfield-cinematic.md && \
curl -o ~/.claude/skills/reels-scripting.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/03-reels-scripting.md && \
curl -o ~/.claude/skills/copywriting.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/04-copywriting.md && \
curl -o ~/.claude/skills/remotion-liquid-glass.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/05-remotion-liquid-glass.md
```

Then restart Claude Code. All 5 skills will be ready to use.

> **Windows users:** run the commands in Git Bash or WSL. Or manually copy each `.md` file to `C:\Users\YourName\.claude\skills\`

---

## The 5 skills

### 01 — Viral Hook Creator
**Command:** `/viral-hook-creator`

Give it your video topic and it generates 6 hook variations built around proven formats: number-led, contrarian, personal transformation, authority steal, admission, and future shock. Every hook is under 40 characters per line — written to stop the scroll.

```bash
curl -o ~/.claude/skills/viral-hook-creator.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/01-viral-hook-creator.md
```

---

### 02 — Cinematic AI Prompting
**Command:** `/higgsfield-cinematic`

Turn a one-line idea into a production-grade video prompt for Seedance on Higgsfield. Uses 15+ cinematic camera techniques, professional lighting setups, and a 2-second hook framework — so your AI videos look like actual films, not generic generations.

```bash
curl -o ~/.claude/skills/higgsfield-cinematic.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/02-higgsfield-cinematic.md
```

---

### 03 — Reels Scripting
**Command:** `/reels-scripting`

Give it your topic and it writes a complete 60-second reel script — structured with hook, problem, revelation, solution, and CTA. Each section comes with timestamps and is built around retention psychology.

```bash
curl -o ~/.claude/skills/reels-scripting.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/03-reels-scripting.md
```

---

### 04 — Copywriting Generator
**Command:** `/copywriting`

Instagram captions, launch posts, hooks, CTAs and ad copy — written in a high-converting structure. Give it your product or topic and it returns copy that stops the scroll and drives action.

```bash
curl -o ~/.claude/skills/copywriting.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/04-copywriting.md
```

---

### 05 — Remotion Liquid Glass
**Command:** `/remotion-liquid-glass`

Creates Apple-style Liquid Glass motion graphics in Remotion (React to video). Glass cards, Inter bold/light typography, white-to-yellow gradients, glow effects, spring animations. The exact visual style used in the reel — reusable for any motion graphic you want to build.

```bash
curl -o ~/.claude/skills/remotion-liquid-glass.md https://raw.githubusercontent.com/marcelgrauu/claude-skills/main/05-remotion-liquid-glass.md
```

---

## How to use a skill

Once installed, open Claude Code and type the skill command followed by your input:

```
/viral-hook-creator my topic is growing on Instagram with AI
```

```
/reels-scripting I want to talk about how AI saves me 10 hours a week
```

Claude will execute the skill immediately with no extra setup.

---

Made by [Marcel Grau](https://instagram.com/marcelgrauu)
