# Reusable Prompts

Copy-paste these prompts into your threads to maintain consistency and maximize clarity.

## 1. Archive Summarization Prompt

**Use at milestones or end of work session.** Copy output directly into project Log.md.

```
Summarize this thread into:

(1) **Goals** – What we were trying to achieve
(2) **Key decisions** – Architecture, trade-offs, tool choices
(3) **Artifacts** – Concrete outputs (files, paths, code modules)
(4) **Open questions** – Unresolved or blocked items
(5) **Next actions** – Prioritized steps for next session

Format as Markdown so I can paste directly into Log.md.
```

## 2. Architecture Critique Prompt

**Use after proposing a design.** Catches flaws early.

```
Critique this [architecture / design / approach] like a senior [engineer / architect / trader reviewing a peer]:
- What's the biggest risk?
- What's the simplest thing I'm over-complicating?
- What's missing that will bite me in 2 months?
- Give one hard constraint I should enforce.
```

## 3. Two-Option Comparison Prompt

**Use when torn between approaches.** Forces tradeoff clarity.

```
Compare Option A vs Option B:

**Option A**: [describe approach]
**Option B**: [describe approach]

For each, list:
- Implementation time (hours)
- Runtime cost / resource footprint
- Maintainability (1–5)
- Risk (what breaks?)
- Extensibility (add features later?)

Then: which do you recommend and why?
```

## 4. Code Review Self-Critique Prompt

**Before submitting code/config.** Saves PR rounds.

```
Review this code/config as a code reviewer:
- Clarity: can someone else understand it in 5 min?
- Edge cases: what breaks with edge inputs?
- Performance: any obvious bottlenecks?
- One simplification I should make
```

## 5. Backtest / Evaluation Post-Mortem Prompt

**After testing a strategy or feature.** Captures learning.

```
Post-mortem on [strategy / system] performance:

- What did we assume that was wrong?
- Which metric surprised us (better or worse)?
- What regime / edge case did we miss?
- One thing to change before v1 is live
```

## 6. Prompt Refinement Prompt

**When a previous answer was mediocre.** Iterates toward clarity.

```
Redo [previous request]. Focus on:
- [specific detail you want clearer]
- [constraint you forgot to mention]
- [example or format that would help]
```

## 7. Documentation Template Prompt

**After building something.** Keeps docs current.

```
Write a 200-word deployment / usage guide for [artifact]:

Include:
1. What it does in 1 sentence
2. Prerequisites (env vars, dependencies)
3. How to run it (exact command or steps)
4. What success looks like
5. One gotcha
```

## 8. Scope Lock Prompt

**At project start or when scope creeps.** Enforces focus.

```
Lock v1 scope for [project]:

**IN scope** (must have):
- [feature]
- [feature]

**OUT of scope** (do not touch):
- [feature]
- [feature]

**FUTURE** (post-v1):
- [feature]

Why these boundaries?
```

## Quick Copy-Paste Template

For any thread, start with your seed, then end each work block with:

```
---

### End-of-block summary

**Today's work**: [1-2 lines]
**Code/artifacts added**: [list files]
**Blockers**: [if any]
**Next block focus**: [1-2 lines]
```

Then run the Archive Summarization Prompt for the full Log.md update.
