# Docker Deployment: Nginx Web Server

## Checkpoint 3: Verify Docker

```bash
docker --version
docker info
```

Screenshot: ![Docker version](screenshots/docker-version.png)

## Checkpoint 4: Deploy Nginx

```bash
docker pull nginx
docker run -d -p 8080:80 --name my-nginx nginx
curl http://localhost:8080
```

Screenshot: ![Nginx running](screenshots/nginx-running.png)

## Checkpoint 5: Container Lifecycle

| Step | Command | What it did |
|---|---|---|
| 1. List running containers | `docker ps` | Showed all currently running containers, including `my-nginx` and its port mapping. |
| 2. Stop the container | `docker stop my-nginx` | Gracefully stopped the running Nginx container. |
| 3. Verify it is stopped | `docker ps -a` | Listed all containers, including stopped ones, and showed `my-nginx` with an "Exited" status. |
| 4. Remove the container | `docker rm my-nginx` | Permanently deleted the stopped container from the system. |

Screenshot: ![Container lifecycle](screenshots/container-lifecycle.png)
