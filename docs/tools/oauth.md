# OAuth Tools

Connect tools using OAuth authorization (Google, Slack, etc.).

## What is OAuth?

OAuth lets you grant Hyver access to external services without sharing your password:

1. You click **Connect**
2. A popup opens to the service (Google, Slack, etc.)
3. You log in and approve permissions
4. The service sends a secure token to Hyver
5. Hyver uses this token to access the service

## Connecting OAuth Tools

### Step 1: Start Connection

1. Go to **Tools** page
2. Find the OAuth tool (e.g., Google Workspace)
3. Click **Connect**

### Step 2: Authorize

1. A popup window opens
2. Log into the service if needed
3. Review the requested permissions
4. Click **Authorize** or **Allow**

### Step 3: Complete

1. Popup closes automatically
2. Tool status changes to "Connected"
3. Tool is ready to use

## Common OAuth Tools

### Google Workspace
- Gmail - Read and send emails
- Calendar - View and create events
- Drive - Access files
- Docs/Sheets - Edit documents

### Slack
- Read channels
- Send messages
- Manage workspace

## Permission Scopes

OAuth tools request specific permissions:

- **Read-only** - View but not modify
- **Read/Write** - View and modify
- **Full access** - Complete control

Review permissions carefully before authorizing.

## Managing OAuth Connections

### Check Status

1. Go to **Tools**
2. Connected tools show ✓
3. Click to see details

### Reconnect

If connection expires:
1. Click **Reconnect**
2. Authorize again
3. New token is stored

### Disconnect

1. Go to **Tools**
2. Click the connected tool
3. Click **Disconnect**

Also revoke access in the service's settings:
- Google: myaccount.google.com → Security → Third-party apps
- Slack: Workspace settings → Apps

## Troubleshooting

### Popup blocked
- Allow popups for Hyver in browser settings
- Try again

### Authorization failed
- Check your service account is active
- Ensure you're logged into the correct account
- Try disconnecting and reconnecting

### Token expired
- Click **Reconnect**
- Authorize again
- Tokens refresh automatically when possible
