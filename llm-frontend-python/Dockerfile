# Use Python 3.11 slim image as base
FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Set environment variables
ENV PYTHONUNBUFFERED=1

# Copy requirements first for better caching
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY app.py config.py ./
COPY templates/ ./templates/
COPY static/ ./static/

# Expose the application port
EXPOSE 5000

# Run the application
CMD ["python", "app.py"]

