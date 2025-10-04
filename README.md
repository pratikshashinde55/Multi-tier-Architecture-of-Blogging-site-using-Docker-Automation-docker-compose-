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

 To download Docker Compose, search on Google:
   **"docker-compose standalone: https://docs.docker.com/compose/install/standalone/"**
   
   <img width="1713" height="822" alt="Screenshot 2025-06-07 222006" src="https://github.com/user-attachments/assets/8c5e1cab-1d57-432a-9a7e-80367447bafe" />

**Installing Docker Compose (Standalone Binary Method)**

To install Docker Compose on a Linux system, follow these steps:

---

**1. Download the Docker Compose Binary**
Use `curl` to download the Docker Compose binary directly into the `/usr/local/bin/` directory:

```bash
curl -SL https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
```

---

**2. Make the Docker Compose Binary Executable**
Grant executable permissions to the downloaded binary:

```bash
chmod +x /usr/local/bin/docker-compose
```

**Explanation:**

* `chmod`: Command used to change file permissions on Unix-like systems.
* `+x`: Adds execute permission, allowing the file to be run as a program.
* `/usr/local/bin/docker-compose`: The full path to the downloaded Docker Compose binary.

Once installed, you can verify the installation with:

```bash
docker-compose --version
```

   <img width="1089" height="414" alt="Screenshot 2025-06-07 222114" src="https://github.com/user-attachments/assets/e6d28a1c-bc35-4b35-9440-d4cbd6a9bd3d" />

   




