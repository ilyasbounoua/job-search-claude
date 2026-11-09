# Playbook — what works in a job search

Defaults learned from a real search. The user can change any of them; write the change and its date in `CLAUDE.md` §5.

## 1. Channels, in order

1. **People.** Alumni of the user's school, former colleagues and managers, teachers, friends of friends. A 15-minute conversation about their own path and their team, never "give me a job" in the first message. The goal is a referral or a name.
2. **Insiders at companies already applied to.** Say openly that an application is in and ask who handles it. Never at a company that already rejected the user.
3. **Direct contact** with a named engineer, hiring manager or recruiter, about a precise offer, before any form.
4. **Cold applications, last resort.** Only when nobody was found after a real search, or the contact stayed silent for a week. Score at the passing line or above. No batches.
5. **Recruitment agencies.** Useful for experienced profiles; for new graduates many clients no longer pay agencies. Test one or two, measure, drop them if they bring nothing.

What the numbers looked like in the original search: about 26 cold applications gave 1 interview process; about 40 notes and messages to people gave about 13 conversations, 2 interview processes and 4 referrals. Measure your own at every sprint review.

## 2. Messages

- **Short.** Two or three lines. A thank-you is one or two casual lines.
- **Peer to peer with engineers:** what caught my eye (their product, a talk, a stack choice) + one real question. Recruiter style only for HR.
- **Match the register** the contact uses (formal or informal, first name or not). Never default to formal if they wrote informally.
- **Connection notes** (LinkedIn): under 200 characters, counted (`wc -m`). Without Premium the free notes are limited: send a blank invitation, then a message the day they accept; keep the notes for the top targets.
- **One block per person**, with their full name, ready to copy. No templates with placeholders.
- **Follow-ups:** one light nudge after 7 to 10 days to a named person, then one last nudge on another channel a week later, then close as ghosted. Never nudge an unanswered connection note.
- **Drafts for a later day** are logged as a follow-up, not drafted in advance: the context changes.
- **Always say the true state:** "graduated in X", "my permit allows me to work until Y", never a vague hook ("this kind of problem") and never a link to something the user can't defend.

## 3. Finding people

- The school's alumni page on LinkedIn (school page → People, filter by city and keyword) guarantees the school; a keyword search by title is noisy.
- Prefer people at small and mid-size product companies (startups, scale-ups) over big groups: they answer and they can push a profile.
- Search slowly: many searches in a row can get the account rate-limited.
- A fast "no role, but your stack fits" is still a warm contact: thank them and keep the door open.

## 4. Applications

- Score every offer first (`score-offer`). Below the passing line: report and stop, unless the user says go.
- Split every gap into **screening risk** (a hard gate: "X years minimum", "confirmed", "excluding internships", nationality, clearance) and **ramp risk** (a technology listed in a stack, or an offer open to beginners). Hard gates weigh heavily; ramp gaps weigh lightly.
- An OR requirement is met in full by one side. An AND requirement with gating words is a real risk.
- Read the body of the offer, not the site's tags.
- The CV is adapted, never inflated: reorder and reframe true facts.
- Keep two processes alive until signing.

## 5. Interviews

- **Preparation sheet** for every call (`prep-call`). Pitch 60–90 seconds; other answers 20–30 seconds with one concrete fact each; details only if asked.
- **Startups** expect product motivation, the company's latest news and often a product-engineering round: a feature, its constraints, the data model, the endpoints, the bottlenecks. Prepare product design and data modelling, not only code.
- **Live coding (five steps):** Understand (rephrase, one own example and an edge case, 2–3 minutes), Naive (the literal brute force, coded fast, say its cost), Check (trace by hand, run the cases), Improve (look for a counter-example before trusting a greedy idea), Cost (say what it depends on). Out loud all the way.
- **Ask the time limit at the start** and keep a clock in sight. Interviews are lost on the time to a first working version far more than on knowledge.
- **Practice format:** 20–30 minutes alone on a problem (40 max), then a video solution, then Claude writes the correction (naive version, the sentence that leads to the better one, code, trace, cost). No hints during the timebox.
- **After each interview:** notes in the sheet the same day, honest odds, the lesson in one line, thank-you within 24 hours.
- **Salary:** never say a number first if avoidable; know the target and the floor; ask the range early; never accept on the spot (ask 48 hours).

## 6. Review gates

- **End of every sprint (`sprint-review`):** counts per channel, conversion (messages → conversations → interviews → offers), why each interview was lost, three targets for the next sprint. If fewer than 3 replies from 15 targeted contacts, change the message, the CV headline or the channel, not only the volume.
- **Mid-point:** which channel produced interviews; double down on it.
- **Decision gate (end of the window):** with no solid offer, lower the bar in stages, never all at once:
  1. Accept offers asking 1–3 years when they come through a referral.
  2. Widen geography and company types.
  3. Accept consulting or service-company roles with real development work.
  4. Last resort: lower the salary target (never below the legal floor in `admin/legal-status.md`).

## 7. Routine (default, adjusted at setup)

| Time | Block |
| --- | --- |
| Morning, first 1.5 h | Hardest preparation while fresh: algorithms or the next interview |
| Morning, next 1.5 h | Preparation sheet for the next call, or the rotating theme |
| Afternoon, 2 h | Outreach: follow-ups due, new messages, one application if an offer passes |
| Afternoon, 1 h | Calls |
| Last 10 min | `/close-day` |

Evenings and at least one day a week are off. A search lasts weeks: the pace must hold. The day after a lost interview stays light.
