#Flask DevOps Lab VERSION A


## Usage

Activate the virtual environment, install requirements, and run the app:

```bash
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Routes

- `/api/health` — Returns `{"status": "ok"}` to confirm the app is running
- `/api/config` — Returns the contents of config.json including app name and version
- `/api/report` — Returns hostname, Python version, and app uptime in seconds
