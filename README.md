# Multi-tier-Architecture-of-Blogging-site-using-Docker-Automation-docker-compose
## Global Blogging Made Easy with Docker and WordPress

* Setup:
  An AWS EC2 instance running Amazon Linux (AMI) is used as the operating system for Docker. Docker Compose is installed manually on this instance.

* Understanding the Three-Tier Architecture:

1.Application Layer: WordPress is used to power the blogging platform.

2.Database Layer: MySQL serves as the backend database for storing WordPress content and user data.

3.Network Layer: A Docker network is present to enable communication between the WordPress and MySQL containers securely and efficiently.

## Step: 1 [Install Docker & start Docker Service]
Docker-comopse work on Docker Engine, So we need to install Docker & Start the Docker Services.

### Install Docker Command:

      yum install docker
### Start Docker service Command:

    systemctl start docker
    systemctl status docker
## Step:2- [Install Docker-compose]

**Docker Compose**
Docker Compose is a tool that enables automation in managing Docker containers. It allows you to define and run multi-container Docker applications using a configuration file written in YAML.

* The automation file must be written in **YAML** format.
* The standard file name for Docker Compose is:
  **`docker-compose.yml`**

---

**Steps to Install Docker Compose:**

1. To download Docker Compose, search on Google:
   **"docker-compose standalone: https://docs.docker.com/compose/install/standalone/"**

2. Alternatively, use the official standalone installation link:
   **Docker Compose Standalone Install Link –** *Docker-compose-download-link*


