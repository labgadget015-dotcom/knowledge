# Workflow Ritual

A concrete daily/weekly routine to keep your knowledge base current and leverage it for decision-making.

## Daily Ritual (5 min)

**When**: End of each focused work block (every 2-4 hours)

**Steps**:

1. Open relevant `projects/[project]/Log.md`
2. Add quick entry:
   ```
   ### [HH:MM] – [Action description]
   - Progress: [1-2 lines]
   - Artifacts added: `path/file.ext`
   - Next: [1 line]
   ```
3. Commit to GitHub (if pausing work for >1 hour)

**Why**: Keeps logs fresh so weekly summaries are easy. Prevents context loss between sessions.

---

## Weekly Ritual (15–30 min)

**When**: Friday EOD or Sunday evening (choose one)

**Steps**:

### 1. Review All Projects (5 min)

For each of `security-stack`, `ai-agent`, `trading-system`:
- Open `projects/[project]/Log.md`
- Scan last 7 days of entries
- Check if seed in `seeds/[project].md` still accurate

### 2. Run Archive Summarization (10 min per active thread)

If you had an active thread this week:

1. Go to the thread
2. Copy-paste the **Archive Summarization Prompt** from `PROMPTS.md`
3. Copy the output
4. Create new dated section in `projects/[project]/Log.md`:
   ```
   ## YYYY-MM-DD – [Milestone name]
   
   [Paste summary output here]
   ```
5. Commit to GitHub

### 3. Update Seeds (5 min)

For each project you worked on:
- Open `seeds/[project].md`
- Update "Current state" checklist (mark items done)
- Update "Next actions" based on latest Log.md
- If major context shift, update "Stack" or "Goal"
- Commit

### 4. Identify Next Week's Focus (5 min)

Add a "Next week" section at the very top of each active project's Log.md:

```
## Next week focus

- [Action 1] (why: [reason])
- [Action 2] (why: [reason])
```

This forces you to pick ONE subsystem per project to focus on.

---

## Monthly Review (30 min)

**When**: Last Friday of the month

**Steps**:

### 1. Read All Logs

Read top-to-bottom through the last month of each project's Log.md.

### 2. Identify Patterns

Answer for each project:
- What took longer than expected? Why?
- Which decisions aged well? Which didn't?
- What should become a permanent constraint or best practice?

### 3. Update README.md

If you discovered a new best practice or pattern, add it to README.md under a "Lessons Learned" section.

### 4. Archive Old Logs (optional)

If a Log.md gets >500 lines, create `projects/[project]/Log-2026-01.md`, move old entries there, keep last 3 months active.

---

## Thread Template (use at start of each thread)

Copy this to the top of a new Perplexity thread:

```markdown
# [Project] – [Subsystem] – [YYYY-MM-DD] – [Action]

## Seed

[Copy entire relevant seed from seeds/]

## Session Notes

- Started: [HH:MM]
- Goal: [what we're shipping today]

---

[Work here]

---

## End-of-Session Summary

[Run Archive Summarization prompt from PROMPTS.md]
```

---

## Critical Habits

✅ **Always timestamp entries** – Makes diffs and context-switching easy

✅ **Use the exact Archive Summarization prompt** – Keeps format consistent, easier to paste into logs

✅ **One thread per subsystem per week** – Don't jump between 5 threads; focus beats breadth

✅ **Commit after each summarization** – GitHub commits are your backup and audit trail

✅ **Skim old logs before starting new thread** – 2-min refresh prevents repeating old mistakes

---

## Example Weekly Flow (Security Stack)

**Monday**: Start thread `[Security] – Network – 2026-02-10 – VPN design`
- Paste `seeds/security-stack.md` at top
- Work 4 hours
- End of block: quick note in Log.md
- Commit

**Wednesday**: 4 more hours
- End of block: quick note in Log.md
- Commit

**Friday EOD**: 
- Run Archive Summarization prompt
- Create new section in `projects/security-stack/Log.md`
- Update `seeds/security-stack.md` (mark checklist items, update next actions)
- Commit
- Add "Next week focus" to Log.md

**Next Monday**: Start fresh thread, paste seed (now updated), go.

---

## Metrics to Track (Monthly)

- **Threads started**: Should be 2-3 per project per month
- **Average thread duration**: Should be 4-8 hours
- **Log entries per project**: Should be 8-12 dated summaries per month
- **Seed updates**: Should happen weekly

If threads are getting long (>8 hrs) or stale, you're hoarding context instead of summarizing and closing.
