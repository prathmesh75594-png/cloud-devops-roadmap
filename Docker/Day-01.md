# Docker Day 1

## Topics Covered

- Introduction to Docker
- Why Docker is used
- Containers vs Virtual Machines
- Docker Images
- Docker Containers
- Docker Hub
- Docker Daemon

## Commands Practiced

```bash
docker --version
docker info
docker run hello-world
docker images
docker ps -a
docker rm <container_id>
```

## What I Learned

- Docker packages applications and dependencies into portable containers.
- Images are templates.
- Containers are running instances of images.
- Docker downloads images from Docker Hub if they are not available locally.

## Interview Question

**Q:** What happens when you run `docker run hello-world`?

**Answer:** Docker checks for the image locally, downloads it from Docker Hub if necessary, creates a container, runs it, prints the output, and exits.
