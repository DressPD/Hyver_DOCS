# Create a Skill

Build a reusable prompt template for work you do often.

## Open the Skill Form

1. In a chat, open the [Files & Skills panel](../chat/files-panel.md)
2. Switch to the **Skills** tab and click **New Skill**
3. The **Create a new skill** form opens

## Generate with AI (optional)

Not sure where to start? Describe it in one line in the **Generate** field — for example "Every time a deal closes in Salesforce, draft a customer welcome email" — and click **Generate**. Hyver drafts a name, description, category, and prompt template. If it can't, fill the fields in by hand.

## Fill in the Details

### Name

Give the skill a clear, specific name:
- "Code Review Assistant"
- "Weekly Update Writer"
- "Research Brief Builder"

### Description

Explain what the skill helps with — when to use it and the expected outcome.

### Category

Choose the category that best fits the workflow so the skill is easy to find later.

### Prompt Template

The core of the skill — the instructions the AI receives when you launch it. Include:
- the role or objective
- the structure you want in the answer
- any constraints or output format
- context that improves consistency

Use `{{variables}}` for parameterised inputs.

### Visibility

Skills you create are **private** — only you can use and edit them. Sharing to the marketplace isn't available yet.

## Save

1. Review the form — **name and prompt template are required**
2. Click **Create skill** (or **Save changes** when editing)
3. The skill appears under **Your skills**

## Editing and Deleting

Click a skill under **Your skills** to edit it. **Delete skill** removes it after you confirm; this can't be undone.

## Make It Recurring

To run a prompt on a schedule, launch it from the **Tasks** page with **Schedule** — see [Managing Tasks](../tasks/manage.md).

## Next Steps

- launch it in chat with `/skill/`
- refine the prompt after real usage
