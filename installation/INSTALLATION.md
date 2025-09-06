# n8n Installation Guide

## 1. Local Installation (macOS/Linux/Windows)

**Prerequisites:**
- Node.js (v16+ recommended)
- npm (comes with Node.js)
- Optional: Docker

**Steps:**

1. **Install Node.js & npm**
   - Download from [nodejs.org](https://nodejs.org/) and follow the installer.

2. **Install n8n via npm**
   ```bash
   npm install n8n -g
   ```

3. **Start n8n**
   ```bash
   n8n
   ```
   - Access n8n at [http://localhost:5678](http://localhost:5678)

4. **(Optional) Install via Docker**
   ```bash
   docker run -it --rm \
     -p 5678:5678 \
     n8nio/n8n
   ```

---

## 2. VM Installation (Ubuntu Example)

**Prerequisites:**
- Ubuntu VM (cloud or local)
- SSH access
- Node.js & npm or Docker

**Steps:**

1. **Update System**
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. **Install Node.js & npm**
   ```bash
   curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
   sudo apt-get install -y nodejs
   ```

3. **Install n8n**
   ```bash
   sudo npm install n8n -g
   ```

4. **Start n8n**
   ```bash
   n8n
   ```
   - Access via `http://<VM-Public-IP>:5678`


5. **Install via Docker Compose (using your own Dockerfile)**
   - If you have a custom `Dockerfile` and `docker-compose.yml`, follow the steps in [DOCKER_INSTALL.md](./DOCKER_INSTALL.md) for building and running n8n on your VM.
   - This method allows for advanced configuration and persistent storage.


**Tips:**
