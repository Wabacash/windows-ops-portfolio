# INC8000140 — Directory attribute update: job title and phone extension

| | |
|---|---|
| **Category** | Identity and Access › Identity › User Attributes |
| **Priority** | P4 Low (Impact: Low, one user · Urgency: Medium, work impaired) |
| **Assignment** | Service Desk Tier 1 |
| **Requester** | Marketing Coordinator, Marketing (Austin HQ) |
| **Resolution code** | Solved (Permanently) |
| **Date** | 2026-10-06 |

## Reported issue

The requester emailed the service desk saying her office location and phone extension still showed her previous desk. She had no ticket yet and asked for one to be opened and for the approval details needed.

## Triage

A one-user, cosmetic directory change, so low priority. The key point is that this is an identity data change requested by email, so the change has to match approved details exactly and nothing more.

## Actions

1. Opened the incident from the requester's email and set the account to update as the requester's own account.
2. Left the short description searchable and recorded the original request in the description.
3. Replied to the requester asking for the new office, new extension and approval of the change.
4. Received the approved details: job title **Senior Marketing Coordinator**, department **Marketing**, office **Austin HQ**, IP phone **x555-0502**.
5. Compared the approved values with the current directory record and entered only the values that actually changed.
6. Made the change in **Active Directory** on the requester's account.

## The change

| Attribute | Current | New | Action |
|---|---|---|---|
| Job title | Marketing Coordinator | Senior Marketing Coordinator | **Changed** |
| Telephone | x555-0501 | x555-0502 | **Changed** |
| Department | Marketing | Marketing | Unchanged, left blank |
| Office | Austin HQ | Austin HQ | Unchanged, left blank |
| Display name | Maya Chen | — | Not in approval, left blank |
| Email | maya.chen@northline.corp | — | Not in approval, left blank |

## Verification and communication

Sent the requester a confirmation listing the updated title and extension, noting that department and office were already correct, and that address book and Outlook may take a little while to refresh. Asked her to report anything still showing old information. Closed with resolution code **Solved (Permanently)**.

## Security note

The simulated inbox included a security advisory about attackers impersonating the help desk and sending unexpected reset requests. In a production environment, for an identity change requested by email I would confirm the request is genuine before making it, for example by calling the user back on a number already on file and confirming the approval with her manager or the approving system.

## Lesson

Only change what was approved. The requester's email mentioned office and extension, but the approved details showed the office was already correct and included a title change. Comparing the approval against the current record, and reporting the difference back to the user, avoids unnecessary or unapproved changes.
