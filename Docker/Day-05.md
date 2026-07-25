# Docker Day 5 - Docker Volumes

## Topics Learned

- What is Docker Volume
- Persistent Storage
- Create Volume
- Inspect Volume
- Mount Volume
- Share Data Between Containers

## Commands

```bash
docker volume ls
docker volume create projectdata
docker volume inspect projectdata
docker run -it -v projectdata:/data ubuntu
docker rm <container_id>
docker volume rm projectdata
```

## Key Points

- Volume stores data outside the container.
- Data remains after container deletion.
- Multiple containers can use the same volume.
- Volumes are managed by Docker.

## Real-World Uses

- MySQL Database
- PostgreSQL
- MongoDB
- Jenkins
- WordPress
- Redis

## Interview Questions

### What is Docker Volume?

Persistent storage managed by Docker.

### Why use Docker Volumes?

To keep data safe even if containers are deleted.

### Can multiple containers share one volume?

Yes.

### Where are Docker Volumes stored?

On the Docker Host, outside the container.
