# Docker Deployment

## Container Lifecycle Commands

| Step | Command | What It Did |
|---|---|---|
| 1. List running containers | `docker ps` | Displayed all currently running containers along with their ID, image, status, and port mappings. |
| 2. Stop the running container | `docker stop my-nginx` | Gracefully shut down the running Nginx container so it no longer serves traffic. |
| 3. Verify it is stopped | `docker ps -a` | Listed all containers, including stopped ones, and showed my-nginx with an "Exited" status. |
| 4. Remove the container completely | `docker rm my-nginx` | Permanently deleted the stopped container so it no longer appears in the container list. |
