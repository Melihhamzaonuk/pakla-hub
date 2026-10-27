# Pakla Hub 4.11 doğrulama

- Background-enabled startup constructor, native Shown/tray initialization, clean exits x3
- 12 pages x five requested window sizes with layout/search/filter/navigation checks
- Original 4.10 feature flow fixture including shared links/GIFs and clip metadata changes
- Drafts: fresh-window DM/channel restore, Windows DPAPI ciphertext, owner isolation/entropy, corruption preservation, save-failure retry, picker/guide rendering and successful-send removal from primary vault
- App/setup self-tests and signed patch integrity/apply/rollback checks
- 4.10.2 updater verifies and applies 4.11.0 and preserves library/history
- Local installation preserves 22 existing user-data files apart from expected release-history metadata

Sınırlar:

- Local draft persistence: newest 100 entries per type; not cloud synchronized; logout does not delete stored drafts; corrupt vault is preserved and auto-save disabled for that owner/session
- No live people messaging or recording in fixtures
- Voice beta six peers/one share/no TURN or SFU; real cross-network testing incomplete
- KLIPY shared testing quota 100 API calls/hour; Spotify OAuth unconfigured; messages are not E2EE
- Authenticode certificate unavailable; separate RSA-SHA256 patch signature