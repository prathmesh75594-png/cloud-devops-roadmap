# Docker Day 4 - Docker Layers & Cache

## What I Learned

- Docker images are built in layers.
- Every Dockerfile instruction creates a new layer.
- Docker stores layers in cache.
- If only one instruction changes, Docker rebuilds only that layer.
- This makes Docker builds much faster.

---

## Dockerfile Used

```dockerfile
FROM ubuntu

RUN apt update

RUN apt install -y curl

CMD ["echo","Hello Prathmesh! Docker Cache Works"]
```

---

## Commands Practiced

```bash
docker build -t layerdemo .

docker run layerdemo
```

---

## Interview Questions

### What is a Docker Layer?

A Docker Layer is a read-only layer created by every instruction in a Dockerfile.

### What is Docker Cache?

Docker Cache stores previously built layers and reuses them if nothing has changed.

### Why is Docker Build Fast?

Docker reuses cached layers instead of rebuilding everything.

---

## Result

Successfully built and ran my Docker image using Docker cache.
