# Deployments

## Overview

This directory contains deployment configurations for AriTech NEXUS.

## Planned Files

- Dockerfile
- docker-compose.yml
- nginx.conf
- production.env
- staging.env
- Kubernetes manifests (future)

## Deployment Targets

- Ubuntu Server
- Docker
- Docker Compose
- Nginx Reverse Proxy
- PostgreSQL
- MikroTik RouterOS

## Deployment Process

1. Build frontend.
2. Build backend.
3. Run database migrations.
4. Start application containers.
5. Configure Nginx.
6. Enable HTTPS.