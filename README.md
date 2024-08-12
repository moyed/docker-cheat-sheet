markdown
Copy code
Docker & Docker Compose Cheat Sheet

Introduction

Docker is a powerful tool that allows developers to create, deploy, and run applications in containers. It simplifies the process of managing dependencies and ensures that your application runs the same in any environment. Docker Compose, on the other hand, is a tool for defining and running multi-container Docker applications. This cheat sheet is designed for beginners and early programmers to get started with Docker and Docker Compose.

---

Docker Commands

Basic Commands

docker version
  Displays the Docker version installed on your system.
bash
  docker version
docker info
Shows system-wide information about Docker.

bash
Copy code
docker info
docker help
Lists available Docker commands and options.

bash
Copy code
docker help
Container Management
docker run
Creates and starts a container from an image.

bash
Copy code
docker run <image_name>
docker ps
Lists all running containers.

bash
Copy code
docker ps
docker ps -a
Lists all containers, including stopped ones.

bash
Copy code
docker ps -a
docker stop
Stops a running container.

bash
Copy code
docker stop <container_id>
docker start
Starts a stopped container.

bash
Copy code
docker start <container_id>
docker rm
Removes a stopped container.

bash
Copy code
docker rm <container_id>
docker exec
Executes a command inside a running container.

bash
Copy code
docker exec -it <container_id> <command>
Image Management
docker images
Lists all Docker images on your system.

bash
Copy code
docker images
docker pull
Downloads a Docker image from a registry.

bash
Copy code
docker pull <image_name>
docker build
Builds an image from a Dockerfile.

bash
Copy code
docker build -t <image_name> .
docker rmi
Removes a Docker image.

bash
Copy code
docker rmi <image_name>
Docker Networks
docker network ls
Lists all Docker networks.

bash
Copy code
docker network ls
docker network create
Creates a new Docker network.

bash
Copy code
docker network create <network_name>
docker network connect
Connects a container to a network.

bash
Copy code
docker network connect <network_name> <container_id>
Docker Volumes
docker volume ls
Lists all Docker volumes.

bash
Copy code
docker volume ls
docker volume create
Creates a new Docker volume.

bash
Copy code
docker volume create <volume_name>
docker volume rm
Removes a Docker volume.

bash
Copy code
docker volume rm <volume_name>
Docker Cleanup Commands
docker system prune
Cleans up unused containers, networks, images, and optionally volumes.

bash
Copy code
docker system prune
docker container prune
Removes all stopped containers.

bash
Copy code
docker container prune
docker volume prune
Removes all unused volumes.

bash
Copy code
docker volume prune
docker network prune
Removes all unused networks.

bash
Copy code
docker network prune
Docker Compose Commands
Basic Commands
docker-compose version
Displays the Docker Compose version installed on your system.

bash
Copy code
docker-compose version
docker-compose up
Builds, (re)creates, starts, and attaches to containers for a service.

bash
Copy code
docker-compose up
docker-compose down
Stops and removes containers, networks, images, and volumes.

bash
Copy code
docker-compose down
docker-compose start
Starts existing containers for a service.

bash
Copy code
docker-compose start
docker-compose stop
Stops running containers without removing them.

bash
Copy code
docker-compose stop
docker-compose restart
Restarts containers.

bash
Copy code
docker-compose restart
docker-compose build
Builds or rebuilds services.

bash
Copy code
docker-compose build
Managing Containers
docker-compose ps
Lists containers.

bash
Copy code
docker-compose ps
docker-compose exec
Executes a command in a running container.

bash
Copy code
docker-compose exec <service_name> <command>
Docker Compose Cleanup Commands
docker-compose rm
Removes stopped service containers.

bash
Copy code
docker-compose rm
docker-compose logs
Displays logs from services.

bash
Copy code
docker-compose logs
docker-compose logs -f
Follows log output.

bash
Copy code
docker-compose logs -f
Conclusion
This cheat sheet provides a basic overview of essential Docker and Docker Compose commands, helping you get started with containerized applications. Whether you're a beginner or an early programmer, these commands will serve as a handy reference as you dive into the world of Docker.
