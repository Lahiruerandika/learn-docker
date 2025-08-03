# 01 Basics - Running Your First Docker Container

## Introduction

Now that Docker is installed, let's run your first container and understand what happens behind the scenes.

---

## What is a Docker Container?

A **container** is a lightweight, standalone, executable package that includes everything needed to run a piece of software — code, runtime, libraries, and settings.

---

## Understanding the Hello World Example (Conceptually)

Docker provides a special image called `hello-world` designed to test if your Docker installation is working properly. While we won't run it here, here's what it does conceptually:

- It checks if Docker can download an image from Docker Hub.
- It spins up a container based on that image.
- The container prints a welcome message and exits.

This is useful as a basic sanity check after installation.

---

## What Happens Internally?

When you run a container:

1. Docker checks if the image is available locally.
2. If not, it pulls the image from Docker Hub.
3. It creates a new container from the image.
4. It runs the container's default command.
5. The container performs its task and exits.

---

## What’s Next?

- Learn key Docker CLI commands  
- Understand how to use images and containers  
- Write your first custom Dockerfile

---

*End of Hello World Overview*