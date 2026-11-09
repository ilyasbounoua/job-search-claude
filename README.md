# Job Search with Claude Code

A ready-made workspace that turns Claude Code into your job-search partner: it plans your day, reads your inbox, tracks every lead, scores offers, adapts your CV, prepares your calls and interviews, and keeps a log so nothing falls through the cracks.

It was built during a real two-month search for a first full-time job and keeps what worked: people first, cold applications last, a short daily routine, and a review at the end of each sprint.

You stay in control: **Claude never sends an email, a message or an application by itself.** It writes drafts and fills in forms, and you click "send".

---

## 1. Before you start: keep it private

Your CV, salary expectations and legal status will end up in these files. **Don't put them in a public repository.**

- **Easiest (no GitHub needed):** click the green **Code** button, then **Download ZIP**, and unzip it somewhere on your computer (for example `Documents/job-search`).
- **With GitHub:** click **Use this template**, then **Create a new repository**, and choose **Private**. Don't use "Fork": a fork of a public repository is public.

During setup, Claude asks whether you use git and, if the repository could ever be public, adds your personal folders (`state/`, `log/`, `cv/`, `admin/`, `interviews/`) to `.gitignore` so they are never pushed.

## 2. Install Claude Code

You need a Claude subscription (Pro or Max) or an Anthropic API account.

- **Desktop app (recommended if you're not a developer):** install the Claude desktop app, open the **Code** tab, and choose the folder you unzipped as the project folder.
- **Terminal:** follow https://docs.claude.com/en/docs/claude-code/quickstart, then run `claude` inside the folder.

A normal chat or a "Project" on claude.ai is **not** the same thing: it can't read these files or run the skills. Use Claude Code (the Code tab).

## 3. First thread: setup

Open a new session in the folder and type:

```
/setup
```

Claude interviews you in short blocks: who you are, what job you want, where, which languages, salary, **legal status** (nationality, permit, right to work), your CV and experience, your network, your tools (email, calendar, browser) and your routine. It then fills in the files, translates the working files into your language and tells you which connectors to switch on.

It takes about 30 to 45 minutes. You can stop at any time and type `/setup` again later: it picks up where you left off.

## 4. Every day

| You type | What happens |
| --- | --- |
| `/today` | Claude checks the date, reads your inbox and your files, lists what's due and gives you the plan for the day |
| `/close-day` | Claude updates the tracker, the pipeline and the metrics, writes the day's log and gives tomorrow's 5 targets |

Everything else happens on its own when the situation calls for it. You can also call these skills yourself:

| Skill | When Claude uses it |
| --- | --- |
| `score-offer` | You paste an offer or ask for offers: score, adapt the CV, motivation, form filled but not sent |
| `prep-call` | A call or interview is booked: Claude writes a preparation sheet and adds it to the calendar |
| `outreach` | You need to write to someone: alumni, an engineer, a recruiter, a follow-up |
| `sprint-review` | The end of your sprint (you choose its length during setup): what worked, by channel, and the next targets |

## 5. What's inside

```
CLAUDE.md          Claude's operating rules (read at every session)
playbook.md        What works in a job search: channels, messages, interviews
state/             Your profile, pipeline, follow-ups, metrics, applications (live)
log/               One daily log file per month
admin/             Your legal status and salary floor, with sources
interviews/        One folder per company or person, one sheet per call
cv/                Your CV sources and adapted versions
locales/           Country packs (France included)
docs/              Connector setup help (email, calendar, browser)
.claude/skills/    The skills listed above
```

## 6. Good to know

- Claude can make mistakes. Check anything legal (permits, salary thresholds) with the official authority before signing.
- Claude only uses facts from your CV and your answers. If something is wrong in a draft, tell it: the correction goes into your profile.
- The more you tell it after each call ("they said X"), the better the next steps get.
