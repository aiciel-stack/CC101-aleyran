# Laboratory 9: The Cloud Automation Engineer

## Mission Overview
In this mission, I joined the Cloud Automation and DevOps Team at CloudNova Technologies. I wrote a Bash script that automatically compresses and backs up a client's application data, made it executable, and scheduled it with cron to run automatically every night at 2:00 AM, removing the need for manual backups.

## Objectives
- Understand the fundamental syntax of a Bash shell script, including variables and basic commands.
- Use nano to write and save executable scripts.
- Modify Linux file permissions using chmod.
- Understand task scheduling and the syntax of a Linux crontab.
- Document automation code and cron job configurations.
- Complete the final chapter of my GitHub Cloud Computing Portfolio.

## Commands Executed
- `mkdir app-data`
- `echo "This is critical client data." > app-data/data.txt`
- `nano backup.sh`
- `./backup.sh`
- `chmod +x backup.sh`
- `ls -l backups/`
- `crontab -l`
- `env EDITOR=nano crontab -e`

## Skills Learned
- Writing a Bash script with variables, commands, and comments.
- Understanding the shebang line and how scripts are interpreted.
- Using chmod to manage file execute permissions.
- Compressing directories into a tarball with tar.
- Scheduling recurring tasks with cron and understanding its five time-fields.
- Documenting automation workflows so another engineer could reproduce them.
