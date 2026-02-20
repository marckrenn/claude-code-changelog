# Claude Code 2.1.49 – Flags

| Flag | Type | Category | Summary | Notes | Confidence | Occurrences |
| --- | --- | --- | --- | --- | --- | ---: |
| `tengu_1p_event_batch_config` | config | telemetry | Configures OpenTelemetry first-party event logging batch sizes, queue limits, and export interval. | Only seen in initializer; downstream usage not fully shown. | high | 1 |
| `tengu_copper_lantern_config` | config | ui | Config date threshold for enabling a pro/max feature only for older subscriptions | Exact feature purpose unclear; appears to gate eligibility by plan and signup date. | medium | 1 |
| `tengu_disable_bypass_permissions_mode` | gate | safety | Disables bypass-permissions mode availability in CLI permission handling based on remote gate/settings | Used to prevent selecting bypassPermissions mode via CLI/config. | high | 3 |
| `tengu_max_version_config` | config | tools | Controls CLI minimum version enforcement and update messaging behavior | Only one occurrence; exact effect of external value unclear. | medium | 1 |
| `tengu_scratch` | gate | filesystem | enable temporary scratchpad directory for session memory summaries | Behavior inferred from nearby path construction and conditional check. | medium | 1 |
| `tengu_sm_compact_config` | config | prompts | Configure compaction thresholds using token and message count limits | Only token/message limit fields are visible. | medium | 1 |
| `tengu_sm_config` | config | caching | Configure thresholds for initializing and updating session memory based on tokens and tool calls | Only shows config read and threshold fields, not how updates are applied. | medium | 1 |
| `tengu_streaming_tool_execution2` | gate | tools | Gates creation of a tool-execution handler in the streaming CLI request loop | Only observed gating EV0 construction; exact behavior of EV0 is unclear. | high | 1 |
| `tengu_thinkback` | gate | tools | Enables Thinkback year-in-review command and hidden animation playback tool | Controls availability of local CLI/plugin commands. | high | 2 |
| `tengu_tool_pear` | gate | tools | Enables stricter tool schema/strict mode when using specific models in CLI tool definitions | Exact behavior of OV0/Ey2 unknown from snippet. | medium | 2 |
| `tengu_vscode_onboarding` | gate | ui | Controls whether VSCode connected experience shows onboarding flow | Only seen declared and sent as a gate; no UI behavior shown. | medium | 1 |
| `tengu_vscode_review_upsell` | gate | ui | Enable VS Code review upsell experiment gate sent to connected client. | Only shows gate transmission and event logging, not the upsell UI itself. | medium | 1 |
