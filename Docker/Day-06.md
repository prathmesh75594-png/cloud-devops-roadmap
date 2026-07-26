# Docker Day 6 - Docker Networking

## Topics Learned

- Docker Networks
- Bridge Network
- Custom Bridge Network
- Docker DNS
- Container Communication
- docker exec
- docker network inspect

---

## Commands Used

```bash
docker network ls
docker network create devops-network
docker network inspect devops-network
docker run -dit --name container1 --network devops-network ubuntu
docker run -dit --name container2 --network devops-network ubuntu
docker exec -it container1 bash
ping container2
getent hosts container2
docker ps
```

---

## Networking Diagram

```
           Docker Host
                │
      -----------------------
      │                     │
 Container1          Container2
      │                     │
      └──── Docker DNS ─────┘
             │
       devops-network
```

---

## Important Concepts

### Docker Network
A Docker network allows containers to communicate securely.

### Bridge Network
The default network driver used by Docker.

### Custom Bridge Network
A user-created network that enables automatic DNS-based communication.

### Docker DNS
Docker automatically converts container names into IP addresses.

Example:

container2 → 172.18.0.3

---

## Interview Questions

### 1. What is Docker Networking?

Docker Networking allows containers to communicate with each other and external systems.

### 2. Why create a custom network?

To allow secure communication and automatic name resolution between containers.

### 3. What is Docker DNS?

Docker DNS automatically resolves container names to IP addresses.

### 4. Which command creates a Docker network?

```bash
docker network create devops-network
```

### 5. Which command lists Docker networks?

```bash
docker network ls
```

---

## Quiz

Q1. Which component resolves container names?

Answer: Docker DNS

Q2. Does Docker store all container names in /etc/hosts?

Answer: No

Q3. Which command verifies Docker DNS?

```bash
getent hosts container2
```

---

## Key Takeaways

- Containers can communicate using names.
- Docker has an internal DNS server.
- Custom bridge networks are preferred over the default bridge.
- Docker Networking is an important DevOps interview topic.
