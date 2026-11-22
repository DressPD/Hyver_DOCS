# Activity Pane

The Activity Pane shows real-time insight into what the AI is doing during complex operations.

## What is the Activity Pane?

When the AI processes your request it may:
- Think through problems step by step
- Call external tools (web search, browsing, and more)
- Process and synthesise information
- Pause to ask for your approval

The Activity Pane lets you watch this unfold as it happens.

## Opening the Activity Pane

1. Look for the **Activity** button in the chat header
2. Click to toggle the pane open or closed (**Collapse panel** / **Expand panel**)
3. The pane appears on the right side of the chat

## What You'll See

### Status

A status line shows what the run is doing right now: **Running**, **Ready**, **Waiting for your approval**, **Paused**, **Completed**, or **Error**. While a run is live you'll see **Live** and the current response; afterwards, the **Last response**.

### Steps and Tool Activity

A step-by-step timeline of the AI's thinking and its tool calls:

- **Thinking** — internal reasoning steps (when Reasoning is on)
- **Tool activity** — which tool was called, what went in, what came back, and whether it succeeded, failed, or is still running (for example **2/3 completed**)
- **Loops** — how many iterations the run has taken

### Usage

Counts of **Steps**, **Tools**, and actions used (in / out / total) for the run.

### Browser Views

When the AI browses the web on your behalf, screenshots and a live view of the browser can appear in the chat.

## Workspace Status

Hyver runs your tasks in a personal workspace that starts on demand:

| Status | Meaning |
|--------|---------|
| **Workspace starting…** | Being set up in the background — the chat works normally in the meantime |
| **Workspace ready** | Ready to run |
| **Workspace hibernated** | Idle; it starts automatically on your next message |
| **Responding…** / **Reconnecting…** | A reply is in progress, or the connection is being restored |
| **Needs approval** / **Needs authorization** | Waiting for you — see [Tool Approvals](approvals.md) or connect the service |
| **Last message failed** / **Workspace error** | Something went wrong; try sending again |

The first message after the workspace has been idle can take a little longer while it wakes up.

## When to Use It

- **Learning** — Understanding how the AI approaches your request
- **Debugging** — Seeing why something didn't work as expected
- **Complex tasks** — Following multi-step operations
- **Tool operations** — Verifying external actions

## Resizing

The pane is resizable — drag its left edge to make it wider or narrower.

## Tips

- Collapse the pane when you don't need it to save screen space
- Open it during multi-step operations
- Check the **Workspace** status if a reply is slow to start
