# Dockerfile
FROM python:3.9-slim

# Set work directory
WORKDIR /app

# Install dependencies
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . /app/

# Run Django server with Gunicorn
CMD ["gunicorn", "todo_api.wsgi:application", "--bind", "0.0.0.0:8000"]
