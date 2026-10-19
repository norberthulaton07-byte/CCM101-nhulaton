# Automation Research

## Bash Script
A Bash script is a plain text file that contains a list of Linux commands, which the computer runs one after another so I don't have to type them manually. The `#!/bin/bash` line at the top is called the shebang. It tells the system to use the Bash program to run the file, so the commands are read and executed correctly.

## Variables
Programmers use variables like `$BACKUP_DIR` to store a value, such as a folder path, in one place and reuse it throughout the script. This saves time and prevents typing mistakes. If the folder path changes, I only update it once at the top of the script instead of fixing it on every line.

## Cron Job
A cron job is a task that Linux runs automatically on a schedule, such as every night at 2:00 AM or every Monday. It is essential for cloud operations because tasks like backups, log cleanup, and system updates need to happen regularly and reliably without anyone doing them by hand. This keeps cloud systems consistent and reduces human error.
