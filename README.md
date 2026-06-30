#Flask DevOps Lab VERSION A


## Usage

Activate the virtual environment, install requirements, and run the app:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Routes

- `/api/health` — Returns `{"status": "ok"}` to confirm the app is running
- `/api/config` — Returns the contents of config.json including app name and version
- `/api/report` — Returns hostname, Python version, and app uptime in seconds

## Running with Docker

```bash
docker build -t flask-devops:v1.1.0 .
docker run -d --name flask-app -p 8080:8080 flask-devops:v1.1.0
```

## Running with Docker Compose

```bash
docker compose up -d --build
```

To stop and remove containers:

```bash
docker compose down
```

To also remove volumes:

```bash
docker compose down -v
```
