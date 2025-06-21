# syntax=docker/dockerfile:1
FROM python:3.11-slim

# Set up working directory
WORKDIR /app

# Install Python dependencies first
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY app ./app
COPY .env.example ./

# Expose default Flask port
EXPOSE 5000

# Run the web service with Gunicorn
CMD ["gunicorn", "-b", "0.0.0.0:5000", "app.main:app"]
