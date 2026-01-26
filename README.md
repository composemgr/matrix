## 👋 Welcome to matrix 🚀

Secure, decentralized communication protocol and server

## 📋 Description

Secure, decentralized communication protocol and server

## 🚀 Services

- **web**: vectorim/element-web:latest
- **server**: docker.io/matrixdotorg/synapse:latest

### Infrastructure Components

- **db**: Postgres database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/matrix/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/matrix" ~/.local/srv/docker/matrix
cd ~/.local/srv/docker/matrix
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install matrix
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59076

## 📂 Volumes

- `./rootfs/config/synapse` - Data storage
- `./rootfs/data/db/postgres/matrix` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f web
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
