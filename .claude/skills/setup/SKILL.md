---
name: setup
description: First-time onboarding of this job-search workspace. Interviews the user in short blocks (target, languages, salary, legal status, experience, network, tools, routine), fills state/profile.md, admin/legal-status.md and CLAUDE.md, localizes the working files, and checks the email, calendar and browser connectors. Use when the user types /setup, or when state/profile.md says "SETUP: NOT DONE" and the user wants to start.
disable-model-invocation: true
---

# Setup

Goal: at the end, the user can type `/today` tomorrow morning and get a real plan.

## How to run it

- Run `date` first. Read `CLAUDE.md`, `playbook.md`, `state/profile.md`, `admin/legal-status.md`.
- If `state/profile.md` is partly filled, say which blocks are done and resume at the first empty one.
- Ask **one block at a time**, a few questions per block, in plain words. Use AskUserQuestion when there are clear options; free text otherwise.
- Write the answers into the files at the end of each block, so a stopped setup loses nothing.
- Never guess a fact about the user. "I don't know" is a valid answer: write it as an open question in `state/followups.md`.
- The user may not be a developer: explain any technical step in one sentence and give the exact click path.

## Block 1 — Languages (first, because it decides the rest)

- Which language do you want to talk to me in?
- In which languages are you searching (offers, CVs, interviews)?
- Which country or countries?

If the country has a pack in `locales/` (e.g. `locales/fr.md` for France), read it now and use it for the rest of the setup.

## Block 2 — Target

- Role(s), seniority (new graduate, junior, experienced, career change), contract type.
- Locations in order of preference, remote policy.
- Company types wanted and excluded (startups, big groups, consulting, public sector, defence…).
- Start date, search window, and a decision date ("if nothing by then, we review the bar").
- Sprint length (default one week; two weeks if the user has less time). Write it in `CLAUDE.md` §1 and `state/metrics.md`.
- Passing score for offers (default 7/10).

## Block 3 — Legal status (do not skip, even if the user thinks it doesn't matter)

Ask plainly, and explain why: the right to work and the permit can set a salary floor or exclude some employers.

- Nationality or nationalities. Citizen of the country of the search, or of a zone with free movement?
- If not: current permit or status, its end date, any pending application, what changes at graduation or at the end of a contract.
- Right to work today (full time, limited hours, none).
- Will the employer need to do something (work authorisation, sponsorship)? Does the user want to say "sponsorship needed" on forms?
- Any bilateral agreement between the user's nationality and the target country.

Then research it on **official sources only** (government sites, the immigration authority, official texts) and write `admin/legal-status.md`: each route to work after hiring, its conditions (salary threshold, degree, employer steps), delays, duration, drawbacks, the **legal salary floor**, the sentence to say to recruiters, and the questions to confirm with the authority. Cite every source. Say clearly that it is not legal advice.

If the user is a citizen with full rights, write that in one line and move on.

## Block 4 — Salary

- Target, and the floor the user accepts (never below the legal floor from Block 3).
- What to type on forms that ask for a number.
- Write both in `state/profile.md` and `CLAUDE.md` §1 context.

## Block 5 — Experience and CV

- Ask for the CV (PDF, DOCX, LaTeX or pasted text) and any other document: internship reports, portfolio, recommendation letters. Ask the user to put them in `cv/` or give a path.
- Read them, then fill `state/profile.md`: education, experience **with exact dates and durations**, projects, skills, languages and certificates.
- Go through the skills with the user: what they can defend for two minutes in an interview, what they used but can't go deep on, what must never be claimed. Anything the user can't explain leaves the CV.
- Ask for two or three stories (a hard bug, a conflict, a failure, something they're proud of) and write them in STAR form.
- Write the sentence to say about the legal status (Block 3) and about the diploma (graduated / graduating on a date).
- CV format: one page by default; ask whether the country's norm differs. If the user wants a LaTeX CV, offer to create `cv/cv.tex` from their CV; otherwise keep their format and produce adapted versions as DOCX or PDF.

## Block 6 — Network and channels

- School(s) and whether they have an alumni network on LinkedIn.
- Former managers, colleagues, teachers, friends in the field. Who could give a name?
- LinkedIn: account in use? Premium or not? (Notes are limited without Premium; see `playbook.md` §2.)
- Job boards relevant for the country and role (ask, and suggest from the locale pack).
- Any process already running: write each one in `state/pipeline.md`.
- Any company already applied to, rejected by, or not to contact again: write them in `state/applications.md`.

## Block 7 — Tools and connectors

Check what is already available by looking at the tools you can call (names starting with `mcp__`). Then ask:

- **Email:** which provider? (Outlook / Hotmail / Microsoft 365, Gmail / Google Workspace, other.) See `docs/connectors.md` for each. Explain what Claude will do: read and search the inbox at `/today`, create drafts; **never send without approval**.
- **Calendar:** same provider as the email, or another? Claude puts booked calls in it, with the preparation sheet path, and the next day's blocks if the user wants them.
- **Browser:** Claude in Chrome lets Claude read LinkedIn and job boards and fill application forms (the user submits). Optional.
- For each connector the user wants, give the exact steps from `docs/connectors.md`, wait for the user to do them, then test with one read-only call (list 3 recent emails, list today's events, open one page). Call mail and calendar tools one at a time.
- If the user declines a connector, write it in `CLAUDE.md` §5 and adapt: the user pastes emails, Claude lists the events to add by hand.

## Block 8 — Routine and preferences

- Hours available per day, days off, best time for hard work.
- Adapt the routine table of `playbook.md` §7 to these hours.
- Preferences: mock interviews yes or no; explanations as videos, written, or worked examples; anything Claude should always or never do.
- Write them in `CLAUDE.md` §5, one line each, with today's date.

## Block 9 — Localize and finish

- Replace every `{{…}}` placeholder in `CLAUDE.md`.
- **Localize the working files** if the chat language is not English: translate `CLAUDE.md`, `playbook.md`, the `state/` files and `interviews/_templates/` into the chat language. Keep file names and the skills in English (they are instructions for Claude). Interview sheets will be written in the language of each interview.
- If a locale pack applies, merge its country-specific parts into `playbook.md` (job boards, contract vocabulary, salary norms, admin steps) and into `admin/legal-status.md`.
- Change `SETUP: NOT DONE` to `SETUP: DONE (date)` in `state/profile.md`.
- Write `state/current.md` (5 lines), the first entry in `log/YYYY-MM.md`, and the first sprint's targets in `state/followups.md`.
- Tell the user: tomorrow, type `/today`; at the end of the day, `/close-day`.
- Git: if `.git` exists, run `git remote -v`. If there is a remote and the user can't confirm it is private, or if they prefer it anyway, append these lines to `.gitignore` and run `git rm -r --cached` on them: `state/`, `log/`, `cv/`, `admin/`, `interviews/*`, `!interviews/_templates/`. Explain in one sentence why.
