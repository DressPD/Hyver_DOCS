# Integrations Overview

Hyver connects to external services in two places: **tools** you connect from chat, and **messaging integrations** (Telegram and Slack) you set up in Settings.

## Connecting Tools (from Chat)

The chat **welcome screen** shows a **Connect your tools** panel with one-click chips for external services (Gmail, GitHub, and more). Connecting a tool lets the AI act on your behalf in that service.

### Connect a tool

1. Click a tool chip
2. For OAuth tools, a popup opens for you to authorize the connection
3. For API-key tools, paste your key and submit

Connected tools show a checkmark. Click the ✕ on a connected chip to disconnect.

### Connecting mid-conversation

If the AI needs access to a service while working, it shows an **Authentication required** banner listing the services to connect. Connect them, then click **I've connected — retry** to continue.

> Once a tool is available, you can point the AI at it in chat with `/tool/`. Administrators can browse the full catalog from the **Tools** page.

## Messaging Integrations (Settings)

Open **Settings → Integrations** to connect messaging platforms so Hyver can reach you — and so you can chat with Hyver — outside the web app.

### Telegram

1. Click **Telegram**
2. Paste your **Bot Token** (from @BotFather) and a **Secret Token** (use the generate button for a random one)
3. Click **Connect Telegram**

### Slack

Click **Slack**, then choose a method:

- **OAuth** — one-click install; authorize in the popup. You can connect multiple workspaces and manage them from the same panel.
- **Token** — paste a **Bot Token** and **Signing Secret** to bring your own credentials.

Connected integrations show a **Connected** badge; use **Disconnect** to remove one. For Slack, a **Linked** indicator shows whether your Hyver account is linked to the workspace — DM the bot or use the `/link` command to link it.

## Tips

- Connect only the tools you need; you can disconnect any of them later
- Use Telegram or Slack to get notified and keep chatting with Hyver on the go
