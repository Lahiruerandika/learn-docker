# 01 Basics - Introduction to Docker

## What is Docker?

Docker is an open-source platform designed to automate the deployment, scaling, and management of applications using containerization. Containers allow you to package an application with all its dependencies into a standardized unit for software development.

### Why Use Docker?

- **Consistency:** Run the same application environment anywhere — your laptop, servers, or the cloud.
- **Isolation:** Each container runs independently without interfering with others.
- **Lightweight:** Containers share the host OS kernel, making them more efficient than traditional virtual machines.
- **Portability:** Containers can run on any system with Docker installed.
- **Faster Deployment:** Quickly start, stop, and replicate containers.

## Key Concepts

- **Image:** A read-only template with instructions for creating a container.
- **Container:** A runnable instance of an image.
- **Docker Engine:** The core runtime that builds, runs, and manages containers.
- **Dockerfile:** A text file with instructions to build Docker images.
- **Docker Hub:** A public registry for sharing Docker images.

## Docker Architecture Overview

Docker uses a client-server architecture:

- **Docker Client:** The command-line interface (CLI) you interact with.
- **Docker Daemon:** Runs on the host machine and manages containers.
- **Docker Registry:** Stores Docker images (Docker Hub is the default public registry).

---

## What's Next?

- Installing Docker on your platform  
- Learning Docker CLI basics  
- Writing your first Dockerfile  

---

*End of Introduction*