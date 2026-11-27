When enabled (the default), approval prompts for tools without a `toolPolicy` entry offer a persistent grant — **Always allow**, or **Allow for all tasks** for tools that can modify data — the Tool permissions picker in Connector settings lets users pre-approve tools, and those grants persist across sessions with no expiry.

When disabled, the persistent options are hidden from approval prompts and from the Connector settings picker, and previously stored persistent grants stop being honored. Scheduled-task runs also stop offering, recording and replaying the **Allow for all scheduled runs** approval, unless a scheduled-task approval lifetime of one day or more is set. Users can still approve each call. Outside scheduled-task runs they can also choose **Allow for this task**, except for read-only tools on servers they added themselves.

A per-tool `toolPolicy` entry on `managedMcpServers` always takes precedence over this key: `blocked`, `ask`, and `allow` behave exactly as documented there whether this key is enabled or not.

This key governs the chat and Cowork surfaces. Code sessions use a separate permission path this key does not cover — govern Code tool approvals with per-tool `toolPolicy` entries, whose `blocked` and `ask` values are forwarded there.
