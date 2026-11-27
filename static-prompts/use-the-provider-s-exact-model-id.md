Use the **provider's exact model ID**: Vertex publisher IDs (`claude-sonnet-5`), Bedrock inference-profile IDs (`us.anthropic.claude-sonnet-5`), or Foundry deployment names. Entries may be plain ID strings or objects.

**Gateway:** the `name` must be the exact ID your gateway's `/v1/models` endpoint returns. If you set `supports1m` on an alias (`sonnet`) but discovery returns the full ID, the variant won't appear.

**Extended context** (`supports1m`) is a capability assertion you make about your deployment; only set it for models you've confirmed support the 1M-token window:
```json
[{"name": "claude-sonnet-5", "supports1m": true}, "claude-opus-4-8"]
```
`"claude-sonnet-5[1m]"` is shorthand for the same entry. When an ID is listed both bare and with `[1m]` (as a gateway lists it), the picker shows one model with a 1M variant; put `labelOverride` on the bare entry (a label on the `[1m]` spelling is ignored there); tier-tagged entries are not folded. `prefer1m: true` (no effect without `supports1m`) shows only the 1M variant of the model. Under dynamic discovery (no explicit list), set `modelPrefer1mContext` instead.

**Display label** (`labelOverride`) is for IDs the picker can't derive a friendly name from (Bedrock ARNs, gateway routing aliases). Display-only; `name` is still what the app sends:
```json
[{"name": "arn:aws:bedrock:us-east-1:123:application-inference-profile/abc", "labelOverride": "Claude Opus (Prod)"}]
```

**Tier mapping** (`anthropicFamilyTier`) tells the app which Claude tier (`haiku`/`sonnet`/`opus`/`fable`/`mythos`) an entry stands in for, so bare tier aliases (e.g. in Code sessions) resolve to your model. `isFamilyDefault: true` picks the winner when several entries share a tier:
```json
[{"name": "us.anthropic.claude-opus-4-8", "anthropicFamilyTier": "opus"}]
```
