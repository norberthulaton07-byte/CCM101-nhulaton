## Mission Overview

Congratulations! Your flawless work in deploying data storage solutions has earned you a spot on the
Cloud Deployment Team at CloudNova Technologies.
Up until now, you have been deploying single containers (like a standalone web server or a storage
bucket). However, real-world enterprise applications are rarely just one container. They are "multi-tier" systems
that require a frontend web application communicating seamlessly with a backend database. Deploying these
one by one manually is prone to error.
Enter Docker Compose. In this mission, you will transition from manual commands to Infrastructure
as Code (IaC). Using a YAML configuration file, you will define a multi-container private cloud storage application
(Nextcloud and MariaDB) and deploy the entire stack simultaneously with a single command!
Remember: A junior engineer deploys servers by typing commands; a senior engineer deploys
infrastructure by writing code.

## Mission Objectives
At the end of this laboratory activity, you should be able to:
- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a docker-compose.yml file.
- Use a Linux command-line text editor (nano) to create configuration files.
- Deploy a multi-container application (Nextcloud + Database) using Docker Compose.
- Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown.
- Continue expanding your professional GitHub Cloud Computing Portfolio. 

## Commands Executed

**Setting up the repository folder**

```bash
git clone https://github.com/norberthulaton07-byte/CCM101-nhulaton.git
mkdir -p Laboratory-06-Cloud-Deployment-Engineer/screenshots
touch README.md multi-tier-architecture.md docker-compose-guide.md reflection.md
git add .
git commit -m "Add Laboratory-06-Cloud-Deployment-Engineer folder structure"
git push origin main
```

**Writing and deploying the infrastructure**

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
```

**Shutting down**

```bash
docker-compose down
```

## Skills Learned

- Understanding two-tier architecture and why separating the application and database layers makes a system easier to manage and more secure.
- Writing a Docker Compose file in YAML, including how strict its indentation is.
- Running a multi-container application with a single command.
- Using service names and environment variables so containers can find each other on the same network.
- Checking container status and exposing a service through a port.
- Cleaning up a deployment with `docker-compose down`.
- Writing technical documentation and organizing work in a GitHub repository.
