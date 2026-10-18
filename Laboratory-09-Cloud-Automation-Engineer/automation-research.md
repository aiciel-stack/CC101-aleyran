# Automation Research

## Bash Script
A Bash script is a text file containing a sequence of Linux commands that the shell executes in order, automating tasks that would otherwise be typed manually one by one. The `#!/bin/bash` line at the top, called the shebang, tells the system which interpreter should run the file, so the operating system knows to execute it using Bash rather than another program.

## Variables
Programmers use variables like `$BACKUP_DIR` instead of hardcoding the exact folder path because it makes the script easier to update and reuse. If the backup location ever changes, only the variable's value needs to be edited once at the top of the script, instead of finding and changing every place the path was typed out.

## Cron Job
A cron job is a scheduled task in Linux that runs a command or script automatically at specified times, managed by the cron daemon. It is essential for cloud operations because it removes the need for a human to manually trigger repetitive tasks, like backups, ensuring they happen reliably and on time, even if no one is watching the server.
