# Backup Script Guide

This guide documents the automated backup solution built for CloudNova Technologies so the client's IT team can understand how it works.

## 1. The Backup Script (backup.sh)

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## 2. What `chmod +x` Does

```bash
chmod +x backup.sh
```

By default, Linux treats a new text file as plain data and will not run it as a program. The `chmod +x` command adds the **execute permission** to the file. After running it, the system allows `./backup.sh` to run as a program. Without it, the script fails with a "Permission denied" error.

## 3. The Cron Expression

```
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|-------|-------|---------|
| Minute | `0` | Run at minute 0 (the start of the hour) |
| Hour | `2` | Run at 2 AM (24-hour clock) |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |
| Command | `/root/backup.sh` | The script that gets executed |

**In plain English:** the backup script runs automatically every night at exactly 2:00 AM.
