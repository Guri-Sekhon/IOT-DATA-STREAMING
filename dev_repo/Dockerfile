# Use an official Python runtime as a parent image
FROM python:3.13.0-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Upgrade pip to the latest version
RUN pip install --no-cache-dir --upgrade pip

# Install any dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Run both producer and consumer in the background
ENTRYPOINT ["sh", "-c", "python producer.py & python consumer.py"]
