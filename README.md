# ☁️ Android Device Backup Cloud

Auto-sync Android device backups to S3, Backblaze B2, OneDrive, or self-hosted storage.

## Features
- **Incremental backups** — only new/changed files
- **Encryption** — AES-256 before upload
- **Scheduled** — runs hourly, daily, or on-demand
- **Multi-cloud** — S3, B2, OneDrive, SFTP
- **Verification** — SHA256 checksums for all uploads

## Quick start
```bash
python3 sync.py --cloud s3 --bucket my-android-backups --schedule daily
```
