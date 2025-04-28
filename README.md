# Metabase

This project sets up a Dockerized environment for running Metabase with Nginx as a reverse proxy and PostgreSQL as the database.

## Prerequisites

- Docker
- Docker Compose

## Project Structure

- `.gitignore`: Specifies files and directories to be ignored by Git.
- `docker-compose.yml`: Defines the services and configurations for the Docker environment.
- `sample.env`: Environment variables for the project.

## Services

1. **Nginx**: Acts as a reverse proxy with SSL support.
2. **PostgreSQL**: Database for Metabase.
3. **Metabase**: Analytics and business intelligence platform.

## Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Copy the `sample.env` file to `.env` and update the variables:
   ```bash
   cp sample.env .env
   ```

3. Build and start the services:
   ```bash
   docker-compose up -d
   ```

4. Access the services:
    - Metabase: `http://<HOST>`
    - Nginx: `http://<HOST>` or `https://<HOST>`

## Environment Variables

Update the `.env` file with the following variables:

- `HOST`: Your domain name.
- `SSL_ENABLED`: Enable or disable SSL (`true` or `false`).
- `DEBUG`: Enable or disable debug mode (`true` or `false`).
- `POSTGRES_DB`: Name of the PostgreSQL database.
- `POSTGRES_USER`: PostgreSQL username.
- `POSTGRES_PASSWORD`: PostgreSQL password.

## Volumes

- `certs`: Stores SSL certificates.
- `postgres`: Stores PostgreSQL data.
