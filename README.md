# Codex and Claude Code records

Private backup containing local Codex and Claude Code records created on or after 2026-07-01 (Asia/Shanghai).

## Integrity

- Archive: `ai-records-from-2026-07-01-20260920T161051.tar.gz`
- Size: `92925062` bytes
- SHA-256: `252a6942ae0852419ba4c852c074bf418a518018dadd59dbebaa2127ec22c1a1`

This archive contains private conversation and development history. Keep the repository private.

## Restore

Exit Codex and Claude Code first, then extract from the destination user's home directory:

```bash
cd "$HOME"
tar -xzf /path/to/ai-records-from-2026-07-01-20260920T161051.tar.gz
chmod 700 "$HOME/.codex" "$HOME/.claude"
```

Project paths should remain the same where possible so that existing sessions continue to map to their original working directories.
