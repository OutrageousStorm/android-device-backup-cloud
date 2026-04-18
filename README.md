# ☁️ Android Device Backup to Cloud

Sync Android device backups to cloud storage — S3, Backblaze B2, Google Cloud Storage, or local NAS.

## Supported Backends

| Service | Cost | Auth | Bandwidth |
|---------|------|------|-----------|
| AWS S3 | ~$0.023/GB | IAM keys | Cheap |
| Backblaze B2 | ~$0.006/GB | API keys | Cheaper |
| Google Cloud Storage | ~$0.020/GB | Service account | Standard |
| Wasabi | ~$0.0049/GB | Access keys | Cheap |
| Local NFS/SMB | Free | Network share | Free |

## Quick Start

```bash
# Configure cloud backend
python3 backup_cloud.py --init --backend b2

# Backup device
python3 backup_cloud.py --backup

# List backups
python3 backup_cloud.py --list

# Restore specific backup
python3 backup_cloud.py --restore --backup-id abc123
```

## Features

- Incremental backup (only changed files)
- Compression (gzip, brotli)
- Encryption (AES-256 optional)
- Resume on interrupt
- Automatic rotation (keep last N)
- Scheduled backups via cron
