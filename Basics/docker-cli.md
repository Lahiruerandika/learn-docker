# 01 Basics - Docker CLI Essentials

## Introduction

Docker provides a powerful command-line interface (CLI) to interact with containers, images, networks, and volumes. Here are the essential commands to get started.

---

## System Information

- Check Docker version:
  ```bash
  docker --version
  ```

- Show Docker system info:
  ```bash
  docker info
  ```

- List all Docker commands:
  ```bash
  docker help
  ```

---

## Working with Images

- List local images:
  ```bash
  docker images
  ```

- Pull an image from Docker Hub:
  ```bash
  docker pull ubuntu
  ```

- Remove an image:
  ```bash
  docker rmi <image-name>
  ```

---

## Working with Containers

- List running containers:
  ```bash
  docker ps
  ```

- List all containers (including stopped):
  ```bash
  docker ps -a
  ```

- Start a container:
  ```bash
  docker start <container-id>
  ```

- Stop a container:
  ```bash
  docker stop <container-id>
  ```

- Remove a container:
  ```bash
  docker rm <container-id>
  ```

---

## Inspect & Logs

- View container logs:
  ```bash
  docker logs <container-id>
  ```

- Inspect container details:
  ```bash
  docker inspect <container-id>
  ```

---

## Executing Commands Inside a Container

- Interactive shell into a running container:
  ```bash
  docker exec -it <container-id> bash
  ```

---

## Clean Up

- Remove all stopped containers:
  ```bash
  docker container prune
  ```

- Remove all unused images:
  ```bash
  docker image prune
  ```

---

## What’s Next?

- Learn how Docker images are built  
- Write your first Dockerfile

---

*End of Docker CLI Guide*