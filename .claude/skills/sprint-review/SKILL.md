---
name: sprint-review
description: Reviews the sprint that just ended (its length is set at setup) - counts and conversion per channel, why interviews were won or lost, what to change - and agrees the next sprint's targets. Also runs the mid-point review and the decision gate. Use at the last close-out of a sprint, when the user asks "how is it going", "what should I change", "review the week", or when the decision date in CLAUDE.md is reached.
---

# Sprint review

Read `CLAUDE.md` §1 (sprint length, window, decision date), `state/metrics.md`, `state/pipeline.md`, `state/applications.md`, `state/archive.md`, and the `log/` entries of the sprint.

1. **Numbers:** fill the sprint row in `state/metrics.md` from the log. Update the "By channel" table: sent, replies, conversations, interview processes, offers.
2. **Conversion:** messages → replies → conversations → interviews → offers, per channel. Which channel produced the interviews?
3. **Losses:** for each lost process, the stage and the one-line reason (the company's feedback if any). Look for the repeated gap (speed in live coding, data modelling, motivation, a hard gate…).
4. **Last sprint's targets:** met or not, and why, in one line each.
5. **What changes:** at most three changes. If fewer than 3 replies from 15 targeted contacts: change the message, the CV headline or the channel, not only the volume. Double down on the channel that converts.
6. **Next sprint's targets:** 3 to 5 measurable ones (e.g. "20 invitations, Nantes first", "timed practice 4 days out of 5", "prep sheet for X").
7. Write it all under "Sprint reviews" in `state/metrics.md` and agree the targets with the user before writing them in `state/followups.md`.

## Mid-point and decision gate

- **Mid-point** (half of the window): the same review, plus a check of the pipeline risk (is everything waiting on others?).
- **Decision gate** (the decision date): with no solid offer, propose the staged lowering of the bar from `playbook.md` §6, one stage at a time. The user decides; write the decision and its date in `CLAUDE.md` §1.
