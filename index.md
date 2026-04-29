# PinPoint Privacy Policy

**Last updated:** April 29, 2026
**Publisher:** Peerstar LLC
**Contact:** privacy@peerstarllc.com

PinPoint is a private feedback-pin Chrome extension built exclusively for
Peerstar LLC staff. This policy describes what data the extension handles,
where it goes, and who can see it.

## Scope

PinPoint runs only when a Peerstar staff member signs in with their existing
Salesforce credentials. Without an authenticated session against Peerstar's
Salesforce organization (Org ID `00Dal00001ODMcHEAX`), the extension performs
no data collection.

## What we collect

When an authenticated user drops a pin or leaves a comment, PinPoint captures:

- The URL and title of the page where the pin was dropped
- The text of comments and replies
- Optional screenshots of the user's active tab — captured **only** when the
  user explicitly clicks the "capture screenshot" button while composing a
  comment
- The signed-in user's Salesforce identity (user ID, name, email)
- Pin location coordinates (CSS selector and viewport position)
- Browser user-agent string and viewport dimensions

The extension does not collect: keystrokes outside the comment composer, page
content beyond the user-clicked location, browsing history, form data, or
data from any tab the user has not explicitly interacted with using PinPoint.

## Where data is stored

All collected data is stored exclusively in **Peerstar LLC's Salesforce
organization** as native `Page_Comment__c` records and ContentVersion files.
No data is sent to third-party servers, analytics tools, advertising networks,
or external APIs at any time.

The extension makes outbound network requests **only** to:

1. `login.salesforce.com` (OAuth authentication)
2. `*.my.salesforce.com` and `*.lightning.force.com` (Peerstar's Salesforce
   instance for API calls)

## Local storage

PinPoint uses Chrome's `chrome.storage.local` API to cache:

- OAuth access and refresh tokens (encrypted by Chrome at rest)
- Offline draft comments (so users don't lose work during connectivity loss)
- User preferences (sidebar open/closed state, keyboard-shortcut overrides)

No protected health information (PHI), patient data, or comment content is
stored locally beyond temporary drafts. Drafts are cleared when sent or after
30 days, whichever is sooner.

## Who can access data

- **In Salesforce**: only Peerstar staff with the `Pin_Tool_User` permission
  set assigned. Salesforce field-level security and record-level sharing rules
  govern all access. Standard Salesforce audit logs apply.
- **In the extension**: only the signed-in user can see their tokens and
  drafts on their own device.
- **Peerstar admins** can access any comment via Salesforce reports, list
  views, or the standard Salesforce data model — same as any other Salesforce
  data.

## Authentication

Sign-in uses **Salesforce OAuth 2.0 with PKCE** (Proof Key for Code Exchange).
The extension never sees, stores, or transmits Salesforce passwords. The
extension's hard-coded organization allowlist (`VITE_SF_ALLOWED_ORG_IDS`)
restricts authentication to Peerstar's Salesforce organization — sign-in
attempts from any other organization are rejected client-side.

## Sharing with third parties

We do not sell, rent, share, or transfer collected data to any third party.

## Data retention and deletion

- **In Salesforce**: data is retained according to Peerstar's standard
  retention policies for Opportunity-linked records.
- **To request deletion**: contact your Peerstar Salesforce administrator
  directly, or email privacy@peerstarllc.com.
- **Removing the extension** stops further collection but does not delete
  existing Salesforce records.

## Compliance

PinPoint is designed for use within a HIPAA-aware Salesforce environment.
Comments may be tied to PHI-related records (e.g., referrals containing
patient identifiers) — but the extension itself is treated as a thin client.
All HIPAA controls are enforced server-side by Peerstar's Salesforce
configuration (encryption at rest, audit log, BAA with Salesforce).

## Children

PinPoint is an internal staff tool. It is not directed at and does not
knowingly collect data from children under 13.

## Changes to this policy

Material changes will be announced via Peerstar internal communication and
the "Last updated" date above will reflect the change. Continued use of the
extension after a policy update constitutes acceptance.

## Contact

For privacy questions, data deletion requests, or to report a concern,
email **info@peerstarllc.com**.
