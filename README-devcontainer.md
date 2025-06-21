# Development Container

This project uses a Docker-based development environment configured for a Flask application.

## Base Image Choice
The container is built from `python:3.11-slim` to provide a lightweight Python runtime suitable for running Flask with Gunicorn.

## VS Code Extensions
- **ms-python.python**: Provides Python language support, linting and debugging features.

## Container Startup
When started, the container installs dependencies and launches the application using Gunicorn bound to port `5000`.

## Using this Environment
1. Open this repository in VS Code and choose **Reopen in Container** (or open in GitHub Codespaces).
2. VS Code will build the Dockerfile and set up the environment.
3. Once running, the Flask app will be available on port 5000.

Use this environment for consistent development across machines or when working in Codespaces.
