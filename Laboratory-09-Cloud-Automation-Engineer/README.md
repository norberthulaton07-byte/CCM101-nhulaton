# Laboratory 09 - Cloud Automation Engineer

## Mission Overview
In this laboratory, I acted as a Cloud Automation Engineer for CloudNova Technologies. The mission was to replace a manual backup process with an automated one by writing a Bash backup script and scheduling it with a cron job, so client data is protected every night without human effort.

## Objectives
- Research and explain Bash scripts, variables, and cron jobs.
- Create dummy client data to represent the data being protected.
- Write a Bash script that compresses the data into a timestamped `.tar.gz` backup.
- Grant execute permission to the script using `chmod`.
- Schedule the script to run automatically every night at 2:00 AM using cron.
- Document the solution for the client's IT team.

## Commands Executed
```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
./backup.sh                  # Permission denied (expected)
chmod +x backup.sh
./backup.sh                  # Runs successfully
ls -l backups/
crontab -l
env EDITOR=nano crontab -e
crontab -l
git add .
git commit -m "Add Laboratory-09-Cloud-Automation-Engineer"
git push origin main
```

## Skills Learned
- Writing and running Bash scripts on Linux
- Using variables to make scripts cleaner and easier to maintain
- Managing file permissions with `chmod`
- Creating compressed archives with `tar`
- Scheduling recurring tasks with cron and reading cron expressions
- Documenting technical work clearly for a client
- Using Git and GitHub to commit and push work
