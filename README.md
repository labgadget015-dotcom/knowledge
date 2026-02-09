# Knowledge Base

Command center for security, AI agents, and trading systems.

## Structure

- `seeds/` - Project seed prompts (goal, stack, constraints, current state)
- `projects/` - Active projects with Log.md files
  - `security-stack/`
  - `ai-agent/`
  - `trading-system/`

## Workflow

1. Start thread with seed from `seeds/`
2. Work in focused chunks, one artifact per prompt
3. Summarize milestones: "Summarize this thread into: (1) goals, (2) key decisions, (3) artifacts with filenames/paths, (4) open questions, (5) next actions."
4. Update Log.md in project folder
5. Update seed if context shifts

## Thread Naming Convention

`[Project] – [Subsystem] – [YYYY-MM-DD] – [Action]`

Example: `[Security] – [Network] – 2026-02-09 – VPN topology design`

## Getting Started

- **Read first**: [README.md](README.md) (you're here)
- **Setup**: Copy relevant seed from `seeds/` to top of your Perplexity thread
- **During work**: Use prompts from [PROMPTS.md](PROMPTS.md)
- **End of session**: Run Archive Summarization prompt, paste into project Log.md
- **Weekly ritual**: Follow [WORKFLOW.md](WORKFLOW.md) checklist

## Files Guide

| File | Purpose |
|------|----------|
| [README.md](README.md) | You are here – structure & overview |
| [PROMPTS.md](PROMPTS.md) | 8 copy-paste prompts for different stages (critique, comparison, archiving) |
| [WORKFLOW.md](WORKFLOW.md) | Daily/weekly/monthly rituals + concrete examples |
| `seeds/` | Project templates – paste at top of thread |
| `projects/` | Active project Logs – archive summaries here |

## Quick Start: Pick One Project

**Pick ONE** of security, AI agents, or trading.

1. Open `seeds/[project].md` → copy entire content
2. Start new Perplexity thread
3. Paste seed + add "## Session Notes" + your work
4. At end: Run Archive Summarization prompt from PROMPTS.md
5. Copy output → paste into `projects/[project]/Log.md`
6. Update `seeds/[project].md` checklist
7. Commit to GitHub

**Next week**: Repeat with updated seed (context will be there).

