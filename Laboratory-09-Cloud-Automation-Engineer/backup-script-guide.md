
# Full Script (backup.sh)
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

## What chmod +x Did
The `chmod +x backup.sh` command added execute permission to the script file. By default, a newly created text file is not executable, so Linux blocks it from running as a program for security reasons. Adding the execute (+x) permission tells the system that this file is allowed to be run directly as a command, which is why `./backup.sh` failed before chmod and succeeded afterward.

## Cron Expression Breakdown
Cron expression used: `0 2 * * * /root/backup.sh`

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | At the top of the hour (minute 0) |
| Hour | 2 | At 2 AM |
| Day of Month | * | Every day of the month |
| Month | * | Every month |
| Day of Week | * | Every day of the week |

Together, these fields mean the script runs every single day at exactly 2:00 AM.

## Evidence
#Script execution
<img width="487" height="228" alt="script-execution" src="https://github.com/user-attachments/assets/decc6aaa-54e2-4d2b-b2cf-0bcf457ddcbd" />

#Cron schedule
<img width="625" height="508" alt="cron-schedule" src="https://github.com/user-attachments/assets/c9ce16bb-df4b-4333-a21d-b8adc31737d4" />
