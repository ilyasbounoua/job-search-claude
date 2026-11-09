---
name: today
description: Opens the job-search day. Checks the date, reads the state files, reads the inbox and calendar since the last close-out, lists what is due and gives the day's plan with concrete targets. Use when the user types /today or asks "what's the plan for today", "what do I do today", "good morning, let's start".
---

# Today

1. Run `date` (day, weekday, time). If `state/profile.md` says `SETUP: NOT DONE`, stop and suggest `/setup`.
2. Read `CLAUDE.md`, `state/current.md`, `state/followups.md`, `state/pipeline.md`, and the last entry of the latest `log/YYYY-MM.md` (it holds yesterday's 5 targets).
3. **Inbox** (if an email connector is available), one call at a time:
   - Read everything since the **morning of the previous working day** (not since the close-out time), including the Junk / Spam folder.
   - For each email about the search: compare with `state/` (a rejection, an invitation, an answer from a contact) and say what changed.
   - Flag useless recurring mail (newsletters, job alerts that never fit) and propose unsubscribing.
   - Without a connector, ask the user if anything came in.
4. **Calendar** (if connected): today's and tomorrow's events. A call without a preparation sheet → write it now (`prep-call`).
5. **LinkedIn** (if the browser is connected and the user wants it): new messages, accepted invitations. Each acceptance gets a short message today (`outreach`).
6. Report in this order, short:
   - What changed since yesterday (one line each).
   - Due today or overdue (from `state/followups.md`).
   - Today's targets: yesterday's 5 targets, updated with what changed.
   - The plan in the user's time blocks (`playbook.md` §7 as adapted in `CLAUDE.md` §5).
7. Update `state/` with what the inbox changed, then start the first block with the user.

Keep the report under 25 lines. No drafts for messages due on a later day.
