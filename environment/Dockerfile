# hash:sha256:160a3329c3a0513e3e9a8b75a36d3ebafd2c1b3be74748db8a5bbfc9b0faeb63
FROM registry.codeocean.com/codeocean/ubuntu:20.04-cuda11.7.0-cudnn8

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        build-essential=12.8ubuntu1.1 \
        gcc=4:9.3.0-1ubuntu2 \
        libc6-dev=2.31-0ubuntu9.9 \
    && rm -rf /var/lib/apt/lists/*
