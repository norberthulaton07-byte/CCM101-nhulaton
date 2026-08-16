## Mission Overview 
Congratulations! 
You have been accepted as a Junior Cloud Infrastructure Engineer Trainee at CloudNova Technologies, a 
company specializing in cloud infrastructure, virtualization, and enterprise cloud solutions. 
As part of your onboarding process, you must complete your first mission. Before deploying cloud services or 
managing enterprise infrastructures, every cloud engineer must first learn how to work inside a Linux 
environment, document their work professionally, and maintain a version-controlled portfolio using GitHub. 
Your task is to complete the onboarding mission using the KillerCoda Playground and create your personal 
Cloud Computing Portfolio on GitHub. This portfolio will serve as your professional workspace throughout the 
semester and will be updated after every laboratory activity. 
Complete each checkpoint carefully. Every completed task represents a real-world responsibility of a cloud 
engineer.

## Mission Objectives 
Upon successful completion of this mission, you should be able to: 
* Access a cloud-based Linux environment using KillerCoda.  
* Explore and navigate the Linux operating system.  
* Gather basic system information.  
* Organize files and directories using Linux commands.  
* Create and maintain a professional GitHub repository.  
* Document technical work using Markdown.  
* Demonstrate proper documentation practices used by cloud professionals.

## Activities Performed 
1. Explored the Linux Playground environment (OS version, kernel, CPU, memory, disk usage)
2. Created a new user (nhulaton) with home directory, Bash shell, and sudo privileges
3. Logged into the new user account and verified username, working directory, and hostname
4. Created a project folder structure (CCM101-nhulaton) with subfolders and files for the lab
5. Initialized a Git repository, configured Git identity, staged and committed files
6. Connected the local repo to a GitHub remote and pushed the project
7. Ran into and resolved several Git errors (see mistakes below) before successfully pushing to GitHub

## Linux Commands Used  
sudo adduser (username) - to create a new user
sudo usermod -aG sudo (username) - to give the new user sudo privileges
su - (username) - to switch to the new user account
whoami - to show the current username
pwd - to show the current working directory
hostname - to show the system hostname
cat /etc/os-release – checked OS name and version (Ubuntu 24.04.4 LTS)
uname -r – checked kernel version
lscpu – viewed CPU architecture and specs
free -h – checked memory (RAM/swap) usage
df -h – checked disk space usage
mkdir – created directories (project and subfolders)
cd – navigated between directories
touch – created empty files (README.md, about-me.md, etc.)
ls -R – listed directory contents recursively to confirm structure
git init – initialized a Git repository
git config --global user.email / user.name – set Git identity
git add . – staged all files
git commit -m "..." – committed changes with a message
git branch -M main – renamed branch to main
git remote add origin <url> – linked local repo to GitHub repository
git push -u origin main – pushed local commits to GitHub
git status – checked repo/staging status
git log --oneline – viewed commit history

## Skills Learned
- How to inspect a Linux system's OS, kernel, CPU, memory, and disk info
- How to create a new user with proper privileges and switch into that account
- How to structure a project directory using mkdir and touch
- How to initialize and configure a Git repository from scratch
- Understanding Git's requirement for a configured identity before committing
- How to diagnose and fix common Git errors (auth failures, wrong remote names, refspec mismatches, unrelated histories)
- How to correctly authenticate to GitHub over HTTPS using a personal access token at the password prompt (not typed as a command)
- The importance of double-checking command syntax (spacing, placeholders, exact usernames) before running it
