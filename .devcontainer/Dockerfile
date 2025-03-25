# Syntax=docker/dockerfile:1
ARG VARIANT="20"
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:0-${VARIANT}

# Install generally useful tools
RUN apt-get update && \
    apt-get -y install --no-install-recommends curl git sqlite3 && \
    rm -rf /var/lib/apt/lists/*

# Install SAP CAP SDK
USER node
RUN npm install -g @sap/cds-dk@6
WORKDIR /home/node