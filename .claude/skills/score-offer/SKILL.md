---
name: score-offer
description: Scores a job offer against the user's profile (0–10, screening risk vs ramp risk), and for offers at or above the passing score adapts a one-page CV, drafts a short motivation in the offer's language, and optionally searches job boards and fills application forms without ever submitting them. Use whenever the user pastes a job offer or a job link, asks "is this a good fit", "should I apply", "adapt my CV", "find me offers", or when an offer comes up in an email or job alert.
---

# Score an offer, adapt, fill

Read `state/profile.md`, `admin/legal-status.md`, `playbook.md` §1 and §4, and `state/applications.md` first.

## 1. Before scoring

- Already in `state/applications.md` (applied, rejected, do not re-apply)? Say so and stop.
- People first: is there a person at this company (alumni, contact, hiring manager) in `state/` or findable? If yes, suggest contacting them **before** applying (`outreach`). Cold application only if nobody was found or the contact was silent for a week.

## 2. Score (0–10)

Read the full body of the offer, not the site's tags. For every gap, decide:

- **Screening risk** (heavy): a hard gate. "X years minimum", "confirmed", "significant experience", "excluding internships", nationality, security clearance, a mandatory language the user doesn't have, a salary below the legal floor.
- **Ramp risk** (light): a technology listed in a stack, or an offer open to beginners ("junior", "first experience", "we train you", a wide range like "0–5 years").

An OR requirement is met in full by one side. An AND requirement with gating words is a real risk. Through a referral, hard gates can become negotiable: re-score with that in mind.

Automatic skips: the user's exclusions in `state/profile.md`, roles the legal status forbids (e.g. clearance or nationality-restricted), salary clearly under the floor.

Report: score, the 2–3 reasons that decided it, the gaps (and how to present them honestly), the salary vs the floor, and the person to contact if one exists. Write the row in `state/applications.md` whatever the score.

Below the passing score: stop, unless the user says go.

## 3. Adapt the CV (passing offers only)

- Start from the reference CV in `state/profile.md` "Sources". Reorder and reframe **true** facts to match what the offer gates on. Never add a claim that isn't in the profile.
- One page (unless the profile says otherwise). In the offer's language.
- LaTeX CV: compile in a folder named after the file (`latexmk -pdf -outdir=<name> <name>.tex`), check the page count, report. Other formats: produce a DOCX or PDF and check it opens.
- One adapted CV can serve several near-identical offers in the same batch.
- Save it as `cv/<Company>/...`.

## 4. Motivation

Short (5–8 lines) unless a full letter is asked. In the offer's language. Name the real matches (the facts that scored it well) and present gaps as adjacent experience plus fast learning, never as done. No em-dashes.

## 5. Search and fill (only when the user asks)

- Use the browser connector. **Never create an account, never type a password, never click the final submit button.** Fill every field, upload the CV, type the motivation, read the fields back (some forms wipe text after an upload: attach the CV first, type after), then leave the tab parked at submit and tell the user.
- File uploads: use the file-upload tool on the input element; never click the native file picker.
- Answers on forms (salary, availability, years per technology, work authorisation, sponsorship) come from `state/profile.md`: keep them consistent across applications.
- Search with several phrasings, including junior-signalling ones; screen in bulk; fill several forms per batch (default up to 10), with a short update every 3–4.
- If the good offers run out, **stop and ask**: widen the stack, the geography, the company types, or stop. Never lower the bar alone.
- After the user submits: `Applied — unconfirmed` until a confirmation email or the user's word.
