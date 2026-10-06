# INC9351235 — Most of inbox disappeared overnight

| | |
|---|---|
| **Category** | Software › Email (NorthMail) |
| **Priority** | P4 Low (as logged) |
| **Assignment** | Service Desk Tier 1 |
| **Requester** | Operations Analyst, Distribution Center |
| **Device** | Windows workstation (NL-DSK-0308) |
| **Resolution code** | Solved (Permanently) |
| **Date** | 2026-10-06 |

## Reported issue

The requester opened her mail client and found only a handful of messages where there had previously been weeks of mail. Nothing was in Deleted Items. She was worried something had wiped her mailbox, had reports in there she still needed, and asked that nothing else be deleted until the cause was known.

## Triage

Logged as P4 Low, but a report of missing mail the user still needs is potentially a data loss or account compromise issue, so I treated it as more serious than the label suggested until I knew the cause. The first priority was to avoid making anything worse: no deleting, moving or rebuilding anything until I had looked.

## Diagnosis

1. Connected to the workstation through a remote session.
2. Opened the mailbox and checked the view settings.
3. Found that a filter was active (the filter button was highlighted red), which was hiding most of the inbox.
4. Checked the mailbox rules as well, to rule out a rule moving or deleting mail. The view filter was the only cause identified.

## Resolution

1. Opened **View** and selected the filter button.
2. Changed the filter to **All**.
3. Confirmed the full inbox, including the older messages and reports, was visible again.

## Verification

Contacted the requester by text, who confirmed her mail and reports were back. Ticket closed after her confirmation, with resolution code **Solved (Permanently)**.

## Root cause and prevention

**Cause:** A view filter was active in the mail client, so only a few messages were displayed. No mail was deleted or lost.

**Prevention:** Advise users to check for an active filter (status bar or highlighted filter button) if only a few messages appear, and to contact the service desk if mail really is missing.

## What I would also check in a production environment

Beyond the view settings and inbox rules I checked here, a "mail disappeared" report in a real environment would also warrant:

- Comparing with webmail to confirm whether the mail exists server-side.
- Reviewing forwarding settings and recent sign-in activity for anything unusual, and escalating as a security incident if it looked suspicious.
- Checking Recoverable Items and retention settings if the mail was missing on the server.

## Lesson

A hidden filter can look exactly like data loss. Checking the view settings and mailbox rules first is quick and non-destructive, and it avoids unnecessary escalation, while still treating the report seriously until the cause is confirmed.
