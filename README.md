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
