# Docker Cheat Sheet

## General

| Command | Description |
| ------- | ----------- |
| `docker system prune` | Remove all resources that are dangling (images, containers, volumes and networks). |
| `docker system prune -a` | Remove any stopped containers and all unused images (not just dangling images). |

## Image Management:

| Command | Description |
| ------- | ----------- |
| `docker images -a` | List all docker images. |
| `docker images -f dangling=true` | List all dangling docker images (images with no relation to tagged images). |
| `docker images purge` | Remove all dangling docker images. |
| `docker images -a | grep "pattern"` | List all docker images where their name matches the supplied pattern. |
| `docker images -a | grep "pattern" | awk '{print $3}' | xargs docker rmi` | Remove all docker images where their name matches the supplied pattern. |
| `docker rmi IMAGE` | Remove the docker images matching the supplied name of identifier. |
| `docker rmi $(docker images -a -q)` | Remove all docker images from the host. |

## Container management:

| Command | Description |
| ------- | ----------- |
| `docker ps` | List active docker containers. |
| `docker ps -a` | List all docker containers. |
| `docker start CONTAINER` | Start a docker container, where CONTAINER is the name or identifier of the container to be started. |
| `docker stop CONTAINER` | Stop a docker container, where CONTAINER is the name or identifier of the container to be stopped. |
| `docker rm CONTAINER` | Remove a docker container matching the supplied name or identifier. |
| `docker rm $(docker ps -a -f status=exited -q)` | Remove all docker containers. |
| `docker exec [OPTIONS] CONTAINER COMMAND [ARG...]` | Execute a command on a running container. For example to start an interactive bash shell on a container named “ubuntu_bash” run: `docker exec -it ubuntu_bash bash`. |

Useful links:

- Official documentation: https://docs.docker.com/
- Containerd website: https://containerd.io/
- Code repository: https://github.com/containerd/containerd