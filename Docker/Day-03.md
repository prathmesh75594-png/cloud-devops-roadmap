# 🐳 Docker Day 3

## 📚 Topics Learned

- What is a Dockerfile?
- Dockerfile Instructions
- FROM
- RUN
- CMD
- docker build
- docker run
- Difference between Image and Container

---

## 📝 Dockerfile Used

```dockerfile
FROM ubuntu

RUN apt update

CMD ["echo", "Hello Prathmesh! This is my first Docker Image."]
```

---

## ⚙️ Commands Practiced

```bash
docker build -t myfirstimage .
```

Builds a Docker image from the Dockerfile.

```bash
docker run myfirstimage
```

Runs a container from the image.

```bash
docker images
```

Shows all Docker images.

```bash
docker ps -a
```

Shows all containers.

---

## 💡 Important Concepts

### What is a Dockerfile?

A Dockerfile is a text file that contains instructions to build a Docker image.

Think of it like a **recipe** for creating an image.

---

### Docker Build Process

Docker reads the Dockerfile from top to bottom.

```
Dockerfile
      │
      ▼
docker build
      │
      ▼
Docker Image
      │
      ▼
docker run
      │
      ▼
Container
```

---

## 🔥 Image vs Container

| Image | Container |
|--------|-----------|
| Blueprint | Running application |
| Read-only | Writable |
| Can create many containers | Created from one image |
| Stored permanently | Can be started or stopped |

---

## 🎯 Interview Questions

### Q1. What is Dockerfile?

**Answer:**
A Dockerfile is a text file that contains instructions to automatically build a Docker image.

---

### Q2. What does FROM do?

**Answer:**
FROM specifies the base image on which our image is built.

Example:

```dockerfile
FROM ubuntu
```

---

### Q3. What is RUN?

**Answer:**
RUN executes commands while building the image.

Example:

```dockerfile
RUN apt update
```

---

### Q4. What is CMD?

**Answer:**
CMD specifies the default command that runs when the container starts.

Example:

```dockerfile
CMD ["echo","Hello"]
```

---

### Q5. Difference between RUN and CMD?

RUN → Executes during image build.

CMD → Executes when the container starts.

---

### Q6. What does docker build do?

**Answer:**
It reads the Dockerfile and creates a Docker image.

---

### Q7. What does docker run do?

**Answer:**
It creates and starts a container from an image.

---

## ⭐ Key Takeaways

- Dockerfile is a recipe for creating images.
- docker build creates an image.
- docker run creates a container.
- FROM defines the base image.
- RUN executes commands during build.
- CMD runs when the container starts.
