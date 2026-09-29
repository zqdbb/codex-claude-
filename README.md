# Codex and Claude Code records

Private backup containing local Codex and Claude Code records created on or after 2026-07-01 (Asia/Shanghai), updated 2026-09-29.

## Archive parts

GitHub's per-file limit requires the archive to be split into two files:

- `ai-records-from-2026-07-01-20260929T100938.tar.gz.part-00` (94,371,840 bytes)
- `ai-records-from-2026-07-01-20260929T100938.tar.gz.part-01` (13,706,189 bytes)

Combined archive SHA-256: `447ecb241dbd041d72d306d094e3fcd7ceb2c5dd363a4bf2337caede9cfa949f`

## Restore

Download both parts into the same directory, then join and extract:

```bash
cat ai-records-from-2026-07-01-20260929T100938.tar.gz.part-* \
  > ai-records-from-2026-07-01-20260929T100938.tar.gz

sha256sum ai-records-from-2026-07-01-20260929T100938.tar.gz
cd "$HOME"
tar -xzf /path/to/ai-records-from-2026-07-01-20260929T100938.tar.gz
chmod 700 "$HOME/.codex" "$HOME/.claude"
```

The expected combined archive hash is the value above. Exit Codex and Claude Code before extracting. Keep this repository private because the archive contains conversation and development history.
