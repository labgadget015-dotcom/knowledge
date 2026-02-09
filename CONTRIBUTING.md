# Contributing Guide

## Philosophy

This repository is a **command center**, not a code repository. It organizes planning, configuration, and logs for three main systems:

1. **Security Stack** - Home lab, VPN, monitoring
2. **AI Agent** - Autonomous revenue agents
3. **Trading System** - Algorithmic trading strategies

## Repository Structure

```
knowledge/
├── seeds/              # Project templates (paste into work sessions)
├── projects/           # Active project logs (archive work here)
├── PROMPTS.md          # Copy-paste prompts for different stages
├── WORKFLOW.md         # Daily/weekly/monthly rituals
└── README.md           # Overview and quick start
```

## How to Contribute

### Adding a New Project

1. Create a seed file in `seeds/new-project.md`:
   ```markdown
   # New Project - Seed
   
   ## Project
   Brief description
   
   ## Goal
   What you're trying to achieve
   
   ## Stack
   - Tool 1
   - Tool 2
   
   ## Constraints
   - Budget, time, or technical limits
   
   ## Current state
   - [ ] Checklist item 1
   - [ ] Checklist item 2
   
   ## Open questions
   - Question 1?
   
   ## Next actions
   1. Action 1
   2. Action 2
   ```

2. Create project directory:
   ```bash
   mkdir -p projects/new-project
   touch projects/new-project/Log.md
   ```

3. Update main README.md to reference the new project

### Updating Logs

After each work session:

1. Run the Archive Summarization prompt from `PROMPTS.md`
2. Copy output to `projects/[project]/Log.md`
3. Update seed checklist items
4. Commit with meaningful message:
   ```bash
   git add projects/[project]/Log.md seeds/[project].md
   git commit -m "[Project] Session YYYY-MM-DD - Brief summary"
   git push
   ```

### Modifying Seeds

Seeds should evolve as projects progress:

- ✅ Update checklists as items complete
- ✅ Add new open questions
- ✅ Refine next actions
- ✅ Update stack as tools change
- ❌ Don't delete historical context (use strikethrough instead)

Example:
```markdown
## Current state
- [x] ~~Core agent prompt~~ (completed 2026-02-09)
- [ ] API surface (FastAPI)
```

### Adding Prompts

If you create a useful prompt pattern, add it to `PROMPTS.md`:

```markdown
## [Prompt Name]

**When to use**: [Context]

**Prompt**:
[Full prompt text here]

**Expected output**: [What you'll get]
```

## Commit Message Convention

Use this format:
```
[Project] - [Subsystem] - Action

Examples:
[Security] - Network - Add VLAN topology
[Trading] - Backtesting - Log BTCUSDT results
[AI Agent] - API - Define FastAPI endpoints
[Meta] - Update WORKFLOW.md checklist
```

## File Naming

- Seeds: `seeds/[project-name].md`
- Logs: `projects/[project-name]/Log.md`
- Artifacts: `projects/[project-name]/[artifact-name].[ext]`

## What NOT to Commit

See `SECURITY.md` for full details:
- API keys or credentials
- Trading account details
- Personal network configuration with secrets
- Live production data

## Code Quality

This is primarily a **documentation** repo, but if code is added:

- Include comments explaining context
- Keep snippets minimal and focused
- Reference external repos for full implementations
- Include a README in any code directory

## Issue Tracking

Use GitHub Issues for:
- 🐛 **Bugs**: System failures or unexpected behavior
- ✨ **Features**: New capabilities or improvements
- 📋 **Tasks**: Specific action items

Use issue templates provided in `.github/ISSUE_TEMPLATE/`

## Pull Requests

1. Create a branch: `git checkout -b feature/your-feature-name`
2. Make changes
3. Commit with clear messages
4. Push: `git push origin feature/your-feature-name`
5. Open PR with description:
   - What changed
   - Why it changed
   - How to test/verify

## Questions?

Open an issue with the label `question` or start a discussion.
