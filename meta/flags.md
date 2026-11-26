# Claude Code 2.1.332 – Flags

1,072 flags: 879 gates, 193 configs. Default is the fallback in the code; the value a user gets is set on the server.

| Flag | Type | Default | Summary | Notes | Confidence |
| --- | --- | --- | --- | --- | --- |
| `bot_protected_tengu_amber_plover` | gate | on |  |  |  |
| `bot_protected_tengu_slate_orchard` | gate | on |  |  |  |
| `cai_proud_planet` | gate | off |  |  |  |
| `tengu-model-error-overrides` | config |  |  |  |  |
| `tengu-off-switch` | config |  |  |  |  |
| `tengu_abundant_thunder` | gate | on |  |  |  |
| `tengu_abundant_trinket` | gate | on |  |  |  |
| `tengu_agents_md_mod` | config |  |  |  |  |
| `tengu_agentview_inherit_mode_demote` | gate | on |  |  |  |
| `tengu_agile_glade` | config |  |  |  |  |
| `tengu_agile_waffle` | gate | off |  |  |  |
| `tengu_alder_compass` | gate | off |  |  |  |
| `tengu_amber_anchor` | gate | off |  |  |  |
| `tengu_amber_doorbell` | gate | off |  |  |  |
| `tengu_amber_ferry` | gate | off |  |  |  |
| `tengu_amber_flint` | gate | on |  |  |  |
| `tengu_amber_kestrel` | gate | off |  |  |  |
| `tengu_amber_larch` | gate | on |  |  |  |
| `tengu_amber_lark` | gate | off |  |  |  |
| `tengu_amber_lattice` | config |  |  |  |  |
| `tengu_amber_lynx` | gate | off |  |  |  |
| `tengu_amber_packet` | gate | off |  |  |  |
| `tengu_amber_prism` | gate | off |  |  |  |
| `tengu_amber_redwood2` | config | "" |  |  |  |
| `tengu_amber_redwood3` | config | "" |  |  |  |
| `tengu_amber_relay` | gate | off |  |  |  |
| `tengu_amber_rokovoko` | config |  |  |  |  |
| `tengu_amber_sextant` | gate | on |  |  |  |
| `tengu_amber_sluice` | gate | off |  |  |  |
| `tengu_amber_thistle` | gate | on |  |  |  |
| `tengu_amber_tollgate` | gate | off |  |  |  |
| `tengu_amber_tributary_dotterel` | gate | off |  |  |  |
| `tengu_amber_tributary_sandpiper` | gate | off |  |  |  |
| `tengu_ambling_tortoise` | config | 0 |  |  |  |
| `tengu_ancient_pudding` | gate | off |  |  |  |
| `tengu_ant_yolo_equiv_strip_config` | config |  |  |  |  |
| `tengu_async_goblet` | gate | on |  |  |  |
| `tengu_attempt_decision_shadow` | gate | off |  |  |  |
| `tengu_auto_mode_config` | config |  | Gates “auto mode” availability, with circuit-breaker disable plus model and org allowlist checks. | Also respects user settings (disableAutoMode) and can disable fast mode. | high |
| `tengu_auto_mode_worktree_fast_path` | gate | off |  |  |  |
| `tengu_basalt_meadow` | gate | off |  |  |  |
| `tengu_basalt_scarp` | gate | off |  |  |  |
| `tengu_basalt_spur` | gate | off |  |  |  |
| `tengu_belated_wren` | gate | off |  |  |  |
| `tengu_bg_attach_stall_ms` | config |  |  |  |  |
| `tengu_bg_attach_upgrade` | gate | on |  |  |  |
| `tengu_bg_binary_takeover` | gate | on |  |  |  |
| `tengu_bg_classifier_config` | config |  |  |  |  |
| `tengu_bg_gateway_mark` | gate | on |  |  |  |
| `tengu_bg_leftarrow_inprocess` | gate | on |  |  |  |
| `tengu_bg_low_mem_mb` | config | 1024 |  |  |  |
| `tengu_bg_prewarm_burst_concurrency` | config | 3 |  |  |  |
| `tengu_bg_prewarm_burst_delay_ms` | config | 15000 |  |  |  |
| `tengu_bg_prewarm_per_sweep` | config | 3 |  |  |  |
| `tengu_bg_revival_guard` | gate | on |  |  |  |
| `tengu_bg_settled_crash_restart` | gate | on |  |  |  |
| `tengu_bg_spare_enable` | gate | on |  |  |  |
| `tengu_bg_worker_ctty` | gate | on |  |  |  |
| `tengu_binary_reef` | gate | off |  |  |  |
| `tengu_birch_kettle` | gate | off |  |  |  |
| `tengu_birch_lantern` | config | "off" |  |  |  |
| `tengu_bracken_sluice` | gate | off |  |  |  |
| `tengu_bramble_lintel` | config |  |  |  |  |
| `tengu_brass_plover` | gate | on |  |  |  |
| `tengu_brass_sled` | gate | off |  |  |  |
| `tengu_breezy_acorn` | gate | on |  |  |  |
| `tengu_breezy_blanket` | gate | on |  |  |  |
| `tengu_breezy_crescent` | gate | on |  |  |  |
| `tengu_breezy_cupcake` | gate | off |  |  |  |
| `tengu_breezy_diffie` | gate | on |  |  |  |
| `tengu_breezy_fairy` | gate | off |  |  |  |
| `tengu_breezy_haven` | gate | on |  |  |  |
| `tengu_breezy_wolf` | config | "" |  |  |  |
| `tengu_brick_follow` | gate | off |  |  |  |
| `tengu_bridge_apply_server_session_config` | gate | on |  |  |  |
| `tengu_bridge_auth_revive` | gate | on |  |  |  |
| `tengu_bridge_child_auto_mode` | gate | on |  |  |  |
| `tengu_bridge_child_auto_over_settings` | gate | on |  |  |  |
| `tengu_bridge_child_file_upload` | gate | on |  |  |  |
| `tengu_bridge_child_machine_settings` | gate | on |  |  |  |
| `tengu_bridge_child_tool_diff` | gate | on |  |  |  |
| `tengu_bridge_host_declined_end` | gate | on |  |  |  |
| `tengu_bridge_host_profile` | config | "off" |  |  |  |
| `tengu_bridge_inbox_pointer_boundary` | gate | on |  |  |  |
| `tengu_bridge_initialize_commands` | gate | off |  |  |  |
| `tengu_bridge_leave_silent_pool_off` | gate | off |  |  |  |
| `tengu_bridge_min_version` | config |  | Blocks Remote Control when Claude Code is below a configured minimum version. |  | high |
| `tengu_bridge_owner_check_attribution` | gate | on |  |  |  |
| `tengu_bridge_owner_pinned_end` | gate | on |  |  |  |
| `tengu_bridge_partial_messages` | gate | off |  |  |  |
| `tengu_bridge_placeholder_sweep` | gate | on |  |  |  |
| `tengu_bridge_poll_interval_config` | config |  | Sets Tengu bridge poll interval (0 disables) plus session reclaim and keepalive timings. | Config is schema-validated; invalid values fall back to defaults. | medium |
| `tengu_bridge_rc_child_artifact` | gate | on |  |  |  |
| `tengu_bridge_rc_child_auto_compact` | gate | on |  |  |  |
| `tengu_bridge_rc_child_idle_exit_ms` | config |  |  |  |  |
| `tengu_bridge_rc_child_restart_resume` | gate | on |  |  |  |
| `tengu_bridge_rc_projects_hint` | gate | on |  |  |  |
| `tengu_bridge_recovery_patience` | gate | on |  |  |  |
| `tengu_bridge_repl_v2_config` | config |  |  |  |  |
| `tengu_bridge_repl_v2_cse_shim_enabled` | gate | on |  |  |  |
| `tengu_bridge_requires_action_details` | gate | on |  |  |  |
| `tengu_bridge_resume_respects_local_owner` | gate | on |  |  |  |
| `tengu_bridge_selfheal_heartbeats` | gate | on |  |  |  |
| `tengu_bridge_signed_out_neutral` | gate | on |  |  |  |
| `tengu_bridge_subagent_frames` | gate | on |  |  |  |
| `tengu_bridge_subagent_text` | gate | off |  |  |  |
| `tengu_bridge_unarchive_on_resume` | gate | on |  |  |  |
| `tengu_bright_kettle` | config |  |  |  |  |
| `tengu_bright_wall` | gate | on |  |  |  |
| `tengu_brimming_kettle` | config | 0 |  |  |  |
| `tengu_brindle_otter` | gate | off |  |  |  |
| `tengu_brisk_acorn` | config | 0 |  |  |  |
| `tengu_bubbly_gadget` | gate | off |  |  |  |
| `tengu_bubbly_harbor` | gate | on |  |  |  |
| `tengu_bubbly_meteor` | gate | on |  |  |  |
| `tengu_byte_stream_idle_timeout_ms` | config |  |  |  |  |
| `tengu_c4e_slash_upsell` | gate | off |  |  |  |
| `tengu_calm_jellyfish` | gate | on |  |  |  |
| `tengu_calm_noodle` | gate | on |  |  |  |
| `tengu_calm_osprey` | gate | on |  |  |  |
| `tengu_calm_riddle` | gate | on |  |  |  |
| `tengu_calm_seal` | config |  |  |  |  |
| `tengu_calm_waffle` | gate | off |  |  |  |
| `tengu_calm_whale` | gate | on |  |  |  |
| `tengu_canary` | config |  |  |  |  |
| `tengu_candid_heron` | gate | on |  |  |  |
| `tengu_candid_lantern` | gate | off |  |  |  |
| `tengu_candid_ledger` | gate | off |  |  |  |
| `tengu_ccr_bridge` | gate |  | Enables the Tengu CCR bridge for Claude Code, with an optional minimum bridge version check. | Only gate checks and a min-version config are visible; what the bridge does beyond enabling is not shown. | medium |
| `tengu_ccr_bundle_max_bytes` | config |  |  |  |  |
| `tengu_ccr_bundle_seed_enabled` | gate |  | Enables seeding a CCR bundle for remote sessions when repo/env gate is set | Also influenced by CCR_FORCE_BUNDLE and CCR_ENABLE_BUNDLE env vars and various git/GitHub checks. | high |
| `tengu_ccr_classifier_keepalive_enabled` | gate | off |  |  |  |
| `tengu_ccr_drop_unwatched_stream_events` | gate | off |  |  |  |
| `tengu_ccr_exclude_dynamic_restore_killswitch` | gate | off |  |  |  |
| `tengu_ccr_external_event_record` | gate | off |  |  |  |
| `tengu_ccr_handoff_metadata` | gate | off |  |  |  |
| `tengu_ccr_hook_keepalive_enabled` | gate | off |  |  |  |
| `tengu_ccr_idle_heartbeat` | gate | off |  |  |  |
| `tengu_ccr_no_subscriber_flush_ms` | config | 0 |  |  |  |
| `tengu_ccr_no_subscriber_hold_ms` | config | 0 |  |  |  |
| `tengu_ccr_orphan_restore_wake` | gate | on |  |  |  |
| `tengu_ccr_orphan_restore_wake_shells` | gate | on |  |  |  |
| `tengu_ccr_reactivation_beat` | gate | off |  |  |  |
| `tengu_ccr_reconnect_beat` | gate | off |  |  |  |
| `tengu_ccr_restate_open_block` | gate | off |  |  |  |
| `tengu_ccr_skip_redundant_heartbeat` | gate | off |  |  |  |
| `tengu_ccr_sse_keepalive_max_interval_s` | config | 0 |  |  |  |
| `tengu_ccr_sse_long_poll_fallback` | gate | on |  |  |  |
| `tengu_ccr_stream_event_flush_ms` | config |  |  |  |  |
| `tengu_ccr_stream_first_flush_ms` | config | 0 |  |  |  |
| `tengu_ccr_subagent_skip_on_delta` | gate | off |  |  |  |
| `tengu_ccr_upload_hold_marker` | gate | off |  |  |  |
| `tengu_ccr_upload_trim` | config |  |  |  |  |
| `tengu_ccr_v2_bridge_create_cli` | gate | off |  |  |  |
| `tengu_ccr_v2_send_events_cli` | gate | on |  |  |  |
| `tengu_ccr_v2_session_crud_cli` | gate | off |  |  |  |
| `tengu_cedar_lantern` | gate | on |  |  |  |
| `tengu_cedar_lattice` | gate | off |  |  |  |
| `tengu_cedar_plume` | gate | off |  |  |  |
| `tengu_cheeky_gizmo` | gate | on | Filters MCP template completion values to drop entries containing hidden characters. | Only affects MCP template completion results; it logs when values are left out for "hidden characters". | high |
| `tengu_cheerful_horizon` | gate | off |  |  |  |
| `tengu_cheerful_lighthouse` | config |  |  |  |  |
| `tengu_cheerful_orbit` | gate | off |  |  |  |
| `tengu_chomp_inflection` | gate | off |  |  |  |
| `tengu_chomp_sable` | gate | off |  |  |  |
| `tengu_chomp_thaw` | gate | off |  |  |  |
| `tengu_chrome_auto_enable` | gate | off | Auto-enable Claude-in-Chrome native host integration via MCP stdio config. | Based on nearby native-host/MCP strings; exact behavior inferred. | medium |
| `tengu_chrome_install_upsell` | gate | off |  |  |  |
| `tengu_chrome_tab_group_close` | gate | on |  |  |  |
| `tengu_cicada_nap_ms` | config | 0 |  |  |  |
| `tengu_cinder_plover` | config | "" |  |  |  |
| `tengu_classifier_disabled_surfaces` | config | "" |  |  |  |
| `tengu_classifier_summary_kill` | gate | off |  |  |  |
| `tengu_classifier_summary_llm_emit` | gate | off |  |  |  |
| `tengu_clever_fern` | gate | off |  |  |  |
| `tengu_clever_hippo` | gate | off |  |  |  |
| `tengu_clever_nebula` | gate | on |  |  |  |
| `tengu_clever_orbit` | gate | off |  |  |  |
| `tengu_clever_pillow` | gate | on |  |  |  |
| `tengu_cloud_delete_unused` | gate | off |  |  |  |
| `tengu_cloud_session_shell` | gate | off |  |  |  |
| `tengu_cobalt_harbor` | gate | off |  |  |  |
| `tengu_cobalt_harbor_notice` | gate | on |  |  |  |
| `tengu_cobalt_plinth` | config |  |  |  |  |
| `tengu_cobalt_plinth_alder` | gate | off |  |  |  |
| `tengu_cobalt_plinth_aspen` | gate | off |  |  |  |
| `tengu_cobalt_plinth_campion` | gate | off |  |  |  |
| `tengu_cobalt_plinth_damson` | gate | off |  |  |  |
| `tengu_cobalt_plinth_dataviz` | gate | off |  |  |  |
| `tengu_cobalt_plinth_fennel` | gate | off |  |  |  |
| `tengu_cobalt_plinth_fern` | gate | on |  |  |  |
| `tengu_cobalt_plinth_mallow` | gate | off |  |  |  |
| `tengu_cobalt_plinth_moss` | gate | on |  |  |  |
| `tengu_cobalt_plinth_sainfoin` | gate | off |  |  |  |
| `tengu_cobalt_plinth_samphire` | gate | off |  |  |  |
| `tengu_cobalt_plinth_sedge` | gate | off |  |  |  |
| `tengu_cobalt_plinth_sill` | config |  |  |  |  |
| `tengu_cobalt_plinth_sorb` | gate | off |  |  |  |
| `tengu_cobalt_plinth_sorrel` | gate | on |  |  |  |
| `tengu_cobalt_plinth_tansy` | gate | off |  |  |  |
| `tengu_cobalt_plinth_thrift` | gate | off |  |  |  |
| `tengu_cobalt_plinth_whin` | gate | off |  |  |  |
| `tengu_cobalt_plinth_willow` | gate | off |  |  |  |
| `tengu_cobalt_plinth_yew` | gate | off |  |  |  |
| `tengu_cobalt_ridge` | gate | off |  |  |  |
| `tengu_cobalt_thicket` | gate | on |  |  |  |
| `tengu_cobalt_wren` | gate | off |  |  |  |
| `tengu_compact_cache_prefix` | gate | on | Enable cache-sharing path for conversation compaction summaries using prefixed cache keys | Exact cache prefix behavior not shown; inferred from logs and naming. | high |
| `tengu_compiled_sprout` | gate | on |  |  |  |
| `tengu_composed_quail` | gate | on |  |  |  |
| `tengu_compressed_marshmallow` | gate | off |  |  |  |
| `tengu_compressed_river` | gate | on |  |  |  |
| `tengu_concurrent_lake` | gate | off |  |  |  |
| `tengu_concurrent_moonbeam` | gate | off |  |  |  |
| `tengu_concurrent_shore` | gate | on |  |  |  |
| `tengu_context_usage_bulk_counts` | gate | off |  |  |  |
| `tengu_copper_hinge_wren` | gate | off |  |  |  |
| `tengu_copper_kestrel` | gate | on |  |  |  |
| `tengu_copper_lantern` | gate | off |  |  |  |
| `tengu_copper_thistle` | gate | off |  |  |  |
| `tengu_coral_anchor` | gate | on |  |  |  |
| `tengu_cosmic_cookie` | gate | off |  |  |  |
| `tengu_cosmic_nautilus` | gate | on |  |  |  |
| `tengu_cosmic_shore` | gate | on |  |  |  |
| `tengu_cowork_auto_mode_include_allowed_write_mcp` | config |  |  |  |  |
| `tengu_cowork_chrome_automode_default` | gate | off |  |  |  |
| `tengu_cozy_babbage` | gate | on |  |  |  |
| `tengu_cozy_dusk` | config |  |  |  |  |
| `tengu_cozy_eagle` | gate | on |  |  |  |
| `tengu_cozy_fern` | gate | off |  |  |  |
| `tengu_cozy_hamming` | gate | off |  |  |  |
| `tengu_cozy_kite` | gate | off |  |  |  |
| `tengu_cozy_sparkle` | gate | off |  |  |  |
| `tengu_crimson_vector` | gate | off |  |  |  |
| `tengu_crispy_flame` | gate | off |  |  |  |
| `tengu_crispy_glade` | config | 0 |  |  |  |
| `tengu_crispy_turtle` | gate | on |  |  |  |
| `tengu_cryptic_sprout` | gate | off |  |  |  |
| `tengu_crystalline_phoenix` | gate | on |  |  |  |
| `tengu_cuddly_cascade` | gate | off | Send bridge results for dropped prompts (aborted_streaming, droppedPrompt:true) and set tellsDropped. | Only runs when a bridge host exists and the engine isn't active or externally loading. | high |
| `tengu_cuddly_swing` | gate | on |  |  |  |
| `tengu_cuddly_willow` | gate | on |  |  |  |
| `tengu_curious_canyon` | gate | off |  |  |  |
| `tengu_curious_river` | config |  |  |  |  |
| `tengu_curious_rivest` | config |  |  |  |  |
| `tengu_curious_tower` | gate | off |  |  |  |
| `tengu_curious_tower_stateless_models` | config | "" |  |  |  |
| `tengu_curried_neumann` | gate | off |  |  |  |
| `tengu_curried_shore` | config | 0 |  |  |  |
| `tengu_curried_sparrow` | gate | off |  |  |  |
| `tengu_daemon_refuse_stale_upgrade` | gate | on |  |  |  |
| `tengu_daemon_upgrade_defer_busy` | gate | on |  |  |  |
| `tengu_dapper_acorn` | gate | off |  |  |  |
| `tengu_dapper_brooks` | gate | off |  |  |  |
| `tengu_dapper_cupcake` | gate | on |  |  |  |
| `tengu_dapper_dawn` | gate | off |  |  |  |
| `tengu_dapper_fountain` | gate | on |  |  |  |
| `tengu_dapper_platypus` | gate | off |  |  |  |
| `tengu_dazzling_garden` | gate | on |  |  |  |
| `tengu_declarative_hippo` | gate | on |  |  |  |
| `tengu_deep_feather` | gate | on |  |  |  |
| `tengu_deep_lemur` | gate | on |  |  |  |
| `tengu_deep_plum` | gate | on |  |  |  |
| `tengu_defer_cap_ms` | config |  |  |  |  |
| `tengu_deferred_stub_tool` | gate | on |  |  |  |
| `tengu_delightful_hamster` | gate | off |  |  |  |
| `tengu_desktop_card_message_approval` | gate | on |  |  |  |
| `tengu_desktop_upsell` | config |  | Enables a startup dialog upsell for a desktop app on macOS or Windows x64. | Gate appears limited to darwin/win32 x64 and checks an enable_startup_dialog setting. | medium |
| `tengu_destructive_command_warning` | gate | off |  |  |  |
| `tengu_disable_live_host_context` | gate | off |  |  |  |
| `tengu_disable_streaming_to_non_streaming_fallback` | gate | off |  |  |  |
| `tengu_distant_bell` | gate | off |  |  |  |
| `tengu_distributed_adleman` | gate | on |  |  |  |
| `tengu_dreamy_flute` | gate | off |  |  |  |
| `tengu_dreamy_frost` | gate | off |  |  |  |
| `tengu_dreamy_reef` | gate | on |  |  |  |
| `tengu_dreamy_sunbeam` | gate | on |  |  |  |
| `tengu_dreamy_sundae` | gate | on |  |  |  |
| `tengu_drift_lantern` | gate | off |  |  |  |
| `tengu_drifting_dream` | gate | off |  |  |  |
| `tengu_dusky_finch` | gate | off |  |  |  |
| `tengu_eager_eagle` | gate | on |  |  |  |
| `tengu_eager_fiddle` | gate | off |  |  |  |
| `tengu_eager_hare` | gate | off |  |  |  |
| `tengu_eager_kazoo` | gate | off |  |  |  |
| `tengu_eager_pillow` | gate | on |  |  |  |
| `tengu_eager_quilt` | gate | off |  |  |  |
| `tengu_eager_rain` | gate | on |  |  |  |
| `tengu_eager_reef` | gate | off |  |  |  |
| `tengu_eager_tiger` | gate | on | Enables the code path that triggers a computer-use "relaunch" instead of refusing a "computeruse_restart". | Only applies when there’s no agentId and the session input/stash are empty (plus other restart eligibility checks). | high |
| `tengu_elegant_breeze` | gate | on | When ANTHROPIC_BASE_URL points to a non‑Anthropic host, it turns off Message Threads for this session and warns that each request sends the full conversation. | Only applies when tetherLiveGate is enabled and CLAUDE_CODE_TETHER_LIVE is not true. | high |
| `tengu_elegant_forest` | gate | off |  |  |  |
| `tengu_elegant_meadow` | gate | on |  |  |  |
| `tengu_elegant_mist` | config | "off" |  |  |  |
| `tengu_elegant_pancake` | config |  |  |  |  |
| `tengu_elegant_puppy` | gate | off |  |  |  |
| `tengu_elegant_whale` | gate | off |  |  |  |
| `tengu_ember_latch` | gate | off |  |  |  |
| `tengu_encapsulated_pebble` | gate | on |  |  |  |
| `tengu_encapsulated_sphinx` | gate | off |  |  |  |
| `tengu_enchanted_leaf` | config | 0 |  |  |  |
| `tengu_enumerated_snowflake` | gate | off |  |  |  |
| `tengu_ethereal_curry` | gate | on |  |  |  |
| `tengu_ethereal_mist` | gate | on |  |  |  |
| `tengu_event_loop_stall` | gate | off |  |  |  |
| `tengu_eventual_noodle` | gate | off |  |  |  |
| `tengu_expressive_quail` | gate | off |  |  |  |
| `tengu_expressive_whistle` | gate | off |  |  |  |
| `tengu_fancy_wand_copy` | config |  |  |  |  |
| `tengu_federated_flask` | gate | off |  |  |  |
| `tengu_federated_petal` | gate | on |  |  |  |
| `tengu_feedback_survey_config` | config |  | Settings for displaying a feedback survey and recording appeared/responded outcomes (good/bad). | Context shows error handling and fallback IDs like "unknown" when config/session data is missing. | medium |
| `tengu_fern_plover` | config |  |  |  |  |
| `tengu_fgts` | config |  |  |  |  |
| `tengu_fizzy_adleman` | gate | off |  |  |  |
| `tengu_fizzy_grove` | gate | off |  |  |  |
| `tengu_fizzy_panda` | gate | off |  |  |  |
| `tengu_fizzy_treasure` | gate | on |  |  |  |
| `tengu_fleet_past_sessions` | gate | off |  |  |  |
| `tengu_flickering_lagoon` | gate | off |  |  |  |
| `tengu_flickering_nest` | gate | off |  |  |  |
| `tengu_flint_harbor_prompt` | config |  |  |  |  |
| `tengu_floating_steele` | config | 0 |  |  |  |
| `tengu_floating_valley` | gate | off |  |  |  |
| `tengu_floating_waffle` | gate | off |  |  |  |
| `tengu_fluffy_wren` | gate | off |  |  |  |
| `tengu_fluttering_planet` | gate | off | Uses alternate “Claude in Chrome” tool responses during the “switched_off_not_linked”/enable-link flow. | Only affects output from the “Claude in Chrome” enable-stub tool (and its link-waiting helper). | medium |
| `tengu_foamy_pond` | gate | off |  |  |  |
| `tengu_foamy_treehouse` | gate | off |  |  |  |
| `tengu_folded_sail` | gate | off |  |  |  |
| `tengu_framed_osprey` | gate | off |  |  |  |
| `tengu_fresh_heron` | config |  |  |  |  |
| `tengu_functional_island` | gate | off |  |  |  |
| `tengu_fuzzy_oasis` | gate | off |  |  |  |
| `tengu_fuzzy_pond` | gate | off |  |  |  |
| `tengu_fuzzy_quilt` | config | 0 |  |  |  |
| `tengu_fuzzy_teapot` | gate | off |  |  |  |
| `tengu_gb_refresh_interval_minutes` | config |  |  |  |  |
| `tengu_generic_ember` | gate | off |  |  |  |
| `tengu_generic_papert` | config |  |  |  |  |
| `tengu_generic_yao` | gate | on |  |  |  |
| `tengu_gentle_anchor` | gate | on |  |  |  |
| `tengu_gentle_brooks` | gate | on |  |  |  |
| `tengu_gentle_hummingbird` | gate | on |  |  |  |
| `tengu_gentle_ocean` | gate | off |  |  |  |
| `tengu_gentle_orchard` | gate | on |  |  |  |
| `tengu_gentle_sky` | gate | off |  |  |  |
| `tengu_gentle_sphinx` | gate | on |  |  |  |
| `tengu_giggly_dragonfly` | gate | on |  |  |  |
| `tengu_giggly_nygaard` | gate | off |  |  |  |
| `tengu_gleaming_fair_reuse` | gate | off |  |  |  |
| `tengu_gleaming_spring` | gate | off |  |  |  |
| `tengu_glimmering_firefly` | gate | off |  |  |  |
| `tengu_glimmering_glade` | gate | on |  |  |  |
| `tengu_glistening_mountain` | gate | off |  |  |  |
| `tengu_glistening_snowglobe` | gate | off |  |  |  |
| `tengu_glittery_mitten` | gate | on |  |  |  |
| `tengu_glowing_lark` | config |  |  |  |  |
| `tengu_glowing_pancake` | gate | off |  |  |  |
| `tengu_golden_bird` | gate | off |  |  |  |
| `tengu_golden_thunder` | gate | off |  |  |  |
| `tengu_golden_wirth` | gate | off |  |  |  |
| `tengu_goofy_moonbeam` | gate | off |  |  |  |
| `tengu_gorse_fathom` | gate | off |  |  |  |
| `tengu_gorse_pylon` | gate | off |  |  |  |
| `tengu_gorse_sill` | gate | off |  |  |  |
| `tengu_graceful_cake` | gate | on |  |  |  |
| `tengu_graceful_pudding` | gate | on |  |  |  |
| `tengu_graceful_quilt` | config |  |  |  |  |
| `tengu_gravel_chorus` | gate | on |  |  |  |
| `tengu_greedy_crane` | gate | on |  |  |  |
| `tengu_groovy_dongarra` | config |  |  |  |  |
| `tengu_groovy_eclipse` | gate | off |  |  |  |
| `tengu_gypsum_kite` | gate | off |  |  |  |
| `tengu_happy_ocean` | gate | off |  |  |  |
| `tengu_happy_thimble` | gate | off |  |  |  |
| `tengu_harbor` | gate | off | Gate controlling onboarding/opt-in flows and channel access including Claude AI OAuth token checks | Also influences UI dialogs (Onboarding, Trust, AutoMode opt-in) and a channel allowlist; not all behavior is fully visible. | medium |
| `tengu_harbor_kite` | gate | on |  |  |  |
| `tengu_harbor_kite_limits` | config |  |  |  |  |
| `tengu_harbor_kite_mode_emit` | gate | on |  |  |  |
| `tengu_harbor_kite_pacing_off` | gate | off |  |  |  |
| `tengu_harbor_kite_win` | gate | on |  |  |  |
| `tengu_harbor_ledger` | config |  |  |  |  |
| `tengu_harbor_moth` | gate | off |  |  |  |
| `tengu_harbor_permissions` | gate | off |  |  |  |
| `tengu_harbor_willow` | gate | on |  |  |  |
| `tengu_harmonic_truffle` | gate | off |  |  |  |
| `tengu_harp_pedal` | gate | on |  |  |  |
| `tengu_hashed_lagoon` | config | 0 |  |  |  |
| `tengu_hawthorn_steeple` | gate | off |  |  |  |
| `tengu_haze_glass` | gate | off |  |  |  |
| `tengu_hazel_lantern` | config | 0 |  |  |  |
| `tengu_hazel_osprey` | gate | off |  |  |  |
| `tengu_hazel_osprey_floor` | config |  |  |  |  |
| `tengu_hazy_boole` | gate | off |  |  |  |
| `tengu_hazy_cosmos` | gate | on |  |  |  |
| `tengu_hazy_elephant` | gate | off |  |  |  |
| `tengu_hazy_horizon` | gate | off |  |  |  |
| `tengu_hazy_noodle` | config | 0 |  |  |  |
| `tengu_hazy_nova` | gate | off |  |  |  |
| `tengu_hazy_origami` | gate | on |  |  |  |
| `tengu_hazy_possum` | gate | on |  |  |  |
| `tengu_hazy_prism` | gate | off |  |  |  |
| `tengu_hearth_member_relay_rows_enabled` | gate | off |  |  |  |
| `tengu_hearth_resolved_rows` | config |  |  |  |  |
| `tengu_heron_brook` | config | "" |  |  |  |
| `tengu_hidden_frog` | gate | on |  |  |  |
| `tengu_hidden_rain` | gate | off |  |  |  |
| `tengu_hidden_volcano` | config |  |  |  |  |
| `tengu_hipaa_history_retention_prune` | gate | on |  |  |  |
| `tengu_hover_rest` | gate | off |  |  |  |
| `tengu_humble_emerson` | gate | on |  |  |  |
| `tengu_humble_petal` | gate | on |  |  |  |
| `tengu_humble_wand` | gate | on |  |  |  |
| `tengu_humble_zephyr` | gate | off |  |  |  |
| `tengu_humming_locket` | gate | on |  |  |  |
| `tengu_humming_mountain` | gate | off |  |  |  |
| `tengu_humming_star` | gate | on |  |  |  |
| `tengu_humming_tiger` | config |  |  |  |  |
| `tengu_humming_waterfall` | gate | off |  |  |  |
| `tengu_hushed_kestrel` | gate | on |  |  |  |
| `tengu_hushed_lantern` | gate | on |  |  |  |
| `tengu_hushed_lark` | config |  |  |  |  |
| `tengu_hushed_lark_text` | config |  |  |  |  |
| `tengu_hushed_plover` | gate | on |  |  |  |
| `tengu_ide_rc_auto_enable` | gate | off |  |  |  |
| `tengu_idempotent_wolf` | gate | on |  |  |  |
| `tengu_idle_amber_finch` | gate | off |  |  |  |
| `tengu_immutable_tide` | config | 0 |  |  |  |
| `tengu_import` | gate | off |  |  |  |
| `tengu_indexed_corbato` | gate | off |  |  |  |
| `tengu_indexed_nautilus` | gate | off |  |  |  |
| `tengu_indexed_pearl` | config |  |  |  |  |
| `tengu_indexed_salamander` | gate | off |  |  |  |
| `tengu_inked_lantern` | gate | off |  |  |  |
| `tengu_iridescent_boot` | gate | on |  |  |  |
| `tengu_iridescent_quail` | gate | off |  |  |  |
| `tengu_iterative_aurora` | gate | off |  |  |  |
| `tengu_iterative_cosmos` | gate | on |  |  |  |
| `tengu_iterative_falcon` | gate | on |  |  |  |
| `tengu_iterative_haven` | gate | off |  |  |  |
| `tengu_iterative_lightning` | gate | off |  |  |  |
| `tengu_jade_anvil_4` | gate | off |  |  |  |
| `tengu_jade_compass` | gate | on |  |  |  |
| `tengu_jaunty_charm` | config |  |  |  |  |
| `tengu_jaunty_deer` | gate | on |  |  |  |
| `tengu_jaunty_ember` | gate | off |  |  |  |
| `tengu_jazzy_corbato` | gate | on |  |  |  |
| `tengu_jazzy_puddle` | gate | on |  |  |  |
| `tengu_jazzy_wren` | gate | on |  |  |  |
| `tengu_jiggly_mochi` | gate | off |  |  |  |
| `tengu_jolly_bee` | config | 0 |  |  |  |
| `tengu_jolly_candy` | config | 0 |  |  |  |
| `tengu_jolly_leaf` | gate | off |  |  |  |
| `tengu_joyful_willow` | gate | off |  |  |  |
| `tengu_juniper_bassoon` | gate | off |  |  |  |
| `tengu_juniper_relay` | gate | off |  |  |  |
| `tengu_juniper_relay_config` | config |  |  |  |  |
| `tengu_juniper_sundial` | config |  |  |  |  |
| `tengu_kairos_brief` | gate | off | Enables a “brief” user message/tool (markdown) when entitled or CLAUDE_CODE_BRIEF is set. | Gated by an entitlement check plus another condition (By()\|\|kZ()). | medium |
| `tengu_kairos_brief_config` | config |  |  |  |  |
| `tengu_kairos_brief_stop_hook_text` | config | "" |  |  |  |
| `tengu_kairos_cron` | gate | on | Enables session-only cron tools to schedule prompts to run later or on a recurring schedule. | Disabled when CLAUDE_CODE_DISABLE_CRON is set. | high |
| `tengu_kairos_cron_config` | config |  | Configures cron scheduling jitter/recurrence limits for a background job runner. | Only schema and accessor names are visible; the specific jobs affected aren’t shown. | medium |
| `tengu_kairos_cron_durable` | gate | on | Controls whether scheduled prompts are persisted to .claude/scheduled_tasks.json (durable vs session-only). | Set durable: true to write to disk; otherwise schedules are session-only. | high |
| `tengu_kairos_input_needed_push` | gate | off |  |  |  |
| `tengu_kairos_loop_keepalive` | gate | off |  |  |  |
| `tengu_kairos_loop_persistent` | gate | off |  |  |  |
| `tengu_kairos_push_notifications` | gate | off | Enables the PushNotification tool to notify users in-terminal and, with Remote Control, on mobile. | Also checks an agent setting (agentPushNotifEnabled) before allowing mobile push. | high |
| `tengu_kairos_ready_nudge` | config |  |  |  |  |
| `tengu_keen_garden` | gate | on |  |  |  |
| `tengu_keen_lantern` | gate | on |  |  |  |
| `tengu_keen_sloth` | gate | on |  |  |  |
| `tengu_keen_umbrella` | gate | off |  |  |  |
| `tengu_kestrel_moor` | gate | on |  |  |  |
| `tengu_keybinding_customization_release` | gate | on | Controls rollout of keybinding customization functionality | Only a simple boolean gate; behavior beyond name is unclear. | medium |
| `tengu_kind_barto` | gate | on |  |  |  |
| `tengu_kind_puzzle` | gate | off |  |  |  |
| `tengu_lantern_hinge` | gate | off |  |  |  |
| `tengu_lantern_prism` | gate | off |  |  |  |
| `tengu_lantern_sconce` | gate | off |  |  |  |
| `tengu_lantern_sconce_copy` | config |  |  |  |  |
| `tengu_lantern_snuffer` | gate | off |  |  |  |
| `tengu_lantern_spool` | gate | off |  |  |  |
| `tengu_lazy_dove` | gate | off |  |  |  |
| `tengu_lazy_ladybug` | gate | on |  |  |  |
| `tengu_lazy_spindle` | gate | off |  |  |  |
| `tengu_left_arrow_carries_queued` | gate | on |  |  |  |
| `tengu_level_dunlin` | gate | on |  |  |  |
| `tengu_level_wren` | gate | on |  |  |  |
| `tengu_lexical_cupcake` | config |  |  |  |  |
| `tengu_lexical_glade` | gate | off |  |  |  |
| `tengu_linear_brook` | gate | on |  |  |  |
| `tengu_linear_fog` | config | "off" |  |  |  |
| `tengu_linear_owl` | gate | off |  |  |  |
| `tengu_linear_quail` | config | 0 |  |  |  |
| `tengu_linen_orbit` | gate | off |  |  |  |
| `tengu_linked_clover` | gate | on |  |  |  |
| `tengu_linked_rose` | gate | on |  |  |  |
| `tengu_linked_shore` | config |  |  |  |  |
| `tengu_lively_crown` | config | "off" |  |  |  |
| `tengu_lively_waffle` | gate | on |  |  |  |
| `tengu_loggia_denkbild` | gate | off |  |  |  |
| `tengu_logical_pillow` | gate | off |  |  |  |
| `tengu_lovely_locket` | gate | off |  |  |  |
| `tengu_lovely_orbit` | gate | on | Allows fetching and caching served catalog “member_programs” and “.badges.json” program badges in the cc CLI. | Only applies when U0()=="cc", running in the "cli", and the active auth is OAuth (otherwise oSr() returns null). | medium |
| `tengu_lovely_rain` | gate | off |  |  |  |
| `tengu_lucid_anchor` | config |  |  |  |  |
| `tengu_lucid_bittern` | gate | off |  |  |  |
| `tengu_lucky_brooks` | gate | off |  |  |  |
| `tengu_lucky_lemur` | gate | off |  |  |  |
| `tengu_lucky_nebula` | gate | off |  |  |  |
| `tengu_lucky_quill` | gate | on |  |  |  |
| `tengu_lucky_tarjan` | gate | on |  |  |  |
| `tengu_luminous_codd` | gate | off |  |  |  |
| `tengu_luminous_locket` | config |  |  |  |  |
| `tengu_luminous_seal` | gate | on |  |  |  |
| `tengu_luminous_truffle` | gate | off |  |  |  |
| `tengu_magical_clock` | config |  |  |  |  |
| `tengu_magical_pixel` | gate | off |  |  |  |
| `tengu_malort_pedway` | config |  | Enables a “Chicago” UI feature (with coordinateMode) only for max/pro tiers. | Flag name is opaque; behavior inferred from exported getters and hotkey usage nearby. | medium |
| `tengu_maple_pier` | gate | on |  |  |  |
| `tengu_maple_rung` | gate | off |  |  |  |
| `tengu_maple_sundial` | gate | off |  |  |  |
| `tengu_marbled_teal` | gate | off |  |  |  |
| `tengu_max_version_config` | config |  | Minimum-version config used to block applying an update when the target version is too old. | Config also exposes optional `external` and `external_message` fields, likely for update messaging. | medium |
| `tengu_mcp_auto_background` | gate | on |  |  |  |
| `tengu_mcp_claudeai_eligibility_gate` | gate | off |  |  |  |
| `tengu_mcp_connect_suspend_redial` | gate | on |  |  |  |
| `tengu_mcp_connect_timeout_retry` | gate | on |  |  |  |
| `tengu_mcp_directory_visibility` | config |  |  |  |  |
| `tengu_mcp_discover_projection_prior` | config | "off" |  |  |  |
| `tengu_mcp_discovery_cache_enable` | config |  |  |  |  |
| `tengu_mcp_issuer_strict_echo` | gate | off |  |  |  |
| `tengu_mcp_legacy_sse_fallback` | gate | on |  |  |  |
| `tengu_mcp_legacy_url_elicitation` | gate | on |  |  |  |
| `tengu_mcp_listen_reopen_park` | gate | on |  |  |  |
| `tengu_mcp_listen_reopen_park_tuning` | config |  |  |  |  |
| `tengu_mcp_local_oauth_blocked_hosts` | config |  |  |  |  |
| `tengu_mcp_protocol_negotiation_ccr` | gate | on |  |  |  |
| `tengu_mcp_protocol_negotiation_claudeai` | gate | on |  |  |  |
| `tengu_mcp_protocol_negotiation_http` | gate | on |  |  |  |
| `tengu_mcp_protocol_negotiation_stdio` | gate | on |  |  |  |
| `tengu_mcp_proxy_needs_approval_retry` | gate | on |  |  |  |
| `tengu_mcp_server_policy_bypass_exempt` | gate | on |  |  |  |
| `tengu_mcp_signed_out_fallback` | gate | on |  |  |  |
| `tengu_mcp_singleton_unwrap` | gate | on |  |  |  |
| `tengu_mcp_startup_policy_seed` | gate | on |  |  |  |
| `tengu_mcp_stateless_skip_init` | gate | on |  |  |  |
| `tengu_mcp_step_up_auth_dialog` | gate | on |  |  |  |
| `tengu_mcp_strip_trailing_xml_tags` | gate | off |  |  |  |
| `tengu_mcp_subagent_prompt` | gate | off |  |  |  |
| `tengu_mcp_task_worker_wake` | gate | off |  |  |  |
| `tengu_mcp_url_elicitation` | gate | on |  |  |  |
| `tengu_mellow_badger` | config | 0 |  |  |  |
| `tengu_mellow_beacon` | gate | off |  |  |  |
| `tengu_mellow_ember` | gate | off |  |  |  |
| `tengu_mellow_kestrel` | gate | off |  |  |  |
| `tengu_mellow_minsky` | gate | on |  |  |  |
| `tengu_mellow_petal` | gate | on |  |  |  |
| `tengu_mellow_pulse` | gate | on |  |  |  |
| `tengu_mellow_sunset` | gate | on |  |  |  |
| `tengu_mellow_thistle` | gate | off |  |  |  |
| `tengu_melodic_ember` | gate | on |  |  |  |
| `tengu_melodic_flute` | gate | off |  |  |  |
| `tengu_melodic_honey` | gate | on |  |  |  |
| `tengu_melodic_mitten` | gate | on |  |  |  |
| `tengu_melodic_octopus` | gate | on |  |  |  |
| `tengu_melodic_pudding` | gate | off |  |  |  |
| `tengu_melodic_squid` | gate | on |  |  |  |
| `tengu_melodic_wolf` | gate | on |  |  |  |
| `tengu_mem_push_delete_mode` | config | "corroborate" |  |  |  |
| `tengu_memoized_newt` | gate | on |  |  |  |
| `tengu_memoized_owl` | gate | off |  |  |  |
| `tengu_memory_bulk_inflate` | gate | on |  |  |  |
| `tengu_memory_store_resync_interval_minutes` | config |  |  |  |  |
| `tengu_memory_stream_list` | gate | on |  |  |  |
| `tengu_mended_kite` | gate | off |  |  |  |
| `tengu_mermaid_mod` | config |  |  |  |  |
| `tengu_merry_castle` | gate | on |  |  |  |
| `tengu_merry_kite` | config | 1 |  |  |  |
| `tengu_merry_lake` | gate | off |  |  |  |
| `tengu_mighty_thimble` | gate | on |  |  |  |
| `tengu_mint_lanes` | gate | off |  |  |  |
| `tengu_misty_anchor` | config |  |  |  |  |
| `tengu_misty_sunbeam` | gate | off |  |  |  |
| `tengu_misty_twilight` | gate | on |  |  |  |
| `tengu_modular_gizmo` | gate | off |  |  |  |
| `tengu_modular_marble` | gate | off |  |  |  |
| `tengu_modular_mochi` | gate | off |  |  |  |
| `tengu_modular_pearl` | gate | off |  |  |  |
| `tengu_modular_sketch` | gate | off |  |  |  |
| `tengu_moonlit_lagoon` | gate | on |  |  |  |
| `tengu_moonlit_mountain` | gate | off |  |  |  |
| `tengu_moonlit_panda` | gate | off |  |  |  |
| `tengu_moonlit_peacock` | gate | off |  |  |  |
| `tengu_moonlit_toucan` | gate | off |  |  |  |
| `tengu_moss_anchor` | gate | off |  |  |  |
| `tengu_mossy_anvil` | gate | on |  |  |  |
| `tengu_mossy_crown` | gate | on |  |  |  |
| `tengu_mossy_dijkstra` | gate | on |  |  |  |
| `tengu_mossy_ferry` | gate | off |  |  |  |
| `tengu_mossy_gray` | gate | off |  |  |  |
| `tengu_mossy_kepler` | gate | off |  |  |  |
| `tengu_mossy_lathe` | gate | on |  |  |  |
| `tengu_mossy_satchel` | config | 0 |  |  |  |
| `tengu_mossy_sky` | gate | off |  |  |  |
| `tengu_mossy_wirth` | gate | off |  |  |  |
| `tengu_moth_copse` | gate | off |  |  |  |
| `tengu_mutable_flask` | gate | off |  |  |  |
| `tengu_mutable_phoenix_killswitch` | gate | off |  |  |  |
| `tengu_nankeen_kestrel` | gate | off |  |  |  |
| `tengu_native_cursor` | gate | off |  |  |  |
| `tengu_neapolitan` | gate | off |  |  |  |
| `tengu_nested_acorn` | config | 0 |  |  |  |
| `tengu_nifty_canyon` | gate | on |  |  |  |
| `tengu_nifty_harbor` | gate | on |  |  |  |
| `tengu_nifty_lemon` | gate | off |  |  |  |
| `tengu_nifty_lobster` | gate | off |  |  |  |
| `tengu_nifty_prism` | gate | off |  |  |  |
| `tengu_nifty_quasar` | config |  |  |  |  |
| `tengu_nimble_doorbell` | gate | off |  |  |  |
| `tengu_nimble_wren` | gate | on |  |  |  |
| `tengu_noble_mountain` | gate | on |  |  |  |
| `tengu_noble_piglet` | config |  |  |  |  |
| `tengu_noble_snowflake` | config |  |  |  |  |
| `tengu_noble_spring` | gate | off |  |  |  |
| `tengu_noble_wozniak` | gate | on |  |  |  |
| `tengu_non_deferrable_builtins` | config |  |  |  |  |
| `tengu_observer_agents_enabled` | gate | on |  |  |  |
| `tengu_observer_subagent_fanout` | gate | on |  |  |  |
| `tengu_ochre_bittern` | gate | off |  |  |  |
| `tengu_ochre_dunlin` | gate | off |  |  |  |
| `tengu_ochre_gannet` | gate | on |  |  |  |
| `tengu_ochre_gantry` | config |  |  |  |  |
| `tengu_ochre_plover` | gate | off |  |  |  |
| `tengu_official_plugin_prompt_overrides` | config |  |  |  |  |
| `tengu_on_branch_default_guard_observe` | gate |  |  |  |  |
| `tengu_onyx_plover` | config |  |  |  |  |
| `tengu_onyx_sluice` | gate | on |  |  |  |
| `tengu_optimized_puzzle` | gate | on |  |  |  |
| `tengu_osier_pylon_trace` | gate | off |  |  |  |
| `tengu_pale_kestrel` | gate | on |  |  |  |
| `tengu_paper_halyard` | gate | off |  |  |  |
| `tengu_parallel_llama` | gate | on |  |  |  |
| `tengu_parsed_spindle` | gate | off |  |  |  |
| `tengu_parsed_willow` | gate | on |  |  |  |
| `tengu_partitioned_brook` | gate | off |  |  |  |
| `tengu_partitioned_finch` | gate | on |  |  |  |
| `tengu_partitioned_platypus` | gate | off |  |  |  |
| `tengu_passport_quail` | gate | off |  |  |  |
| `tengu_patient_drawbridge` | gate | off |  |  |  |
| `tengu_patient_finch` | gate | on |  |  |  |
| `tengu_patient_tide` | config | 0 |  |  |  |
| `tengu_peaceful_leaf` | gate | off |  |  |  |
| `tengu_peaceful_valiant` | gate | off |  |  |  |
| `tengu_pencil_farmer` | gate | off |  |  |  |
| `tengu_penguins_off` | config |  |  |  |  |
| `tengu_peppy_giraffe` | gate | off |  |  |  |
| `tengu_peppy_gosling` | config | 0 |  |  |  |
| `tengu_peppy_muffin` | gate | on |  |  |  |
| `tengu_peppy_nest` | gate | off |  |  |  |
| `tengu_peppy_starfish` | gate | off |  |  |  |
| `tengu_peppy_starlight` | gate | on |  |  |  |
| `tengu_pewter_avocet` | gate | on |  |  |  |
| `tengu_pewter_brook` | gate | off |  |  |  |
| `tengu_pewter_canteen` | gate | off |  |  |  |
| `tengu_pewter_owl_model` | config | "" |  |  |  |
| `tengu_plain_kestrel` | config |  |  |  |  |
| `tengu_plain_kettle` | gate | on |  |  |  |
| `tengu_plain_locket` | gate | on |  |  |  |
| `tengu_plain_sorrel` | gate | on |  |  |  |
| `tengu_playful_hare` | gate | on |  |  |  |
| `tengu_playful_lobster` | gate | on |  |  |  |
| `tengu_playful_panda` | gate | on |  |  |  |
| `tengu_playful_sifakis` | gate | off | For max/pro accounts, saves the cu-desktop MCP server toggle as `computerUseChoices` “on”/“off”. | Only takes effect when toggling the cu-desktop MCP server, and when an account UUID is available to key the saved choice. | high |
| `tengu_playful_valley` | gate | on |  |  |  |
| `tengu_plugin_binary_assets` | gate | off |  |  |  |
| `tengu_plugin_command_source_refresh` | gate | on |  |  |  |
| `tengu_plugin_input_refusal` | gate | on |  |  |  |
| `tengu_plugin_official_mkt_git_fallback` | gate | on |  |  |  |
| `tengu_plum_vx3` | gate | off | Force web search tool call with zero thinking tokens and alternate model selection | Exact behavior outside web_search call path unknown. | high |
| `tengu_polished_tulip` | gate | on |  |  |  |
| `tengu_prancy_charm` | gate | off |  |  |  |
| `tengu_prancy_pebble` | config |  |  |  |  |
| `tengu_precious_brook` | gate | off |  |  |  |
| `tengu_precious_crab` | gate | off |  |  |  |
| `tengu_precious_ember` | gate | on |  |  |  |
| `tengu_precious_koala` | config | "off" |  |  |  |
| `tengu_print_ceiling_stop_agents` | gate | on |  |  |  |
| `tengu_proactivity_selector` | gate | on |  |  |  |
| `tengu_projects_compact_thread_rule_enabled` | config |  |  |  |  |
| `tengu_projects_thread_recap` | gate | off |  |  |  |
| `tengu_projects_thread_recap_prompt` | config | "" |  |  |  |
| `tengu_projects_thread_reply_lead_killswitch` | gate | off |  |  |  |
| `tengu_prompt_cache_1h_config` | config |  |  |  |  |
| `tengu_propose_goal` | gate | off |  |  |  |
| `tengu_proud_clover` | gate | off |  |  |  |
| `tengu_ptc_enabled` | gate | on |  |  |  |
| `tengu_pure_squid` | config |  |  |  |  |
| `tengu_pure_turtle` | gate | off |  |  |  |
| `tengu_purring_aurora` | gate | off |  |  |  |
| `tengu_purring_micali` | gate | on |  |  |  |
| `tengu_quartz_pipit` | gate | on |  |  |  |
| `tengu_quartz_thimble` | gate | on |  |  |  |
| `tengu_quick_otter` | gate | off |  |  |  |
| `tengu_quiet_aurora` | gate | off |  |  |  |
| `tengu_quiet_badger` | gate | off |  |  |  |
| `tengu_quiet_elephant` | gate | on |  |  |  |
| `tengu_quiet_ember` | config |  |  |  |  |
| `tengu_quiet_heron` | config |  |  |  |  |
| `tengu_quiet_kite` | gate | on |  |  |  |
| `tengu_quiet_lantern` | gate | on |  |  |  |
| `tengu_quiet_larch` | gate | off |  |  |  |
| `tengu_quiet_larkspur` | gate | on |  |  |  |
| `tengu_quiet_pike` | gate | off |  |  |  |
| `tengu_quiet_turnstile` | gate | on |  |  |  |
| `tengu_quill_marten` | gate | off |  |  |  |
| `tengu_quirky_goblet` | gate | off |  |  |  |
| `tengu_quirky_seahorse` | gate | off |  |  |  |
| `tengu_quirky_shore` | config | "off" |  |  |  |
| `tengu_quirky_teacup` | gate | on |  |  |  |
| `tengu_quirky_volcano` | config | 0 |  |  |  |
| `tengu_quizzical_giraffe` | gate | off |  |  |  |
| `tengu_quizzical_lampson` | gate | off |  |  |  |
| `tengu_quizzical_mango` | gate | on |  |  |  |
| `tengu_quizzical_thimble` | gate | on |  |  |  |
| `tengu_radiant_fern` | config |  |  |  |  |
| `tengu_radiant_heron` | gate | off |  |  |  |
| `tengu_radiant_lemur` | gate | off |  |  |  |
| `tengu_radiant_teapot` | gate | on |  |  |  |
| `tengu_rc_long_turn_nudge` | config |  |  |  |  |
| `tengu_rc_permission_nudge` | config |  |  |  |  |
| `tengu_reactive_compact_remote` | config |  |  |  |  |
| `tengu_reactive_heron` | gate | off |  |  |  |
| `tengu_reactive_quilt` | gate | off |  |  |  |
| `tengu_record_created_pr_to_ccr` | gate | off |  |  |  |
| `tengu_reflective_goblet` | gate | off |  |  |  |
| `tengu_reflective_thimble` | gate | on | Keeps compaction from being skipped with reason "failure_breaker_open" after too many failures. | Only affects the path when consecutiveFailures hits the threshold and DISABLE_COMPACT is not set. | medium |
| `tengu_reflective_wren` | gate | on |  |  |  |
| `tengu_remote_auto_mode_include_destructive_mcp` | gate | off |  |  |  |
| `tengu_remote_backend` | gate | off | Permits starting a remote session without an initial description for the CLI remote command. | Only seen gating the missing-description error path. | high |
| `tengu_rename_full_session_fork` | gate | off |  |  |  |
| `tengu_repl_mcp_error_throw` | gate | on |  |  |  |
| `tengu_repl_mcp_undeclared_args_refuse` | gate | on |  |  |  |
| `tengu_repl_unwritable_args_refuse` | gate | on |  |  |  |
| `tengu_resilient_waffle` | gate | on |  |  |  |
| `tengu_resume_cache_warm_config` | config |  |  |  |  |
| `tengu_rippling_map` | gate | on |  |  |  |
| `tengu_rippling_orbit` | gate | off |  |  |  |
| `tengu_rippling_sketch` | gate | on |  |  |  |
| `tengu_robust_pine` | gate | off |  |  |  |
| `tengu_rosy_cloud` | gate | off | Sets textEarlyUploadsMs to [150] (instead of []) for the CCR/bridge client config. | Only applies when outboundOnly is false (dt is not set). | high |
| `tengu_rosy_crab` | gate | on |  |  |  |
| `tengu_rosy_donut` | gate | on |  |  |  |
| `tengu_rosy_finch` | gate | off |  |  |  |
| `tengu_rosy_flute` | gate | on |  |  |  |
| `tengu_rosy_llama` | gate | off |  |  |  |
| `tengu_rosy_quail` | gate | off |  |  |  |
| `tengu_rosy_rocket` | gate | on |  |  |  |
| `tengu_russet_envelope` | gate | off |  |  |  |
| `tengu_rustling_crescent` | gate | on |  |  |  |
| `tengu_rustling_gizmo` | config | 0 |  |  |  |
| `tengu_rustling_orbit` | gate | off |  |  |  |
| `tengu_rustling_star` | gate | off |  |  |  |
| `tengu_rustling_sunset` | gate | on |  |  |  |
| `tengu_sable_orrery` | gate | on |  |  |  |
| `tengu_saffron_ferry` | gate | on |  |  |  |
| `tengu_saffron_ladder` | gate | off |  |  |  |
| `tengu_saffron_lattice` | config |  |  |  |  |
| `tengu_saffron_picker_dim` | gate | off |  |  |  |
| `tengu_saffron_wren` | gate | on |  |  |  |
| `tengu_sage_compass2` | config |  |  |  |  |
| `tengu_satchel_banjo` | gate | off |  |  |  |
| `tengu_scalable_meteor` | gate | off |  |  |  |
| `tengu_scratch` | gate | off | Enables writing a session-memory scratchpad with a summary.md file under a per-user Claude folder. |  | high |
| `tengu_sdk_mcp_manifests` | gate | on |  |  |  |
| `tengu_sedge_lantern_config` | config |  |  |  |  |
| `tengu_send_file` | gate | off |  |  |  |
| `tengu_send_user_file` | gate | on |  |  |  |
| `tengu_sepia_cormorant` | config |  |  |  |  |
| `tengu_sepia_moth` | gate | off |  |  |  |
| `tengu_sequential_puffin` | gate | on |  |  |  |
| `tengu_serene_hare` | gate | on |  |  |  |
| `tengu_serene_rain` | gate | off |  |  |  |
| `tengu_serene_teacup` | gate | on |  |  |  |
| `tengu_serene_teapot` | gate | on |  |  |  |
| `tengu_session_name_uniqueness` | gate | on |  |  |  |
| `tengu_session_stable_address` | gate | off |  |  |  |
| `tengu_sharded_beacon` | gate | on |  |  |  |
| `tengu_sharded_moonbeam` | gate | on |  |  |  |
| `tengu_sharded_snowflake` | gate | off |  |  |  |
| `tengu_shimmering_avalanche` | gate | off |  |  |  |
| `tengu_shimmering_clock` | gate | on |  |  |  |
| `tengu_shimmering_firefly` | gate | off |  |  |  |
| `tengu_shimmying_stardust` | gate | off |  |  |  |
| `tengu_shining_fractals` | gate | off |  |  |  |
| `tengu_shiny_stardust` | gate | off |  |  |  |
| `tengu_silent_harbor` | gate | off |  |  |  |
| `tengu_silent_heron` | config | 0 |  |  |  |
| `tengu_silk_hinge` | gate | off |  |  |  |
| `tengu_silly_hamster` | gate | on |  |  |  |
| `tengu_silly_waterfall` | gate | off |  |  |  |
| `tengu_skills_dashboard_enabled` | gate | off |  |  |  |
| `tengu_slate_bittern` | gate | on |  |  |  |
| `tengu_slate_finch` | gate | off |  |  |  |
| `tengu_slate_harbor_experiment` | gate | off |  |  |  |
| `tengu_slate_lantern` | gate | on |  |  |  |
| `tengu_slate_lantern_ember` | gate | on |  |  |  |
| `tengu_slate_marten` | gate | off |  |  |  |
| `tengu_slate_thimble` | gate | off |  |  |  |
| `tengu_sleepy_rabbit` | gate | off |  |  |  |
| `tengu_sleepy_ripple` | gate | on |  |  |  |
| `tengu_sleepy_shore` | config |  |  |  |  |
| `tengu_sleepy_snowflake` | config | "all" |  |  |  |
| `tengu_smooth_lark` | gate | on |  |  |  |
| `tengu_smooth_peach` | gate | on |  |  |  |
| `tengu_snappy_hammock` | gate | on | In "ldr" runs, normalizes generated profile pins to use "profile:unnamed:" instead of the real profile name. | Only applies in "ldr" runs, and only for profile pins (e.g. ones starting "profile::" or in ANTHROPIC_BASE_URL mismatch cases). | medium |
| `tengu_snappy_parasol` | gate | off |  |  |  |
| `tengu_snappy_pelican` | gate | off |  |  |  |
| `tengu_snappy_plum` | gate | off |  |  |  |
| `tengu_snazzy_graham` | gate | on |  |  |  |
| `tengu_snazzy_hare` | gate | off |  |  |  |
| `tengu_snug_balloon` | gate | off |  |  |  |
| `tengu_snug_catmull` | gate | on |  |  |  |
| `tengu_snug_cocoa` | gate | off |  |  |  |
| `tengu_snug_crystal` | gate | off |  |  |  |
| `tengu_snug_nautilus` | config |  |  |  |  |
| `tengu_snug_orbit` | config |  |  |  |  |
| `tengu_snug_reef` | config | 0 |  |  |  |
| `tengu_snug_starfish` | gate | off |  |  |  |
| `tengu_snuggly_dongarra` | gate | off |  |  |  |
| `tengu_snuggly_snail` | gate | off |  |  |  |
| `tengu_soft_spark` | config |  |  |  |  |
| `tengu_soft_spindle` | gate | on |  |  |  |
| `tengu_sorrel_trellis` | gate | on |  |  |  |
| `tengu_sorted_otter` | gate | off |  |  |  |
| `tengu_sorted_summit` | gate | on |  |  |  |
| `tengu_sorted_zebra` | gate | off |  |  |  |
| `tengu_spare_attic` | config | 0 |  |  |  |
| `tengu_spicy_blossom` | gate | off |  |  |  |
| `tengu_splendid_locket` | config | "off" |  |  |  |
| `tengu_splendid_puzzle` | gate | off | When set to "direct" or "all", adds an extra empty entry to request params `_meta` extensions on some RPC calls. | Only applies if the RPC request has params with `_meta`/extensions; "direct" mode only runs when not behind a gateway/proxy. | medium |
| `tengu_splendid_sutton` | gate | off |  |  |  |
| `tengu_sprightly_orbit` | gate | on |  |  |  |
| `tengu_squishy_spring` | gate | on |  |  |  |
| `tengu_staged_ladybug` | gate | on |  |  |  |
| `tengu_starry_beacon` | gate | off |  |  |  |
| `tengu_starry_breeze` | config | 0 |  |  |  |
| `tengu_starry_squid` | gate | on |  |  |  |
| `tengu_startup_announcements` | config |  |  |  |  |
| `tengu_startup_notice` | config | "" |  |  |  |
| `tengu_stateful_petal` | gate | off |  |  |  |
| `tengu_stateless_lagoon` | gate | off |  |  |  |
| `tengu_stateless_music` | gate | on |  |  |  |
| `tengu_stateless_treasure` | gate | off |  |  |  |
| `tengu_steady_anchor` | gate | on |  |  |  |
| `tengu_steady_heron` | gate | on |  |  |  |
| `tengu_steady_panda` | config |  |  |  |  |
| `tengu_steady_plover` | gate | on |  |  |  |
| `tengu_steady_puppy` | gate | off |  |  |  |
| `tengu_stellar_drift` | gate | off |  |  |  |
| `tengu_still_heron` | gate | on |  |  |  |
| `tengu_stream_watchdog_default_on` | gate | on |  |  |  |
| `tengu_streamed_thimble` | gate | on |  |  |  |
| `tengu_structured_output_strict` | gate | off |  |  |  |
| `tengu_sturdy_plover` | gate | off |  |  |  |
| `tengu_subagent_cache_evict` | gate | off |  |  |  |
| `tengu_sunny_mountain` | gate | off |  |  |  |
| `tengu_sunny_pancake` | gate | off |  |  |  |
| `tengu_sunny_perlis` | gate | off |  |  |  |
| `tengu_sunny_squid` | gate | on |  |  |  |
| `tengu_sunset_penguin_opus48` | config | "2026-11-30" |  |  |  |
| `tengu_surface_failed_mcp_servers` | gate | on |  |  |  |
| `tengu_swift_bear` | gate | on |  |  |  |
| `tengu_swift_pelican` | config |  |  |  |  |
| `tengu_swift_whistle` | gate | off |  |  |  |
| `tengu_swirling_meteor` | gate | on |  |  |  |
| `tengu_swirling_squid` | gate | off |  |  |  |
| `tengu_tab_read_sep` | gate | off |  |  |  |
| `tengu_teal_corbel` | gate | on |  |  |  |
| `tengu_teal_corbel_finial` | gate | on |  |  |  |
| `tengu_teal_corbel_newel` | gate | off |  |  |  |
| `tengu_teleport_github_access_precheck` | gate | on |  |  |  |
| `tengu_teleport_send_to_cloud` | gate | off |  |  |  |
| `tengu_temporal_haven` | gate | off |  |  |  |
| `tengu_temporal_kazoo` | config |  |  |  |  |
| `tengu_terminal_sidebar` | gate | off |  |  |  |
| `tengu_tethered_buoy` | gate | on |  |  |  |
| `tengu_thinking_block_resumption` | gate | off |  |  |  |
| `tengu_ticklish_moon` | gate | off |  |  |  |
| `tengu_ticklish_pnueli` | gate | off |  |  |  |
| `tengu_ticklish_whisper` | gate | off |  |  |  |
| `tengu_tidy_abacus` | gate | on |  |  |  |
| `tengu_tidy_burrow` | config |  |  |  |  |
| `tengu_tidy_cloud` | gate | on |  |  |  |
| `tengu_tidy_eclipse` | gate | on |  |  |  |
| `tengu_tidy_fern` | gate | on |  |  |  |
| `tengu_tidy_lake` | gate | off |  |  |  |
| `tengu_tidy_lantern` | gate | on |  |  |  |
| `tengu_tidy_rocket` | gate | on |  |  |  |
| `tengu_tidy_shelf` | config | "tell" |  |  |  |
| `tengu_tidy_sloth` | gate | on |  |  |  |
| `tengu_tidy_starfish` | gate | off |  |  |  |
| `tengu_tidy_swing` | gate | off |  |  |  |
| `tengu_tidy_thimble` | gate | off |  |  |  |
| `tengu_tidy_widget` | gate | on |  |  |  |
| `tengu_tingly_flute` | config | "" |  |  |  |
| `tengu_tips_mod` | config |  |  |  |  |
| `tengu_toasty_giraffe` | gate | off |  |  |  |
| `tengu_toasty_phoenix` | gate | off |  |  |  |
| `tengu_toasty_robin` | gate | on |  |  |  |
| `tengu_tool_detach` | gate | on |  |  |  |
| `tengu_tool_pear` | gate | off | Enables additional tool-definition handling for strict tools, including extra processing for supported models. | Exact effect is obfuscated; observable uses include adding a feature to the tool context list and gating a crypto hash path. | medium |
| `tengu_tool_search_unsupported_models` | config |  | Provides list of model substrings that disable tool search support checks | Used to filter model names by substring match. | high |
| `tengu_trace_lantern` | gate | off |  |  |  |
| `tengu_tranquil_cloud` | gate | on |  |  |  |
| `tengu_tranquil_cocoa` | gate | off |  |  |  |
| `tengu_tranquil_diffie` | gate | on |  |  |  |
| `tengu_tranquil_gadget` | gate | off |  |  |  |
| `tengu_tranquil_locket` | config | 0 |  |  |  |
| `tengu_tranquil_starlight` | gate | off |  |  |  |
| `tengu_tranquil_sun` | gate | off | When on, include alwaysLoad MCP tools from a specific server as “leading tools” even if none request anthropic/toolsPlacement=first. | Only applies when the MCP leading-tools logic runs; output differs if CLAUDE_CODE_REMOTE is set. | medium |
| `tengu_trim_dunnock` | gate | off |  |  |  |
| `tengu_trim_nuthatch` | gate | on |  |  |  |
| `tengu_truncated_response_recovery` | gate | on |  |  |  |
| `tengu_truthful_wren` | gate | on |  |  |  |
| `tengu_turtle_carbon` | gate | on |  |  |  |
| `tengu_twinkling_boole` | gate | off |  |  |  |
| `tengu_twinkling_cosmos` | gate | off |  |  |  |
| `tengu_twinkling_crown` | gate | off |  |  |  |
| `tengu_twinkling_hoare` | gate | off |  |  |  |
| `tengu_twinkling_robin` | gate | on |  |  |  |
| `tengu_twinkling_thunder` | gate | off |  |  |  |
| `tengu_twinkly_sundae` | gate | on |  |  |  |
| `tengu_twinkly_sunrise` | gate | on |  |  |  |
| `tengu_typed_koala` | gate | on |  |  |  |
| `tengu_typed_pebble` | config | 0 |  |  |  |
| `tengu_typed_snail` | gate | off |  |  |  |
| `tengu_ultraplan_config` | config |  |  |  |  |
| `tengu_ultraplan_prompt_identifier` | config |  |  |  |  |
| `tengu_ultraplan_timeout_seconds` | config |  |  |  |  |
| `tengu_ultrareview_post_enabled` | gate | on |  |  |  |
| `tengu_umber_petrel` | gate | off |  |  |  |
| `tengu_umber_plover` | gate | on |  |  |  |
| `tengu_umber_sluice` | gate | off |  |  |  |
| `tengu_umber_stile` | gate | off |  |  |  |
| `tengu_valiant_crayon` | gate | off |  |  |  |
| `tengu_valiant_rain` | gate | off |  |  |  |
| `tengu_valiant_teapot` | gate | off |  |  |  |
| `tengu_vast_jellyfish` | gate | off |  |  |  |
| `tengu_vast_sunset` | gate | on |  |  |  |
| `tengu_vast_tulip` | gate | off |  |  |  |
| `tengu_vectorized_mitten` | gate | off |  |  |  |
| `tengu_vellum_anchor` | gate | off |  |  |  |
| `tengu_vellum_siding` | gate | off |  |  |  |
| `tengu_velvet_cairn` | gate | on |  |  |  |
| `tengu_velvet_crab` | config |  |  |  |  |
| `tengu_velvet_heron` | gate | on |  |  |  |
| `tengu_velvet_ibis` | config |  |  |  |  |
| `tengu_velvet_panda` | gate | on |  |  |  |
| `tengu_velvet_tide` | gate | off |  |  |  |
| `tengu_velvety_aurora` | gate | on |  |  |  |
| `tengu_velvety_duckling` | gate | off |  |  |  |
| `tengu_velvety_kay` | gate | off |  |  |  |
| `tengu_velvety_mango` | gate | on |  |  |  |
| `tengu_velvety_robin` | gate | off |  |  |  |
| `tengu_velvety_sprout` | gate | off |  |  |  |
| `tengu_verified_vs_assumed` | gate | off |  |  |  |
| `tengu_version_config` | config |  | Fetches a minimum required Claude Code version and shows an update-required message. | Minimum version appears server-configured via the config fetch. | high |
| `tengu_violin_adjuster` | gate | off |  |  |  |
| `tengu_violin_amati` | gate | off |  |  |  |
| `tengu_violin_arching` | gate | off |  |  |  |
| `tengu_violin_corner` | gate | off |  |  |  |
| `tengu_violin_endpin` | gate | off |  |  |  |
| `tengu_violin_eye` | gate | off |  |  |  |
| `tengu_violin_ferrule` | gate | off |  |  |  |
| `tengu_violin_fhole` | gate | off |  |  |  |
| `tengu_violin_finetuner` | gate | off |  |  |  |
| `tengu_violin_frog` | gate | on |  |  |  |
| `tengu_violin_hair` | gate | off |  |  |  |
| `tengu_violin_lapping` | gate | off |  |  |  |
| `tengu_violin_luthier` | gate | off |  |  |  |
| `tengu_violin_neck` | gate | off |  |  |  |
| `tengu_violin_nut` | gate | off |  |  |  |
| `tengu_violin_overstand` | gate | off |  |  |  |
| `tengu_violin_pernambuco` | gate | off |  |  |  |
| `tengu_violin_pochette` | gate | off |  |  |  |
| `tengu_violin_rib` | gate | off |  |  |  |
| `tengu_violin_rosin` | gate | off |  |  |  |
| `tengu_violin_scroll` | gate | off |  |  |  |
| `tengu_violin_sordino` | config |  |  |  |  |
| `tengu_violin_spruce` | config |  |  |  |  |
| `tengu_violin_strad` | gate | off |  |  |  |
| `tengu_violin_table` | gate | off |  |  |  |
| `tengu_violin_tailgut` | gate | off |  |  |  |
| `tengu_violin_tip` | gate | off |  |  |  |
| `tengu_violin_varnish` | gate | off |  |  |  |
| `tengu_violin_waist` | gate | off |  |  |  |
| `tengu_violin_winding` | gate | off |  |  |  |
| `tengu_violin_wood` | gate | off |  |  |  |
| `tengu_virtual_knuth` | config |  |  |  |  |
| `tengu_virtual_pancake` | config |  |  |  |  |
| `tengu_virtual_parasol` | config |  |  |  |  |
| `tengu_virtual_quiche` | gate | off |  |  |  |
| `tengu_virtual_toast` | gate | off |  |  |  |
| `tengu_virtual_tulip` | gate | off |  |  |  |
| `tengu_vivid_crown` | gate | off |  |  |  |
| `tengu_vivid_peach` | config |  |  |  |  |
| `tengu_vivid_treehouse` | config | 0 |  |  |  |
| `tengu_vscode_card_message_approval` | gate | on |  |  |  |
| `tengu_vscode_code_colors` | gate | on |  |  |  |
| `tengu_vscode_feedback_survey` | gate | off |  |  |  |
| `tengu_vscode_inline_pastes` | gate | on |  |  |  |
| `tengu_vscode_math_rendering` | gate | on |  |  |  |
| `tengu_vscode_onboarding` | gate | off | Enables an onboarding experience/flow in the Claude VSCode integration. | Only seen being sent as an experiment gate; specific onboarding screens/steps aren’t shown. | medium |
| `tengu_vscode_python_beside_start` | gate | on |  |  |  |
| `tengu_vscode_restore_breaker` | gate | on |  |  |  |
| `tengu_vscode_resume_precheck` | gate | on |  |  |  |
| `tengu_vscode_start_second_try` | gate | on |  |  |  |
| `tengu_vscode_stored_startup_config` | gate | on |  |  |  |
| `tengu_walnut_tiller` | gate | on |  |  |  |
| `tengu_warm_crescent` | gate | off |  |  |  |
| `tengu_warm_newt` | config | 0 | Sets autocompact's testPctOverride to this percentage, changing the computed compaction limit/threshold. | Only in hosted, only if the value is a number > current % and <=100, and additional internal checks pass. | medium |
| `tengu_warm_twilight` | gate | off |  |  |  |
| `tengu_watchdog_skip_nonstreaming_fallback` | gate | off |  |  |  |
| `tengu_webfetch_deadline_ms` | config |  |  |  |  |
| `tengu_whimsical_marble` | gate | on | Allows paths under claude-science-work or /home/claude/results (excluding .cache) to count as inside outputs. | Only applies if the resolved real path matches the built-in regex for those directories. | high |
| `tengu_whimsical_trinket` | gate | off |  |  |  |
| `tengu_wiggly_crystal` | gate | off |  |  |  |
| `tengu_wiggly_fog` | gate | off |  |  |  |
| `tengu_wiggly_gray` | gate | off |  |  |  |
| `tengu_wiggly_lemur` | gate | off |  |  |  |
| `tengu_wiggly_locket` | gate | off |  |  |  |
| `tengu_wiggly_zephyr` | gate | on |  |  |  |
| `tengu_wild_crayon` | gate | off |  |  |  |
| `tengu_wild_forest` | gate | off |  |  |  |
| `tengu_wild_gosling` | gate | off |  |  |  |
| `tengu_wild_orbit` | gate | off |  |  |  |
| `tengu_wild_tome` | gate | off |  |  |  |
| `tengu_wise_kite` | gate | off |  |  |  |
| `tengu_wise_newt` | config |  |  |  |  |
| `tengu_wise_pillow` | gate | off |  |  |  |
| `tengu_wise_salamander` | config | 0 |  |  |  |
| `tengu_witty_hearth` | gate | on |  |  |  |
| `tengu_wobbly_pinwheel` | gate | on |  |  |  |
| `tengu_wobbly_sundae` | gate | off |  |  |  |
| `tengu_wondrous_acorn` | config |  |  |  |  |
| `tengu_wondrous_island` | gate | off |  |  |  |
| `tengu_wondrous_oasis` | gate | off |  |  |  |
| `tengu_woolly_emerson` | gate | on |  |  |  |
| `tengu_woolly_gadget` | gate | on |  |  |  |
| `tengu_woolly_kettle` | gate | off |  |  |  |
| `tengu_woolly_origami` | gate | on | Lets computer-use “save check” allow input when the window can’t be read due to accessibility errors. | Only applies when `windowDocumentReadFailed` is true and the save check’s internal “safe to continue” condition is met. | medium |
| `tengu_woolly_sundial` | gate | on | Shows a warning when part of a session can’t be saved, prompting you to run /compact. | No warning if DISABLE_COMPACT is set. | high |
| `tengu_woolly_toast` | gate | off |  |  |  |
| `tengu_woolly_umbrella` | gate | on |  |  |  |
| `tengu_worker_owner_rows_killswitch` | gate | off |  |  |  |
| `tengu_workflow_schema_lint_enforce` | gate | on |  |  |  |
| `tengu_workflows_enabled` | gate | on |  |  |  |
| `tengu_woven_ladder` | config |  |  |  |  |
| `tengu_woven_tassel` | config | 0 |  |  |  |
| `tengu_xterm_atlas_reset` | gate | on |  |  |  |
| `tengu_zany_flask` | config | 2 |  |  |  |
| `tengu_zazzy_dusk` | gate | off |  |  |  |
| `tengu_zesty_horizon_wait` | gate | on |  |  |  |
| `tengu_zesty_pearl` | gate | off |  |  |  |
| `tengu_zesty_pudding` | gate | off |  |  |  |
| `tengu_zinc_harbor` | gate | off |  |  |  |
| `tengu_zippy_gosling` | config | 0 |  |  |  |
| `tengu_zippy_piglet` | gate | off |  |  |  |
| `tengu_zippy_spindle` | gate | off |  |  |  |
