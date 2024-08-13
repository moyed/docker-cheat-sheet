# Docker & Docker Compose Cheat Sheet

## Introduction

Docker is a powerful tool that allows developers to create, deploy, and run applications in containers. It simplifies the process of managing dependencies and ensures that your application runs the same in any environment. Docker Compose, on the other hand, is a tool for defining and running multi-container Docker applications. This cheat sheet is designed for beginners and early programmers to get started with Docker and Docker Compose.

---

## Docker Commands

### Basic Commands

- `docker version`  Displays the Docker version installed on your system.
  ```bash
  docker version
        Client:
         Version:           26.1.4
         API version:       1.45
         Go version:        go1.21.11
         Git commit:        5650f9b
         Built:             Wed Jun  5 11:26:02 2024
         OS/Arch:           darwin/arm64
         Context:           desktop-linux
        
        Server: Docker Desktop 4.31.0 (153195)
         Engine:
          Version:          26.1.4
          API version:      1.45 (minimum version 1.24)
          Go version:       go1.21.11
          Git commit:       de5c9cf
          Built:            Wed Jun  5 11:29:12 2024
          OS/Arch:          linux/arm64
          Experimental:     false
         containerd:
          Version:          1.6.33
          GitCommit:        d2d58213f83a351ca8f528a95fbd145f5654e957
         runc:
          Version:          1.1.12
          GitCommit:        v1.1.12-0-g51d5e94
         docker-init:
          Version:          0.19.0
          GitCommit:        de40ad0
  
- `docker info`  Shows system-wide information about Docker.
```bash
  docker info
        Client:
           Version:    26.1.4
           Context:    desktop-linux
           Debug Mode: false
           Plugins:
            buildx: Docker Buildx (Docker Inc.)
              Version:  v0.14.1-desktop.1
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-buildx
            compose: Docker Compose (Docker Inc.)
              Version:  v2.27.1-desktop.1
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-compose
            debug: Get a shell into any image or container (Docker Inc.)
              Version:  0.0.32
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-debug
            dev: Docker Dev Environments (Docker Inc.)
              Version:  v0.1.2
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-dev
            extension: Manages Docker extensions (Docker Inc.)
              Version:  v0.2.24
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-extension
            feedback: Provide feedback, right in your terminal! (Docker Inc.)
              Version:  v1.0.5
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-feedback
            init: Creates Docker-related starter files for your project (Docker Inc.)
              Version:  v1.2.0
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-init
            sbom: View the packaged-based Software Bill Of Materials (SBOM) for an image (Anchore Inc.)
              Version:  0.6.0
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-sbom
            scout: Docker Scout (Docker Inc.)
              Version:  v1.9.3
              Path:     /Users/{youruser}/.docker/cli-plugins/docker-scout

          Server:
               Containers: 13
                Running: 1
                Paused: 0
                Stopped: 12
               Images: 26
               Server Version: 26.1.4
               Storage Driver: overlay2
                Backing Filesystem: extfs
                Supports d_type: true
                Using metacopy: false
                Native Overlay Diff: true
                userxattr: false
               Logging Driver: json-file
               Cgroup Driver: cgroupfs
               Cgroup Version: 2
               Plugins:
                Volume: local
                Network: bridge host ipvlan macvlan null overlay
                Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
               Swarm: inactive
               Runtimes: io.containerd.runc.v2 runc
               Default Runtime: runc
               Init Binary: docker-init
               containerd version: d2d58213f83a351ca8f528a95fbd145f5654e957
               runc version: v1.1.12-0-g51d5e94
               init version: de40ad0
               Security Options:
                seccomp
                 Profile: unconfined
                cgroupns
               Kernel Version: 6.6.31-linuxkit
               Operating System: Docker Desktop
               OSType: linux
               Architecture: aarch64
               CPUs: 4
               Total Memory: 7.658GiB
               Name: docker-desktop
               ID: 16d098b2-0c46-45c0-9131-3bbf94e8ee94
               Docker Root Dir: /var/lib/docker
               Debug Mode: false
               HTTP Proxy: http.docker.internal:3128
               HTTPS Proxy: http.docker.internal:3128
               No Proxy: hubproxy.docker.internal
               Labels:
                com.docker.desktop.address=unix:///Users/ansari/Library/Containers/com.docker.docker/Data/docker-cli.sock
               Experimental: false
               Insecure Registries:
                hubproxy.docker.internal:5555
                127.0.0.0/8
               Live Restore Enabled: false
              
              WARNING: daemon is not using the default seccomp profile

`docker help`
Lists available Docker commands and options.

`docker run`
Creates and starts a container from an image.

`docker run <image_name>`
docker ps
Lists all running containers.

`docker ps -a`
Lists all containers, including stopped ones.

`docker stop`
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
---
## Conclusion
This cheat sheet provides a basic overview of essential Docker and Docker Compose commands, helping you get started with containerized applications. Whether you're a beginner or an early programmer, these commands will serve as a handy reference as you dive into the world of Docker.
