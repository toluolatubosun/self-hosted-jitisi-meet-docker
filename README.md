# Self Host Jitsi Meet + Excalidraw  With Docker Compose

This is a simple guide to self-host Jitsi Meet and Excalidraw using Docker. This guide is based on the official Jitsi Meet Docker installation guide and the Excalidraw Docker installation guide.

It uses Jitsi Meet `stable-10133` and the latest Excalidraw Docker image.

For configuring Jitsi Meet, you can refer to the official Jitsi Meet handbook. I mounted the web configuration files because some configurations set in the `.env` file are not working, and some configurations are not available in the `.env` file.

## Prerequisites

- Docker
- Docker Compose
- A domain name pointing to your server's IP address
- Ubuntu 20.04 LTS, At least 4GB RAM, 2 CPU Cores

## Setup

1. Clone this repository

```bash
git clone self-hosted-jitisi-meet-docker

cd self-hosted-jitisi-meet-docker
```

2. Update the configuration files. Search for `toluolatubosun.com` and replace it with your domain name. Also search for `King Meet` and replace it with your desired name.

### Note:
- `jitsi.toluolatubosun.com` is where the Jitsi Meet instance will be hosted. The domain points to port 80 on the `web` service in the `docker-compose.yml` file.

- `whiteboard.toluolatubosun.com` is where the Excalidraw backend will be hosted. The domain points to port 80 on the `excalidraw-backend` service in the `docker-compose.yml` file.

3. Run the docker-compose file

```bash
docker-compose up -d
```
