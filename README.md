# Multi-tier-Architecture-of-Blogging-site-using-Docker-Automation-docker-compose
## Global Blogging Made Easy with Docker and WordPress

* Setup:
  An AWS EC2 instance running Amazon Linux (AMI) is used as the operating system for Docker. Docker Compose is installed manually on this instance.
<img width="1863" height="757" alt="Screenshot 2025-06-07 231058" src="https://github.com/user-attachments/assets/e36d46bb-8024-4169-aae2-9e0652f44912" />

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
docker-compose version
```

   <img width="1089" height="414" alt="Screenshot 2025-06-07 222114" src="https://github.com/user-attachments/assets/e6d28a1c-bc35-4b35-9440-d4cbd6a9bd3d" />

   **Step 2 – [Creating `docker-compose.yml` Automation File]**

First, create two directories:

* One for **MySQL database volume** (to persist data)
* Another for the **Docker Compose code**

---
<img width="743" height="190" alt="Screenshot 2025-09-15 222218" src="https://github.com/user-attachments/assets/2a107f2b-1948-41c8-86c4-d22f374d12f0" />


**Docker Compose Code File (`docker-compose.yml`)**
Docker Compose uses **YAML (Yet Another Markup Language)** syntax for its configuration file.

> Docker Compose DSL (Domain-Specific Language) is written in YAML.

<img width="1532" height="670" alt="Screenshot 2025-09-15 224909" src="https://github.com/user-attachments/assets/df944d74-36d7-4d81-9733-a8d79e948c93" />

---

**To view the docker-compose file:**
Use any text editor like `cat`, `nano`, or `vi`:

```bash
cat docker-compose.yml
```
<img width="1810" height="652" alt="Screenshot 2025-09-15 225154" src="https://github.com/user-attachments/assets/4b421907-7a6d-4517-827b-3fa8fccc55fa" />

---

**To run the Docker Compose setup:**

```bash
docker-compose up -d
```

* The `-d` (detached mode) flag runs the containers in the background.
<img width="1528" height="526" alt="Screenshot 2025-06-07 231023" src="https://github.com/user-attachments/assets/44d5de33-dac8-4497-aca9-f2fdcac88243" />

> This command sets up the entire **(Multi)three-tier architecture** using Docker Compose.

---

**Useful Docker Compose Commands:**

* **To check which compose file/project launched containers:**

  ```bash
  docker-compose ls
  ```
<img width="843" height="97" alt="Screenshot 2025-09-15 225756" src="https://github.com/user-attachments/assets/80ab6e56-aea7-48ae-a46b-a59eb2e97203" />

* **To see running containers managed by Docker Compose:**

  ```bash
  docker-compose ps
  ```
<img width="1741" height="657" alt="Screenshot 2025-06-07 232051" src="https://github.com/user-attachments/assets/9557f07a-7dec-442b-b3b6-a01ba8772002" />

* **To view logs from containers:**

  ```bash
  docker-compose logs
  ```
<img width="1647" height="764" alt="Screenshot 2025-09-15 225939" src="https://github.com/user-attachments/assets/2adacade-c615-4b25-b456-9419d4675c0a" />

---

**Step 3 – [Accessing WordPress in the Browser]**

To access the WordPress site:

* Open your **web browser**
* Enter:
  **`http://<EC2-Public-IP>:<Port>`**
  <img width="935" height="882" alt="Screenshot 2025-06-07 231247" src="https://github.com/user-attachments/assets/a6e65086-baac-4e10-90d9-ebf59136a497" />

  <img width="1529" height="944" alt="Screenshot 2025-09-15 231243" src="https://github.com/user-attachments/assets/a28d1614-b72b-4709-a5f7-64c887cc71d7" />

  (Ensure the **port is open** in the EC2 **inbound security group rules**)
  <img width="1525" height="342" alt="Screenshot 2025-06-07 231359" src="https://github.com/user-attachments/assets/51806b14-c1a7-4c9a-94c4-c3b052a3f444" />


---

**What You’ll See:**
The WordPress setup interface will load in the browser via the provided IP and port.

---
<img width="1612" height="565" alt="Screenshot 2025-09-15 231416" src="https://github.com/user-attachments/assets/11017f77-6282-47fb-bb5e-88ea8a8212cd" />
<img width="1869" height="863" alt="Screenshot 2025-06-07 231622" src="https://github.com/user-attachments/assets/a097801c-8811-4ec1-92da-84ab2dfed46a" />

**About the Project**
This project sets up a **Global Blogging Site** using Docker Compose.

* **WordPress** – Blogging application
* **MySQL** – Database for WordPress
* **Docker Custom Network** – Enables secure container communication

---

**Topics Covered:**

* `docker`
* `wordpress`
* `docker-compose`
* `mysql-database`
* `aws-ec2`
* `docker-automation`
* `docker-compose-files`
* `docker-network-driver`





