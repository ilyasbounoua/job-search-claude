---
name: close-day
description: Closes the job-search day. Updates state/current.md, follow-ups, pipeline, applications and metrics, appends the day's log entry, archives closed rows, and gives tomorrow's 5 targets (and calendar blocks if connected). Use when the user types /close-day or says "close the day", "end of day", "let's wrap up", "I'm done for today".
---

# Close the day

1. Run `date`. Read `CLAUDE.md` and every `state/` file.
2. If anything happened today that is not written yet (a call, a reply, a decision), ask the user in one question before writing.
3. Update, in this order:
   - `state/pipeline.md`: stage changes, last action, next action with a due date.
   - `state/followups.md`: add new ones with due dates; update the "latest status" column (latest first, short).
   - `state/applications.md`: any application, rejection or acknowledgement of the day. "Applied" only with evidence.
   - `state/archive.md`: move every closed follow-up and pipeline row **word for word**, then remove it from the live file.
   - `state/metrics.md`: add today's counts to the current sprint row (applications, outreach, replies, conversations, screens, tech rounds, finals, offers).
   - `state/current.md`: rewrite, 10 lines max: live processes, what's waiting on whom, decisions in force.
4. Append to `log/YYYY-MM.md` (create the file for a new month):

```
### YYYY-MM-DD (Day N, weekday)
- Done: ...
- Counts: apps X | outreach X | replies X | calls X | prep: ...
- Learned / blockers: ...
- Tomorrow's 5 targets: ...
```

5. Give **tomorrow's 5 targets**: concrete, each with its block or time.
6. If the calendar is connected and the user wants it: create tomorrow's blocks (one call at a time).
7. If today is the last day of the sprint: say so and run `sprint-review`.
8. If the user corrected Claude or stated a preference today, write it in `CLAUDE.md` §5 with the date.
9. If a fact about the user changed (an experience date, a skill they can't defend), fix `state/profile.md`.

The day after a lost interview: plan it light.
