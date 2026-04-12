# Connect Credentials

Set up tools by providing authentication credentials.

## Credential Types

Different tools require different authentication:

| Type | What You Provide |
|------|------------------|
| **OAuth** | Authorize via popup (Google, Slack) |
| **API Key** | Your API key from the service |
| **Bearer Token** | Access token |
| **Basic Auth** | Username and password |

## Connecting a Tool

### Step 1: Find the Tool

1. Go to **Tools** page
2. Find the tool you want to connect
3. Click **Connect**

### Step 2: Enter Credentials

**For API Key / Token:**
1. Credential form opens
2. Enter your key or token
3. Click **Save**

**For OAuth:**
1. See [OAuth Tools](oauth.md)

### Step 3: Verify

After saving:
- Tool status changes to "Connected"
- Tool becomes usable in chats
- Can be added to agents

## Getting API Keys

Each service has different steps to get an API key:

1. Log into the service's developer portal
2. Create or find your API key
3. Copy the key
4. Paste into Hyver

> **Tip:** Check the tool's description for specific instructions.

## Managing Credentials

### Update Credentials

1. Go to **Tools**
2. Click on a connected tool
3. Click **Update Credentials**
4. Enter new credentials
5. Save

### Disconnect

1. Go to **Tools**
2. Click on a connected tool
3. Click **Disconnect**
4. Confirm

Disconnecting:
- Removes your stored credentials
- Tool no longer works in chats
- Agents using this tool will skip it

## Security

- Credentials are encrypted at rest
- Transmitted securely (HTTPS)
- Only used when agents need them
- You can revoke anytime

## Troubleshooting

### "Invalid credentials"
- Double-check the key/token
- Ensure no extra spaces
- Verify the key hasn't expired

### "Permission denied"
- The key may lack required permissions
- Check the service's permission settings
- Generate a new key with correct scopes
