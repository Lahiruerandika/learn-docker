# 01 Basics - Installing Docker

This guide covers how to install Docker on the three major platforms: **Linux**, **Windows**, and **macOS**.

---

## Installing Docker on Linux

Docker supports many Linux distributions. Below are instructions for **Ubuntu** and **CentOS** as examples.

### Ubuntu

1. **Update existing packages:**

   ```bash
   sudo apt update
   sudo apt upgrade -y
   ```

2. **Install prerequisites:**

   ```bash
   sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
   ```

3. **Add Docker’s official GPG key:**

   ```bash
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   ```

4. **Add Docker repository:**

   ```bash
   echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```

5. **Update package list and install Docker:**

   ```bash
   sudo apt update
   sudo apt install -y docker-ce docker-ce-cli containerd.io
   ```

6. **Verify Docker is installed:**

   ```bash
   sudo systemctl status docker
   ```

7. **(Optional) Run Docker without sudo:**

   ```bash
   sudo usermod -aG docker $USER
   ```

   Log out and back in for group changes to take effect.

---

### CentOS

1. **Remove old Docker versions:**

   ```bash
   sudo yum remove docker                    docker-client                    docker-client-latest                    docker-common                    docker-latest                    docker-latest-logrotate                    docker-logrotate                    docker-engine
   ```

2. **Set up repository:**

   ```bash
   sudo yum install -y yum-utils
   sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
   ```

3. **Install Docker:**

   ```bash
   sudo yum install -y docker-ce docker-ce-cli containerd.io
   ```

4. **Start Docker service:**

   ```bash
   sudo systemctl start docker
   sudo systemctl enable docker
   ```

5. **Verify Docker status:**

   ```bash
   sudo systemctl status docker
   ```

---

## Installing Docker on Windows

- Download and install **Docker Desktop for Windows** from the official site:  
  [https://docs.docker.com/desktop/install/windows-install/](https://docs.docker.com/desktop/install/windows-install/)

- System requirements: Windows 10 64-bit: Pro, Enterprise, or Education (Build 19041 or later)

- After installation, launch Docker Desktop and verify it is running.

---

## Installing Docker on macOS

- Download and install **Docker Desktop for Mac** from the official site:  
  [https://docs.docker.com/desktop/install/mac-install/](https://docs.docker.com/desktop/install/mac-install/)

- System requirements: macOS must be version 10.15 or newer.

- After installation, launch Docker Desktop and verify it is running.

---

## Verifying the Installation

Once installed, confirm Docker is working by opening a terminal or command prompt and running:

```bash
docker --version
```

You should see the installed Docker version displayed.

---

## What's Next?

- Learn basic Docker commands  
- Run your first container  
- Write a simple Dockerfile  

---

*End of Installation Guide*