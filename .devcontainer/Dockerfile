# Use the official Python 3.12 dev container image
FROM mcr.microsoft.com/vscode/devcontainers/python:3.12

# Install additional packages as root
USER root
RUN apt-get update && apt-get install -y \
    git \
  && rm -rf /var/lib/apt/lists/*

# Switch to vscode user to install uv into the correct home directory
USER vscode
RUN curl -LsSf https://astral.sh/uv/install.sh | sh

# Ensure uv is in the PATH for the vscode user
ENV PATH="/home/vscode/.local/bin:${PATH}"

# Set the working directory
WORKDIR /workspace

# Ensure the container starts as the vscode user
USER vscode
