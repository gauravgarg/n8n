# n8n Docker Installation on VM

This section describes how to install n8n on a VM using your own Dockerfile and `docker-compose.yml`.

## Prerequisites
- Ubuntu VM (cloud or local)
- SSH access
- Docker & Docker Compose installed
- Your custom `Dockerfile` and `docker-compose.yml` in the project directory

## Steps

1. **Update System**
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. **Install Docker & Docker Compose**
   ```bash
   sudo apt install docker.io docker-compose -y
   ```

3. **Copy your project files to the VM**
   - Ensure your `Dockerfile` and `docker-compose.yml` are present in the desired directory.

4. **Build and Start n8n using Docker Compose**
   ```bash
   cd /path/to/your/project
   sudo docker-compose up -d --build
   ```
   - This will build the image from your Dockerfile and start n8n in the background.

5. **Access n8n**
   - Open `http://<VM-Public-IP>:5678` in your browser.

## Notes
- For persistent data, configure volumes in your `docker-compose.yml`.
- Set environment variables in `docker-compose.yml` for production use.
- Secure your instance (firewall, HTTPS, authentication).

Refer to your `docker-compose.yml` and `Dockerfile` for custom configuration options.
