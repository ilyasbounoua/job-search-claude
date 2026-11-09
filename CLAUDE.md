# CLAUDE.md — Job search operating file

> Read this file first in every session. It holds the rules. The live state is in `state/`, the history in `log/`.
> If `state/profile.md` still says `SETUP: NOT DONE`, tell the user to run `/setup` before anything else.

## 1. Mission

- Goal: {{GOAL}} (filled by setup: role, seniority, contract type).
- Search window: {{START_DATE}} to {{DECISION_DATE}}. Sprint length: {{SPRINT_LENGTH}}.
- Passing score for an offer: {{PASSING_SCORE}}/10. It stays there until the decision gate; lowering the bar is a deliberate, staged decision (see `playbook.md` §6), never a drift.
- Languages: the user talks to Claude in {{CHAT_LANGUAGE}}. The search runs in {{SEARCH_LANGUAGES}}. Write to a company in the language of its offer.

## 2. Files

| File | Holds | Who updates it |
| --- | --- | --- |
| `state/profile.md` | Facts about the user: experience, skills, education, durations, salary, constraints. **The only source for CVs, messages and answers** | `/setup`, and any correction from the user |
| `state/current.md` | Short summary of where things stand (10 lines max) | `/close-day` |
| `state/followups.md` | Open actions with a due date | Any skill, `/close-day` |
| `state/pipeline.md` | Live processes, one row per company | Any skill, `/close-day` |
| `state/applications.md` | Every offer scored, applied to or skipped, and where the user is known or rejected | `score-offer` |
| `state/metrics.md` | Counts per day and per sprint, review notes | `/close-day`, `sprint-review` |
| `state/archive.md` | Closed rows, moved word for word | `/close-day` |
| `log/YYYY-MM.md` | One entry per day | `/close-day` |
| `admin/legal-status.md` | Legal status, right to work, salary floor and its sources | `/setup` |
| `playbook.md` | Channels, messages, interviews, review gates | Lessons from the user |
| `interviews/<Company or person>/NN_<topic>.md` | One sheet per call | `prep-call` |

Keep `state/` files short: when a row is closed, move it to `state/archive.md`. Never let this file grow with state.

## 3. Hard rules

- **Never send anything** (email, LinkedIn message, application) without the user's explicit approval for that specific item. Drafts and filled forms are fine; the user clicks send or submit.
- **Never create accounts or type passwords.** If a site needs a login, ask the user to log in.
- **Never invent facts about the user.** Everything comes from `state/profile.md` or the documents it points to. Check durations and dates before writing them. If something is missing, ask.
- **Never mark something "Applied" without evidence** (confirmation email, or the user saying they submitted). Otherwise write `Applied — unconfirmed`.
- Run `date` before stating the date, the weekday, the time or a countdown.
- Before suggesting a contact or an application, check `state/applications.md` and `state/archive.md`: no note to a company that already rejected the user, no duplicate application.
- Mail and calendar tools: call them one at a time, not in parallel (parallel calls can break the login token).
- Legal and salary-threshold facts come from official sources, cited in `admin/legal-status.md`. Say when something must be confirmed with the authority.
- CV variants stay one page unless the country's norm says otherwise (see `state/profile.md`).

## 4. Daily protocol

- One day = one session. `/today` opens the day, `/close-day` closes it.
- Between them, handle replies as they come: read, update `state/`, draft the answer, wait for approval.
- Every booked call goes into the calendar (if connected) with its preparation sheet written at the same time (`prep-call`), and the sheet's path in the event description.
- After every call or interview, ask the user how it went and write the notes in the sheet (Part D), then update the pipeline and follow-ups.

## 5. The user's preferences

{{PREFERENCES}}

(Filled by setup and by later corrections: routine and hours, mock interviews yes or no, how they like explanations (videos, written, examples), register with contacts, anything they asked Claude to stop or keep doing. Each line has a date.)
