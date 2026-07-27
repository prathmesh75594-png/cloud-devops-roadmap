# Docker Day 7

## Topics Learned

- Docker Compose
- docker-compose.yml
- Multi-container applications
- Nginx container
- MySQL container
- Starting multiple containers with one command

---

## What is Docker Compose?

Docker Compose is a tool used to define and manage multiple Docker containers using a single YAML file.

Instead of running many `docker run` commands, we define all services in one file and start them together.

---

## docker-compose.yml Structure

```yaml
version: "3.9"

services:
  web:
    image: nginx:latest
    container_name: webserver
    ports:
      - "8080:80"

  database:
    image: mysql:8
    container_name: mysql-db
    environment:
      MYSQL_ROOT_PASSWORD: root123
```

---

## Commands Learned

```bash
docker-compose up -d
docker-compose ps
docker-compose down
docker ps
```

---

## What We Built

- Nginx Web Server
- MySQL Database
- Multi-container application
- Managed both containers using Docker Compose

---

## Interview Questions

### 1. What is Docker Compose?

Docker Compose is a tool for defining and running multiple Docker containers using one YAML configuration file.

---

### 2. Why use Docker Compose?

To manage multiple containers with a single command.

---

### 3. Which file does Docker Compose use?

docker-compose.yml

---

### 4. What command starts all services?

```bash
docker-compose up -d
```

---

### 5. What command stops all services?

```bash
docker-compose down
```

---

## Key Takeaways

- One YAML file can define an entire application.
- Docker Compose simplifies multi-container deployments.
- Useful for development and testing environments.
- Commonly used in DevOps workflows.
