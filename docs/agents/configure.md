# Configure Agent

Customize your agent's settings, tools, and behavior.

## Accessing Configuration

1. Go to **Agents** in the navigation
2. Find your agent in "Your Agents"
3. Click **Configure** (or the gear icon)

## Configuration Sections

### Basic Info

- **Name** - Update the display name
- **Description** - Change the overview text
- **Icon/Avatar** - Set a visual identifier

### Instructions

Edit the system prompt that defines agent behavior:

```
You are a [role].
Your expertise is in [domain].
When responding:
- [behavior 1]
- [behavior 2]
Always [important rule].
Never [restriction].
```

**Best practices:**
- Start with role definition
- Be specific about expertise
- Include behavioral guidelines
- Add restrictions where needed

### Model

Select which AI model powers this agent:
- Higher capability models for complex tasks
- Faster models for simple/high-volume tasks
- Consider cost vs. capability tradeoffs

### Tools

Manage which tools the agent can use:

**Add Tools:**
1. Click **Add Tool**
2. Browse or search available tools
3. Select tools to enable
4. Click **Add**

**Remove Tools:**
1. Find the tool in the list
2. Click the remove button (X)
3. Tool is disabled for this agent

**Notes:**
- Some tools require your credentials
- Missing credentials show warnings
- Agent can't use tools without proper auth

### Knowledge Base

Upload documents for the agent to reference.

See [Knowledge Base](knowledge-base.md) for details.

## Visibility

Control who can see and use your agent:

- **Private** - Only you
- **Shared** - Specific users/teams
- **Public** - Anyone can use (marketplace)

## Saving Changes

- Changes auto-save as you edit (in most cases)
- Click **Save** for immediate confirmation
- Changes apply to new conversations immediately

## Deleting an Agent

1. Open agent configuration
2. Scroll to bottom
3. Click **Delete Agent**
4. Confirm deletion

⚠️ **Warning:** Deletion is permanent. Chats using this agent will show it as unavailable.
