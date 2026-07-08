# WordPress Docker Compose

Quickly deploy a WordPress instance with MySQL using Docker Compose.

## Prerequisites

- Docker
- Docker Compose

## Usage

1. Copy the `.env` file and configure your environment variables:

   ```bash
   cp .env.example .env
   ```
2. Edit the `.env` file and set your database credentials:

   ```env
   DB_NAME=wordpress
   DB_ROOT_PASSWORD=root
   ```
3. Start the services:

   ```bash
   docker compose up -d
   ```
4. Access WordPress at `http://localhost:8080`

## Stopping the Services

```bash
docker compose down
```

## Configuration

### `docker-compose.yml`

- **WordPress**: Exposed on port `8080`
- **MySQL**: Internal only (not exposed)

### Environment Variables

| Variable             | Description              | Default        |
| -------------------- | ------------------------ | -------------- |
| `DB_NAME`          | Database name            | `wordpress`  |
| `DB_ROOT_PASSWORD` | PostgreSQL root password | _(required)_ |

## Directory Structure

```
wordpress/
├── docker-compose.yml
└── README.md
```
