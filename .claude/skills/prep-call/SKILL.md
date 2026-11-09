---
name: prep-call
description: Writes the preparation sheet for a booked call or interview and links it in the calendar. Two formats - a full self-contained sheet for recruiters, HR and real interviews (pitch, stories, answers, company research), and a short casual sheet for alumni and peers. Also writes the debrief after the call. Use whenever a call, screen, interview, coffee chat or live coding gets booked, when the user asks to prepare for one, or after a call to record how it went.
---

# Prepare a call

Read `state/profile.md`, `state/pipeline.md`, the contact's history in `state/` and `log/`, and any earlier sheet in `interviews/<Company or person>/`.

## 1. Pick the format

- **Peer** (alumni, friend of a friend, an engineer who agreed to chat): it is a conversation, not an interview. Template `interviews/_templates/peer.md`.
- **Recruiter / interview** (agency, HR screen, hiring manager, technical round, final): template `interviews/_templates/interview.md`.

File: `interviews/<Company or person>/NN_<Type>_<Name>.md` (NN = order of the calls with them). Language: the language of the call. Register: the one the contact uses.

## 2. Fill it completely

- No blanks left for the user: answer from `state/profile.md`. If a fact is missing, ask.
- Every sheet is self-contained: never "see the other sheet".
- A summary at the top so it can be scanned in 2 minutes.
- **Company section** (interview format, and the table in the peer format): web research on what they do, size, clients, stack, funding and latest news, hiring signals, the interviewers' public profiles; what it means for the user; sources.
- For technical rounds: the format if known (ask the recruiter), the likely topics, and a short method reminder (`playbook.md` §5). Product-engineering round at a startup: one feature of their product designed end to end (data model, endpoints, constraints).
- Answers are short and spoken: pitch 60–90 s, others 20–30 s with one concrete fact, "if they dig" lines underneath.

## 3. Calendar

If the calendar is connected: create or update the event (one call at a time) with the meeting link and the sheet's path in the description. One call = one event = one sheet.

## 4. Preparation time

Peer and agency calls: the sheet is enough, about 30 minutes on the day. Real interviews: plan preparation blocks in the days before (fiche reading, timed practice, company research); mocks only if the user wants them (`CLAUDE.md` §5).

## 5. After the call (Part D)

Ask the user how it went (or read the transcript if they have one). Write Part D: what was asked, what went well, what didn't, honest odds, next step and its date, the lesson in one line. Then update `state/pipeline.md` and `state/followups.md`, and draft the thank-you (sent within 24 hours, after approval). If the lesson is general, add it to `playbook.md`.
