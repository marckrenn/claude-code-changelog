# Claude Code 2.1.208 – Flags

| Flag | Type | Category | Summary | Notes | Confidence | Occurrences |
| --- | --- | --- | --- | --- | --- | ---: |
| `tengu_auto_mode_config` | config | ui | Gates “auto mode” availability, with circuit-breaker disable plus model and org allowlist checks. | Also respects user settings (disableAutoMode) and can disable fast mode. | high | 1 |
| `tengu_bridge_min_version` | config | tools | Blocks Remote Control when Claude Code is below a configured minimum version. |  | high | 1 |
| `tengu_bridge_poll_interval_config` | config | networking | Sets Tengu bridge poll interval (0 disables) plus session reclaim and keepalive timings. | Config is schema-validated; invalid values fall back to defaults. | medium | 1 |
| `tengu_bridge_repl_v2_config` | config | other | Config named "tengu_bridge_repl_v2_config" referenced, likely for a "bridge" REPL v2 setting set. | Only the config name/type is shown; no observable behavior or UI impact in the provided context. | low | 1 |
| `tengu_ccr_bridge` | gate | tools | Enables the Tengu CCR bridge for Claude Code, with an optional minimum bridge version check. | Only gate checks and a min-version config are visible; what the bridge does beyond enabling is not shown. | medium | 4 |
| `tengu_ccr_bundle_seed_enabled` | gate | tools | Enables seeding a CCR bundle for remote sessions when repo/env gate is set | Also influenced by CCR_FORCE_BUNDLE and CCR_ENABLE_BUNDLE env vars and various git/GitHub checks. | high | 3 |
| `tengu_desktop_upsell` | config | prompts | Enables a startup dialog upsell for a desktop app on macOS or Windows x64. | Gate appears limited to darwin/win32 x64 and checks an enable_startup_dialog setting. | medium | 1 |
| `tengu_harbor` | gate | auth | Gate controlling onboarding/opt-in flows and channel access including Claude AI OAuth token checks | Also influences UI dialogs (Onboarding, Trust, AutoMode opt-in) and a channel allowlist; not all behavior is fully visible. | medium | 1 |
| `tengu_kairos_brief` | config | prompts | Enables a “brief” user message/tool (markdown) when entitled or CLAUDE_CODE_BRIEF is set. | Gated by an entitlement check plus another condition (By()\|\|kZ()). | medium | 1 |
| `tengu_kairos_cron` | config | tools | Enables session-only cron tools to schedule prompts to run later or on a recurring schedule. | Disabled when CLAUDE_CODE_DISABLE_CRON is set. | high | 1 |
| `tengu_kairos_cron_config` | config | tools | Configures cron scheduling jitter/recurrence limits for a background job runner. | Only schema and accessor names are visible; the specific jobs affected aren’t shown. | medium | 1 |
| `tengu_kairos_cron_durable` | config | filesystem | Controls whether scheduled prompts are persisted to .claude/scheduled_tasks.json (durable vs session-only). | Set durable: true to write to disk; otherwise schedules are session-only. | high | 1 |
| `tengu_kairos_push_notifications` | config | tools | Enables the PushNotification tool to notify users in-terminal and, with Remote Control, on mobile. | Also checks an agent setting (agentPushNotifEnabled) before allowing mobile push. | high | 1 |
| `tengu_malort_pedway` | config | ui | Enables a “Chicago” UI feature (with coordinateMode) only for max/pro tiers. | Flag name is opaque; behavior inferred from exported getters and hotkey usage nearby. | medium | 1 |
| `tengu_max_version_config` | config | tools | Minimum-version config used to block applying an update when the target version is too old. | Config also exposes optional `external` and `external_message` fields, likely for update messaging. | medium | 1 |
| `tengu_on_branch_default_guard_observe` | gate | telemetry | Observes or logs default guard behavior for “on-branch” flow in Tengu. | Only the flag name and type are present; behavior inferred from naming (“observe”, “default_guard”). | low | 1 |
| `tengu_startup_announcements` | config | ui | Enables startup announcements to be shown on app launch. | Only the flag name and type are present; no behavior or call sites shown. | low | 1 |
| `tengu_version_config` | config | tools | Fetches a minimum required Claude Code version and shows an update-required message. | Minimum version appears server-configured via the config fetch. | high | 1 |
