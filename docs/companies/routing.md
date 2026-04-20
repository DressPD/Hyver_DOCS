# Routing Strategies

Control how tasks are distributed among agents in a company.

## What is Routing?

When a message comes to a company:
1. The orchestrator receives it
2. Routing strategy determines which agent(s) handle it
3. Response flows back through the orchestrator

## Available Strategies

### Automatic Routing

The orchestrator decides based on:
- Message content
- Agent capabilities
- Context

**Best for:** General use, varied task types

### Sequential

Agents process in order:
1. First agent handles message
2. Output goes to second agent
3. And so on...

**Best for:** Pipeline workflows (draft → review → edit)

### Parallel

Multiple agents work simultaneously:
- All relevant agents receive the task
- Responses are combined

**Best for:** Getting multiple perspectives

### Skill-Based

Route based on agent expertise:
- Match task requirements to agent skills
- Most qualified agent handles each part

**Best for:** Specialized teams

## Configuring Routing

1. Open company configuration
2. Find **Routing Strategy** section
3. Select your preferred strategy
4. Configure strategy-specific options

## Strategy Selection Tips

| Use Case | Recommended Strategy |
|----------|---------------------|
| General assistant team | Automatic |
| Content creation pipeline | Sequential |
| Research with multiple angles | Parallel |
| Technical support team | Skill-Based |

## The Orchestrator's Role

Regardless of strategy, the orchestrator:

- Makes final routing decisions
- Can override strategy when appropriate
- Handles edge cases
- Coordinates multi-step workflows

## Adjusting Over Time

Routing can be refined:
- Monitor which agents get used
- Check if tasks go to right specialists
- Adjust strategy or agent selection
- Add agents if gaps appear
