# Connectors: email, calendar, browser

All optional. Without them, you paste emails into the chat and add calendar events yourself.

Whatever is connected, Claude **reads** and **drafts**; it never sends an email or a message without your explicit approval.

## Gmail and Google Calendar

- **Claude desktop app or claude.ai:** Settings → Connectors → add **Gmail** and **Google Calendar**, and sign in with Google. Connectors added on your claude.ai account are also available in Claude Code when you're logged in with the same account.
- Test: ask Claude "list my 3 latest emails" and "what's in my calendar today".

## Outlook, Hotmail, Microsoft 365 (mail and calendar)

The connector used in the original search is the open-source `ms-365-mcp-server`. It needs Node.js (https://nodejs.org, LTS version).

In a terminal, inside this folder:

```
claude mcp add ms365 -- npx -y @softeria/ms-365-mcp-server --preset mail,calendar
```

Then restart Claude Code and ask Claude to log in: it gives you a code to enter on a Microsoft page.

Tips: Claude should call these tools one at a time (parallel calls can break the login token); if a "token expired" error comes, retry once before logging in again.

Microsoft 365 work accounts may also be available as an official connector in Settings → Connectors: use it if it's there.

## Other providers

Look in Settings → Connectors first. Otherwise forward the important emails to yourself in a connected mailbox, or paste them.

## Browser (LinkedIn, job boards, application forms)

Install the **Claude in Chrome** extension (https://claude.ai/chrome) in Chrome or Chromium and sign in. Claude Code can then open pages in your browser, read LinkedIn and job boards, pre-fill invitations and application forms.

- You stay logged in yourself: Claude never types passwords or creates accounts.
- Claude never clicks the final "send" or "submit": it leaves the tab ready for you.
- LinkedIn limits fast automated browsing: Claude searches slowly.
