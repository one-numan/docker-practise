Docker Cheat Code
---

## 🐳 **Docker Installation & Setup**

```bash
docker --version            # Show Docker version
docker info                 # Show Docker system-wide information
```

---

## 📦 **Docker Images**

```bash
docker pull <image>                  # Download image from Docker Hub
docker build -t <name>:<tag> .       # Build image from Dockerfile
docker images                        # List all local images
docker rmi <image_id or name>        # Remove image
docker tag <image> <repo>:<tag>      # Tag an image
```

---

## 🏃‍♂️ **Docker Containers**

```bash
docker run <image>                              # Run container from image
docker run -it <image>                          # Run interactively (with terminal)
docker run -d <image>                           # Run in detached mode
docker run --name <name> <image>                # Run and name the container
docker run -p <host_port>:<container_port> ...  # Map ports
docker run -v <host_path>:<container_path> ...  # Mount volume
docker exec -it <container_id> /bin/bash        # Access container shell
docker start <container_id>                     # Start stopped container
docker stop <container_id>                      # Stop running container
docker restart <container_id>                   # Restart container
docker kill <container_id>                      # Kill container
docker rm <container_id>                        # Remove container
docker ps                                       # List running containers
docker ps -a                                    # List all containers
```

---

## 📝 **Dockerfile**

Used to automate image creation. Basic commands inside a Dockerfile:

```Dockerfile
FROM <base_image>           # Base image
COPY <src> <dest>           # Copy files
RUN <command>               # Run command during image build
CMD ["command"]             # Default command at container run
EXPOSE <port>               # Document port (used for -p)
ENV <key> <value>           # Set environment variable
WORKDIR <path>              # Set working directory
ENTRYPOINT ["command"]      # Entry point command
```

---

## 📂 **Volumes (Data Persistence)**

```bash
docker volume create <name>              # Create volume
docker volume ls                         # List volumes
docker volume inspect <name>             # View volume details
docker volume rm <name>                  # Remove volume
```

---

## 🌐 **Docker Networks**

```bash
docker network ls                        # List networks
docker network create <name>            # Create new network
docker network inspect <name>           # Show network details
docker network connect <network> <container>
docker network disconnect <network> <container>
docker network rm <name>                # Remove network
```

---

## 🧹 **Clean Up**

```bash
docker system prune                      # Remove unused data
docker image prune                       # Remove unused images
docker container prune                   # Remove stopped containers
docker volume prune                      # Remove unused volumes
```

---

## 🐳 **Docker Compose (Multi-container apps)**

```bash
docker-compose up                        # Start services
docker-compose up -d                     # Start in detached mode
docker-compose down                      # Stop and remove containers
docker-compose build                     # Build or rebuild services
docker-compose logs                      # Show logs
```

*`docker-compose.yml`* defines services, networks, volumes.

---

## 📤 **Export/Import**

```bash
docker save -o <file.tar> <image>        # Save image to tarball
docker load -i <file.tar>                # Load image from tarball
docker export <container> > file.tar     # Export container’s filesystem
docker import file.tar                   # Import as image
```

---

## 🔍 **Inspection & Logs**

```bash
docker inspect <container/image>         # Detailed info in JSON
docker logs <container_id>               # View container logs
```

---
