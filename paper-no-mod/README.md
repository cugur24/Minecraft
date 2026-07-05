# Minecraft Server Setup

This repository provides a streamlined configuration for a high-performance **PaperMC** Minecraft server, containerized with **Docker** for resource management and easy maintenance.

## Prerequisites
- **Docker** and **Docker Compose** installed on your host machine.
- A VPS or local machine with at least **2 Cores** and **4GB RAM**.
- Port `25565` opened in your firewall (TCP).

## Quick Start Guide

### 1. Configuration
The server is managed via `docker-compose.yml`. The provided configuration includes:
- **PaperMC** server type (optimized for performance).
- **Resource Limits:** Restricted to 2 cores and 4GB RAM to protect host stability.
- **Aikar's Flags:** Advanced Java garbage collection optimization.

### 2. Starting the Server
1. Clone this repository or copy the `docker-compose.yml` file to your server.
2. Navigate to the directory:
   ```bash
   cd /path/to/your/server
### 3. Start the container in detached mode:

Bash
docker-compose up -d
[cite: 1]

### 4. Follow the console logs to see the startup process:

```bash
docker-compose logs -f
```
[cite: 1]

Managing the Server
Granting Operator (OP) Status
To give yourself admin rights, run the following command from your host terminal:

```bash
docker exec minecraft-server rcon-cli op <YourMinecraftUsername>
```
[cite: 1]

Stopping the Server
To shut down the server gracefully:

```bash
docker-compose down
```
[cite: 1]

Updating the Server
To update the Docker image to the latest version, simply run:

```bash
docker-compose pull
docker-compose up -d
```
[cite: 1]