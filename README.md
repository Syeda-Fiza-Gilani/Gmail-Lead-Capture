# 📥 Gmail Lead Capture → HubSpot + Slack

An n8n workflow that watches Gmail for new inquiry emails, automatically creates or updates the contact in HubSpot, and instantly alerts your sales team on Slack — no manual data entry, no missed leads.

<img width="1288" height="740" alt="image" src="https://github.com/user-attachments/assets/02dbfdd5-bdd3-4730-9c9e-56cc2f45bf7d" />

## What it does
- 📧 Triggers on new incoming emails (Gmail)
- 🧩 Extracts sender name, email, subject, and message (Code node)
- 🧑‍💼 Creates or updates the contact in HubSpot
- 🔔 Posts an instant Slack alert with the message + direct HubSpot link

## Stack
Gmail → n8n (Code) → HubSpot → Slack

## Setup
1. **Gmail** — connect OAuth2 credential (Gmail API enabled). Optionally filter by label.
2. **HubSpot** — create a Private App with `crm.objects.contacts.read/write` scopes, add the token as a credential.
3. **Slack** — create a Slack app with `chat:write` scope, invite the bot to your target channel (default: `#new-leads`).
4. Import `Gmail-HubSpot-Slack.json` into n8n, attach credentials, activate.

## License
MIT
