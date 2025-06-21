# Development Container Setup

This repository includes configuration files for running the Flask application inside a VS Code Dev Container or GitHub Codespace.

## Base Image
The container uses **python:3.11-slim** providing a minimal runtime with the latest Python features.

## Exposed Port
The app listens on port **5000**, so this port is forwarded automatically.

## Installed Extensions
- `ms-python.python` – Python language support and debugging tools.

## Container Commands
Dependencies are installed with `pip install -r requirements.txt` during image build and again after creation to ensure they are up to date. The service is started via:

```bash
gunicorn -b 0.0.0.0:5000 app.main:app
```

## Getting Started
1. Open this repository in VS Code and choose **Reopen in Container** (or create a Codespace).
2. Wait for the build to finish; dependencies will be installed automatically.
3. Access the running Flask application at `http://localhost:5000`.

Use this environment for consistent, reproducible development.
