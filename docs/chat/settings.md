# Chat Settings

Customize each conversation from the **Chat settings** popover.

## Accessing Settings

1. Click the **Settings** icon (⚙️) in the chat header
2. The **Chat settings** popover opens
3. Pick a model or toggle an option
4. Changes apply immediately

## Available Settings

### Model

Choose which AI model the conversation uses. Models that can't do extended thinking say so — **Reasoning** is unavailable for them.

Your default model for new chats is set under **Settings → Chat settings → Default model**.

### Reasoning

Shows the AI's thought process as it works:

- **On** - See step-by-step reasoning in responses
- **Off** - See only final answers

Reasoning helps you understand how the AI reaches conclusions. It's disabled when the selected model doesn't support it.

### Search

Lets the AI search the web:

- **On** - AI can find current information online
- **Off** - AI uses only its training data

Enable it for questions about recent events or specific facts.

## What Moved

- **Human control** is no longer a chat setting. Approvals are decided per request, with the scope choice on the approval card — see [Tool Approvals](approvals.md).
- **Knowledge base** is no longer a toggle. Keep documents in the [Files & Skills panel](files-panel.md) and reference them with `/file/`.

## Per-Chat Settings

Settings are saved per chat — each conversation remembers its own choices, so you can keep reasoning on in one chat and search off in another.

## Tips

- Enable **Reasoning** when debugging or learning
- Turn **Search** off when you want faster responses from the model alone
