#  Docker Cheat Sheet

## 🔹 Container Commands
```bash
docker run -it image_name            # Run container interactive
docker run -d image_name             # Run container detached
docker ps                            # List running containers
docker ps -a                         # List all containers
docker stop container_id             # Stop container
docker rm container_id               # Remove container
docker exec -it container_id bash    # Enter container shell
docker logs container_id             # View logs
```

---

## 🔹 Image Commands
```bash
docker build -t name:tag .           # Build image
docker images                        # List images
docker rmi image_id                  # Remove image
docker pull image                    # Pull from Docker Hub
docker push repo/image:tag           # Push image
docker tag image repo/image:tag      # Tag image
```

---

## 🔹 Volume Commands
```bash
docker volume create vol_name        # Create volume
docker volume ls                     # List volumes
docker volume inspect vol_name       # Inspect volume
docker volume rm vol_name            # Remove volume
```

---

## 🔹 Network Commands
```bash
docker network create net_name       # Create network
docker network ls                    # List networks
docker network inspect net_name      # Inspect network
docker network connect net container # Connect container
```

---

## 🔹 Docker Compose Commands
```bash
docker compose up -d                 # Start services
docker compose down                 # Stop services
docker compose ps                   # List services
docker compose logs                 # View logs
docker compose build                # Build services
```

---

## 🔹 Cleanup Commands
```bash
docker system prune -a              # Remove unused data
docker volume prune                 # Remove unused volumes
docker network prune                # Remove unused networks
docker system df                    # Check disk usage
```

---

## 🔹 Dockerfile Instructions
```text
FROM        Base image
RUN         Execute command
COPY        Copy files
WORKDIR     Set working directory
EXPOSE      Expose port
CMD         Default command
ENTRYPOINT  Fixed command
```

---

## 🔹 Quick Tips
```text
-p 8080:80 → Host:Container port mapping  
--name → Assign container name  
-e → Environment variable  
-v → Volume mount  
```
