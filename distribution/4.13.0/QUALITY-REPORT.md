# Pakla Hub 4.13 doğrulama

- Eight native quick-search types; scope isolation; true 101 total vs 80 displayed; stale-result clearing; Ctrl+L and narrow input controls
- Loaded DM search: Turkish folding, AND tokens, sender filter, cross-conversation exclusion, no-match, narrow rows and name/time separation; draft unchanged
- Background-enabled startup x3, idle/active header visibility fixture; 12 pages x five requested window sizes including game action bounds
- Prior shared content, bulk clips and protected draft fixtures passed against 4.13
- App/setup self-tests; RSA patch integrity/apply/rollback and original 4.12 updater compatibility
- Installed 4.13 patch with existing user-data hashes checked; no forced shutdown or app launch

Sınırlar:

- Local draft persistence: newest 100 entries per type; not cloud synchronized; logout does not delete stored drafts; corrupt vault is preserved and auto-save disabled for that owner/session
- No live people messaging or recording in fixtures
- Voice beta six peers/one share/no TURN or SFU; real cross-network testing incomplete
- KLIPY shared testing quota 100 API calls/hour; Spotify OAuth unconfigured; messages are not E2EE
- Authenticode certificate unavailable; separate RSA-SHA256 patch signature