## Mission Overview

Congratulations! After successfully guiding our clients through multi-cloud evaluations, you have been
promoted to the Cloud-Native Engineering Team at CloudNova Technologies.
Modern cloud computing is no longer just about renting Virtual Machines (VMs) from AWS or Azure. Today's
enterprise applications are built using lightweight, portable, and lightning-fast technologies called Containers.
Your new mission is to understand the shift from traditional virtualization to containerization.
Using the KillerCoda Playground, you will step into the shoes of a Cloud-Native Engineer. You will research the
differences between VMs and containers, execute your very first Docker commands, and deploy a live,
containerized web server in seconds.
Remember: A traditional system administrator manages servers, but a cloud-native engineer manages
the services running on them.

## Mission Objectives

At the end of this laboratory activity, I should be able to:

- Differentiate between traditional Virtual Machines (VMs) and Containers.
- Access a Docker-enabled cloud environment using KillerCoda.
- Execute fundamental Docker CLI (Command Line Interface) commands.
- Pull, run, manage, and terminate a containerized application (Nginx).
- Create professional technical documentation of container operations using Markdown.
- Continue developing a well-organized GitHub Cloud Computing Portfolio.

## Docker Commands Executed

### Checkpoint 3 - Enter the Docker Playground

| Command | Purpose |
|---|---|
| `docker --version` | Verified that Docker is installed and showed its version. |
| `docker info` | Displayed the status of the Docker environment and daemon. |
| `docker ps` | Listed running containers (empty at this point). |

### Checkpoint 4 - Deploy Your First Container

| Command | Purpose |
|---|---|
| `docker pull nginx` | Downloaded the official Nginx image from Docker Hub. |
| `docker run -d --name my-nginx -p 8080:80 nginx` | Ran Nginx in detached mode and mapped host port 8080 to container port 80. |
| `docker ps` | Confirmed the `my-nginx` container was running. |
| `curl http://localhost:8080` | Returned the "Welcome to nginx!" HTML page, proving the web server worked. |

### Checkpoint 5 - The Container Lifecycle

| Command | Purpose |
|---|---|
| `docker ps` | Listed the running containers. |
| `docker stop my-nginx` | Stopped the running container. |
| `docker ps -a` | Verified the container was stopped (status: Exited). |
| `docker rm my-nginx` | Removed the container completely. |

## Skills Learned

- Explaining the differences between VMs and containers in terms of architecture, boot time, resource efficiency, and isolation.
- Launching and using a cloud-based Docker playground on KillerCoda.
- Pulling images from Docker Hub and running containers in detached mode.
- Mapping host ports to container ports with the `-p` flag.
- Testing a running web server from the terminal using `curl`.
- Managing the full container lifecycle: list, stop, verify, and remove.
- Writing technical documentation in Markdown, including tables and embedded screenshots.
- Organizing lab work in a GitHub repository with folders, commits, and pushes.

## Challenges Encountered

- **Temporary environment:** KillerCoda sessions do not save files, so I had to push my work to GitHub before closing the session.
- **GitHub authentication:** Pushing from the terminal required a Personal Access Token instead of my account password.
- **Repository structure:** I had to recreate the lab folder after it was deleted from the repository, and make sure the empty `screenshots` folder was tracked by adding a `.gitkeep` file.
- **Verifying a stopped container:** `docker ps` only shows running containers, so I learned to use `docker ps -a` to confirm the container had stopped.
