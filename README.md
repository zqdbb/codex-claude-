# Codex and Claude Code records

Encrypted backup containing local Codex and Claude Code records created on or after 2026-07-01 (Asia/Shanghai).

## Integrity

- Encrypted file: `ai-records-from-2026-07-01-20260920T161051.tar.gz.enc`
- Encryption: AES-256-CBC, PBKDF2, 600000 iterations
- SHA-256: `27d7a6aff0df82870cb20cae992eeb1d097947299d57861d74bb61b2ab93cacb`

The password is intentionally stored separately and is not committed to this repository.

## Decrypt

```bash
openssl enc -d -aes-256-cbc -pbkdf2 -iter 600000 \
  -in ai-records-from-2026-07-01-20260920T161051.tar.gz.enc \
  -out ai-records-from-2026-07-01.tar.gz
```

Enter the separately stored password when prompted, then verify the decrypted archive:

```bash
sha256sum ai-records-from-2026-07-01.tar.gz
```

Expected SHA-256:

```text
252a6942ae0852419ba4c852c074bf418a518018dadd59dbebaa2127ec22c1a1
```

## Restore

Exit Codex and Claude Code first, then extract from the destination user's home directory:

```bash
cd "$HOME"
tar -xzf /path/to/ai-records-from-2026-07-01.tar.gz
chmod 700 "$HOME/.codex" "$HOME/.claude"
```

Project paths should remain the same where possible so that existing sessions continue to map to their original working directories.
