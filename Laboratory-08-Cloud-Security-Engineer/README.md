# Laboratory 08 - Cloud Security Engineer

## Mission Overview
In this laboratory, I acted as a Cloud Security Engineer. I deployed a vulnerable Nginx web application in a Docker container on an Ubuntu server, then secured it using the UFW firewall. The mission was to apply the Principle of Least Privilege and a Default Deny policy so that only the traffic needed for administration and the web service could reach the server.

## Objectives
- Define key security concepts: Principle of Least Privilege, Attack Surface, and Default Deny Policy.
- Deploy a web application (Nginx) in a container on port 8080.
- Configure UFW to allow SSH and block all other incoming traffic by default.
- Open only the required port (8080/tcp) for legitimate web users.
- Verify the firewall rules and test access using curl.
- Document the configuration and results with screenshots.

## Commands Executed

    docker run -d --name secure-web-app -p 8080:80 nginx
    curl http://localhost:8080
    sudo ufw allow ssh
    sudo ufw default deny incoming
    sudo ufw default allow outgoing
    sudo ufw enable
    sudo ufw status verbose
    sudo ufw allow 8080/tcp
    sudo ufw status numbered
    curl -I http://localhost:8080

## Skills Learned
- Deploying and testing a containerized web server with Docker and curl.
- Configuring and managing a host firewall with UFW.
- Applying the Principle of Least Privilege and Default Deny in practice.
- Understanding how to reduce a virtual machine's attack surface.
- Avoiding lockouts by allowing SSH before enabling the firewall.
- Documenting security work clearly using Markdown and screenshots.

## Files in This Folder
- `security-audit-report.md` - security concepts and application deployment
- `firewall-configuration.md` - firewall commands and explanations
- `reflection.md` - lab reflection
- `screenshots/` - evidence of each step
