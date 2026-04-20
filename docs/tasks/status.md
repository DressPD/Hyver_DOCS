# Task Status

Understanding task states and what they mean.

## Status Types

### Processing

The AI is actively working:
- Generating a response
- Running tool operations
- Thinking through complex problems

**What you can do:**
- Watch progress in chat
- Wait for completion
- Cancel if needed

### Awaiting Approval

Human Control is enabled and the AI needs your permission:
- Tool action requested
- External operation pending

**What you can do:**
- Open the chat
- Review the requested action
- Approve or deny

### Completed

The operation finished successfully:
- Response delivered
- All operations done
- No further action needed

**What you can do:**
- Review the results
- Continue the conversation
- Archive if done

### Failed

Something went wrong:
- External service error
- Timeout occurred
- Processing problem

**What you can do:**
- Check the error message
- Retry the operation
- Contact support if persistent

### Cancelled

You stopped the operation:
- Manually cancelled
- Session terminated

**What you can do:**
- Start a new conversation
- Review partial results

### Idle

Session exists but nothing is happening:
- Waiting for your next message
- No active processing

### Archived

Old session moved to storage:
- Still accessible
- Not in active list

## Status Indicators

In the Tasks list, status shows as:

- 🟢 Completed
- 🔵 Processing
- 🟡 Awaiting Approval
- 🔴 Failed
- ⚫ Cancelled / Idle

## Status Changes

Tasks automatically update:
- Refresh happens regularly
- Status changes appear in real-time
- Notifications sent for important changes
