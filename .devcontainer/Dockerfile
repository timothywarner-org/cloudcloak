# Use the official devcontainer base image for Ubuntu
FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# Install Node.js and npm, curl, and git to avoid re-installing during rebuilds
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs \
    && apt-get install -y \
        curl \
        git \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install global npm packages such as TypeScript
RUN npm install -g typescript

# Set the default user to 'vscode' for correct permissions
USER vscode

# Set the working directory for the container to /workspace
WORKDIR /workspace

# Expose ports if necessary (e.g., for web development)
# EXPOSE 3000
