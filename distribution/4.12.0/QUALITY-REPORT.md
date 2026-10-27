# Pakla Hub 4.12 doğrulama

- Three real background-enabled startup fixtures; idle/active/idle header recording visibility tested with simulated capture state, no recording
- 12 product pages x five requested sizes; game-card play/edit/favorite controls additionally checked for vertical clipping
- 4.10 feature fixture and 4.11 protected draft fixture passed against 4.12
- App/setup self-tests; signed patch integrity/apply/rollback tests
- Original 4.11 updater verifies/applies 4.12 and preserves library/history
- Installed 4.12 signed patch; 22 existing user-data files unchanged except expected update-history metadata

Sınırlar:

- Local draft persistence: newest 100 entries per type; not cloud synchronized; logout does not delete stored drafts; corrupt vault is preserved and auto-save disabled for that owner/session
- No live people messaging or recording in fixtures
- Voice beta six peers/one share/no TURN or SFU; real cross-network testing incomplete
- KLIPY shared testing quota 100 API calls/hour; Spotify OAuth unconfigured; messages are not E2EE
- Authenticode certificate unavailable; separate RSA-SHA256 patch signature