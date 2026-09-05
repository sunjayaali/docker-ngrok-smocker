# Smocker + Ngrok

Docker Compose setup for running Smocker and exposing it through Ngrok.

## Requirements

- Docker
- Docker Compose
- Ngrok account
- Ngrok authentication token

## Configuration

Copy `.env.example` to `.env`:

```bash
cp .env.example .env
```

Configure the environment variables in .env:

```bash
SMOCKER_HTTP_PORT=8080
SMOCKER_UI_PORT=8081

NGROK_AUTHTOKEN=your-ngrok-auth-token
NGROK_URL=https://your-domain.ngrok.app
```

## Start

```bash
docker compose up -d
```

Check the services:

```bash
docker compose ps
```

## Access

### Smocker HTTP API

```bash
http://localhost:${SMOCKER_HTTP_PORT}
```

### Smocker UI

```bash
http://localhost:${SMOCKER_UI_PORT}
```

### Ngrok

```bash
${NGROK_URL}
```

### Ngrok Inspector

```bash
http://localhost:4040
```

## Stop

```bash
docker compose down
```
