# Docker & Docker Compose Cheat Sheet

## Introduction

Docker is a powerful tool that allows developers to create, deploy, and run applications in containers. It simplifies the process of managing dependencies and ensures that your application runs the same in any environment. Docker Compose, on the other hand, is a tool for defining and running multi-container Docker applications. This cheat sheet is designed for beginners and early programmers to get started with Docker and Docker Compose.

---

## Docker Commands

### Basic Commands

- `docker version`  Displays the Docker version installed on your system.
  
- `docker info`  Shows system-wide information about Docker.

- `docker help`  Lists available Docker commands and options.

- `docker run <image_name>`  Creates and starts a container from an image.

- `docker ps` Lists all running containers.

- `docker ps -a` Lists all containers, including stopped ones.

- `docker stop <container_id>` Stops a running container.

- `docker start <container_id>` Starts a running container.

- `docker rm <container_id>` Removes a stopped container.

- `docker exec -it <container_id> <command>` Executes a command inside a running container.

### Image Management
- `docker images` Lists all Docker images on your system.

- `docker pull <image_name>` Downloads a Docker image from a registry.

- `docker build -t <image_name>` Builds an image from a Dockerfile.

- `docker rmi <image_name>` Builds an image from a Dockerfile.

### Docker Networks
- `docker network ls` Lists all Docker networks.

- `docker network create  <network_name>` Creates a new Docker network.

- `docker network connect <network_name> <container_id>` Connects a container to a network.

### Docker Volumes
- `docker volume ls` Lists all Docker volumes.

- `docker volume create <volume_name>` Creates a new Docker volume.

- `docker volume rm <volume_name>` Removes a Docker volume.

### Docker Cleanup Commands
- `docker system prune` Cleans up unused containers, networks, images, and optionally volumes.

- `docker container prune` Removes all stopped containers.

- `docker volume prune` Removes all unused volumes.

- `docker network prune` Removes all unused networks.

## Docker Compose Commands
### Basic Commands
- `docker-compose version` Displays the Docker Compose version installed on your system.

- `docker-compose up` Builds, (re)creates, starts, and attaches to containers for a service.

- `docker-compose down` Stops and removes containers, networks, images, and volumes.

- `docker-compose start` Starts existing containers for a service.

- `docker-compose stop` Stops running containers without removing them.

- `docker-compose restart` Restarts containers.

- `docker-compose build` Builds or rebuilds services.

### Managing Containers
- `docker-compose ps` Lists containers.

- `docker-compose exec <service_name> <command>` Executes a command in a running container.

### Docker Compose Cleanup Commands
- `docker-compose rm` Removes stopped service containers.

- `docker-compose logs` Displays logs from services.

- `docker-compose logs -f` Follows log output.

---
## Conclusion
This cheat sheet provides a basic overview of essential Docker and Docker Compose commands, helping you get started with containerized applications. Whether you're a beginner or an early programmer, these commands will serve as a handy reference as you dive into the world of Docker.
