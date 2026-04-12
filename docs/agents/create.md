# Create an Agent

Build custom agents tailored to your specific needs.

## Starting Creation

1. Go to **Agents** in the navigation
2. Click **Create Agent** button
3. The agent creation form opens

## Agent Types

### Internal Agent

- Uses Hyver's AI infrastructure
- Runs on your selected model
- Supports knowledge base uploads
- Full tool integration

### External Agent

- Connects to an external API endpoint
- You provide the AI backend
- Advanced use case

Most users choose **Internal Agent**.

## Basic Configuration

### Name

Give your agent a clear, descriptive name:
- "Research Assistant"
- "Code Reviewer"
- "Customer Support Bot"

### Description

Explain what your agent does:
- Keep it concise but informative
- Mention key capabilities
- Help others understand the purpose

### Instructions

The most important field - define how your agent behaves:

```
You are a helpful research assistant. 
You specialize in finding and summarizing academic papers.
Always cite your sources and provide links when available.
Be thorough but concise in your responses.
```

**Tips for instructions:**
- Be specific about personality and tone
- Define the agent's expertise area
- Include do's and don'ts
- Mention any constraints or limitations

## Model Selection

Choose the underlying AI model:

| Model | Best For |
|-------|----------|
| **GPT-4** | Complex reasoning, nuanced tasks |
| **Claude** | Long documents, detailed analysis |
| **Faster models** | Quick responses, simple tasks |

## Tools

Add tools your agent can use:

1. Click **Add Tools**
2. Select from available tools
3. Some tools require credentials - connect them first

See [Tools Overview](../tools/overview.md) for more.

## Saving

1. Review all settings
2. Click **Create** or **Save**
3. Your agent appears in "Your Agents"

## Next Steps

After creating:
- [Configure advanced settings](configure.md)
- [Add knowledge base documents](knowledge-base.md)
- Start chatting with your new agent!
