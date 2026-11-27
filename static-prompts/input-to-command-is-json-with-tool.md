Input to command is JSON with tool_name, tool_input, tool_use_id, and reason.
Return {"hookSpecificOutput":{"hookEventName":"PermissionDenied","retry":true}} to tell the model to make the call again only if the user asked for it; auto mode checks it again.
Exit code 0 - stdout/stderr not shown
Other exit codes - show stderr to user only
