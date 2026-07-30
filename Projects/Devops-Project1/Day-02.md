# Day 2 - Dockerizing a Node.js Application

## Objective
Containerize a Node.js + Express application using Docker.

## Dockerfile

```dockerfile
FROM node:20

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node","app.js"]
```

## Commands Learned

### Build Docker Image

```bash
docker build -t devops-project1:v1 .
```

### List Images

```bash
docker images
```

### Run Container

```bash
docker run -d -p 3000:3000 --name devops-container devops-project1:v1
```

### List Running Containers

```bash
docker ps
```

### Test Application

```bash
curl http://localhost:3000
```

## Concepts Learned

- Dockerfile
- Docker Image
- Docker Container
- Port Mapping
- Image Build Process
- Container Deployment
- Running Node.js inside Docker

## Interview Questions

### Difference between Image and Container

Image = Blueprint

Container = Running instance of an image

### What does docker build do?

Creates a Docker image from a Dockerfile.

### What does docker run do?

Creates and starts a container from an image.

### What is EXPOSE?

Documents the port used by the application.

### What is CMD?

Specifies the default command executed when the container starts.

## Outcome

Successfully deployed a Dockerized Node.js application on an AWS EC2 instance and accessed it through the browser.
