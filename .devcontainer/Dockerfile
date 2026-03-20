FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    curl \
    git \
    sudo \
    && rm -rf /var/lib/apt/lists/*

RUN useradd -m -s /bin/bash vscode && \
    echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

RUN curl -sSL "https://github.com/buildpacks/pack/releases/download/v0.36.4/pack-v0.36.4-linux.tgz" \
    | tar -C /usr/local/bin/ --no-same-owner -xzv pack

USER vscode