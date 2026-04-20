# Tools Overview

Tools connect Hyver agents to external services and APIs.

## What are Tools?

Tools let agents take actions in the real world:

- **Send emails** via Gmail
- **Create documents** in Google Docs
- **Manage calendars** in Google Calendar
- **Post messages** to Slack
- **Access data** from external APIs

## How Tools Work

1. You **connect** your credentials (once)
2. You **add** tools to agents
3. Agents **use** tools during chat
4. You may **approve** sensitive actions

## Tool Categories

### Productivity

- Google Workspace (Gmail, Drive, Calendar, Docs)
- Microsoft 365
- Slack

### Development

- GitHub
- Jira
- Database access

### Data

- Web search
- API integrations
- Custom endpoints

## Credential Requirements

Most tools require authentication:

| Type | Example |
|------|---------|
| **API Key** | Simple token you provide |
| **OAuth** | Sign in with your account |
| **Basic Auth** | Username and password |

You connect credentials once, then any agent with that tool can use it.

## Using Tools

### Direct Chat

Type `@` in the message box, find a tool, and add it to your chat.

### Via Agents

Agents with tools configured use them automatically when relevant.

## Tool Approval

When **Human Control** is enabled:
- Agent requests to use a tool
- You see what action will happen
- Click **Approve** or **Deny**
- Agent proceeds based on your decision

## Learn More

- [Browse Tools](browse.md)
- [Connect Credentials](credentials.md)
- [OAuth Tools](oauth.md)
