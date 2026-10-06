# INC8859730 — Need to change display resolution before a presentation

| | |
|---|---|
| **Category** | Hardware › Display |
| **Priority** | P4 Low |
| **Assignment** | Service Desk Tier 1 |
| **Requester** | Accounting Specialist, Finance |
| **Device** | Windows workstation (NL-DSK-0195) |
| **Resolution code** | Solved (Permanently) |
| **Date** | 2026-10-06 |

## Reported issue

The requester was about to connect to the projector in the large conference room for a presentation. The last time he connected, the text was huge and blurry. He asked for help getting the resolution right beforehand.

## Triage

Low impact and low priority on paper, but it was time-sensitive because of the upcoming presentation. A quick, low-risk fix that could be done remotely.

## Diagnosis

Joined a remote session to the workstation. The desktop was **blank**: no icons were visible. That was a clue that the display settings were off, since a resolution or scaling mismatch can leave icons off-screen or unrendered, and it matched the user's report of display problems on the projector.

## Resolution

1. Joined the remote session and found the blank desktop.
2. Right-clicked the desktop and opened **Display settings**.
3. Changed the resolution to the **recommended** value.
4. The desktop icons appeared, confirming the display settings were the problem.

## Verification

Contacted the requester, who confirmed everything looked fine. Closed with resolution code **Solved (Permanently)**.

## Root cause and prevention

**Likely cause:** The display resolution was not set to the recommended value. This would explain both the blank desktop in my session and the blurry or oversized text on the projector.

**Limitation:** I could not test against the conference room projector itself, so the fix was verified on the workstation display and by the requester's confirmation, not on the projector.

**Prevention and advice for the user:**

- Use **Win + P** and choose Duplicate or Extend when connecting to a projector.
- If text looks blurry again, check Display settings and make sure the resolution matches the projector's native resolution (commonly 1920x1080).
- Connect and test a few minutes before the presentation, not at the start.

## Lesson

What you see in the remote session can reveal more than the ticket says. Here a blank desktop confirmed the display was misconfigured before I changed anything. Being clear about what was and was not tested, and giving the user a quick pre-presentation check, closes the gap on the projector side.
