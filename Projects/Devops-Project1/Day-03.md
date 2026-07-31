# Day 3 - Docker Container Management

## Objective

Learn how to manage and troubleshoot Docker containers.

## Commands Learned

### List Running Containers

```bash
docker ps
```

### List All Containers

```bash
docker ps -a
```

### Inspect Container

```bash
docker inspect devops-container
```

### View Logs

```bash
docker logs devops-container
```

### Stop Container

```bash
docker stop devops-container
```

### Start Container

```bash
docker start devops-container
```

### Restart Container

```bash
docker restart devops-container
```

### Enter Running Container

```bash
docker exec -it devops-container /bin/bash
```

### Remove Container

```bash
docker rm devops-container
```

## Concepts Learned

- Container lifecycle
- Inspecting containers
- Viewing logs
- Starting and stopping containers
- Restarting containers
- Accessing a running container
- Removing containers
- Difference between Image and Container

## Interview Questions

### Difference between docker run and docker start

- `docker run` creates a new container and starts it.
- `docker start` starts an existing stopped container.

### Difference between docker stop and docker rm

- `docker stop` stops a container.
- `docker rm` deletes a container.

### Does docker rm delete the image?

No. It only removes the container.

## Outcome

Successfully managed Docker containers, inspected them, viewed logs, entered a running container, and removed containers.
