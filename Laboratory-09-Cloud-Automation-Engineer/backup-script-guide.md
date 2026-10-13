# Backup Script Guide

## The Script

#!/bin/bash

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

mkdir -p $BACKUP_DIR

tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"


## What `chmod +x` Did

It adds execute permission to the file. The first run was denied because Linux blocks newly created text files from running by default, which keeps the system safe from accidental or unauthorized execution.

## The Cron Expression

```
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | At minute 0 |
| Hour | 2 | At hour 2 (2:00 AM, 24-hour clock) |
| Day of Month | * | Every day of the month |
| Month | * | Every month of the year |
| Day of Week | * | Every day of the week |
