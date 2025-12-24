# Docker:

## Docker Commands Cheat Sheet

| Command | CLI |
|---------|-----|
| Show Docker version | `docker version` |
| Show system info | `docker info` |
| List images | `docker image ls` |
| Pull image | `docker image pull nginx:latest` |
| Build image | `docker build -t myapp:dev .` |
| Remove image | `docker image rm myapp:dev` |
| Run container (interactive) | `docker container run -it ubuntu:22.04 bash` |
| Run detached with ports | `docker container run -d --name web -p 8080:80 nginx` |
| List running containers | `docker container ls` |
| List all containers | `docker container ls -a` |
| Stop container | `docker container stop web` |
| Start container | `docker container start web` |
| Restart container | `docker container restart web` |
| Remove container | `docker container rm web` |
| Show logs (follow) | `docker logs -f web` |
| Inspect container | `docker container inspect web` |
| Exec into container | `docker exec -it web bash` |
| List volumes | `docker volume ls` |
| Prune unused data | `docker system prune` |
| Prune unused images | `docker image prune` |
| Compose up (detached) | `docker compose up -d` |
| Compose logs | `docker compose logs -f` |
| Compose down | `docker compose down` |
