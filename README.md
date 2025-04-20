# TwistAPI

TwistAPI is a Docker-based project that sets up two APIs using Traefik as a reverse proxy. This project demonstrates how to configure and deploy multiple services with Docker Compose and Traefik.

## Project Structure

- **docker-compose.yaml**: Defines the services, networks, and volumes for the project.
- **traefik.yaml**: Configuration file for Traefik, including logging, entry points, and providers.
- **README.md**: Documentation for the project.

## Services

1. **Traefik**: A reverse proxy and load balancer that routes traffic to the appropriate services.
   - Dashboard available at `http://dashboard.local` (requires host configuration).
   - Exposes services based on labels defined in `docker-compose.yaml`.

2. **Profile API**: A sample API service.
   - Accessible at `http://<traefik-host>/profile`.

## Prerequisites

- Docker and Docker Compose installed on your system.
- A manager node in Docker Swarm mode (required for the `deploy` section in `docker-compose.yaml`).

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd twistapi