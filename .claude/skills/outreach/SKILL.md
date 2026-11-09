---
name: outreach
description: Finds the right person and drafts short, peer-to-peer messages for the job search - alumni notes, LinkedIn invitations and messages on acceptance, messages to engineers and hiring managers, thank-yous, follow-ups and nudges. Use whenever the user needs to write to someone, a contact accepts or replies, a follow-up is due, or a company has an offer and nobody has been contacted there yet.
---

# Outreach

Read `playbook.md` §1–3, `state/profile.md`, and the contact's history in `state/` and `log/` before drafting.

## Before writing

- Check `state/applications.md` and `state/archive.md`: no note at a company that already rejected the user; no second message to someone who didn't answer a connection note.
- Check the **register** the contact used (formal or informal) and the language. Match it.
- Find something real to say: their product, their role, a talk, the offer, a shared school or city.

## Drafting rules

- Two or three lines. One block per person, full name above it, ready to copy, no placeholders.
- Engineers and hiring managers: what caught my eye + one real question (about their team, their stack, how they hire juniors). Recruiter style only for HR.
- Connection notes under 200 characters: count with `wc -m` and show the count.
- A request for a call asks for 15 minutes and offers two slots.
- True facts only: graduation date, legal-status sentence and durations come from `state/profile.md`.
- Thank-you after a call: one or two casual lines, the same day or the next.
- Nudge: one light message after 7–10 days, then one last on another channel a week later, then close as ghosted.

## Finding people

- Alumni: the school's LinkedIn page → People → filter by city and keyword; confirm the school on the profile.
- Prefer small and mid-size product companies. Spread over the target cities.
- Search slowly (pauses between searches) to avoid being rate-limited.
- With the browser connector: open each profile, pre-fill the invitation or message, and leave the tab for the user to send. Never send.

## After

Log each message sent in `state/followups.md` (who, what, when, next step) once the user confirms it went out. When someone accepts or answers: a message the same day, and `prep-call` if a call gets booked.
