# PinPoint Privacy Policy

Last updated: October 15, 2026. Publisher: Peerstar LLC. Contact: info@peerstarllc.com.

This policy describes the information handled by PinPoint, where it goes and who can access it. PinPoint is an internal operational feedback and ticketing tool for approved Peerstar staff.

## Information handled

PinPoint lets approved staff report a request on a selected webpage. It handles the signed-in Salesforce identity; page URL/title; comment and reply text; priority, category, assignment and mentions; optional record references and needed-by date; conditional bug/feature details; and location/browser metadata needed to place a pin. Anchor metadata can include a short text preview and fingerprint of the selected element.

Screenshots are optional and captured only when the user selects the capture option. The updated intake also supports optional user-selected image, PDF, Office, OpenDocument and text files. Users should review selected pages/files and avoid sending participant names, dates of birth or clinical details through support text, screenshots or files. Link the authorized Salesforce record instead when appropriate.

PinPoint's purpose is operational feedback and ticketing. It does not use the collected information for advertising or sell it to data brokers.

## Salesforce and Monday data flow

PinPoint records, support tickets and uploaded files are stored in Peerstar Salesforce. The Salesforce integration sends the resulting ticket's operational description, request fields, requester/assignment details, status and authenticated Salesforce links to Peerstar's Monday Tickets board for triage and development.

For the confirmed intake release, attachment content remains in Salesforce; Monday receives authenticated links rather than file bytes. A link requires Salesforce sign-in and the appropriate file/record access. PinPoint does not create public file distribution links for this flow. Existing board membership controls access to ticket information held in Monday; a filtered queue view is not an access restriction.

The extension authenticates with Salesforce over HTTPS. Its service worker holds OAuth credentials and sends authenticated requests only to validated Salesforce endpoints. The Monday credential stays in the Salesforce integration, not in content scripts or the extension's requester form.

## Local extension storage and access

OAuth tokens and extension preferences use Chrome extension storage. Local browser storage is not described here as a separate encrypted vault, and no unverified draft-retention period is promised. The selected files and screenshot data are processed temporarily during submission. Signing out removes stored Salesforce authentication through the extension's sign-out flow; removing the extension stops its collection but does not delete server records.

Salesforce sharing and field/object permissions govern record and file access. PinPoint users require the relevant permission set and approved application access. Administrators may access records according to their Salesforce privileges. Monday access is governed independently by Peerstar's workspace and board settings. No blanket promise that every staff member sees only their assigned records is made.

## Retention and requests

Salesforce and Monday data follow Peerstar's applicable retention and administrative policies. Ask the Peerstar administrator or info@peerstarllc.com for access, correction or deletion requests. A successful request may require changes in both systems; uninstalling the extension alone does not remove submitted tickets or files.

## Policy updates

Peerstar will update this policy when the workflow changes. PinPoint is an internal staff tool and is not directed at children.
