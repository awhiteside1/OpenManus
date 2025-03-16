# Use the official Python 3.12 dev container image
FROM mcr.microsoft.com/vscode/devcontainers/python:3.12

# Install uv for fast dependency management
RUN curl -LsSf https://astral.sh/uv/install.sh | sh

# Optionally install additional packages if needed (e.g., git)
RUN apt-get update && apt-get install -y \
    git \
  && rm -rf /var/lib/apt/lists/*

# Set the working directory
WORKDIR /workspace
