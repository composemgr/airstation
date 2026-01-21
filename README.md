## 👋 Welcome to airstation 🚀

Airstation - Your own online radio station

## 📋 Description

Airstation is a self-hosted web app for streaming music over the Internet as an online radio station. Features a simple interface for uploading tracks and managing the playback queue, along with a minimalistic player for listeners. Streams music over HTTP using HLS.

## 🚀 Services

- **app**: Airstation server (`cheatsnake/airstation:latest`)

## 📦 Installation

### Using curl
```shell
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/airstation/main/docker-compose.yaml" | docker compose -f - up -d
```

### Using git
```shell
git clone "https://github.com/composemgr/airstation" ~/.local/srv/docker/airstation
cd ~/.local/srv/docker/airstation
docker compose up -d
```

### Using composemgr
```shell
composemgr install airstation
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
BASE_HOST_NAME=${HOSTNAME}
```

## 🌐 Access

- **Web Studio**: http://172.17.0.1:60069/studio
- **Player**: http://172.17.0.1:60069/player  
- **Stream**: http://172.17.0.1:60069/stream

## 📂 Volumes

- `./rootfs/data/airstation` - Uploaded tracks and database

## 🎵 Usage

1. Access /studio to upload tracks
2. Manage playback queue
3. Share /player URL with listeners
4. FFmpeg handles audio processing automatically

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```shell
docker compose up -d
docker compose down  
docker compose pull && docker compose up -d
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+
- Music files in common formats

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
