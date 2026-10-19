## Mission Overview 

Congratulations! Your ability to deploy multi-tier architectures has proven your technical capabilities.
You have now been promoted to the Cloud Operations Team (often referred to in the industry as Site Reliability
Engineering, or SRE) at CloudNova Technologies.
Deploying a cloud application is only the first step; keeping it running smoothly is the real challenge.
When a server crashes or a web page takes ten seconds to load, you cannot simply guess what is wrong. You
must rely on Observability and Monitoring to see inside your infrastructure.
Using the KillerCoda Playground, you will step into the role of a Cloud Operations Engineer. You will
establish a performance baseline for your Linux server, deploy a containerized application, generate artificial web
traffic, and hunt down performance metrics and system logs to prove the application is healthy.
Remember: A developer hopes the application works; a Site Reliability Engineer uses metrics and logs to
prove it.

## Mission Objectives

At the end of this laboratory activity, you should be able to:
- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container and track its real-time performance using Docker metrics.
- Generate web traffic and extract application access logs for analysis.
- Translate raw performance data into a readable technical report using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio. 

## Monitoring Commands Executed

| Command | What it does |
|---|---|
| `free -h` | Shows how much RAM the server has and how much is in use. |
| `df -h` | Shows disk space for each file system, including the root (/) file system. |
| `top` | Opens a live view of running processes and CPU load (I exited with `q`). |
| `docker run -d --name client-website -p 8080:80 nginx` | Starts the Nginx container in the background, names it `client-website`, and maps port 8080 to the container's port 80. |
| `docker ps` | Lists running containers so I could confirm `client-website` was up. |
| `curl http://localhost:8080` | Acts like a user visiting the website (I ran it three times). |
| `curl http://localhost:8080/hidden-admin-page` | Requests a page that doesn't exist to trigger a 404 error. |
| `docker logs client-website` | Shows the container's logs, including the 200 and 404 requests. |
| `docker stats` | Shows live CPU, memory, and network usage for the container. |

## Skills Learned

- Checking a server's RAM, disk, and CPU to set a baseline before deploying anything.
- Running and naming a Docker container and mapping ports from the host to the container.
- Generating test traffic with `curl` and telling successful requests (200) apart from errors (404).
- Reading Nginx access logs to trace what happened, which is a lot like watching security camera footage.
- Using `docker stats` to confirm a container isn't eating too much CPU or memory.
- Writing short, clear technical documentation, and saving evidence (screenshots) as I went.

## Folder Contents

- `system-baseline-report.md` - the host server's RAM, storage, and why disk space matters.
- `container-observability.md` - the log evidence and the container's live metrics.
- `reflection.md` - my thoughts on the lab.
- `screenshots/` - proof of each command's output.
