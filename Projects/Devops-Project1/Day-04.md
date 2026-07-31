# Day 4 - Docker Volumes

## Objective

Learn how Docker Volumes provide persistent storage.

## Commands Learned

### List Volumes

```bash
docker volume ls
```

### Create Volume

```bash
docker volume create devops-volume
```

### Inspect Volume

```bash
docker volume inspect devops-volume
```

### Run Container with Volume

```bash
docker run -it --name volume-demo -v devops-volume:/data ubuntu /bin/bash
```

### Remove Container

```bash
docker rm volume-demo
```

## Concepts Learned

- Docker Volumes
- Persistent Storage
- Mount Points
- Data Persistence
- Volume Reuse

## Practical

1. Created a Docker Volume.
2. Mounted it inside a container.
3. Created `message.txt` in the volume.
4. Removed the container.
5. Created a new container with the same volume.
6. Verified that `message.txt` still existed.

## Interview Questions

### What is a Docker Volume?

A Docker Volume stores persistent data outside the container.

### Why use Docker Volumes?

To preserve application data even when containers are removed.

### Does deleting a container delete the volume?

No. The volume remains until it is explicitly removed.

## Outcome

Successfully demonstrated persistent storage using Docker Volumes.
