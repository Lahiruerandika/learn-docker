# 01 Basics - Dockerfile Basics

## What is a Dockerfile?

A **Dockerfile** is a text file that contains step-by-step instructions for building a Docker image.

---

## Basic Dockerfile Structure

```Dockerfile
# Use an official base image
FROM ubuntu:20.04

# Set environment variables
ENV DEBIAN_FRONTEND=noninteractive

# Install packages
RUN apt update && apt install -y nginx

# Copy application files
COPY . /usr/share/nginx/html

# Expose port
EXPOSE 80

# Define default command
CMD ["nginx", "-g", "daemon off;"]
```

---

## Common Dockerfile Instructions

- `FROM`: Base image to build upon.
- `RUN`: Execute commands in the image.
- `COPY`: Copy files from host to image.
- `ADD`: Like COPY but supports URLs and tar files.
- `EXPOSE`: Inform Docker which ports the container listens on.
- `CMD`: Default command to run when the container starts.
- `ENTRYPOINT`: Similar to CMD but more strict and used for wrapping scripts.

---

## Building a Docker Image

To build an image from a Dockerfile:

```bash
docker build -t my-nginx-image .
```

---

## Running the Built Image

```bash
docker run -p 8080:80 my-nginx-image
```

This maps port 80 inside the container to port 8080 on your host.

---

## What’s Next?

- Learn about Docker volumes and networking  
- Move on to multi-container setups with Docker Compose

---

*End of Dockerfile Basics*