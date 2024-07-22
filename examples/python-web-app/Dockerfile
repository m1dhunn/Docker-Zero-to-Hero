FROM ubuntu:latest

# Set the working directory
WORKDIR /app

# Copy the requirements file and the devops directory
COPY requirements.txt /app
COPY devops /app

# Install necessary packages, create a virtual environment, activate it, and install dependencies
RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv && \
    python3 -m venv devops_env && \
    /bin/bash -c "source devops_env/bin/activate && pip install -r requirements.txt"

# Set the working directory to /app/devops
WORKDIR /app/devops
