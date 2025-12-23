# Raspberry Pi Docker Backup

This repository contains the configuration for various self-hosted services running on a Raspberry Pi using Docker. Each service is defined in its own directory using Docker Compose.

## Directory Structure

All services are located in the `services` directory. The repository is organized by service, and each service has its own directory containing the necessary `docker-compose.yml` or `compose.yaml` file and any associated configuration files.

Below is a list of the services included in this repository:

-   [**Arcane**](./services/arcane/) - `compose.yaml`, `.env`
-   [**Dockage**](./services/dockage/) - `docker-compose.yml`, `data` directory
-   [**Dockpeek**](./services/dockpeek/) - `docker-compose.yml`
-   [**Haus**](./services/haus/) - `compose.yaml`, `.env`
-   [**n8n**](./services/n8n/) - `compose.yaml`, `.env`
-   [**Paperless-ngx**](./services/paperless-ngx/) - `docker-compose.yml`, `docker-compose.env`
-   [**Pi-hole**](./services/pi-hole/) - `docker-compose.yml`, `etc-pihole` data directory
-   [**Readeck**](./services/readeck/) - `docker-compose.yml`
-   [**Searxng**](./services/searxng/) - `compose.yaml`, `.env`
-   [**ThinkDashboard**](./services/thinkdashboard/) - `docker-compose.yml`, `data` directory
-   [**Trilium**](./services/trilium/) - `docker-compose.yml`, `trilium-data` directory
-   [**WG-Easy**](./services/wg-easy/) - `docker-compose.yml`
-   [**Whoogle**](./services/whoogle/) - `docker-compose.yml`

## Usage

To start a specific service, navigate to its directory inside the `services` folder and run:

```bash
docker-compose up -d
```

Or, if the file is named `compose.yaml`:

```bash
docker compose up -d
```

Make sure to set up the necessary environment variables in the `.env` files where applicable before starting the services.

## Backup

This repository serves as a backup of the Docker configurations. The `data` directories are included for some services, but be aware that backing up running databases or large data volumes might require a more robust backup strategy.
