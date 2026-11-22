# Tool Approvals

Before the AI runs a tool that could change something, Hyver can stop and ask you first. This replaces the old **Human control** toggle: you decide per request, and choose how long your answer applies.

## The Approval Card

When approval is needed, a card appears in the chat showing:

- **Tool approval required** and the tool the AI wants to use
- The **real payload** it will send, so you can see exactly what's about to happen
- **Review N fields before approving** when the request has fields you should check

## Approve or Deny

1. Pick a scope under **Approve:**
   - **Just this once** — this request only
   - **For this session** — further uses of the tool in this session
   - **Always allow** — don't ask again for this tool
2. Click **Approve** to let it run, or **Deny** to stop it

If submitting your answer fails, Hyver shows an error instead of failing silently — try again.

## Where Pending Approvals Appear

A run that is waiting on you doesn't get lost:

- The **Activity pane** shows **Waiting for your approval**
- The **Tasks** page lists it under **Needs approval**, where you can **Approve** or **Reject** from the card — see [Task Status](../tasks/status.md)
- You get an **Action required** [notification](../notifications/overview.md)

## When a Service Needs Authorization

If the AI needs access to a service you haven't connected, an **Authentication required** banner lists what to connect. Connect it, then retry — see [Integrations](../integrations/overview.md).

## Tips

- Use **Just this once** for anything sensitive or unfamiliar
- Choose **Always allow** only for tools you fully trust
- Read the payload before approving — it's the exact data the tool will receive
